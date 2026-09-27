# Run the Experimental Preview on Windows

Version **0.1.0-rc.1**, build **20260925.1**, Windows x64. The package documents Windows 10/11 x64; the validation includes a separate Windows 10 Pro x64 machine (build 19045). This is not a guarantee for every Windows build or configuration. No narrower minimum Windows build is asserted.

## Download and verify

From this repository's **Releases**, open **v0.1.0-rc.1 — First Public Experimental Preview** and download `NIVOTION_0.1.0-rc.1_WINDOWS_X64_EXPERIMENTAL_PREVIEW.zip` and `SHA256SUMS.txt`. Do not use GitHub's “Source code (zip)” download: it contains this documentation repository, not the application.

In PowerShell, in the folder containing the downloaded ZIP:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath ".\NIVOTION_0.1.0-rc.1_WINDOWS_X64_EXPERIMENTAL_PREVIEW.zip"
```

The SHA256 must be exactly (letter case does not matter):

```text
09aef537bde2f7d5451ddbb8d941fd0244b9ccb4a2a57661c662095973cd0193
```

The ZIP size is **101,859,858 bytes (97.14 MiB)**. If the hash differs, do not run it. Download again from the intended release. A checksum detects a different file; it is not a code signature or a guarantee that software is safe.

## Extract and launch

1. Right-click the ZIP and choose **Extract All** into a writable local folder.
2. Open the extracted `NIVOTION` folder and run `NIVOTION.exe`.
3. Keep the entire extracted package together, including `_internal`, `LIBRARY_SOURCES` and `LIBRARY_RELINK`. Do not launch from inside the ZIP or copy the EXE alone.

Normal use needs no separate Python, PySide or Visual Studio installation. Developer tools mentioned in library rebuilding instructions are optional and unrelated to ordinary use.

## SmartScreen

This Experimental Preview is unsigned. Windows may display “Windows protected your PC” or an unknown-publisher warning. Verify the download and decide whether you trust its origin. On a standard SmartScreen dialog, **More info** may reveal **Run anyway**; choose it only if you decide to proceed. If your device policy blocks the app, stop and consult its administrator. Do not disable Defender, antivirus or SmartScreen globally.

## Local settings and package labels

Preferences and bounded failure diagnostics are stored under `%LOCALAPPDATA%\NIVOTION`. CSV exports go to the new destination you explicitly choose. Activity is kept for the current session.

Some packaged text retains older PRIVATE/BLOCKED validation labels. The exact unchanged candidate later completed technical validation; the release notes and checksum identify that candidate. Those old labels are not evidence that a different build should be substituted, and do not themselves grant distribution rights.

See [Quickstart](QUICKSTART.md), [limitations](KNOWN_LIMITATIONS.md) and [third-party notices](THIRD_PARTY_NOTICES.md).
