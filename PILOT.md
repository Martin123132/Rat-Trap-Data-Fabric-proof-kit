# Request A Rat-Trap Private Beta Pilot

Rat-Trap is in private beta. This public repo shows measured evidence, not the
private implementation and not a commercial/open-source release.

## AI Lab Pilot Scan

The first recommended step is a narrow pilot scan for one approved AI workload:
model checkpoints, dataset versions, eval outputs, logs, research exports, or
backup snapshots. The point is to measure whether Rat-Trap creates enough
storage, transfer, restore, or archive-inspection value on your real data to
justify a deeper private beta review.

Use the [pilot request checklist](docs/pilot-request-checklist.md) before
sharing anything. Do not upload sensitive datasets, proof ZIPs, or private
archives to this public repository.

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

## Pilot Request Flow

1. Review the public proof summaries and combined buyer proof report.
2. Pick one approved workload that is large enough to matter.
3. Choose customer-run proof, owner-run proof, or discovery-only review.
4. Fill in the pilot request checklist.
5. Run or approve the proof.
6. Review the verification receipt, limitations, and next-step recommendation.

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
boundaries. Use the pilot request checklist so the first conversation can focus
on whether the workload is likely to produce a meaningful measured result.
