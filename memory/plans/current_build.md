# Current Build Plan

## Goal

Ship the first external MCP product candidate for Skillfoundry's AgenticMarket launch
lane.

## Immediate Work

1. Translate the current target into a concrete MCP product contract.
2. Implement the V1 tool surface for `audit_launch_readiness` and `draft_launch_package`.
3. Add tests for tool discovery and representative builder-facing outputs.
4. Produce deployment and listing-readiness notes.
5. Keep the product implementation clearly separated from internal mechanisms.

## Current Implementation Repo

- local repo: `/Users/evanfollis/projects/skillfoundry/skillfoundry-products`
- product path: `products/launchpad-lint`
- current status: product is deployed for preview at
  `https://skillfoundry.synaplex.ai/products/launchpad-lint/`
- remaining blockers: top up AgenticMarket, validate one real two-call activation path,
  and switch to `AGENTICMARKET_SECRET` after marketplace approval

## Non-goals For V1

- broad workflow orchestration
- more than two public tools
- generalized launch automation outside the chosen ICP
- solving every marketplace edge case in the first release

## Validation Bar

- `tools/list` is stable and legible
- example calls return structured, launch-useful output
- deployment path to a public HTTPS endpoint is straightforward
- the resulting server can support an AgenticMarket listing without obvious copy drift
