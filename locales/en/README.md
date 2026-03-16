# hitomiViewer dataset (English localization)

This file is localized using AI translation and may contain inaccuracies.
If there is any difference, the Japanese source file takes precedence.

---

## Language and Localization

- Localized documents are managed under `locales`.
- Translation uses AI assistance.
- Localized documents are for reference. If there is any inconsistency, the Japanese original takes precedence.

### Localized README Files

- Japanese (source): [README.md](../../../README.md)
- English (localized): [locales/en/README.md](README.md)
- Chinese (localized): [locales/zh/README.md](../zh/README.md)
- Korean (localized): [locales/ko/README.md](../ko/README.md)

## Overview

This directory stores the tag translation dataset for hitomiViewer.

- Main data: [src/data.jsonc](../../../src/data.jsonc)
- Purpose: distribution and maintenance of dictionary data used by the extension

## Data Format

- Format: JSONC (JSON with comments)
- Example root keys: `tag`, `seriesTag`, `characterTag`
- Some keys use an object with `default` and `series` for context-dependent resolution

JSONC may not be parseable by standard JSON parsers.
Remove comments if you need strict JSON.

## License and Notice

This dataset is prepared with reference to public information from EHWiki.
EHWiki indicates that content is available under GNU Free Documentation License 1.2+
unless otherwise noted.

- Reference: <https://ehwiki.org/wiki/EHWiki:About>
- Reference: <https://ehwiki.org/wiki/EHWiki:Copyrights>

The dataset in this repository is distributed under GNU Free Documentation License 1.2 or later (GFDL-1.2-or-later).

- License full text (source): [LICENSE](../../../LICENSE)
- Attribution and source notes (Japanese source): [NOTICE.md](../../../NOTICE.md)
- Attribution and source notes (localized): [locales/en/NOTICE.md](NOTICE.md)
- Attribution and source notes (Chinese localized): [locales/zh/NOTICE.md](../zh/NOTICE.md)
- Attribution and source notes (Korean localized): [locales/ko/NOTICE.md](../ko/NOTICE.md)

## Disclaimer

- This dataset is prepared for personal use and is provided without warranty.
- Users are responsible for checking applicable license terms and other policies.
