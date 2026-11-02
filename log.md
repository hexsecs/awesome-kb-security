# Log

## [2026-11-01] scaffold | Security (Awesome KB) created

Repository scaffolded to the OpenShelf `awesome` profile following the
network's established pattern (hexsecs/awesome-kb-automotive-security):
kb.yaml manifest, AGENTS.md maintainer schema, generated-index layout,
standalone GitHub Pages render via the registry builder pinned at an
exact commit. No canon list has been designated by the owner yet, so the
KB holds no entity pages and runs no ingest; the canon designation is
the next step and is the owner's decision.

## [2026-11-02] adopt | OpenShelf spec 1.4 adoption: KB uid + restamp

Minted the KB `uid` with `openshelf uid` (the spec 1.4 adoption path,
SPEC §2/§4.1) and restamped kb.yaml `openshelf: "0.1"` → `"1.4"`.
No pages exist yet (scaffold); when an ingester is added it mints page
uids on creation and preserves them on rewrites, per the pattern of
hexsecs/awesome-kb-automotive-security. `openshelf lint --strict` clean.
