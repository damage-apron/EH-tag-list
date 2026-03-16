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

이 디렉터리는 hitomiViewer용 태그 번역 데이터셋을 저장합니다.

- 주요 데이터: [src/data.jsonc](../../../src/data.jsonc)
- 목적: 확장 기능에서 사용하는 사전 데이터의 배포 및 관리

## 데이터 형식

- 형식: JSONC (주석 포함 JSON)
- 루트 키 예시: `tag`, `seriesTag`, `characterTag`
- 일부 키는 문맥 기반 해석을 위해 `default`와 `series`를 가진 객체를 사용합니다

JSONC는 표준 JSON 파서에서 바로 읽히지 않을 수 있습니다.
엄격한 JSON이 필요하면 주석을 제거한 뒤 사용하세요.

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
