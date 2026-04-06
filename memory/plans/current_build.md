# Current Build Plan

## Goal

Ship the first hosted MCP server candidate for Skillfoundry's AgenticMarket launch loop.

## Immediate Work

1. Translate the current target into a concrete MCP tool contract.
2. Choose the implementation stack and deployment shape.
3. Define request and response schemas for `analyze_signals` and `draft_brief`.
4. Add tests for tool discovery and core happy-path behavior.
5. Produce deployment and listing-readiness notes.

## Current Implementation Repo

- local repo: `/Users/evanfollis/projects/skillfoundry/bottleneck-radar-server`
- current status: local implementation scaffold exists with MCP app, tests, and Render deployment config
- remaining external blockers: deployment credentials and public remote setup

## Non-goals For V1

- broad workflow orchestration
- more than two public tools
- generalized market research automation beyond the chosen ICP

## Validation Bar

- `tools/list` is stable and legible
- example calls return structured, decision-useful output
- deployment path to public HTTPS is straightforward
- the resulting server can support the drafted AgenticMarket listing without copy drift
