# Third-party components and library rights

NIVOTION uses **Qt, PySide6 and Shiboken 6.11.2 under LGPLv3**, alongside separately licensed components. The complete Windows Release ZIP preserves the accompanying notices, license texts, corresponding library sources and replacement/recombination toolkit.

After extracting the complete ZIP, consult:

| Packaged path | Purpose |
| --- | --- |
| `NIVOTION/THIRD_PARTY_NOTICES.txt` | Component notices and attribution |
| `NIVOTION/THIRD_PARTY_RIGHTS.txt` | Library modification, replacement and application recombination rights |
| `NIVOTION/LICENSES/` | License texts, including LGPLv3 and GPLv3 |
| `NIVOTION/license_inventory.json` | License-file inventory |
| `NIVOTION/dependency-inventory.json` | Component versions and hashes |
| `LIBRARY_SOURCES/` | Corresponding Qt/PySide library source archives and instructions |
| `LIBRARY_RELINK/README.md` | Instructions for replacing/recombining LGPL portions |
| `LIBRARY_RELINK/library_sources/` | Library support-module sources |

The application object code is supplied as `NIVOTION/NIVOTION.exe`. The packaged rights text permits compatible LGPL library replacement and recombination, including reverse engineering for debugging those modifications. Preserve the accompanying instructions and notices. Library-source and relink materials must stay available with the distribution.

These library rights do not publish or grant a general license to the proprietary NIVOTION application source. This repository is documentation/media only. Microsoft runtime components retain their separate terms; they are not relicensed under LGPL. The packaged runtime lineage is **14.51.36247.0**. Normal application use does not require installing developer tools.

This page points to the preserved package materials; it is not a new NIVOTION end-user license or a legal-clearance statement.

## Document and OCR runtime in 0.2.0-rc.1

The Windows package includes pypdf, pdfplumber/pdfminer.six, pypdfium2/PDFium, Pillow, openpyxl, defusedxml, et_xmlfile and their required dependencies. Exact license files and package inventory are supplied under NIVOTION/LICENSES/document-runtime.

Local OCR uses conda-forge Tesseract 5.5.3 with Czech and English tessdata_fast 4.1.0 models (Apache-2.0). Exact binary, model, configuration and package hashes are in NIVOTION/ocr-dependencies.json. OCR third-party licenses are under NIVOTION/_internal/ocr/LICENSES. The libiconv LGPL-2.1 library remains a replaceable shared DLL; exact corresponding upstream source, build recipe and patches are included under LIBRARY_SOURCES/OCR. Qt/PySide LGPL materials and recombination instructions remain included. No claim of legal certification is made.
