# Current Build Plan

## Goal

Ship the first internal MCP mechanism candidate for Skillfoundry's opportunity
selection loop.

## Immediate Work

1. Translate the current target into a concrete MCP tool contract.
2. Choose the implementation stack and deployment shape.
3. Define request and response schemas for `analyze_signals` and `draft_brief`.
4. Add tests for tool discovery and core happy-path behavior.
5. Produce deployment and operator-readiness notes.

## Current Implementation Repo

- local repo: `/Users/evanfollis/projects/skillfoundry/skillfoundry-products`
- mechanism path: `mechanisms/bottleneck-radar`
- current status: local implementation scaffold exists with MCP app, tests, and a simple hosted deployment config
- remaining blockers: finalize internal deployment posture and wire the monorepo remote

## Non-goals For V1

- broad workflow orchestration
- more than two mechanism tools
- external pricing or listing work before a downstream product is selected

## Validation Bar

- `tools/list` is stable and legible
- example calls return structured, decision-useful output
- deployment path to an internal or shared-secret HTTPS endpoint is straightforward
- the resulting server produces briefs clean enough to feed later product work without
  copy drift
