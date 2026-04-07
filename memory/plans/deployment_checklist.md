# Deployment Checklist

## Hosting Shape

- hosted or local-first MCP server
- stable endpoint if hosted
- request logging and basic usage telemetry
- health check endpoint if the framework does not provide one automatically
- optional shared-secret gate for non-public access

## Pre-publish Requirements

- implement `tools/list` cleanly
- implement `analyze_signals`
- implement `draft_brief`
- add tests for tool discovery and representative success cases
- verify example prompts against real responses
- ensure operator documentation matches actual tool behavior

## Explicit Non-goal For This Mechanism

Do not turn this mechanism into a public listing by accident. Public launch work
belongs to the downstream product lane once a real product candidate is selected.

## Operational Questions

- Which runtime/framework is the simplest production-safe MCP server stack for this mechanism?
- Where should telemetry live for fast post-launch interpretation?
- What timeout and payload limits keep calls reliable and legible?
