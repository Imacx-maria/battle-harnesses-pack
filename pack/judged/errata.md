# Judged Layer — Errata and Post-Gapfill Additions

S1-S10 named below are historical research notes; they are not visitor jobs
and are not in judged.md anymore. Do not treat those scenario labels as a
skill job list. The errata still correct dated supporting language.

```
errata_version: 2026-08-16
source: AI_OS/HANDOFFS/2026-08-16-judged-layer-research/23-addendum.md
```

judged.md verdicts stand; these errata correct dated supporting language and add
post-gapfill evidence rows. On any divergence, judged.md's verdicts win; on evidence
recency, this file wins.

Single-seat (Claude Opus 5), refereed in fresh context, reasoned over pack
`2026-08-16+9f224d9e` — the gap-fill wave that landed after judged.md was extracted. Nothing here
is a test result; `honesty.hands_on_observation_rows` is still `0`. Labels and inheritance as in
judged.md; conditions use vocabulary v2 only.

---

## 1. Errata to supporting language (no verdict changes)

### E1 — S5 `atomic`: the reviewer-rarity sentence

Dated: *"One of the few verdicts resting on reviewer-accepted evidence."* True when written
(accepted claims then sat on 4 Pi-lineage products, 244 of 244). The pack's honesty block now
reports 438 accepted / 2,102 unreviewed with `accepted_claims_by_product` non-zero on **all 27**
site products; `atomic`'s share is 70 of 72. `[corpus, index-level: index.json honesty block,
pack 2026-08-16+9f224d9e — not a single claim id]` Dense is not rare `[judgment]`.

Read instead: *"Rests on accepted evidence (70 of `atomic`'s 72 claims), as now does at least
some evidence on all 27 products — read `accepted_claims_by_product` from `index.json` at
runtime rather than reading this row's evidence base as rare."*

Verdict body and both citations unchanged, still `reviewer_status: accepted`
[corpus: `claim-atomic-orchestration`, `claim-atomic-durable-workflows`].

### E2 — S6/S3 `github-copilot`: the blanket 59-minute framing

Dated: *"**`github-copilot`** 59-minute hard cap (4/4 on the fact, 3/4 in S6)"* — read blank, it
implies the product has no unattended path past 59 minutes. The cap is real but scoped to the
**cloud agent**, single-repo, GitHub-hosted-only [corpus: `claim-github-copilot-sf-drawback`].

Read instead: *"**`github-copilot`** — 59-minute hard cap on each **cloud-agent session**,
single-repo, GitHub-hosted repositories only (4/4 on the fact, 3/4 in S6) [corpus:
`claim-github-copilot-sf-drawback`]. Agentic Workflows (public preview) is a second and different
object: markdown-defined repository automations that run as GitHub Actions workflows rather than
as cloud-agent sessions, under frontmatter guardrails for triggers, permissions and safe outputs
[corpus: `claim-github-copilot-gf-gc-agentic-workflows`]. The corpus states no duration cap for
them, in either direction. Read the 59-minute cap as scoped to cloud-agent sessions, not as a
proven ceiling on every unattended surface — and not as evidence of a path past it."*

Weaker-than-reputation verdict — excellent issue-to-PR robot, poor fleet — stands.

### E3 — S8: the four-daemon architectural affordance note

Dated: the list presents `goose serve`, `crush serve`, `qwen serve` and `opencode` API as four
equally plausible duplex daemons. `qwen serve` is contested: the launch-template page calls
v0.16-alpha local-only, single-user, bring-your-own bearer token, deferring containerized,
multi-host and TLS-fronted deployment to v0.16.x
[corpus: `claim-qwen-code-gf-qc-serve-local-only-alpha`], against the daemon page's LAN HTTPS Web
Shell reachable from a phone or tablet [corpus: `claim-qwen-code-sf-remote-access-serve`].

Read instead: *"...the plausible path to live voice runs through the duplex/serve-style daemons
(`goose serve`, `crush serve`, `opencode` API), not request-response CLIs. `qwen serve` belongs on
the list only with its contradiction attached; both readings kept, neither resolved."*

S8 no-verdict headline (4/4) stands.

---

## 2. Post-gapfill additions (single-seat, refereed)

Additive only. No verdict below promotes, demotes or averages anything in judged.md. Three table
rows; the `codex-family` item is a note, not a row (§3).

| scenario | product id | Conditions | Seats | Verdict | Label |
|---|---|---|---|---|---|
| S4 | qwen-code | `byok:yes`, `machines:1`, `agent_tenure:established` | **single-seat (addendum)** | Agent Arena: `/arena --models <a,b,c> "task"` dispatches several models on the same task as independent top-level agents, each in its own git worktree under `~/.qwen/arena/<session-id>/worktrees/<model-name>/` mirroring staged, unstaged and untracked files with no shared state; the user compares and merges a winner. Attempts differ by *model*, not by seed. Experimental; the docs warn it uses far more tokens. `byok:yes` is a documented product requirement — credentials are ModelStudio, third-party or custom-provider API keys and env vars, no product account login. Comparison and merge are the user's; no automated cross-review. **S4, not S1** — the S1 4/4 no-council headline is untouched, as is the existing weaker-than-reputation note on `claim-qwen-code-sf-orchestration-teams`. No uniqueness, vendor-spread or `data` condition is asserted. | [corpus: `claim-qwen-code-gf-qc-arena`, `claim-qwen-code-gf-qc-arena-worktrees`, `claim-qwen-code-sf-tag-byok`, `claim-qwen-code-sf-auth-strategy`] [judgment] |
| S6 | oh-my-pi | `oss:required`, `machines:1`, `unattended:supervised`, `agent_tenure:established` | **single-seat (addendum)** | Director-over-workers with a real supervision console: `/vibe` makes the top-level session a director whose tools are read/todo/`vibe_spawn`/`vibe_send`, controlling persistent background workers in fast or good tiers; Agent Hub is an interactive TUI over session subagents with roster, per-agent usage, transcript, steering, revive and kill. Best-documented *steering* surface in the corpus — **not** a walk-away story: vibe mode is mutually exclusive with plan and goal modes, exiting kills every worker in scope, and Agent Hub does not list the main agent. Hence `supervised`, never `walk-away`. MIT-licensed, so `oss:required` is met at product level. | [corpus: `claim-oh-my-pi-gf-omp-vibe-mode`, `claim-oh-my-pi-gf-omp-agent-hub`, `claim-oh-my-pi-license-mit`] [judgment] |
| S7 | zcode | `subs:one` or `byok:yes`, `machines:1` | **single-seat (addendum)** | Mechanism, not capacity: a repository wiki reads the codebase and generates a per-workspace architecture guide whose claims each carry a clickable source location — checkable against the tree rather than trusted, closer in kind to `aider`'s ranked repository map than to any window-size claim. Access is documented: a bound Z.ai/BigModel account with a GLM Coding Plan uses that plan and quota, or third-party/custom providers connect by API key on Anthropic- or OpenAI-compatible base URLs. **The rejected 1M-window promotion stays rejected** (judged.md §6 item 3), and the two-seat `zcode` abstention on licence-unknown and isolation-unknown (§6 item 7) is inherited in full. Untested, like everything in S7. | [corpus: `claim-zcode-gf-zc-repo-wiki`, `claim-zcode-sf-subscription-reuse`, `claim-zcode-sf-byok`] [judgment] |

Mandatory caveats on the `zcode` row:

- **Data path.** Generating the wiki sends code context — safety-filtered, read on demand — to the
  selected model service and stores the result in the workspace runtime environment; the page does
  not say the whole repository is sent, nor bound what is sent.
  [corpus: `claim-zcode-gf-zc-repo-wiki-data-path`] That path is chosen inference, so it triggers
  no `data` condition under v2 and no cited claim establishes a relay, third-party processor or
  training path beyond it. Missing is a documented *bound* on volume — get it before enabling; not
  a `data:sensitive` disqualification. [judgment]
- **Remote limit.** The wiki entry is hidden while a remote workspace is disconnected or read-only
  — weakest exactly where `zcode`'s S2 verdict is strongest.
  [corpus: `claim-zcode-gf-zc-repo-wiki-remote-limit`]

---

## 3. S2 note — `codex-family` Remote (weaker than reputation, single-seat)

A dedicated Codex Remote page says to use the ChatGPT mobile app with a connected Mac or Windows
PC, paired by QR code from Settings > Connections > Control this Mac or PC. A cockpit for a
machine you already have, not a route to a bigger box — the shape judged.md §6 item 2 already
resolved against `claude-code` Remote Control, applied here **by analogy, not as a fresh
verdict**. Useful under `machines:split` or `machines:many`, `os:macos` or `os:windows` (no Linux
host documented). No `subs` condition: the page states rollout- and workspace-dependent
availability, not a paid plan; the host computer must stay awake and online. Managed cloud tasks
remain a real **S3** route (`claim-codex-family-w2-surface-cloud`); this note weakens the S2
reading only. [corpus: `claim-codex-family-gf-cf-remote-page`] [judgment]

---

## 4. PROPOSED `cloud` boundary sentence — awaiting Maria's sign-off (NOT signed)

**Binds nothing until signed.** Not part of vocabulary v2; no row in the pack is conditioned on
it. Context: the OpenHands agent server can be deployed on Modal, a third-party managed container
host, as a remote Agent Canvas backend on a user-held account
[corpus: `claim-openhands-gf-oh-modal-backend`], with a documented warning that anyone holding the
API key can execute arbitrary code on it [corpus: `claim-openhands-gf-oh-modal-key-risk`].

> A deployment is `cloud:yes` whenever the machine executing the agent is **operated** by someone
> other than the user, whatever the software on it and whoever holds the account: a self-deployed
> agent server on a third-party managed container host (`openhands` on Modal) is `cloud:yes`
> even though the user chose the image, holds the account, and could run the identical server on
> their own box — the test is who operates the host, never who configured or paid for it; such
> self-deployed-on-rented-host cases are recorded as `cloud:yes` with the self-hosted software
> shape noted inside the reasoning, and the API-key-holder-executes-arbitrary-code exposure is
> carried with them as the reason the line is drawn at operation rather than ownership.

Left open: whether a rented single-tenant VM the user administers end-to-end falls the same way as
a managed container platform. As drafted, yes — stricter than some readers expect, and a call to
be signed rather than assumed.
