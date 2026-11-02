# Maintainer schema — Security (Awesome KB)

This KB conforms to the **OpenShelf** standard (`openshelf: "1.4"`,
`profile: awesome`) — spec and schemas live in
[hexsecs/openshelf](https://github.com/hexsecs/openshelf); this file carries only
what is local to this KB. Read `kb.yaml` for the declared layout.
The maintenance **method** (deepening pipeline, evidence discipline,
concept mining, gates, traps) lives in the awesome-kb skill —
[hexsecs/awesome-kb-skill](https://github.com/hexsecs/awesome-kb-skill) —
not in this file; this file wins on local facts, the skill on method,
the spec on format.

## Status: scaffold

This KB was scaffolded 2026-11-01 (structure, manifest, registry
registration, standalone render). It has **no canon list yet**: the owner
designates the source awesome list, and until then the KB holds no entity
pages and runs no ingest. Do not add pages for unlisted resources; do not
invent a canon list. When the owner designates one, this file gains the
canon rule and the `x-ingest` block appears in `kb.yaml`, following the
pattern of hexsecs/awesome-kb-automotive-security.

## Layout (takes effect when canon is designated)

- `wiki/<slug>.md` — entity pages, one per list entry (`type: entity`).
- `wiki/concepts/<slug>.md` — concept pages (`type: concept`),
  cross-linked synthesis over entities; listed in `index.md` directly.
- `wiki/index-<category>.md` — generated sub-index per list section
  (no frontmatter; do not edit by hand).
- `index.md` — the L1 index, generated from page frontmatter; it reads
  as a classic awesome list. Do not edit by hand.
- `tools/ingest.py` — the ingester (see `x-ingest` in `kb.yaml`).

## Page contract (from the OpenShelf spec, restated for editors)

- `summary` ≤ 160 chars. The list's verbatim description lives in the
  body and in `list_summary`.
- `depth: stub | brief | full | deep` (SPEC §4.5): stubs are generated;
  `brief` is the shortest authored tier (a short orientation — who it is
  for, what you actually get, caveats — outbound link checked, status
  verified, no how-it-works section); `full` is the standard researched
  page; `deep` is the rare research-grade tier, on demand only.
- `created` is the date the page first entered the KB; set once by the
  ingester, never changes — distinct from `updated` and `last_checked`.
- `uid` is a page's durable identity (SPEC §4.1): minted once by tooling
  — never written by hand — when the page first enters the KB, and
  preserved verbatim thereafter. This KB's own `uid` was minted
  2026-11-02 with `openshelf uid` at the spec 1.4 adoption.
- `status` is verified from primary sources; `published` is for finished
  works (papers, talks, books), `unknown` only for living resources whose
  state is unverified.
