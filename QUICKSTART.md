# Prepare a CSV draft

Start NIVOTION and choose a workflow from Home or Workflows. Inputs must be comma-separated UTF-8 CSV (a UTF-8 BOM is accepted), with a header row. Keep a backup and review the result before using it elsewhere.

## Single CSV

1. Choose **Prepare a CSV** → **Select CSV…** and select one file.
2. Review the source preview and row/column counts.
3. Optionally select **Remove exact duplicate original rows**. This compares original rows, before whitespace trimming; rows that only become equal after trimming are not removed by that rule.
4. Choose **Prepare Draft**. Outer cell whitespace is trimmed; headers are preserved.
5. Review **Prepared preview**, counts and status. **DRAFT_PREPARED** means a draft exists in this session; it has not yet been exported.
6. Choose **Export Draft…**, select a new filename, review the confirmation and both destinations, then confirm **Export draft**.

## Combine 2–4 CSVs

1. Choose **Combine CSVs** → **Select CSV files…**.
2. Select 2–4 distinct files. Their non-empty, unique column headers must match exactly and in the same order.
3. Review validation and the displayed file order. That order is the vertical append order; there is no key-based merge. Reselect files if the order is wrong.
4. Choose **Prepare Draft**, then inspect the prepared preview and total counts.
5. Choose **Export Draft…**, select a new destination and confirm.

Combine preserves rows, text values, whitespace and duplicates. It performs no automatic deduplication.

## What export creates

For a destination named `draft.csv`, the app writes `draft.csv` and `draft.csv.provenance.json`. Provenance records source identity/digest/revision information, preparation choices and output information so the draft can be traced to its inputs. Keep the pair together. Review the JSON before sharing it.

**DRAFT_PREPARED is not ACTION_SUCCESS.** It does not mean a downstream business action occurred. A successful explicit local export is reported as `DRAFT_EXPORTED`; no downstream action is implied.

Existing destinations, including an existing provenance sidecar, are rejected. Choose two new filenames; source files cannot be overwritten. If the source changes, select and prepare it again. If export is reported as unverified/recovery required, inspect the indicated locations: partial CSV, sidecar or staging files may exist. Do not treat an unverified result as successful.

The table is a preview of the first 20 rows and 256 characters per cell/header, not the entire dataset. Exports retain full accepted text. Formula-like values are not sanitized: take care before opening a CSV in a spreadsheet program.

[Full limits](KNOWN_LIMITATIONS.md) · [Report a problem](SUPPORT.md)
