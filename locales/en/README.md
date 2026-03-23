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

This directory stores the tag translation data for hitomiViewer.

- Purpose: distribution and maintenance of dictionary data used by the extension

## File Structure

| File | Contents |
|------|----------|
| [src/data1.jsonc](../../../src/data1.jsonc) | Simple one-to-one translation mappings (source) |
| [src/data2.jsonc](../../../src/data2.jsonc) | Context-dependent translation data (source) |
| [dist/data1.json](../../../dist/data1.json) | Minified JSON for distribution (no comments) |
| [dist/data2.json](../../../dist/data2.json) | Minified JSON for distribution (no comments) |

## Data Format

Both files use JSONC (JSON with comments) format.

### Root Keys

| Key | Contents |
|-----|----------|
| `tag` | General tags |
| `seriesTag` | Series/work tags |
| `characterTag` | Character tags |
| `artistTag` | Creator/artist tags |
| `circleTag` | Circle/group tags |

### data1: Simple String Mappings

Used when a tag has a single unambiguous translation:

```jsonc
"uncensored": "検閲なし"
```

### data2: Context-Dependent Objects

Used when the same tag name has different translations depending on the work.
`default` is the fallback translation, `series` maps work names to specific translations:

```jsonc
"robin": {
  "default": "ロビン",
  "series": {
    "batman": "ロビン",
    "fire emblem awakening": "ルフレ"
  }
}
```

### Comment Lines (data2)

```jsonc
// 10101
"robin": { ... }
```

Leading numeric comments are EH (e-hentai) tag IDs for editorial reference only.

### Note

JSONC cannot be parsed by standard JSON parsers. Remove comments and trailing commas before use.

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
