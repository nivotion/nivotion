# Install NIVOTION 0.2.0-rc.1

Windows x64 Experimental Preview, build 20260929.1. The executable is unsigned. Keep the complete extracted package together.

1. Download the Windows ZIP from the official v0.2.0-rc.1 GitHub Release, not the generated source archive.
2. Compare its SHA256 with that release and CHECKSUMS.md using `Get-FileHash -Algorithm SHA256 -LiteralPath <downloaded ZIP>`.
3. Extract the entire ZIP to a writable local folder. Run NIVOTION/NIVOTION.exe. Do not run inside the ZIP or move the EXE alone.
4. No separate Python or OCR installation is needed. Third-party sources and replacement instructions accompany the runtime.

Windows may show an unknown-publisher warning. Verify the origin and checksum before deciding to proceed; never disable security protections globally. Follow your device administrator's policy.

Preferences and bounded diagnostics are local under %LOCALAPPDATA%/NIVOTION. Exports go only to the new destination you explicitly select. Session inventory is not restored after restart.

See QUICKSTART.md, KNOWN_LIMITATIONS.md and THIRD_PARTY_NOTICES.md. A checksum proves file identity, not software safety. Current-release validation results belong to the release notes; prior Windows-machine tests do not certify this build.
