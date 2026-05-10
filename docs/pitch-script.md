# Rat-Trap Short Pitch Script

Rat-Trap is a data-fabric layer for AI and data teams that need to control the
cost and movement of large datasets, checkpoints, logs, and research artifacts.
It packages many files into a SQLite-backed `.gmw` archive, stores repeated
chunks once, validates integrity, restores normal files, and exposes chunks over
HTTP for distributed workers.

The first public proof used GH Archive data so the source could not be accused
of being hand-picked or tampered with. On 8.13 GiB of public JSONL data,
Rat-Trap produced a 1.34 GiB archive, a 6.07x logical-to-archive ratio, passed
archive validation with zero issues, restored a 1.39 GiB sample, and served
chunks through a local manifest/chunk API.

The second proof used 1.00 GiB of deterministic repeated logs, checkpoints, and
backups. Rat-Trap found 1,067,450,368 duplicate bytes, reduced 512 chunk
references to 3 unique chunks, passed validation, restored the full 1.00 GiB,
and produced a 180,224-byte archive.

The honest positioning is important: Proof #1 proves compression, provenance,
archive validation, restore, and streaming. Proof #2 proves dedupe on repeated
operational data. The buyer question is whether the same proof process saves
meaningful storage, transfer, and restore time on the buyer's real datasets.
