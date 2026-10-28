# Worked examples

Use these to explain the method or to show what a good row looks like. The product-launch and car examples are fictitious teaching examples from Dan Walsh's training.

## 1. Product launch (hardware)

| Attribute | Minimum | Target | Outstanding |
|---|---|---|---|
| Retail on shelf | Dec 1 | Nov 15 | Nov 1 |
| Manufacturing cost per unit | $11.50 | $10.00 | $9.00 |
| Peak project personnel | 400 | 350 | 250 |
| Markets at launch | US, Asia | US, Asia | US, Asia, Europe |
| Design wins at launch | 20 | 30 | 50 |
| Total first-year volume | 75K | 110K | 125K |
| Functions & constraints | Dual-monitor support, 3G, USB 2 | Min + 4G, USB 3 | Target + USB-C, Thunderbolt |

Teaching points: every level is quantified; date, cost and headcount are lower-is-better, so Minimum is the latest or highest value; volume is higher-is-better; features sit in one list row.

## 2. Car purchase (personal)

| Attribute | Minimum | Target | Outstanding |
|---|---|---|---|
| Cost | $27,000 | $20,000 | $17,500 |
| Mileage (city) | 18 mpg | 25 mpg | 35 mpg |
| Seating | 4 adults | 5 adults | 6 adults |
| Functions & constraints | Bluetooth audio, USB | Min + self-parking, backup camera | Target + collision avoidance |
| Interior noise at 65 mph | 65 dBA | 60 dBA | 55 dBA |
| Projected 3-year maintenance cost | $3,000 | $2,000 | $1,500 |

Teaching points: a mix of more-is-better and less-is-better rows. Ask learners what *they* would add or drop (acceleration? handling?). The table makes missing or unnecessary rows obvious, just as it will at work.

## 3. Reinforcement-learning model acceptance (AI product)

From Dan's blog post *When is a model "good enough"?* (in this repo under `blog/`). While consulting for Imubit (closed-loop AI optimization for industrial process plants), Dan introduced Landing Zones to model development teams as the definition of "good enough to deploy," set before training began. It helped cut model development cycle time by 23%.

Key ideas to coach with:
- **Reward is not success.** Reward collapses many dimensions into one and has no stopping rule. The reward function stays the *training objective*; the Landing Zone is the *acceptance test*, scored row by row.
- **Satisfice, don't maximize.** The model is ready when every row clears Minimum, not when reward stops rising.
- **Outstanding stops endless tuning**, the RL version of gold plating.
- Include rows for **sim-to-real transfer**, because simulator results don't guarantee plant results.

Illustrative row types (levels depend on the plant and customer): economic benefit, constraint-violation rate, control-move smoothness, operator acceptance (share of time left switched on), and simulation-to-plant performance gap.

## 4. Personal: next job

A good first practice Landing Zone. Prompt the learner to quantify each row themselves:

| Attribute | Minimum | Target | Outstanding |
|---|---|---|---|
| Base salary | | | |
| Commute or remote days per week | | | |
| Scope (team size or product ownership) | | | |
| Growth (learning budget, promotion path) | | | |
| Functions & constraints | | | |

Other personal topics from the training: a child's college choice, the next place to live, a major purchase.
