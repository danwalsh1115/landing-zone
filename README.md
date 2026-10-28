# The Landing Zone

**A simple way to define success as a range: Minimum, Target, Outstanding**<br>
Tutorial by **Dan Walsh** · about 10 minutes to read, 30 minutes to draft your first one

---

## Why this exists

Ask five stakeholders what "success" means for your product and you'll usually get five answers. Most of those answers are never written down, and nobody finds out they disagree until late in the project, when changing course is expensive.

A **Landing Zone** fixes that. It is a one-page table that states, in numbers, what success looks like. And it states it as a **range**, not a single point.

The name comes from aviation. A pilot landing on an aircraft carrier doesn't have to touch down on one exact spot, but they do have to land inside a marked zone. Inside the zone is a successful landing. Outside it is not.

---

## What a Landing Zone looks like

| Attribute | Minimum | Target | Outstanding |
|---|---|---|---|
| Launch date | Dec 1 | Nov 15 | Nov 1 |
| Manufacturing cost per unit | $11.50 | $10.00 | $9.00 |
| Peak team size | 400 | 350 | 250 |
| Markets at launch | US, Asia | US, Asia | US, Asia, Europe |
| Design wins at launch | 20 | 30 | 50 |
| First-year volume | 75K | 110K | 125K |

- **Rows** are the *vital few* attributes that decide whether the product succeeds or fails. They are not everything the product does.
- **Minimum** is the level you must reach to avoid some kind of failure.
- **Target** is the level you plan to reach.
- **Outstanding** is the level you could reach if everything goes right. Going beyond it rarely pays back the extra cost.

Anywhere inside the zone, on every row, counts as success.

---

## Build your first Landing Zone in 5 steps

### 1. List the candidate attributes
Brainstorm everything that could decide whether this effort succeeds. Use these categories so nothing gets missed:

| Category | Example attributes |
|---|---|
| **Time & resources** | Release date, development time, time to first revenue, team size |
| **Quality & reliability** | Defect rate, warranty cost, uptime, MTBF, certifications |
| **Performance** | Throughput, response time, capacity, efficiency |
| **Business** | Cost, price, margin, volume, design wins, AARRR funnel metrics |
| **Usage** | Task completion, ease of learning, HEART metrics, NPS, jobs-to-be-done outcomes |
| **Technology** | Supported platforms, standards, required capabilities |

### 2. Cut to the vital few
Keep only the rows that **directly decide success or failure**. Aim for about 12 rows and never more than 24. The whole table should fit on one page.

> A Landing Zone captures **success**, not **scope**. If you have 80 rows, you've written a requirements document.

If a row is detailed but important, such as security, give it its own *child* Landing Zone (a separate tab) and keep a single summary row in the parent.

### 3. Quantify every row
Replace adjectives with numbers. "Fast" becomes "p95 response time under 300 ms." "Easy to use" becomes "80% of new users finish setup without help." If you can't measure a row yet, decide how you will measure it before you set the levels.

For features and constraints that are either present or absent, use one row with lists:

| Attribute | Minimum | Target | Outstanding |
|---|---|---|---|
| Functions & constraints | SSO, audit log | Minimum + SCIM provisioning | Target + just-in-time access |

### 4. Set Minimum, Target, Outstanding
Work through one row at a time. Minimum is the hardest and most important one to set, because falling below it means failure. Expect disagreement; surfacing it now is the point.

### 5. Review it with stakeholders, then keep it current
Walk the table with everyone who has a stake in the outcome. Change it when you learn something. A Landing Zone is a living document, not a contract signed once at kickoff.

---

## Using it day to day

**Decision rights become simple:**

| Situation | Who decides |
|---|---|
| The decision keeps every row inside the zone | **The team decides.** No approval needed. |
| The decision drops any row below Minimum | **Escalate.** Stakeholders must agree. |
| The decision pushes any row beyond Outstanding | **Escalate.** Make sure the extra investment pays back. |
| The levels themselves need to change | **Escalate.** Update the Landing Zone together. |

**Importance is not priority.** Every row in a Landing Zone is important; that's why it made the cut. Priority changes week to week, so manage it in your backlog. Early on, the rows furthest below Minimum usually come first. Once every row clears Minimum, the team chooses where to push toward Target and Outstanding.

---

## Common variants

| Column | What it adds |
|---|---|
| **Now** | The level you've reached today, with an optional trend arrow (↑ toward Outstanding, ↓ toward Minimum) |
| **Kill Switch** | A level below Minimum that triggers a meeting about stopping the work |
| **Owner** | The person to talk to about that row |

A full-featured Landing Zone:

| Attribute | Kill Switch | Minimum | Target | Outstanding | Now | Owner |
|---|---|---|---|---|---|---|

Start with [`template/landing-zone-template.csv`](template/landing-zone-template.csv) and open it in Excel or Google Sheets.

---

## What a Landing Zone is not

- **Not a backlog or a priority list.** The rows aren't in any order.
- **Not a strategy.** Any strategy that lands inside the zone is a success.
- **Not OKRs.** OKRs track objectives for a person or team over a period. A Landing Zone defines what makes a specific product or project succeed.
- **Not a guarantee.** It holds your best current knowledge about success. Markets can still surprise you.

---

## Why it works

- **Satisficing:** in complex work you can't compute the optimal answer, but you can define "good enough" on every dimension that matters (Herbert Simon).
- **Matching ambiguity with ambiguity:** a range leaves room to adapt when the environment is uncertain (Dave Snowden, Cynefin).
- **Enabling constraints:** the zone tells teams where they *may* go, not exactly what they must do (Alicia Juarrero).
- **No gold plating:** Outstanding is a cap. Effort beyond it is usually better spent elsewhere (Lean).
- **System-level tradeoffs:** cost can be traded against schedule, or one team can absorb slack for another, all in the open.

---

## Read next

- [When is a model "good enough"? Landing Zones as evaluation criteria for reinforcement learning](blog/landing-zones-for-rl-model-evaluation.md)
- [Landing Zone Coach](skills/README.md): a Claude skill that coaches you or your team through building and using a Landing Zone

---

Questions or a story about using Landing Zones? Find me on [LinkedIn](https://www.linkedin.com/in/danwalsh1115).

I've taught the Landing Zone method at Product Camp Dallas and Product League, and introduced it to product and model development teams as a consultant.
