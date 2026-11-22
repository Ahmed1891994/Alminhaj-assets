# Alminhaj Assets

Assets for the Minhaj Al-Quran app, kept outside the application source so Quran editions can be inspected, versioned, and downloaded on demand.

## Contents

| Path | Contents | Source |
|---|---|---|
| `datasets/minhaj/quran_data.db.gz` | Compressed Quran page-layout database | Upstream publisher M-H-AFIFI, release v1.0.0 |
| `fonts/minhaj/quran-page-fonts.zip` | 605 QCF page-font files, `QCF_BSML.ttf` and `QCF_P001.ttf` through `QCF_P604.ttf` | Upstream publisher M-H-AFIFI, release v1.0.0 |
| `datasets/minhaj-import/quran/` | Quran metadata, QCF glyph text, reciter catalog, and Shamarly line-break data imported from reader APK 1.5.4 | Package `com.siiraj.app`; APK SHA-256 is recorded in `manifest.json` |
| `fonts/minhaj/apk/` | Quran fonts imported from the same reader APK, including IndoPak/Nastaleeq, Warsh, Qalun, Hafs, and Digital Khatt fonts | Package `com.siiraj.app` |
| `sources/upstream-license/` | Upstream MIT license copy | Upstream publisher M-H-AFIFI |
| `manifest.json` | Per-file byte sizes, SHA-256 hashes, source URLs, and collection details | Generated for this repository |

The release font archive is the QCF page-font set. The imported APK also contains an IndoPak font and a separate Shamarly line-break file. Its Quran database schema has page-line and word rows keyed by script type; validate database contents and page rendering before relying on a layout.

## Integrity

Use `manifest.json` to verify every file after download. Keep the database compressed in GitHub and download/extract it on demand; do not load it during app startup. The app should pin the expected hash and reject incomplete or changed downloads.

## Source and license notes

The upstream v1.0.0 data release includes an MIT license, copied at `sources/upstream-license/LICENSE`. The release documents do not separately identify the original source and terms for every Quran database or font file. APK-extracted resources also do not include individual license metadata. Keep per-file provenance in `manifest.json`; this repository does not change upstream terms.

The release source URL is recorded as a percent-encoded GitHub path in `SOURCES.md` and `manifest.json`.