# Judged Layer — Battle Harnesses

```
judged_version: 2026-08-17+no-s1s10
source: judged-layer research synthesis, referee pass over four independent researcher seats, dated 2026-08-16
extracted: 2026-08-16
```

This file is product judgment for the visitor skill: clusters, live disagreements, and contested facts. A visitor's agent reads it from the pack. S1-S10 research scenarios are NOT in this file; they live only in the internal synthesis (AI_OS/HANDOFFS/2026-08-16-judged-layer-research/20-synthesis.md); they are not visitor jobs; the site does not run them.

Sections 1–3, 8, and 9 of the source synthesis (seat discards, baseline dimensions, the
deviation map, the corpus gap list, and vocabulary proposals) are internal research
bookkeeping and are not reproduced here. Section numbers below match the source document.

---

**Binding evidence posture.** This document is bound by the pack's own honesty block, not
by any number frozen here. Read `honesty` and `counts` from `index.json` at runtime and
restate its numbers. Nothing below is a test result — every judgment is reasoned
judgment over documented claims. Check reviewer-status concentration yourself: if accepted
claims cluster on a small set of products, any comparison between that cluster and anything
else compares reviewed evidence against unreviewed evidence — the report must show that
asymmetry, not hide it.

**Label inheritance.** `[corpus]` cites a pack claim or dossier field; `[external]` carries a
URL and date from a seat; `[judgment]` is reasoned opinion. A row inherits the weakest label
in its chain: judgment built on judgment stays `[judgment]`. Where a cell rests on unreviewed
official-docs, `[corpus]` means "the pack documents this," never "verified."

---

## 4. Clusters — same loop, different hat

The corpus supplies exactly one recorded neighborhood; every other grouping below is seat
judgment refereed against the relationship edges. Grouping rule enforced: catalogue groups
are editorial placement; edges are the lineage facts.

### 4.1 Pi lineage — one recorded neighborhood, not four interchangeable products

`pi`, `atomic`, `oh-my-pi`, `prime-agent`. [corpus: `neighborhood-pi-lineage-terminal-runtimes`;
edges `atomic --fork_of--> pi`, `oh-my-pi --fork_of--> pi`, `prime-agent --built_on--> pi`]
All four seats converge, hard: membership proves lineage, not feature parity. Only
`oh-my-pi` is "Pi with batteries" — same spine, opposite loadout. `atomic` is a durable
workflow engine that happens to be a Pi fork. `prime-agent` is a different computational
model (persistent IPython RLM) that happens to be built on Pi. [judgment, 4/4 seats]
Presenting these four as substitutes is the most likely error a lineage-driven UI makes.

### 4.2 Lab-owned terminal runtimes — the strongest "same hat" set

`claude-code`, `codex-family`, `gemini-cli`, `grok-build`, `qwen-code`,
`google-antigravity`. Same tool set, same skills spec, same hooks-and-MCP stack, same
threshold compaction, same ask-first default, same opt-in-sandbox posture. What differs:
default lab model, how many non-terminal surfaces the vendor bolted on, and the licence.
`qwen-code --fork_of--> gemini-cli` is a recorded edge — two of these are the same codebase
in origin. Inside the cluster, `google-antigravity` is the one architectural departure
(Artifacts as the review object) and the corpus records it as the consumer successor after
`gemini-cli`'s consumer access ended 2026-06-18. [corpus: edges; `claim-gemini-cli-sf-consumer-ended-2026-08-15`]
[judgment: grouping — one seat proposed 4 members, another proposed 6; adopted at 6]

### 4.3 Provider-neutral independent terminals

`crush`, `opencode`, `goose`, `aider`, with `deepseek-harness` at the economic edge.
`crush` and `opencode` are the closest true near-substitutes in the corpus — terminal
runtime, broad BYOK, local models, MCP/skills/hooks, serve/attach API, no agent sandbox —
down to a recorded credential bridge (`crush --reuses_auth_from--> opencode`). Real
distinctions: licence (FSL-1.1-MIT vs MIT) and context feed (LSP vs plain reads). `aider`
and `goose` sit here by economics, not architecture: `aider` deviates on context and
decomposition; `goose` on loop ownership (ACP handoff) and gating (autonomous default).
[corpus: edges and licence claims] [judgment: grouping — three seats convergent]

