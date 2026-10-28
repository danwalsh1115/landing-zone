# Skills

## landing-zone-coach

A Claude skill that coaches a person or team through building, reviewing and using a Landing Zone. It works in five modes: learn, build, review, use (tradeoffs and decision rights) and teach others.

```
landing-zone-coach/
├── SKILL.md                      # coaching flow and stance
├── references/
│   ├── method.md                 # full method, nine reasons it works, sources
│   ├── coaching-playbook.md      # questions per step, common mistakes, review rubric, workshop plan
│   ├── attribute-catalog.md      # generic attributes and how to quantify vague ones
│   └── examples.md               # product launch, car, RL model, personal
└── assets/
    └── landing-zone-template.csv
```

### Install

- **Claude apps:** zip the `landing-zone-coach` folder and upload it under Settings → Capabilities → Skills.
- **Claude Code:** copy the folder to `~/.claude/skills/` (personal) or `.claude/skills/` in a project.

Then ask something like *"Coach me through a Landing Zone for our Q2 launch"* or *"Review this Landing Zone draft."*
