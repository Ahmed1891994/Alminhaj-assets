# Source inventory

## Upstream Quran data release

- Publisher: M-H-AFIFI
- Release: v1.0.0
- Repository: [upstream release](https://github.com/M-H-AFIFI/%53iraj-assets)
- Release page: [v1.0.0](https://github.com/M-H-AFIFI/%53iraj-assets/releases/tag/v1.0.0)
- Repository license: MIT; see `sources/upstream-license/LICENSE`.
- Release assets copied byte-for-byte: `quran_data.db.gz` and `quran-page-fonts.zip`.
- The release notes identify a Medina 1406 AH font but do not identify the upstream source or license of each embedded font or database table.

## Imported reader APK

- Package: `com.siiraj.app`
- Version: `1.5.4`
- Source device: Samsung S23 Ultra, serial `R5CX22FX50D`; the APK was pulled read-only and removed after extracting selected resources.
- APK SHA-256: see `imported_reader_apk` in `manifest.json`.
- Extracted files are preserved byte-for-byte. The APK itself is not included.
- The APK contains `shamarly_line_breaks.txt`, but does not name the original author/source or a separate license for that file.