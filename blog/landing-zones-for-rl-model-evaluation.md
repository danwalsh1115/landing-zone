# When is a model "good enough"?

**Landing Zones as evaluation criteria for reinforcement learning**<br>
By **Dan Walsh** · about 8 minutes to read

---

Every model development team eventually has the same argument. A data scientist says the new policy is better. A process engineer says it isn't ready. A product manager asks whether it can ship this quarter. Someone suggests one more training run.

Nobody is wrong, exactly. They're each judging the model against a different, unwritten definition of "good."

While consulting for [Imubit](https://imubit.com), which builds closed-loop AI optimization for industrial process plants, I introduced model development teams to a method I'd used for years on hardware and software products: the **Landing Zone**. We wrote down, before training started, what "good enough to deploy" meant in numbers, as a range. That one change helped cut model development cycle time by **23%**.

This post explains why the method fits reinforcement learning so well and how to apply it.

---

## The problem: reward is not success

In reinforcement learning, an agent learns a policy by maximizing a reward signal. It's tempting to treat the reward curve as the measure of progress. If reward went up, the model got better.

In practice, that breaks down in four ways.

**1. Success has many dimensions, and reward collapses them into one.** A controller for an industrial process has to raise economic performance *and* respect safety and equipment limits *and* behave smoothly enough that operators trust it. Squeezing those into one weighted reward hides the tradeoffs. A policy can score a higher reward while getting worse on the dimension your customer cares about most.

**2. There's no stopping rule.** Reward can almost always be nudged a little higher with more tuning, more data or a different architecture. Without an explicit definition of "good enough," teams keep training. That's the RL version of gold-plating, and it eats calendar time.

**3. Different people hold different definitions of good.** Data scientists look at reward and validation loss. Process engineers look at constraint violations and how hard the valves are being worked. Customers look at dollars per day and whether their operators will leave the controller switched on. When these definitions stay implicit, the disagreement shows up late, often during commissioning at the plant.

**4. The simulator is not the plant.** RL agents are usually trained in a simulated or learned model of the environment. Strong results in simulation don't guarantee results in the real world. "Good" needs to include evidence that the policy will transfer.

---

## The Landing Zone, in one paragraph

A Landing Zone is a short table. Each **row** is an attribute that directly decides success or failure. Each row has three quantified levels: **Minimum** (below this, we've failed), **Target** (what we plan to hit) and **Outstanding** (what we'd hit if everything went right; going further rarely pays back). Anywhere inside the zone, on every row, counts as success. The [tutorial](../README.md) covers the basics.

---

## Why it fits reinforcement learning

**It replaces "maximize" with "satisfice."** Herbert Simon coined *satisficing* for decisions where the optimal answer can't be computed. That's exactly the RL situation: there's no way to know the best achievable policy in advance. What you *can* define is "good enough on every dimension that matters." The model is ready when every row clears Minimum, not when reward stops rising.

**It keeps the dimensions separate.** The reward function stays the training objective. The Landing Zone becomes the *acceptance* test, scored row by row. If a new policy improves economics but drops below Minimum on constraint violations, the table shows it immediately, without anyone arguing about reward weights.

**It's test-first.** Writing acceptance criteria before writing code is standard practice in software. A Landing Zone does the same for models: it's the evaluation suite, agreed before the first training run. Every experiment is then scored against the same table.

**Outstanding is a stopping rule.** Once a row reaches Outstanding, further work on it needs a reason. That redirects effort to rows still below Target, or ends the iteration.

**It clarifies who decides.** If an experiment keeps every row in the zone, the model team decides what to do next. If a decision would drop a row below Minimum, or the levels themselves need to change, it goes to the stakeholders. Teams move faster because they know where their authority ends.

---

## An example Landing Zone for an RL process controller

This example is illustrative. The rows are typical for a controller that optimizes a continuous industrial process, but the numbers are made up for this post.

| Attribute | Kill Switch | Minimum | Target | Outstanding |
|---|---|---|---|---|
| Economic uplift vs. current control (simulation, $/day) | < 0.5% | 1.0% | 2.0% | 3.0% |
| Hard constraint violations per 1,000 simulated hours | > 5 | 1 | 0 | 0 |
| Soft constraint time outside limits | > 5% | 2% | 1% | 0.5% |
| Control smoothness (average valve move per step vs. baseline) | > 150% | ≤ 120% | ≤ 100% | ≤ 80% |
| Robustness: share of held-out operating scenarios that pass all rows | < 70% | 85% | 95% | 99% |
| Sim-to-real check: process model error on recent plant data | > 10% | 5% | 3% | 2% |
| Operator acceptance during trial (share of time in closed loop) | < 50% | 80% | 90% | 95% |
| Time from data snapshot to candidate model | > 6 wks | 4 wks | 2 wks | 1 wk |

A few things to notice:

- **Safety rows have no slack.** For hard constraints, Target and Outstanding are both zero. Not every row needs a wide range.
- **"Less is better" and "more is better" rows sit side by side.** That's normal.
- **Robustness is its own row.** A policy that's brilliant in the average scenario and fails in edge cases isn't ready.
- **The last row measures the team, not the model.** Including cycle time in the definition of success keeps it visible.
- **Kill Switch** marks the point where the team should meet and decide whether this approach is worth continuing.

Add a **Now** column and update it after every candidate model. The table becomes the status report.

---

## How to introduce it to a model team

1. **Start from the customer's definition of value, not the reward function.** Ask what the plant (or user, or business) would measure to decide the model worked. Those become the rows.
2. **Bring the people who'll judge the model into the room.** Data scientists, domain engineers, the customer-facing team and, ideally, someone who represents the end user. Disagreement in this meeting is cheap. Disagreement at deployment is expensive.
3. **Keep it under a dozen rows.** Put detailed metrics in a child Landing Zone if the team needs them, and keep one summary row in the main table.
4. **Make every row measurable in your evaluation harness.** If you can't compute a row automatically for each candidate model, you'll stop checking it.
5. **Score every experiment against the full table.** Not just the row the experiment was meant to improve.
6. **Revisit the levels when you learn something.** A new customer, a new operating regime or a better baseline can all move the zone. Change it deliberately, together, and keep the history.

---

## What changed

Before, "is the model ready?" was a debate that restarted with every candidate. After, it was a lookup: does every row clear Minimum? Teams stopped polishing metrics that were already good enough, caught problems on rows nobody had been watching, and had a shared language with domain experts and customers.

The result was a **23% reduction in model development cycle time.**

---

## The broader point

As more products include models, especially in AI where "better" is easy to measure and hard to define, product leaders need a way to say when a model is good enough. Benchmarks and reward curves tell you which direction is up. A Landing Zone tells you when you've arrived.

If you're building with RL, LLMs or any other ML, try writing one before your next training run.

---

*Dan Walsh is a technical product manager who builds AI-enabled products. Connect on [LinkedIn](https://www.linkedin.com/in/danwalsh1115).*
