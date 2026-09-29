# Quick Start · 0.2.0-rc.1

1. Download [NIVOTION_0.2.0-rc.1_WINDOWS_X64_EXPERIMENTAL_PREVIEW.zip](https://github.com/nivotion/nivotion/releases/download/v0.2.0-rc.1/NIVOTION_0.2.0-rc.1_WINDOWS_X64_EXPERIMENTAL_PREVIEW.zip), verify the published SHA256, and extract the **entire** ZIP. Keep all runtime and library-rights folders together. Run `NIVOTION/NIVOTION.exe` on Windows x64.
2. The executable is unsigned and Windows may warn. Check the official release and checksum before deciding whether to run it; do not disable Windows protections globally.
3. Add CSV, PDF or XLSX files. Additional drops append to the session inventory. Select the workflow and review the source before preparing it.
4. **CSV:** review one file and choose supported cleanup options. For Combine, select compatible CSVs with identical, unique headers in the same order. Confirm their displayed order.
5. **PDF:** inspect native text or table candidates. For scanned pages, explicitly enable OCR and select Czech, English or both. Check text and table accuracy; OCR is fallible.
6. **XLSX:** inspect the workbook, select a worksheet and review warnings. Choose cleanup options, then Prepare. Formulas are not calculated; cached values can be stale.
7. **Prepare:** review the resulting draft. Switching away from an unsaved draft requires an explicit discard decision.
8. **Export:** choose a new destination. Keep the exported file and its `.provenance.json` sidecar together. The sidecar records sources, selections and processing details; it is not a certification.

The mixed inventory is process-local and is not restored after restarting. Resource limits apply; one expensive operation runs at a time. Only one selected PDF or worksheet produces a document result. No cloud upload, AI workflow, general conversion or cross-format merge is included. See [known limits](KNOWN_LIMITATIONS.md).
