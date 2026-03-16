# hitomiViewer dataset (한국어 로컬라이즈)

이 문서는 AI 번역으로 작성되었으며, 부정확할 수 있습니다.
일본어 원문과 차이가 있는 경우 일본어 원문을 우선합니다.

---

## 언어와 로컬라이즈

- 로컬라이즈 문서는 `locales` 디렉터리에서 관리합니다.
- 번역에는 AI 보조를 사용합니다.
- 로컬라이즈 문서는 참고용이며, 차이가 있는 경우 일본어 원문을 우선합니다.

### 언어별 README

- 일본어(원문): [README.md](../../../README.md)
- English (localized): [locales/en/README.md](../en/README.md)
- 中文(本地化): [locales/zh/README.md](../zh/README.md)
- 한국어(로컬라이즈): [locales/ko/README.md](README.md)

## 개요

이 디렉터리는 hitomiViewer용 태그 번역 데이터를 저장합니다.

- 목적: 확장 기능에서 사용하는 사전 데이터의 배포 및 관리

## 파일 구성

| 파일 | 내용 |
|------|------|
| [src/data1.jsonc](../../../src/data1.jsonc) | 단순 일대일 번역 데이터 (원본) |
| [src/data2.jsonc](../../../src/data2.jsonc) | 문맥 의존 번역 데이터 (원본) |
| [dist/data1.json](../../../dist/data1.json) | 배포용 최소화 JSON (주석 없음) |
| [dist/data2.json](../../../dist/data2.json) | 배포용 최소화 JSON (주석 없음) |

## 데이터 형식

두 파일 모두 JSONC(주석 포함 JSON) 형식을 사용합니다.

### 루트 키

| 키 | 내용 |
|----|------|
| `tag` | 일반 태그 |
| `seriesTag` | 작품・시리즈 태그 |
| `characterTag` | 캐릭터 태그 |
| `creatorTag` | 작가 태그 |
| `groupTag` | 서클・그룹 태그 |

### data1: 단순 문자열 매핑

태그 이름이 문맥과 관계없이 하나의 번역어로 결정되는 경우:

```jsonc
"uncensored": "検閲なし"
```

### data2: 문맥 의존 객체

같은 태그 이름이 작품에 따라 다른 번역어를 가지는 경우.
`default`는 매칭되는 작품이 없을 때의 폴백 번역어,
`series`는 작품명을 키로 하는 개별 번역어 맵:

```jsonc
"robin": {
  "default": "ロビン",
  "series": {
    "batman": "ロビン",
    "fire emblem awakening": "ルフレ"
  }
}
```

### 주석 행（data2）

```jsonc
// 10101
"robin": { ... }
```

행 앞의 숫자 주석은 EH (e-hentai) 태그 ID로, 편집 참조용이며 데이터로서의 의미는 없습니다.

### 주의

JSONC는 표준 JSON 파서에서 직접 읽히지 않습니다. 사용 전에 주석과 후행 쉼표를 제거하고 사용하세요.

## 라이선스와 고지

이 데이터셋은 EHWiki의 공개 정보를 참고하여 작성되었습니다.
EHWiki는 별도 명시가 없는 한 GNU Free Documentation License 1.2+로 콘텐츠를 제공한다고 안내합니다.

- 참고: <https://ehwiki.org/wiki/EHWiki:About>
- 참고: <https://ehwiki.org/wiki/EHWiki:Copyrights>

이 저장소의 데이터셋은 GNU Free Documentation License 1.2 or later (GFDL-1.2-or-later)로 배포됩니다.

- 라이선스 전문(원문): [LICENSE](../../../LICENSE)
- 출처/귀속 고지(일본어 원문): [NOTICE.md](../../../NOTICE.md)
- 출처/귀속 고지(한국어 로컬라이즈): [locales/ko/NOTICE.md](NOTICE.md)

## 면책

- 본 데이터셋은 개인 사용 목적에 맞춰 정리된 것으로, 정확성/완전성을 보장하지 않습니다.
- 사용자는 적용되는 라이선스 조건 및 관련 규정을 스스로 확인해야 합니다.
