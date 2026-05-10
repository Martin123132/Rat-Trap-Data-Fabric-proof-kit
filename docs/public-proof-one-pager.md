# Rat-Trap Public Proofs #1 and #2

Rat-Trap Data Fabric has two separate proof bundles. Proof #1 uses public,
reproducible GH Archive data to prove compression, validation, restore, and
streaming. Proof #2 uses a deterministic repeated logs/checkpoints/backups
workload to isolate chunk-level deduplication behavior.

## Proof #1: Public Compression

| Metric | Proof #1 result |
| --- | ---: |
| Public source | GH Archive, 2025-01-01 00:00-17:00 UTC |
| Source files | 18 hourly JSONL files |
| Logical dataset | 8,726,574,947 bytes, about 8.13 GiB |
| Archive size | 1,438,494,720 bytes, about 1.34 GiB |
| Logical-to-archive ratio | 6.07x |
| Estimated storage saved | 7,293,713,698 bytes, about 6.79 GiB |
| Validation | Passed, 0 issues |
| Restore sample | 1,490,619,303 bytes restored |
| Streaming proof | `/manifest` plus `/chunks/<id>` served locally |
| Proof ZIP SHA-256 | `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d` |

## Proof #2: Controlled Dedupe

| Metric | Proof #2 result |
| --- | ---: |
| Workload | Deterministic repeated logs/checkpoints/backups |
| Files | 256 |
| Logical dataset | 1,073,741,824 bytes, exactly 1.00 GiB |
| Chunk references | 512 |
| Unique chunks | 3 |
| Duplicate bytes | 1,067,450,368 bytes, about 0.99 GiB |
| Duplicate byte ratio | 99.41% |
| Archive size | 180,224 bytes |
| Logical-to-archive ratio | 5,957.82x |
| Validation | Passed, 0 issues |
| Restore sample | Full 1.00 GiB restored |
| Streaming proof | 3 chunks requested through `/manifest` and `/chunks/<id>` |
| Proof ZIP SHA-256 | `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2` |

## Buyer Claim

The combined story is intentionally split. Proof #1 shows measurable
compression, integrity validation, restore, and streaming on public data. Proof
#2 shows chunk-level deduplication on repeated operational data. Together they
support a conservative buyer claim: Rat-Trap can package, validate, restore,
stream, compress, and deduplicate data, but real ROI must be measured on the
customer's own dataset.
