# Battle Harnesses — public pack

This repository publishes two things: the evidence pack behind Battle
Harnesses, and the interview prompt that reads it.

## What this is

One person trying to make sense of the AI coding harness landscape.

There are a lot of these tools now — CLIs, IDEs, cloud agents, control planes,
orchestrators — and from the outside it is genuinely hard to tell what any one
of them does differently, or whether it is worth your afternoon. I wanted to
understand that properly instead of guessing, so I started writing down what
each product's own documentation says, with a link for every line. This is that
pile of notes, cleaned up enough to be useful to someone else.

**It is nothing official.** Not affiliated with, endorsed by, sponsored by, or
reviewed by any of the products described. Nobody asked for it. It is not a
benchmark, not a ranking, and not a league table — the whole point of the shape
it takes is that different tools are built for different work, and flattening
them into one ordering would throw away the only interesting part.

## What is in here

| Path | What it holds |
|---|---|
| `pack/index.json` | Manifest: `pack_version`, counts, per-file digests, and the honesty block |
| `pack/products/` | One file per product — claims, each with its source |
| `pack/relationships.json` | Forks, wrappers, lineage, and shared runtimes between products |
| `pack/contradictions.json` | Where the corpus disagrees with itself, kept rather than averaged |
| `pack/judged/judged.md` | The editorial layer — clusters, live disagreements, contested facts |
| `interview-prompt.md` | The skill: paste it into your own agent, it reads the pack |
| `dist/` | The same pack as a zip, with sha256 sidecars |

## What the evidence actually is

Read `honesty` in `pack/index.json` before you trust a number, but the short
version, as of this writing:

- **Zero hands-on observation rows.** Nothing here was produced by installing a
  product and using it. Every claim comes from documentation, source, or public
  material.
- **1596 claims reviewed, 1931 not.** A claim being present means the corpus
  documents it. It does not mean it was verified.
- Review is unevenly spread across products. Comparing a heavily reviewed
  product against a barely reviewed one compares reviewed evidence with
  unreviewed evidence, and any honest report has to say so.

`judged/judged.md` is opinion, and labels itself that way line by line —
`[corpus]` cites a claim, `[external]` carries a URL and a date, `[judgment]`
is me reasoning over the two. A row inherits the weakest label in its chain.

## The interview prompt

`interview-prompt.md` is meant to be copied into whatever coding agent you
already use. It fetches this pack, looks at as much of your setup as you
explicitly allow, and writes an HTML report to your own disk.

Nothing is sent anywhere. There is no server, no account, and no telemetry —
this repository is a pile of static files, and the only request involved is you
downloading it. Your own AI provider will see the conversation, because it is
happening inside their product; the prompt says so out loud before it asks you
for anything.

You should read it before you run it. It asks for permission in tiers, each
separately refusable, and it is read-only: it never executes a discovered
binary, never opens `.env` files or key material, and reads config structure
rather than config values.

## If one of these is your product

I would genuinely rather be corrected than be right. If something here is
wrong, out of date, or reads as unfair, please open an issue — a link to the
correct documentation is enough, and I will take a wrong line down without an
argument. Products move fast and a corpus like this is out of date the moment
it is written.

If you would prefer not to be listed at all, say so and I will remove you.

## Verifying what you downloaded

`pack/checksums.json` carries the digest of `index.json` and of `judged.md`;
every other file's digest is in `index.json` under `files[]`. The zip has a
`.sha256` sidecar next to it.

Being honest about what that proves: these digests are published from the same
repository that serves the files, so they detect a truncated or corrupted
download, not a compromised origin. What you can actually do about the second
thing is pin the `pack_version` your report cites and compare it across runs.

## Licence and reuse

The corpus is a set of factual claims about public products, each with a
source. Take it, check it, argue with it. If you republish it, please carry the
`pack_version` along so people can tell which snapshot they are reading.
