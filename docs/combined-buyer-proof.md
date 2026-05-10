# Rat-Trap Combined Buyer Proof Report

This report combines two proof ZIPs: one public compression proof and one controlled dedupe proof. It is meant for buyer review without rerunning the large proof jobs.

## Executive Summary

| Proof | Source basis | Logical data | Archive size | Ratio | Duplicate data | Validation | Restore | Streaming |
| --- | --- | ---: | ---: | ---: | ---: | --- | ---: | ---: |
| Proof #1 | public GH Archive data | 8.13 GiB | 1.34 GiB | 6.07x | 0 B (0.00%) | OK | 1.39 GiB | 50 |
| Proof #2 | controlled repeated workload | 1.00 GiB | 176.00 KiB | 5957.82x | 1018.00 MiB (99.41%) | OK | 1.00 GiB | 3 |

## Verification Receipts

- Proof #1 ZIP SHA-256: `8f5c92a9c9e4bd30f6d295fa7a83775c098718963b062cf4c50d461a3994e23d`.
- Proof #1 verification: OK with 0 issue(s).
- Proof #2 ZIP SHA-256: `f25c4589df8d2f8f17f30fbd2a32ff81551345e8c021da18bb711d492db129c2`.
- Proof #2 verification: OK with 0 issue(s).

## Buyer Claim

Proof #1 shows Rat-Trap can package public data into a validated, restorable, streamable archive with measured compression. Proof #2 isolates chunk-level deduplication on repeated operational data. Together, they support a conservative pilot claim: Rat-Trap can measure, archive, validate, restore, stream, compress, and deduplicate data, but production ROI should be measured on the buyer's own dataset.

## Limitations

- These proof ratios are evidence, not guarantees for every dataset.
- The implementation remains private beta and is not distributed through this report.
- Money estimates are omitted unless a storage price is supplied by the evaluator.