### 4.4 Editor/desktop verticals — and the mislabeled lineage

`cline` and `kilo-code` share the catalogue group `cline-lineage-editor-agents`; `cursor`,
`github-copilot`, and `zcode` share the shape (one agent core behind an editor/desktop, a
CLI, a cloud runner, messaging) by judgment. **The "Cline-lineage" label is editorial, not
code lineage** [corpus: the only recorded fork edge into this set is
`kilo-code --fork_of--> opencode` (the CLI); no
cline fork edge exists; `cursor` and `zcode` have no fork edge at all]. One seat's
correction is adopted; all four seats' evidence is consistent with it. `kilo-code` straddles
4.3 and 4.4: an OpenCode-derived terminal wearing a Cline-shaped editor hat — any UI that
puts it in exactly one cluster loses information. [judgment: one seat, adopted]

### 4.5 Control planes — identifiable by their silence

`conductor`, `t3-code`, `symphony`. None owns a loop [corpus: the three
`agent_loop_owner` claims]. Their structural signature is per-product: `conductor` compaction is `unknown`; `symphony` compaction is `unknown`; `t3-code` has no context_behavior / compaction / MCP / skills / hooks claim row. `conductor` and `symphony` have documented context and memory — do not call those unknown. The cluster still holds on the three `agent_loop_owner` claims. That silence, where it is real, is the shape of a product that owns no loop — read it as architecture, not missing research. [judgment: one seat, adopted]

They are **not** one product. They differ by unit of work: `conductor`'s unit is a
workspace a human picks (macOS app over local worktrees or vendor sandboxes, review/PR
lifecycle); `t3-code`'s is a thread on a server the user owns (five wrapped CLIs; desktop/
web/iOS/Android cockpit); `symphony`'s is an issue in a tracker (codex-family only, no
interactive steering). [corpus: `claim-conductor-sf-architecture`,
`claim-t3-code-sf-architecture`, `claim-symphony-sf-what-it-is-spec`] One seat's
"conductor and t3-code are the same job" is a labeled judgment about job-similarity, not
architecture; it is flagged in section 6, not adopted — confusing them is exactly how S2
and S3 get blurred.

### 4.6 Split-brain vendor runtimes

`amp` and `devin`. The model-and-thread brain lives in the vendor cloud even when tools run
on your machine. `amp` keeps a real local CLI executor; `devin` is cloud-primary and
refuses customer LLM keys. **`amp` is not an independent local runtime in the architectural
sense**: its catalogue group says `independent-local-runtimes`, its loop-owner claim says
Amp Server authorizes inference and stores threads. All four seats flag the tension; the
loop-owner claim is the architecture fact. [corpus: `claim-amp-sf-agent-loop-owner`,
`claim-devin-sf-what-it-is-not-byok` vs the `catalogGroup` field]

### 4.7 Delegated cloud pair — same job, opposite construction

`devin` and `openhands` share a catalogue group because they share a user job (hand off a
task, get a PR back), not an architecture: `devin` is closed at both ends (vendor Brain, no
BYOK); `openhands` is MIT, LiteLLM-based, runs on your own Docker, and can even pilot other
harnesses over ACP. The group label must not imply privacy or licensing similarity.
[corpus: licence/model-strategy claims] [judgment: two seats, adopted]

### 4.8 Structural singletons

Grouping these costs information (3–4 seats each):

