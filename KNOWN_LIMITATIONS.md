# Experimental Preview limitations

Version 0.1.0-rc.1 is experimental, not a stable/final release. Only the two documented CSV workflows are available. Review results before relying on them.

| Boundary | Current limit |
| --- | --- |
| Input size | 10,000,000 bytes per file (decimal 10 MB) |
| Combined input | 2–4 files; 25,000,000 bytes total (decimal 25 MB) |
| Rows | 100,000 data rows per file and 100,000 total when combining |
| Columns | 128 per file |
| Data cells | 2,000,000 per file; 4,000,000 combined |
| Field | 32,768 UTF-8 bytes |
| Output | 32,000,000 bytes (decimal 32 MB); larger results are rejected |
| Display preview | First 20 rows; first 256 characters per cell/header |

Limits apply together. The output ceiling is not a promise that every 32 MB result can be produced within the input limits. Parsing/export also have bounded processing time and may stop on slow or unsuitable storage.

- Comma-separated UTF-8 / UTF-8-SIG CSV only; malformed records or incompatible headers are rejected. Semicolon-separated and other encodings are not supported by these workflows.
- Combine appends vertically with identical unique headers in the same order. It preserves duplicates and whitespace; it does not merge by a key.
- Single CSV trims outer cell whitespace and optionally removes exact duplicate original rows.
- Activity and prepared drafts are session-local. Restarting clears the session view; exported files remain on disk.
- Export is explicit and refuses existing CSV or provenance destinations. Incomplete/unverified export requires inspection before retrying.
- Formula-like CSV cells are not sanitized. Spreadsheet programs can interpret such values as formulas.
- The Windows x64 binary is unsigned; SmartScreen may warn. There is no installer in this distribution.

[Installation](INSTALL.md) · [Quickstart](QUICKSTART.md)
