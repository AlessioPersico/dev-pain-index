![dev-pain-index](assets/banner.png)

# Validated Developer Pain Signals — Week of August 24, 2026

![Updated weekly](https://img.shields.io/badge/updated-every%20monday-3ddc84) ![License](https://img.shields.io/badge/report%20license-CC%20BY%204.0-blue) ![Source](https://img.shields.io/badge/source-41%2C378%20clustered%20complaints-06080d)

10 developer pains worth building for, ranked by **distinct companies affected**,
not upvotes. Every row links to public issues you can read yourself.
Arrows show the last 7 days against the prior 7.
Sources: GitHub Issues, Stack Overflow, Hacker News, Bluesky.

| # | Pain | Companies | 7d | Type |
|---|------|-----------|----|------|
| 1 | One component error takes down the whole page, no boundary, no recovery | 58 | ↑ 0 → 2 | feature request |
| 2 | E2E testing is the first thing teams cut and the first thing that bites them | 57 | ↓ 6 → 2 | feature request |
| 3 | API endpoints shipped with no rate limiting | 56 | → steady | bug |
| 4 | Documentation links rot faster than anyone fixes them | 40 | ↓ 8 → 1 | bug |
| 5 | MCP tools that connect but don't behave (visibility, naming, schemas) | 38 | ↓ 5 → 4 | bug |
| 6 | OAuth flows that break exactly where you can't debug them | 31 | ↓ 6 → 0 | complaint |
| 7 | No good way to find, install and version MCP servers | 30 | ↓ 2 → 1 | complaint |
| 8 | CI pipelines that gate nothing or flake constantly | 24 | ↓ 11 → 7 | bug |
| 9 | Access tokens expire and the frontend never refreshes them | 18 | ↑ 0 → 2 | complaint |
| 10 | AI agents forget everything between sessions | 17 | ↓ 4 → 1 | feature request |

**New this week:** #1 (error boundaries) and #9 (token refresh).
**Dropped:** single-step admin transfer and npm peer dependency resolution, both now below the cut.

## The evidence

<details>
<summary><b>1. Missing error boundaries (58 companies)</b></summary>

- "An unexpected component error may cause a large section of the application to become unusable. Users may see a blank or broken page" — [Stellar-Royalty-Splitter#702](https://github.com/Just-Bamford/Stellar-Royalty-Splitter/issues/702)
- "Add App Router error, not-found and loading boundaries with client error reporting, with branded recoverable fallbacks and a retry action" — [Invoisio#462](https://github.com/ZyntariHQ/Invoisio/issues/462)
- "Add skeleton loading states and error boundary components across all data-fetching pages" — [StudyMatePlus#717](https://github.com/lovelymahor/StudyMatePlus/issues/717)
</details>

<details>
<summary><b>2. E2E testing (57 companies)</b></summary>

- "e2e: repair the 44 quarantined end-to-end tests" — [upnext-frontend#248](https://github.com/binhphanbp/upnext-frontend/issues/248)
- "CI never runs the sealed acceptance suite — a red slice sat on main for a day" — [coord-portal#77](https://github.com/JDonaghy/coord-portal/issues/77)
- "[P1] Add deterministic frontend E2E and accessibility gates" — [little-mere-news#12](https://github.com/Gyliardson/little-mere-news/issues/12)
</details>

<details>
<summary><b>3. Missing rate limiting (56 companies)</b></summary>

- "Extend the Redis sliding-window guard to cover proxy endpoints: per-user limit on balance-fetch and FX-rate, per-IP on unauthenticated auth endpoints, 429 with Retry-After" — [AfroPay-Stellar#204](https://github.com/Afro-Pay/AfroPay-Stellar/issues/204)
- "Add rate limiting to create-payment, the Companies House proxy, both PDF routes and the public accept/sign actions" — [motkoquote#97](https://github.com/jacobabuckland/motkoquote/issues/97)
- "A blanket per-session limit treats lightweight GET reads identically to heavy AI reasoning POSTs" — [faultmaven#994](https://github.com/FaultMaven/faultmaven/issues/994)
</details>

<details>
<summary><b>4. Broken documentation links (40 companies)</b></summary>

- "README links to missing docs/screenshot.png" — [beam#243](https://github.com/frecar/beam/issues/243)
- "Merged route sources link to nonexistent anchor" — [pokemon-sims#3419](https://github.com/FlareZ123/pokemon-sims/issues/3419)
- "Two stale index.md line references, already wrong at origin/main" — [insight-wave#1435](https://github.com/cogni-work/insight-wave/issues/1435)
</details>

<details>
<summary><b>5. MCP tool reliability (38 companies)</b></summary>

- "Every MCP tool call fails with ENTITY_VISIBILITY_ENFORCED (entity-independent tools included)" — [ha-mcp#2228](https://github.com/homeassistant-ai/ha-mcp/issues/2228)
- "The MCP server never publishes tool annotations or output schemas" — [platform#561](https://github.com/ProAgentStore/platform/issues/561)
- "MCP tools with hyphens in tool names fail via standard dispatcher" — [jcode#936](https://github.com/1jehuang/jcode/issues/936)
</details>

<details>
<summary><b>6. OAuth breakage (31 companies)</b></summary>

- "MCP OAuth authorization URL never surfaced in remote environments, connection times out" — [Kiro#10817](https://github.com/kirodotdev/Kiro/issues/10817)
- "Custom HTTP MCP servers cannot enter preregistered OAuth client secrets" — [zed#62553](https://github.com/zed-industries/zed/issues/62553)
- "OAuth callback responds 400 missing nonce. The nonce is present in the callback URL" — [platform#135](https://github.com/proappstore-online/platform/issues/135)
</details>

<details>
<summary><b>7. Finding and installing MCP servers (30 companies)</b></summary>

- "Show HN: Pharos, a package manager for MCP servers. Search across all registries in one place, install with dependency resolution" — [pharos-cli](https://github.com/Wpnx330/pharos-cli)
- "[epic] MCP for third-party clients: partner secret keys, OAuth front door, per-token scopes" — [v2#1306](https://github.com/Jaal-Yantra-Textiles/v2/issues/1306)
- "Discoverable MCP: agents can only ever use the tools they were pre-configured with. MCP allows tool discovery but doesn't solve the registry problem" — [ore#247](https://github.com/andrewhowdencom/ore/issues/247)
</details>

<details>
<summary><b>8. CI pipelines gating nothing (24 companies)</b></summary>

- "Recurrent CI flakes: CPU-efficiency below threshold on unrelated heads" — [gomap#4183](https://github.com/snissn/gomap/issues/4183)
- "Push validation misaligned with documented branch lanes: no Actions run for its head" — [workbench-kit#283](https://github.com/NewChoBo/workbench-kit/issues/283)
</details>

<details>
<summary><b>9. Access token refresh (18 companies)</b></summary>

- "Frontend token refresh is broken and never invoked: sessions end at the 15-minute access-token expiry" — [NovaLabs#233](https://github.com/NovaCoreLabs1/NovaLabs/issues/233)
- "Token refresh failure leaves stale authentication state and does not redirect users to the login page" — [CropChain#967](https://github.com/Nitya-003/CropChain/issues/967)
- "[frontend] No access token refresh, silent auth failures" — [ArenaX#718](https://github.com/Arenax-gaming/ArenaX/issues/718)
</details>

<details>
<summary><b>10. AI agent memory (17 companies)</b></summary>

- "Feature Request: Portable Memory Transfer for MCP Agents" — [sarvam-mcp#75](https://github.com/sarvamai/sarvam-mcp/issues/75)
- "Agents that forget everything between conversations cannot act as co-workers" — [aihub-core#1710](https://github.com/bbvch-ai/aihub-core/issues/1710)
</details>

## How this is generated

Complaints from GitHub / Stack Overflow / Hacker News / Bluesky are clustered
nightly with NLP into 41,378 tracked pain signals, then ranked by **distinct
companies affected** (owner count), not by upvotes. 316 signals currently span
5+ independent products, roughly 1% of everything tracked.

Three things worth knowing about the selection:

**Some linked issues are closed.** That counts as evidence the pain cost someone
engineering hours, not that the market solved it.

**Wider is not always better.** A growing share of GitHub issues are written by
coding agents, and agent-written backlog text is formulaic enough to cluster
across completely unrelated repos. Several of the widest clusters in the corpus
(160+ owners) are mostly that, and they are held back. This week that filter also
removed a CI/CD cluster at 49 owners and a benchmarking cluster at 21.

**Pure UI polish is left out on purpose.** Contrast ratios and theme toggles are
real bugs, but they are implementation work, not markets.

Generated with [EchoSift](https://echosift.io). Full board: 41,000+ clusters,
MCP server for your coding agent included.

---

⭐ **Star** if this saved you research time
🔔 **Watch → Custom → Releases** to get next Monday's drop

Report license: CC BY 4.0. Quotes belong to their authors, linked above.
