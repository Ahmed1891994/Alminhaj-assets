# Per-layout Mushaf data

Each folder holds a copy of `datasets/minhaj/quran_data.db.gz` with only the page-line and word rows of one script.
Shared tables (surahs, ayahs, translations, tafsirs, reciter data) are unchanged.

- `indopak/quran_data.db.gz`: rows for `scriptType = indopak`. Uses the page fonts in `fonts/minhaj/quran-page-fonts.zip`.
- `shamarly/quran_data.db.gz`: rows for `scriptType = shamarly`. Uses the app-bundled Shamarly font, so no font archive is needed.

Built from `datasets/minhaj/quran_data.db.gz` (SHA-256 `0e3608ceeae6f520520082fe799ed4cd0f165f8aa3a765764bdf06382207a647`).
