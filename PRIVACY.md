# Privacy in this Experimental Preview

The two current CSV workflows read the local files you select and prepare drafts on your device. Original files are read-only inputs; exporting creates a new CSV and provenance JSON at your chosen destination.

Preferences and bounded failure diagnostics are stored under `%LOCALAPPDATA%\NIVOTION`. Diagnostics can include a fixed failure code, build information and module/function/line metadata; review them before sharing. The Activity view and prepared drafts are session-local.

Provenance contains source identity/digest/revision and output/preparation metadata. Treat it and exported CSVs as your data and inspect them before sharing. Filenames, screenshots and logs can disclose sensitive information even when the CSV itself is omitted.

This describes the current workflows. It is not an absolute guarantee about every possible environment or all future versions. Downloading from GitHub and submitting an issue use GitHub's service and its policies.

Do not attach private CSV files, credentials or sensitive screenshots to public feedback issues. [Support](SUPPORT.md) explains how to provide a small, non-sensitive reproduction.
