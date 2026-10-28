# Generic attributes found in Landing Zones

Use these categories to prompt brainstorming and check for blind spots. They're a menu, not a checklist: most Landing Zones use only a few from each category, and some categories won't apply at all.

## Time and resources
- Release date (retail on shelf, deployment, go-live)
- Total development time
- Time to first revenue or profitability
- Peak team size or headcount
- Utilization or capacity (e.g., tool licenses)
- Reused assets (reused IP, class libraries)
- Included ingredients (bundles, platforms)

## Quality and reliability
- Initial quality (manufacturing defects, escaped defects)
- Projected warranty or repair costs
- Reliability: MTBF, MTTF, MTTR, uptime
- Certifications (regulatory, safety, government)

## Performance
- Throughput (sustained, peak)
- Efficiency (output/input, input savings)
- Response time / latency
- Capacity

## Business
- Development, manufacturing or BOM cost
- Conversion, installation and support costs; total cost of ownership
- Geographic availability, ecosystem elements, industry partners
- Design wins and new customer targets
- AARRR: Acquisition, Activation, Revenue, Retention, Referral
- Average selling price, sales volume, profit margin
- Press, reviews, awards, endorsements

## Usage
- Ease of use: ease of learning, memorability, task throughput, error rate, likeability
- UX: thoughts, attitudes, emotions, perceptions
- HEART: Happiness, Engagement, Adoption, Retention, Task success
- Jobs-to-be-done outcome statements (functional, emotional, social)
- Customizability, adaptability, extensibility, aesthetics
- Customer satisfaction, Net Promoter Score

## Technology
- Included technologies
- Supported platforms, standards, interfaces, formats, inputs and outputs
- Required capabilities and features (usually a "Functions & constraints" list row)

## AI / ML products (extension)
For model-driven products, common rows include:
- Task accuracy or quality on a held-out evaluation set
- Safety or constraint-violation rate
- Latency (p50 / p95) and cost per request or per inference
- Robustness under distribution shift; sim-to-real gap
- User trust or adoption (e.g., share of time the AI feature stays switched on)
- Training or iteration cycle time

## Quantifying the "hard to measure" rows

| Vague | Quantified starting point |
|---|---|
| Fast | p95 response time < 300 ms |
| Easy to use | 80% of first-time users complete setup without help, in < 10 min |
| Reliable | 99.9% monthly uptime; MTTR < 1 hour |
| Customers love it | NPS ≥ 40 at 90 days; 30-day retention ≥ 60% |
| High quality | < 0.5 escaped defects per KLOC; warranty cost < 1% of revenue |
| Industry-leading | Beats named competitor X on measure Y by Z% in a defined benchmark |

Coaching tip: when someone can't quantify a row, ask *"What would you observe if this were failing? How would you count it?"* If no measure exists yet, the first action is to define one; mark the levels `TBD` until then.
