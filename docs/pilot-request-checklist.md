# AI Lab Pilot Scan Request Checklist

Use this checklist before requesting a Rat-Trap private beta pilot scan. It
keeps the pilot narrow, safe, and measurable.

## What To Share First

Do not send data in a public issue. Start with a short description:

- dataset or artifact type,
- rough logical size,
- whether it contains repeated checkpoints, dataset versions, logs, eval
  outputs, exports, or backups,
- whether the data is sensitive,
- preferred run mode: customer-run, owner-run, or discovery-only,
- the success metric that matters most: storage size, transfer size, restore
  behavior, archive inspection, or streaming access,
- optional storage cost assumption if ROI should be estimated.

## Best Pilot Shape

The strongest first pilot is one approved folder that is big enough to matter
and likely to contain repetition. Good examples include checkpoint directories,
versioned datasets, training logs, repeated research exports, or backup
snapshots.

Tiny folders, already-compressed media-only collections, and sensitive
production data without a customer-run path are usually poor first pilots.

## Pilot Run Modes

- Customer-run proof: safest for sensitive data; you run Rat-Trap locally and
  share approved metrics or a report.
- Owner-run proof: you provide an approved non-sensitive sample and receive a
  proof ZIP, verification receipt, and buyer-readable report.
- Discovery-only review: no data moves; both sides decide whether the workload
  is likely to fit before running anything.

## Request Template

```text
I would like to request a Rat-Trap pilot scan.

Data/artifact type:
Approximate size:
Repeated data signal:
Sensitivity boundary:
Preferred run mode:
Success metric:
Storage price assumption, if ROI is wanted:
Anything the proof must not include:
```

## What The Result Should Prove

A useful pilot result should show:

- logical size,
- archive size,
- duplicate bytes and duplicate byte ratio,
- validation status,
- restore status,
- streaming benchmark status,
- proof ZIP SHA-256,
- limitations and next-step recommendation.
