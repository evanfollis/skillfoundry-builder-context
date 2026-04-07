# Bottleneck Radar Mechanism Contract

## Goal

Implement an MCP mechanism that helps technical builders move from noisy product
signals to ranked bottlenecks and concise opportunity briefs.

## Mechanism Tools

### `analyze_signals`

Purpose:

Cluster source signals into ranked bottlenecks with evidence-backed summaries.

Inputs:

- `sources`: array of objects
  - `kind`: `url` or `text`
  - `value`: URL string or pasted signal text
- `target_user`: optional string
- `max_clusters`: optional integer, default `5`

Outputs:

- `target_user`
- `clusters`: array
  - `cluster_id`
  - `title`
  - `pain_summary`
  - `evidence_snippets`
  - `confidence`
  - `why_now`
  - `suggested_next_question`

### `draft_brief`

Purpose:

Turn one selected bottleneck cluster into a concise opportunity brief.

Inputs:

- `cluster_title`
- `pain_summary`
- `evidence_snippets`
- `target_user`
- `distribution_surface`: default `chosen distribution surface`

Outputs:

- `product_name`
- `target_user`
- `problem_statement`
- `narrow_solution`
- `tool_surface`
- `deployment_constraints`
- `pricing_hypothesis`
- `open_questions`

## V1 Guardrails

- Return structured JSON-friendly content only.
- Optimize for clarity and usefulness over novelty.
- Do not expose more than the two mechanism tools above in V1.
- Keep output small enough to be readable in one client response.

## Non-goals

- full web crawling
- persistent user accounts
- internal stateful project management
- external launch packaging or pricing work
