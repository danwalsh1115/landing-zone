# The Landing Zone method: full reference

Source: Dan Walsh, *The Landing Zone: A simple, agile, and powerful way to define and communicate the definition of success* (white paper, rev. April 2024), and the accompanying training deck (June 2024).

## The problem it solves

Product and program work happens amid unprecedented complexity: stakeholders, markets, supply chains, ecosystems, competition, product lines and business goals all interact. Forecasts are less certain. Many teams have **no explicit definition of success at all**, and stakeholders hold different, implicit expectations that surface only when it becomes clear they won't be met, usually late, when correcting course is costly or impossible.

Dan's own experience as a strategic product planner at a large high-tech company: teams of hundreds to thousands of engineers across the globe, breathtaking competition, stakeholders across business units each with their own view. Attempts to control complexity through process created bureaucracy, distraction and **metrics fatigue**.

Unlike algebra (x = 8) or linear programming (a computable optimum), complex problems have no knowable optimal answer. You can only define what is *good enough* on each dimension that matters.

## Definition

A Landing Zone is a table that defines a **region** of success for a product or project.

- **Rows**: the subset of attributes that directly and materially define success or failure.
- **Columns**: a quantified range of performance levels:
  - **Minimum**: required to avoid some sort of failure
  - **Target**: what the team would like to achieve
  - **Outstanding**: achievable if everything goes perfectly
- Together they hold the *necessary and sufficient* success definition.

Name and metaphor: on an aircraft carrier, the landing zone is the marked section of deck a pilot must touch down in. The pilot needn't hit one exact spot, but must land inside the zone. The same idea applies to dropping rescue workers after a disaster or landing a mission on the moon.

**Direction matters.** Minimum is the success/failure boundary, not the smallest value. For lower-is-better attributes (cost, headcount, finish date), Minimum is the highest or latest acceptable value, and Target and Outstanding sit below or before it.

**Functions and constraints** are Boolean (present or absent), so they don't fit a range. Put them in a single row with lists per level. Lists are usually cumulative ("Min + 4G, USB3"; "Target + USB-C, Thunderbolt") but can be distinct.

## Length

- Fits on one page, so it can be seen at a glance.
- Two dozen rows at most; one dozen is better.
- The top-level Landing Zone holds only what upper management must review regularly.
- **Child Landing Zones** (spreadsheet tabs work well) hold detail for components or aspects like security or performance.
- Trouble staying under 24 usually signals a lack of understanding of what really drives success. If there truly are that many critical factors, the work can fail in many ways and needs heavy investment to protect against failure.
- **Landing Zones capture success, not scope.** Use other models for scope (use-case diagrams, feature models).

## What a Landing Zone is not

- **Not a backlog or priority list.** Row order means nothing; all rows are required.
- **Not a strategy.** It's informed by strategy (competition, differentiation, business priorities make good rows), but any strategy that lands inside the zone is, by definition, success.
- **Not OKRs.** OKRs define and track objectives and outcomes for an individual, team or group. A Landing Zone characterizes what will make a specific product or project succeed.
- **Not Big Requirements Up Front.** It changes as learning happens.
- **Not a guarantee** of market success.

## What it's used for

- Gaining explicit consensus on success at the start, with a clear finish line (like test-driven development for the whole effort)
- Preventing scope creep and over-engineering, and making any choice to expand scope explicit
- Quantifying required levels as input to feasibility and risk analysis, surfacing issues early
- Driving tradeoff discussions
- Empowering decisions and fostering autonomy
- Monitoring and communicating status

## Nine reasons it works

1. **Necessary ambiguity.** From sense-making work with Dave Snowden (Cynefin): *match ambiguity with ambiguity.* A range absorbs uncertainty and gives latitude for tradeoffs. It isn't sloppy; it's the right response to complexity.
2. **Satisficing.** Herbert Simon's blend of *satisfy* and *suffice*: a decision heuristic when the optimum can't be computed. Meeting every requirement at least at Minimum. (How did you pick your last phone? The first one good enough on everything that mattered.)
3. **Enabling constraints.** Alicia Juarrero's idea: constraints that enable things to happen. Juan Carlos Castro describes them as conditions that let us "enter into spaces of uncertainty and be able to reorganize previous understandings into new patterns." In Davis, Sumara and Luce-Kapler's words, enabling constraints "don't dictate what MUST be done, rather they are expansive, indicating what MIGHT be done."
4. **Distributed decision making.** Lean and Agile push decisions to the lowest feasible level. Inside the zone, teams decide; outside it, they consult. This balances central and distributed authority.
5. **Limits over-processing waste.** In Lean terms, Outstanding caps effort that won't return value in proportion to its cost, preventing "gold plating on battleships."
6. **System-level tradeoffs.** Cost can be traded for schedule; one team can absorb a larger technical gap to help another that's below Minimum. Similar to set-based concurrent engineering (SBCE).
7. **Focus on what matters.** Some teams add hundreds of rows, which is really a bloated market requirements document. Fewer is better. Lean Startup teams may keep one Landing Zone per MVP to control scope.
8. **Agile and adaptable.** A living document updated as conditions and knowledge change.
9. **Scale-free.** The same structure works for a team of ten or ten thousand, with parent and child Landing Zones keeping each team at the right level of abstraction.

