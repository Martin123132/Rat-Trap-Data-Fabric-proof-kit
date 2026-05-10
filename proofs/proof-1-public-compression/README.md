# Proof #1: Public Compression

This proof used public GH Archive data from 2025-01-01 00:00-17:00 UTC. It is
the public-source compression, validation, restore, and streaming proof.

## Result

| Metric | Value |
| --- | ---: |
| Source files | 18 hourly JSONL files |
| Logical dataset | 8,726,574,947 bytes |
| Archive size | 1,438,494,720 bytes |
| Logical-to-archive ratio | 6.07x |
| Estimated storage saved | 7,293,713,698 bytes |
| Validation | Passed, 0 issues |
| Restore sample | 1,490,619,303 bytes |
| Streaming chunks requested | 50 |
| Proof ZIP SHA-256 | `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d` |

## Files

- `proof-summary.public.json`
- `source-manifest.public.json`
- `input-file-manifest.public.json`
- `artifact-manifest.public.json`
- `validation.json`
- `restore-benchmark.json`
- `streaming-benchmark.json`
- `proof-zip.sha256`

The large proof ZIP and `.gmw` archive are intentionally not committed.
