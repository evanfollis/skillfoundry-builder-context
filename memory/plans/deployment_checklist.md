# Deployment Checklist

## Hosting Shape

- hosted HTTPS MCP server
- stable public endpoint
- request logging and basic usage telemetry
- health check endpoint if the framework does not provide one automatically

## Pre-publish Requirements

- implement `tools/list` cleanly
- implement `analyze_signals`
- implement `draft_brief`
- add tests for tool discovery and representative success cases
- verify example prompts against real responses
- ensure long description matches actual tool behavior

## AgenticMarket-specific Requirements

- choose final server identifier carefully
- choose initial price carefully
- verify URL stability before submit
- make long description README-quality
- launch unlisted first

## Operational Questions

- Which runtime/framework is the simplest production-safe MCP server stack for this launch?
- Where should telemetry live for fast post-launch interpretation?
- What timeout and payload limits keep calls reliable and legible?