## Evolution

Success definitions change because of a changing stakeholder population, shifting needs and preferences, market conditions, and competitors' offerings and performance. A Landing Zone changes in two ways: **adding or removing rows**, or **changing levels**. Keep it current so the definition stays clear, common and coherent.

## Importance vs. priority

All rows are important; priority is about urgency and changes almost continuously. Tom Gilb's example: food, water and shelter are all necessary for life, but which you prioritize depends on how much of each you have. Early priority usually follows the size of the gap below Minimum. Once all rows clear Minimum, other concerns drive priority, including dependencies between rows and preferred combinations (e.g., hitting the Outstanding ship date even at the largest headcount). Manage priorities in a backlog or evolutionary delivery plan.

## Decision rights

- Decisions that keep every row inside the zone: the team makes them as normal work.
- Decisions that would violate a row need ratification from higher authority. That includes falling below Minimum, changing Minimum, **and pursuing anything beyond Outstanding**. Ask: will the market pay in proportion to cost? Is there a better investment elsewhere? Too often teams build more because they can, not because it pays.
- Most teams get every row to Minimum before pushing selected rows toward Target or Outstanding.

## Variants

| Column | Meaning |
|---|---|
| **Now** | Current achievement level; optional trend arrow (↑ toward Outstanding, → flat, ↓ toward Minimum) |
| **Kill Switch** | A generally unrecoverable level below Minimum that triggers a meeting on cancellation; prevents "zombie" projects |
| **Owner** | Whom to approach with questions or change requests for the row |

Full layout: `Attribute | Kill Switch | Minimum | Target | Outstanding | Now | Owner`. Add any of these in any combination.

## Why it's harder than it looks

- **Choosing rows is an art.** For incremental products, the vital few are often known from the last generation. For new and novel products, expect research, experimentation and several "touch-and-go" landing runs.
- **Forecasts can be wrong** in two ways: bad or missing information leads to unneeded rows or wrong levels; and stakeholders can **miswant**, misjudging how much they'll like something later ("This is not what we wanted," after signing off on the screens).
- **Quantifying subjective attributes** (UX, ease of use) is hard but possible. Don't settle for "fast," "easy," "industry-leading" or "state-of-the-art." Those words let every stakeholder imagine something different.
- **No guarantee.** Wrong assumptions, knowledge gaps or unforeseen events can still sink a product that met every row.

## Who it's for

It's especially valuable for large teams with complex products and programs. It improves transparency, aligns the organization, prevents late surprises, and reduces politics: tradeoffs are agreed in advance, so there's less maneuvering when hard calls arrive. It takes little time and no special tools: low risk, high reward. It also works for personal decisions such as a next job, a home, a college or a major purchase.

## References

1. Juran, J. M. *Quality-Control Handbook.* McGraw-Hill, 1951.
2. Dave Snowden, Cynefin framework (The Cynefin Co., formerly Cognitive Edge).
3. Juarrero, Alicia. *Dynamics in Action: Intentional Behavior as a Complex System.* MIT Press, 1999.
4. Castro, Juan Carlos. "Constraints that Enable: Creating Spaces for Artistic Inquiry." *Proceedings of the 2007 Complexity Science and Educational Research Conference*, Vancouver, pp. 75–86.
5. Davis, Brent, Dennis Sumara and Rebecca Luce-Kapler. *Engaging Minds: Cultures of Education and Practices of Teaching.* 2015.
6. Simon, Herbert A., on satisficing and bounded rationality.
7. Gilb, Tom, on competitive engineering and requirements (food, water, shelter illustration).
