# PReSto Temp12k run on PReSto12k 0_0_1

This repository runs the PReSto Temp12k reconstruction on the [PReSto12k 0_0_1](https://lipdverse.org/PReSto12k/0_0_1/) compilation: 1803 records.

- Membership comes only from the published compilation, read from the
  LiPDverse whole-database export
  [2026-10-15b](https://lipdverse.org/dev/export/database-2026-10-15b/)
  (`compilations` table) by presto-recipes `pools/compilation_pool.R`.
- `query_params.json` (`mode: bundle`) pins the bundle by URL and sha256:
  presto-recipes release
  [pools-2026-10-15b-r1](https://github.com/paleopresto/presto-recipes/releases/tag/pools-2026-10-15b-r1).
  Its files are the compilation's LiPD files, checked against the export's
  md5 values and trimmed to the member records.
- The code and algorithm config are those of
  [presto-Temp12k-run-2026-10-08b](https://github.com/paleopresto/presto-Temp12k-run-2026-10-08b),
  unchanged, so this run differs from that one only in where its data come
  from.

Committing `query_params.json` triggers the reconstruction workflow.
