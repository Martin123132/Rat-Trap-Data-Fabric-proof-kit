# Rat-Trap Proof Kit

Rat-Trap Data Fabric is a private-beta data logistics product for AI and
data-heavy teams. It packages folders into SQLite-backed `.gmw` archives,
deduplicates repeated chunks, validates integrity, restores normal files, and
serves archive manifests and chunks over HTTP.

This public repo is not the product source code and is not an open-source
release. It is a buyer-facing proof kit: measured results, evidence summaries,
verification notes, and the current roadmap for evidence packaging.

## Proofs

| Proof | What it proves | Headline result |
| --- | --- | ---: |
| [Proof #1: Public Compression](proofs/proof-1-public-compression/README.md) | Public-source compression, archive validation, restore, and streaming | 8.13 GiB to 1.34 GiB, 6.07x |
| [Proof #2: Controlled Dedupe](proofs/proof-2-controlled-dedupe/README.md) | Chunk-level deduplication on repeated operational data | 99.41% duplicate bytes |

## Locked Results

Proof #1 used public GH Archive data from 2025-01-01 00:00-17:00 UTC:

- 18 hourly JSONL files.
- 8,726,574,947 logical bytes, about 8.13 GiB.
- 1,438,494,720-byte archive, about 1.34 GiB.
- 6.07x logical-to-archive ratio.
- Validation passed with 0 issues.
- Restore sample: 1,490,619,303 bytes.
- Local `/manifest` and `/chunks/<id>` streaming proof.
- Proof ZIP SHA-256: `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d`.

Proof #2 used a deterministic repeated logs/checkpoints/backups workload:

- 1,073,741,824 logical bytes, exactly 1.00 GiB.
- 256 files, 512 chunk references, 3 unique chunks.
- 1,067,450,368 duplicate bytes.
- 99.41% duplicate byte ratio.
- 180,224-byte archive.
- Full 1.00 GiB restore.
- 3 chunks requested through the streaming benchmark.
- Proof ZIP SHA-256: `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2`.

## What This Proves

- Rat-Trap can create a portable archive from public data and validate it.
- Rat-Trap can restore archived data back to normal files.
- Rat-Trap can expose archive manifests and chunks over HTTP.
- Rat-Trap can deduplicate repeated chunks when the workload contains repeated
  logs, checkpoints, backups, or similar operational data.

## What This Does Not Prove

- It does not claim every dataset will compress or deduplicate by the same
  ratio.
- It does not publish the private Rat-Trap implementation.
- It does not grant a commercial or open-source license.
- It does not replace a pilot on a customer's own dataset.

## Verification

Start with [docs/verification-guide.md](docs/verification-guide.md). The public
evidence folders include sanitized JSON summaries, source/input manifests,
validation results, restore benchmark results, streaming benchmark results, and
proof ZIP SHA-256 values. Large `.gmw` archives and large proof ZIPs are
intentionally not committed.

## Buyer Materials

- [Public proof one-pager](docs/public-proof-one-pager.md)
- [Proof evidence checklist](docs/proof-evidence-checklist.md)
- [Short pitch script](docs/pitch-script.md)
- [v0.2 evidence packaging backlog](docs/v0.2-evidence-packaging-backlog.md)

## Private Beta Access

The implementation is in private beta. Contact Martin Ollett for pilot access,
commercial evaluation, or a customer-approved proof run.
