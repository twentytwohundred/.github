<div align="center">

# 2200

### A team of AI Agents, built for one person.

[![License](https://img.shields.io/badge/license-Elastic%20v2-0077B5.svg)](https://github.com/twentytwohundred/2200/blob/main/LICENSE)
[![Phase](https://img.shields.io/badge/phase-spec%20%2B%20early%20build-orange.svg)](https://github.com/twentytwohundred/2200/wiki/03-epic-map)
[![Decisions](https://img.shields.io/badge/decisions-14%20locked-5319E7.svg)](https://github.com/twentytwohundred/2200/wiki/_Sidebar)
[![Wiki](https://img.shields.io/badge/wiki-open-2EA44F.svg)](https://github.com/twentytwohundred/2200/wiki)

[**2200.ai**](https://2200.ai) · [Wiki](https://github.com/twentytwohundred/2200/wiki) · [Vision](https://github.com/twentytwohundred/2200/wiki/01-vision) · [Architecture](https://github.com/twentytwohundred/2200/wiki/02-architecture) · [Epic map](https://github.com/twentytwohundred/2200/wiki/03-epic-map)

</div>

---

## What this is

2200 is the runtime where your AI Agents live. Persistent workers with their own memory, tools, scheduled tasks, and personalities, who do work continuously and ask questions only when they are genuinely stuck.

Two audiences. The busy person who wants Agents that just work. The technical person who wants every knob exposed. Opinionated defaults serve the first. Advanced mode serves the second. Run it on your own hardware, or use the managed service. Same software either way.

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

## Status

**Spec phase, transitioning to build.** Fourteen architecture decisions locked. Prior-art analysis complete (twelve targets, executive doc plus deep findings appendix). The runtime kernel ([Epic 2](https://github.com/twentytwohundred/2200/wiki/02-agent-runtime-minimum)) is in active build with a UDS + JSON-RPC supervisor scaffold landing in PR review.

## Posture

| | |
|---|---|
| **License** | [Elastic License v2](https://github.com/twentytwohundred/2200/blob/main/LICENSE). Source-available. Use, copy, distribute, and create derivative works are permitted; hosting as a managed service to third parties and license-key tampering are prohibited. |
| **Build in public, eventually** | Repos are private during the spec and early-build phase. The full commit history surfaces at launch. |
| **Discipline** | Architecture Decision Records for every load-bearing call. Per-epic specs with explicit upgrade-readiness sections. Pattern-lift over code-lift, with attribution. Schema versioning everywhere. State on disk, not in memory. The conventions are documented, applied, and dogfooded. |
| **Team** | A small seed team of Agents and a product lead. The first Agent born on the platform is the launch moment. See [the seed-team doc](https://github.com/twentytwohundred/2200/wiki/04-seed-team). |

## Where to read

The full project knowledge base lives in the wiki. Read in order:

1. **[Vision](https://github.com/twentytwohundred/2200/wiki/01-vision)** — what 2200 is, who it is for, why it exists. Thirty-second pitch and the longer story.
2. **[Architecture](https://github.com/twentytwohundred/2200/wiki/02-architecture)** — nine-object model, runtime shape, how [OpenPub](https://github.com/douglashardman/openpub) and [SCUT](https://github.com/douglashardman/openscut) compose underneath. With diagrams.
3. **[Epic map](https://github.com/twentytwohundred/2200/wiki/03-epic-map)** — nineteen epics with scope, done-when criteria, and dependencies. The build sequence.
4. **[Seed team](https://github.com/twentytwohundred/2200/wiki/04-seed-team)** — who is building this, how they coordinate, when they migrate.

Then follow the wiki's [sidebar](https://github.com/twentytwohundred/2200/wiki/_Sidebar) into the decision records, conventions, and per-epic specs.

## Repositories

- **[twentytwohundred/2200](https://github.com/twentytwohundred/2200)** — runtime, project home, and wiki.

More repositories will be added as components ship. The 2200 runtime itself stays in `2200`.

## Contact

- **Web:** [2200.ai](https://2200.ai)
- **Email:** [hello@2200.ai](mailto:hello@2200.ai)
- **Security:** see [SECURITY.md](https://github.com/twentytwohundred/2200/blob/main/SECURITY.md) on the runtime repo for responsible disclosure.

---

<div align="center">

*Building 2200 is the biggest thing on the bench right now. Ship when ready, never before.*

</div>
