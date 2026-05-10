# Verification Guide

This public proof kit publishes sanitized evidence summaries, not the full
private implementation and not the large `.gmw` archives.

## How To Review A Proof

1. Open the proof folder.
2. Read `proof-summary.public.json`.
3. Confirm `validation.ok` is `true`.
4. Confirm `restore_benchmark.restored_total_bytes` is greater than `0`.
5. Confirm `streaming_benchmark.chunks_requested` is greater than `0`.
6. Compare the SHA-256 in `proof-zip.sha256` with any full proof ZIP shared
   directly by the owner.

## Proof #1 Expected Values

- Proof folder: `proofs/proof-1-public-compression/`
- Proof ZIP SHA-256: `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d`
- Validation: passed with 0 issues.
- Restore: 1,490,619,303 bytes restored.
- Streaming: 50 chunks requested in the original run.

## Proof #2 Expected Values

- Proof folder: `proofs/proof-2-controlled-dedupe/`
- Proof ZIP SHA-256: `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2`
- Validation: passed with 0 issues.
- Restore: full 1,073,741,824 bytes restored.
- Streaming: 3 chunks requested in the original run.

## Redaction Policy

Public JSON removes local filesystem paths and server URLs. Relative artifact
names, byte counts, SHA-256 hashes, validation results, restore results, and
streaming metrics are preserved.