| product id | Why it is alone | Label |
|---|---|---|
| prime-agent | Persistent IPython as the model-facing control environment; context is a Python variable; the harness rewrites itself between runs. | [corpus: `claim-prime-agent-context-behavior`, `claim-prime-agent-memory`] |
| deepseek-harness | Everything is a Cordis plugin including the agent loop; the session log is the context. Architecturally the most interesting product in the corpus and a breaking-changes developer preview. | [corpus: `claim-deepseek-harness-sf-agent-loop`, `claim-deepseek-harness-sf-status-breaking`] |
| atomic | Versioned workflow graphs with DBOS/Postgres durable replay — nothing else in the corpus has durable replay. | [corpus: `claim-atomic-durable-workflows`] |

Near-singletons: `aider` (the ranked repository map — a different context machine in an
otherwise baseline terminal), `google-antigravity` (Artifacts as the review object — the
only product that changes what the user reads), `symphony` (the issue tracker as the
control plane — also in 4.5). [corpus: cited above] [judgment: merged from two seats'
singleton lists]

### 4.9 Cross-cutting shapes (not clusters)

- **Split-loop remote control.** Ten products document a phone/browser/second-desktop
  supervising a loop running elsewhere: `claude-code`, `codex-family`, `cursor`, `amp`,
  `github-copilot`, `kilo-code`, `factory-droids`, `t3-code`, `zcode`, `oh-my-pi`. This is
  architecturally distinct from cloud execution; S2 and S3 are different scenarios because
  of it. [corpus: execution-topology data across surfaces] [judgment: one seat, adopted]
- **One runtime fanned across many surfaces.** The vendor verticals (`claude-code` 34
  surface rows, `cursor` 25, `qwen-code` 21, `codex-family` 20) are internally "the same
  product wearing different hats"; the differentiators are execution-location options and
  model openness, not the loop. [corpus: surfaces_summary counts] [judgment: one seat,
  adopted as a shape rather than a cluster]

---

## 5. Scenario verdict matrix (S1-S10)

Removed from the visitor pack on 2026-08-17.

S1-S10 were offline research scenarios used to build the corpus. They are not visitor jobs and they are not a site feature. The full matrix lives only in the internal synthesis:

AI_OS/HANDOFFS/2026-08-16-judged-layer-research/20-synthesis.md

A visitor's agent must not use those scenarios as a job list. Judge from the honesty block, clusters (section 4), live disagreements (section 6), contested facts (section 7), the unique-job add rule, and this person's actual inventory.

---

## 6. Live disagreements

Flagged, not averaged. Each entry states the positions, the corpus reading, and — where the
scenario definition settles it — the editorial resolution with its label.

