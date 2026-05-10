# Request A Rat-Trap Private Beta Pilot

Rat-Trap is in private beta. This public repo shows measured evidence, not the
private implementation and not a commercial/open-source release.

## What The Public Proofs Show

- Proof #1 used public GH Archive data to show compression, validation, restore,
  and streaming on independently sourced data.
- Proof #2 used a deterministic repeated workload to isolate chunk-level
  deduplication behavior.
- The combined buyer proof report is in
  [docs/combined-buyer-proof.md](docs/combined-buyer-proof.md).

## What A Customer Pilot Measures

A pilot uses a customer-approved dataset or a customer-run local proof to answer
one practical question: does Rat-Trap create meaningful storage, transfer,
restore, or archive-inspection value on your real workload?

The pilot report should include:

- logical dataset size,
- archive size,
- duplicate bytes and duplicate byte ratio,
- validation status,
- restore status,
- streaming benchmark status,
- proof ZIP SHA-256,
- limitations and next-step recommendation.

Any ROI estimate must use the evaluator's own storage price assumption. This
repo intentionally avoids quoting fixed cloud pricing.

## Best-Fit Pilot Data

Good pilot candidates include repeated:

- model checkpoints,
- dataset versions,
- evaluation outputs,
- support or training logs,
- research exports,
- backup snapshots.

Poor pilot candidates include tiny folders, one-off files, already-compressed
media-only collections, or sensitive production data that cannot be approved for
local proof handling.

## Pilot Options

1. Customer-run proof: the buyer runs Rat-Trap in their own environment and
   shares only the proof report or approved metrics.
2. Owner-run proof: the buyer provides an approved sample dataset and receives a
   proof ZIP, verification receipt, and buyer-readable report.
3. Discovery-only review: the buyer reviews this public proof kit and confirms
   whether their data shape is likely to fit before running anything.

## Access

Contact Martin Ollett for private beta access, pilot terms, and data-handling
boundaries. Do not upload sensitive datasets, proof ZIPs, or private archives to
this public repository.

