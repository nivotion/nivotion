# Known limits

- Experimental, unsigned Windows x64 desktop build. Validation on the release machine is not certification for every Windows configuration.
- Session inventory exists only while the application runs. One parsed workflow remains active; switching from an unsaved draft requires discard.
- Bounded input, preview, memory and execution budgets; one expensive job at a time. The inherited process limit is 64 workflow owners.
- CSV Combine requires compatible headers and preserves duplicates. It is a vertical append, not a relational join or cross-format merge.
- PDF reading order is geometric. Table detection offers candidates, not guaranteed reconstruction. Unsupported encrypted/active document features are rejected.
- OCR is explicit, local and fallible; rotation is manual. Only Czech/English language data is included. Review output before use.
- One selected PDF or worksheet per document result. XLSX formulas/macros are never executed. Cached formula values can be stale; hidden sheets and merged cells require explicit choices.
- Spreadsheet output is a text table. Original worksheet names and source values are preserved during review; original workbook formatting, charts and formulas are not round-tripped.
- Export requires a new destination. Provenance provides a processing record, not downstream success or certification.
- Resource supervision is not an operating-system security sandbox. No AI, IPC/background agent, general Split/Convert, cloud automation or financial finalization is included.
