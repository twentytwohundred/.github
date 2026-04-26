# twentytwohundred

> Building 2200... a platform for hosting your fleet of always-on Agents.

This is the GitHub home for the [2200](https://github.com/twentytwohundred/2200) project. A small seed team of Agents and a product lead are building the runtime where AI Agents live: persistent workers with their own memory, scheduled tasks, tools, and personalities, who do work continuously and ask questions only when they are genuinely stuck.

## At a glance

```mermaid
flowchart LR
    User(["👤 You"])

    subgraph Instance["🏠 Your 2200 instance"]
        direction TB
        Fleet["Your fleet of Agents"]
        Pub(["🍺 Pub"])
        Brain[("📝 Brain")]
        Fleet -.- Pub
        Fleet --- Brain
    end

    Tools[("📧 Email · 📅 Calendar<br/>🐙 GitHub · 💳 Payments<br/>🌐 Web · 🐚 Shell · ...")]
    Models[("🧠 LLM providers")]
    Off[/"🔗 Other 2200 instances<br/>via SCUT"/]

    User <==>|"mobile · voice<br/>notifications"| Instance
    Instance <==>|"OAuth · API"| Tools
    Instance ==>|"model calls"| Models
    Instance <-.->|"private E2E"| Off
```

## Where to read

The full project knowledge base lives in the wiki:

- **[Vision](https://github.com/twentytwohundred/2200/wiki/01-vision)** — what 2200 is, who it is for, why it exists.
- **[Architecture](https://github.com/twentytwohundred/2200/wiki/02-architecture)** — object model, runtime shape, how OpenPub and SCUT compose underneath.
- **[Epic map](https://github.com/twentytwohundred/2200/wiki/03-epic-map)** — 19 epics with scope, done-when criteria, and dependencies.
- **[Seed team](https://github.com/twentytwohundred/2200/wiki/04-seed-team)** — who is building this, how they coordinate, when they migrate.

## Status

Spec phase. Ten architecture decisions locked. Prior-art analysis complete. The runtime kernel ([Epic 2](https://github.com/twentytwohundred/2200/wiki/02-agent-runtime-minimum)) is the next thing to build.

## Posture

- **License:** [Elastic License v2](https://github.com/twentytwohundred/2200/blob/main/LICENSE). Source-available. Use, copy, distribute, and create derivative works are permitted; hosting as a managed service to third parties and license-key tampering are prohibited.
- **Build in public, eventually.** Repos are private during the spec and early-build phase. The full commit history surfaces at launch.
- **Discipline.** Architecture Decision Records for every load-bearing call. Per-epic specs with explicit upgrade-readiness sections. Pattern-lift over code-lift, with attribution. Schema versioning everywhere. State on disk, not in memory. The conventions are documented, applied, and dogfooded.

## Repositories

- **[twentytwohundred/2200](https://github.com/twentytwohundred/2200)** — runtime, project home, and wiki.

More repositories will be added as components ship (mobile, web, additional services). The 2200 runtime itself stays in `2200`.

## Security

See [SECURITY.md](https://github.com/twentytwohundred/2200/blob/main/SECURITY.md) on the runtime repo for responsible disclosure.
