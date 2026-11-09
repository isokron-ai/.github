<p align="center">
  <a href="https://isokron.ai"><img src="isokron-logo.png" alt="IsoKron" width="276"></a>
</p>

# IsoKron

**MCP servers that agents can safely change things through.** We audit and build
[Model Context Protocol](https://modelcontextprotocol.io) servers, and we publish the
research and tools behind that work.

An MCP server is part of the system's correctness boundary. A tool can return a perfectly
formatted success while it overwrites someone else's edit, changes the wrong object, drops
fields the caller never mentioned, or does nothing at all. Our work tests for exactly that:
concurrent and stale writes, preconditions, partial failure, honest results, and the extra
calls and turns that clumsy tools cost an agent.

## Research

| | |
| --- | --- |
| [GitHub MCP server v2.1.0 audit](https://isokron.ai/research/github-mcp-server-audit) | Concurrent issue-field updates lost a change in 19 of 30 pairs while both calls reported success. 17 findings, 13 reported upstream, and a before/after benchmark. |
| [How to test an MCP server without fooling yourself](https://isokron.ai/research/how-to-test-an-mcp-server) | The rules our audits run under and the refutation funnel every claim passes through. |
| [Verify an audit's evidence yourself](https://isokron.ai/research/verify-mcp-audit-evidence) | Check an IsoKron Evidence Pack offline with one command. |
| [Why MCP tool design matters](https://isokron.ai/research/why-mcp-tool-design-matters) | What a clumsy tool really costs: accuracy, failed runs, time and plan limits. |
| [Shipping a production MCP server](https://isokron.ai/research/production-mcp-server) | Auth, per-user limits and tracing on the 2026-07-28 spec. |

## Open source

| Repository | What it does |
| --- | --- |
| [github-mcp-writepath-experiment](https://github.com/isokron-ai/github-mcp-writepath-experiment) | The changes behind our GitHub MCP server before/after benchmark, as a build and a patch series. Research only; not affiliated with GitHub. |
| [kronicle-lite](https://github.com/isokron-ai/kronicle-lite) | Local-first MCP server: hash-chained document store, signed receipts, and the `verify-audit` command that checks an Evidence Pack offline. |
| [sea-lite](https://github.com/isokron-ai/sea-lite) | MCP work queue for parallel coding agents: claim fencing, path-scoped claims and atomic batches. |
| [mcp-catalog-snap](https://github.com/isokron-ai/mcp-catalog-snap) | Snapshot an MCP server's tool catalog as canonical JSON and fail CI on drift. |
| [cc-anchor](https://github.com/isokron-ai/cc-anchor) | Claude Code plugin: an anchor card that survives context compaction. |

## How we report what we find

Findings go to the maintainers first, with a reproduction and, where practical, a fix.
Security-sensitive findings go through the vendor's own security process and stay private
until it is resolved. Every claim in a write-up is one that survived an attempt to disprove it.

## Work with us

Fixed-price [MCP server audits](https://isokron.ai/mcp-audit) and
[MCP server builds](https://isokron.ai/mcp-development). See a
[sample report](https://isokron.ai/sample-report), or write to
[hello@isokron.ai](mailto:hello@isokron.ai).

<sub>IsoKron is a brand of Stormhaven Enterprises LLC.</sub>