1. **`claude-code` agent teams in S1.** One seat: positive verdict (a council on one
   subscription). The other three: weaker than reputation (experimental; same-model-family
   teammates fail the scenario's "multiple models" note). Corpus: teams documented and
   experimental; model strategy Claude-only. **Resolution: carried as weaker-than-
   reputation because S1's own definition requires multiple models; that first seat's
   verdict stands in its own file for a reader who drops that requirement.** [judgment]
2. **`claude-code` in S2.** One seat: positive (Desktop SSH + Remote Control keep execution
   local). A second seat: weaker for this scenario (Remote Control is a cockpit for the
   laptop you already have, not a route to a beefier box; SSH resume unknown). Facts agree;
   the dispute is whether supervising your own laptop satisfies "work runs on a beefier
   box." **Resolution: the second seat's reading matches the scenario note; the first
   seat's Desktop-SSH route preserved as a real but resume-unknown path.** [judgment]
3. **S7 promotions without hands-on rows.** One seat promotes `crush` (LSP context) to
   first place; a second seat promotes `cursor` (backend indexing) and `zcode` (1M window);
   a third seat explicitly refuses to promote any of these on mechanism folklore; the first
   seat separately rejects all window-size arguments. **Resolution: `crush` carried as a
   labeled single-seat verdict (the LSP claim is specific and structural); window-size
   promotions not carried; all of S7 wears the zero-hands-on header.** [judgment]
4. **A1 for `claude-code`: `closed` (two seats) vs `vendor-first` (the other two).** 2–2.
   The corpus documents Bedrock, Google Cloud Agent Platform, Microsoft Foundry, and org
   gateways [corpus: `claim-claude-code-w2-provider-support`] — an escape hatch on billing,
   residency and procurement, never on model family. The axis definition does not settle
   whether that counts. **Contested — both positions carried (section 7). The two readings
   give opposite answers for an enterprise reader with an existing cloud commitment.**
5. **A1 for `grok-build`: `open` (two seats) vs `vendor-first` (the other two).** 2–2.
   Facts agree (xAI-first defaults; documented OpenAI-compatible and Anthropic Messages
   custom endpoints). The dispute is definitional: does a documented custom-endpoint route
   make a first-party-default product `open`? **Contested — both positions carried; the
   axis definition needs sharpening.**
6. **Are `conductor` and `t3-code` "the same job"?** One seat: yes — multi-harness mission
   control as a macOS app vs an MIT server. The other two: structurally distinct (vendor
   sandboxes + review/PR lifecycle vs user-hosted server + device cockpit; different unit
   of work). Corpus supports the structural distinction. **Resolution: clusters keep them
   as one control-plane family with different units of work; the "same job" framing is
   preserved as that first seat's labeled judgment, useful at the job-to-be-done level
   only.**
7. **`zcode` verdicts vs abstentions.** One seat issues S2/S7/S10 verdicts; the other two
   refuse all `zcode` verdicts (licence unknown, isolation unknown, zero accepted claims).
   **Resolution: one of that first seat's verdicts carried (S2, the strongest) with the
   abstention warning attached; the rest not carried.**
8. **S9 scope.** One seat treats messaging-channel inheritance as a real dictation answer;
   the other two treat anything outside a first-party voice surface as accessory judgment,
   not a product verdict. **Both carried with labels; the scope decision (does OS/inherited
   dictation count?) goes to Maria.**
9. **`amp`'s catalogue placement.** All four seats agree the loop-owner claim contradicts
   the `independent-local-runtimes` catalogue group. Not a seat-vs-seat disagreement — a
   corpus-label tension the site must resolve.

---

## 7. Contested facts

### 7.1 Seat-vs-seat, corpus silent or ambiguous — `contested`, both positions kept

| Fact | Position A | Position B | Corpus state |
|---|---|---|---|
| A1 `claude-code` | `closed` — vendor models only, whatever the pipe (two seats) | `vendor-first` — Bedrock/GCAP/Foundry/gateways are real procurement escape hatches (the other two) | Routes documented [corpus: `claim-claude-code-w2-provider-support`]; the axis definition does not decide which reading is right |
| A1 `grok-build` | `open` — custom OpenAI-compatible and Anthropic endpoints documented (two seats) | `vendor-first` — xAI-first defaults; endpoints are configuration, not positioning (the other two) | Both facts in the pack [corpus: `claim-grok-build-sf-provider-support`]; definitional |
| A1 `codex-family` | `open` on local surfaces — API keys, custom providers, Ollama, LM Studio, Bedrock (one seat; a second, "open locally") | `vendor-first` — every cloud feature requires ChatGPT auth (the other two) | Surface-split is itself the documented fact [corpus: `claim-codex-family-w2-provider-support`, `claim-codex-family-w2-auth`]; the honest site cell is per-surface, not per-product |
| A2 `crush` "open source" tag | Tag it open source — the pack records FSL-1.1-MIT as the licence, not a proprietary ToS (one seat; a second leaning that way) | Source-available, not OSI open source — FSL restricts competing use until MIT conversion (the other two) | Licence text is undisputed [corpus: `claim-crush-sf-license`]; the tag taxonomy is the dispute. Same issue, milder, for `atomic`'s MIT-plus-display-condition [corpus: `claim-atomic-license-terms`] |

### 7.2 Corpus-internal first-party contradictions — carried, never averaged

The pack's own rule: keep both sides. These conditioned multiple verdicts above.

| Product | Contradiction | Claim ids |
|---|---|---|
| oh-my-pi | `yolo` documented as default vs ACP/README permission wording; flagged in the recorded neighborhood | `claim-oh-my-pi-approval-policy` (accepted) vs the dossier's noted conflict |
| grok-build | Subagents default-on per docs vs `GROK_SUBAGENTS=0` env default; also version (changelog v1.0.3 vs crate 1.0.4, empty Releases) and rewind (Sessions page vs changelog) | `claim-grok-build-sf-subagents-docs-default` vs `claim-grok-build-sf-subagents-env-default`; `claim-grok-build-sf-version` vs `claim-grok-build-sf-version-crate` |
| kilo-code | Hosted Code Reviewer marketed vs agents docs saying VS Code/CLI ship no Review agent; Orchestrator deprecated vs CLI copy; cloud-compute billing dates conflict | `claim-kilo-code-sf-surface-code-reviewer` vs `claim-kilo-code-sf-agents-docs-no-review`; `claim-kilo-code-sf-cloud-compute-date` |
| google-antigravity | Plans page denies BYOK vs CLI/SDK documenting `GEMINI_API_KEY` and custom endpoints; MCP `url` docs vs changelog; CLI licence undeclared with an independent source disputing openness (the corpus's only independent-source claim) | `claim-google-antigravity-sf-no-byok` vs `claim-google-antigravity-sf-cli-gemini-api-key`; `claim-google-antigravity-sf-license-cli-undeclared`, `claim-google-antigravity-sf-closed-source-accusation` |
| gemini-cli | Consumer access ended 2026-06-18 vs official quota docs still listing consumer plans at the 2026-08-10 check | `claim-gemini-cli-sf-consumer-ended-2026-08-15` vs `claim-gemini-cli-w2-status-docs` |
| openhands | MEMORY.md opt-in memory vs when-to-use page claiming no persistent state | `claim-openhands-sf-memory` vs `claim-openhands-sf-memory-faq-contradiction` |
| amp | Oracle routing: manual ChatGPT-link page vs Modes tab | `claim-amp-sf-oracle-manual-chatgpt` vs `claim-amp-sf-oracle-modes-chatgpt` |
| cline | YOLO Mode documented and also removed as a cosmetic toggle in 4.1.8; CLI auto-approve true vs ACP false is a real split, not a contradiction, but reads like one | `claim-cline-sf-permissions-yolo-docs` vs `claim-cline-sf-permissions-yolo-removed` |
| claude-code | Team Premium seat pricing conflicts between pages | `claim-claude-code-w2-pricing-page` vs `claim-claude-code-w2-pricing-deployment` |
| cursor | Marketing page vs docs on Pro+/Ultra amounts | `claim-cursor-sf-pricing-page` vs `claim-cursor-sf-pricing-docs` |
| conductor | Pricing plans page vs docs FAQ still describing a free tool | `claim-conductor-sf-pricing-plans` vs `claim-conductor-sf-pricing-faq-free` |

### 7.3 Facts resolved against the corpus during synthesis

Axis positions that resolved cleanly: `devin` `closed` (4/4,
the only unambiguous closed); `cursor`, `github-copilot`, `factory-droids` `vendor-first`
(4/4); `amp` `vendor-first` (3 seats + the corpus's own constraint record — BYOK on
unconstrained mode only, all inference Amp-proxied, not self-hosted [corpus:
`claim-amp-sf-byok`, `claim-amp-sf-what-it-is-not-self-hosted`]; one seat's `open` noted);
`gemini-cli` `closed`-leaning (3 seats; one seat's borderline note about three distinct Google
billing routes preserved); `zcode` `open` (3 seats; corpus documents a broad BYOK list
[corpus: `claim-zcode-sf-provider-support`]; one seat's `vendor-first` noted); `symphony` and
the control planes: best described as **delegated** — the position belongs to the wrapped
runtime. All remaining runtimes `open` (4/4): `aider`,
`atomic`, `cline`, `crush`, `goose`, `kilo-code`, `oh-my-pi`, `opencode`, `openhands`,
`pi`, `prime-agent`, `qwen-code`.
