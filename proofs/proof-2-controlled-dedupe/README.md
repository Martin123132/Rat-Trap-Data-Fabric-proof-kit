# Proof #2: Controlled Dedupe

This proof used a deterministic repeated logs/checkpoints/backups workload. It
isolates chunk-level deduplication behavior separately from the public-source
compression proof.

## Result

| Metric | Value |
| --- | ---: |
| Logical dataset | 1,073,741,824 bytes |
| Files | 256 |
| Chunk references | 512 |
| Unique chunks | 3 |
| Duplicate bytes | 1,067,450,368 bytes |
| Duplicate byte ratio | 99.41% |
| Archive size | 180,224 bytes |
| Logical-to-archive ratio | 5,957.82x |
| Validation | Passed, 0 issues |
| Restore | Full 1,073,741,824 bytes |
| Streaming chunks requested | 3 |
| Proof ZIP SHA-256 | `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2` |

## Files

- `proof-summary.public.json`
- `source-manifest.public.json`
- `input-file-manifest.public.json`
- `artifact-manifest.public.json`
- `validation.json`
- `restore-benchmark.json`
- `streaming-benchmark.json`
- `proof-zip.sha256`

The proof ZIP and `.gmw` archive are intentionally not committed.
