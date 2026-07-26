# Builder Context

This repository is the canonical context lineage for one Skillfoundry agent.
The harness runs inside this repository root. Fresh runtime instances may come
and go, but this context lineage remains the durable working mind.

## Front Door

- `memory/mission.md`
- `memory/profiles/builder.md`
- `memory/findings/current_target.md`
- `memory/plans/current_build.md`

This context is for building both internal Skillfoundry mechanisms and external
products. The current target is now the first external product candidate, while the
earlier internal mechanism remains part of the build history.

## Lifecycle and verification

Maintained, not currently an independently deployed service. The fastest
complete contract check is `make check`. See
[docs/architecture.md](docs/architecture.md) for authority boundaries and the
dated prompt-governance and runtime-path exceptions.
