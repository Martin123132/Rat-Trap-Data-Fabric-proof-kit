# Rat-Trap Proof Evidence Checklist

Use this checklist when reviewing a proof folder with a buyer, advisor, or
pilot customer.

## Required Public Evidence

| Artifact | What it proves |
| --- | --- |
| `proof-summary.public.json` | Headline metrics, validation, restore, streaming, and proof ZIP SHA-256. |
| `source-manifest.public.json` | Public URLs or generated workload recipe, byte counts, and source hashes. |
| `input-file-manifest.public.json` | Materialized input file paths, byte counts, and SHA-256 hashes. |
| `artifact-manifest.public.json` | Relative artifact names, byte counts, and hashes from the original proof ZIP. |
| `validation.json` | Chunk digest and decompression validation result. |
| `restore-benchmark.json` | Restore mode, byte count, file count, elapsed time, and throughput. |
| `streaming-benchmark.json` | Local manifest/chunk endpoint behavior, latency, and bytes streamed. |
| `proof-zip.sha256` | SHA-256 of the original proof ZIP. |

## Acceptance Rules

For compression proof:

- `validation.ok` is `true`.
- `archive.logical_to_archive_ratio` is greater than `1.0`.
- `restore_benchmark.restored_total_bytes` is greater than `0`.
- `streaming_benchmark.chunks_requested` is greater than `0`.
- `source-manifest.public.json` contains public source URLs.

For dedupe proof:

- All compression proof rules pass.
- `analysis.duplicate_bytes` is greater than `0`.
- `analysis.duplicate_byte_ratio` is greater than `0`.
- `source-manifest.public.json` clearly describes the repeated workload recipe.

## Locked Proofs

Proof #1 is the public compression proof:

- GH Archive 2025-01-01 00:00-17:00 UTC.
- 8.13 GiB logical data to 1.34 GiB archive.
- 6.07x logical-to-archive ratio.
- Validation passed with 0 issues.
- ZIP SHA-256: `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d`.

Proof #2 is the controlled dedupe proof:

- Deterministic repeated logs/checkpoints/backups workload.
- 1.00 GiB logical data with 99.41% duplicate bytes.
- 512 chunk references reduced to 3 unique chunks.
- Validation passed with 0 issues and full 1.00 GiB restore.
- ZIP SHA-256: `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2`.
