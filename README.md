# Alminhaj Assets

Assets for the Minhaj Al-Quran app, kept outside the application source so Quran editions can be inspected, versioned, and downloaded on demand.

## Contents

| Path | Contents | Source |
|---|---|---|
| `datasets/siraj/quran_data.db.gz` | Siraj Quran database release, compressed | `M-H-AFIFI/Siraj-assets`, release `v1.0.0` |
| `fonts/siraj/quran-page-fonts.zip` | 605 QCF page-font files: `QCF_BSML.ttf` and `QCF_P001.ttf` through `QCF_P604.ttf` | `M-H-AFIFI/Siraj-assets`, release `v1.0.0` |
| `datasets/siraj-apk/quran/` | Quran metadata, QCF glyph text, reciter catalog, and Shamarly line-break data extracted from the installed Siraj APK 1.5.4 | Package `com.siiraj.app`; APK SHA-256 is recorded in `manifest.json` |
| `fonts/siraj/apk/` | Quran fonts bundled in the same Siraj APK, including IndoPak/Nastaleeq, Warsh, Qalun, Hafs, and Digital Khatt fonts | Package `com.siiraj.app` |
| `sources/siraj-assets/` | Upstream README and MIT license | `M-H-AFIFI/Siraj-assets` |
| `manifest.json` | Per-file byte sizes, SHA-256 hashes, source URLs, and collection details | Generated for this repository |

The release font archive is the QCF page-font set, not an IndoPak or Shamarly page-font pack. The APK also contains an IndoPak font and a separate Shamarly line-break file. The Quran database schema in the APK has page-line and word rows keyed by script type; validate the database contents and page rendering before wiring a reader to it.

## Integrity

Use `manifest.json` to verify every file after download. Keep the database compressed in GitHub and download/extract it on demand in the app; do not load the database during app startup. The app should pin the expected hash and reject incomplete or changed downloads.

## Source and license notes

The upstream Siraj-assets repository has an MIT license, copied at `sources/siraj-assets/LICENSE`. The repository release README and asset manifest do not separately identify the original source and terms for every Quran database or font file. APK-extracted resources also do not include individual license metadata. Keep the per-file provenance in `manifest.json`; do not treat this repository as changing upstream terms.

QUL provides a 610-page, 15-line Indopak/Qudratullah layout, but that layout and its associated font have no copyright information on their QUL resource pages. They are not included in this initial package. Add them only with their source details and a rights decision recorded in the manifest.

