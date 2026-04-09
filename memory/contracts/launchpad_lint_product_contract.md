# Launchpad Lint Product Contract

## Goal

Implement an MCP product that helps technical builders turn a working MCP server into
a launch-ready package for marketplaces such as AgenticMarket.

## Public Tools

### `audit_launch_readiness`

Purpose:

Audit a candidate server package and identify blockers to a credible public launch.

Inputs:

- `server_name`
- `tool_names`: array of strings
- `tool_descriptions`: array of strings
- `readme_text`: optional string
- `listing_draft`: optional string
- `endpoint_url`: optional string

Outputs:

- `readiness_score`
- `blockers`: array of strings
- `warnings`: array of strings
- `strengths`: array of strings
- `suggested_fixes`: array of strings

### `draft_launch_package`

Purpose:

Draft the minimum launch package needed for a clear first marketplace submission.

Inputs:

- `server_name`
- `target_user`
- `tool_names`: array of strings
- `tool_descriptions`: array of strings
- `positioning_hints`: optional array of strings
- `constraints`: optional array of strings

Outputs:

- `short_description`
- `long_description`
- `example_prompts`: array of strings
- `explicit_limits`: array of strings
- `pricing_questions`: array of strings

## V1 Guardrails

- Return structured JSON-friendly content only.
- Keep the product narrow and builder-facing.
- Do not expose more than the two public tools above in V1.
- Optimize for actionable audit and draft quality over clever language.

## Non-goals

- final pricing decisions
- automated server submission
- billing or payout management
- broad GTM orchestration beyond the first launch package
