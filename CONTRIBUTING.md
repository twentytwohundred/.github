# Contributing

This is the org-wide contributing intro for `twentytwohundred`. Individual repos may have their own `CONTRIBUTING.md` with project-specific guidelines; when they do, the per-repo file takes precedence.

## During the build phase

The 2200 seed team is closed during the spec-and-early-build phase. Outside contributions are welcome after launch; until then:

- **GitHub Issues** are the right place for bug reports and feature requests on shipped functionality.
- **GitHub Discussions** open post-launch for broader conversation.
- **[hello@2200.ai](mailto:hello@2200.ai)** for security reports (see [SECURITY.md](SECURITY.md)).

## After launch

The contribution model carries forward the patterns established during the seed-team build:

- **Branching and PRs.** Feature branches named `<epic>/<short-description>` (or `<surface>/<short-description>` for non-epic work). Small focused commits with messages that explain the WHY. PR descriptions follow the project's PR template, including the upgrade-readiness checklist where relevant. Squash-merge once CI is green.
- **Decision records.** Load-bearing decisions land as Architecture Decision Records in the project's wiki. Format: `YYYY-MM-DD-short-name.md`. Sections: Context, Decision, Consequences, Implementation guidance, References.
- **Code conventions.** TypeScript strict, type-aware ESLint, Prettier, vitest. Document the WHY, not the WHAT. Schema versioning everywhere. State on disk, not in memory.
- **License posture.** Pattern-lift over code-lift. Code-lifts preserve the source's copyright notice and are documented in `THIRD_PARTY_NOTICES.md`. AGPL is incompatible.
- **Voice.** Ellipses, not em-dashes. Agent is a proper noun, always capitalized. Direct, factual, no marketing speak. See the [voice convention](https://github.com/twentytwohundred/2200/wiki/voice-and-framing) on the wiki for the full discipline.

See the per-repo `AGENTS.md` (when present) for project-specific conventions.

## Code of Conduct

By participating in any 2200 project, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).
