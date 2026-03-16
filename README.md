# hitomiViewer dataset

## 言語とローカライズ

- ローカライズ文書は `locales` 配下で管理します。
- 翻訳には AI を利用しています。
- ローカライズ版は参考情報であり、不一致がある場合は日本語の正本を優先してください。

### 言語別 README

- 日本語(正本): [README.md](README.md)
- English (localized): [locales/en/README.md](locales/en/README.md)
- 中文(本地化): [locales/zh/README.md](locales/zh/README.md)
- 한국어(로컬라이즈): [locales/ko/README.md](locales/ko/README.md)

## 概要

このディレクトリは、hitomiViewer 用のタグ翻訳データセットを格納しています。

- 主なデータ: [src/data.jsonc](src/data.jsonc)
- 目的: 拡張機能で使用する翻訳辞書データの配布と管理

## データ形式

- 形式: JSONC (コメント付き JSON)
- ルートキー例: `tag`, `seriesTag`, `characterTag`
- 一部キーは文脈依存の解決用に `default` と `series` を持つオブジェクトを使用

JSONC は標準 JSON パーサでは読めない場合があります。必要に応じてコメントを除去して JSON として利用してください。

## ライセンス

このデータセットは、EHWiki の公開情報を参考に作成しています。
EHWiki 側の案内では、コンテンツは特記ない限り GNU Free Documentation License 1.2 以降 (GFDL 1.2+) で提供されています。

- 参考: <https://ehwiki.org/wiki/EHWiki:About>
- 参考: <https://ehwiki.org/wiki/EHWiki:Copyrights>

このリポジトリ内の dataset は、上記との整合のため GNU Free Documentation License 1.2 以降 (GFDL-1.2-or-later) で配布します。

- ライセンス本文/通知: [LICENSE](LICENSE)
- 帰属・出典メモ: [NOTICE.md](NOTICE.md)

## 免責

- 本データセットは個人利用向けに整備したものであり、内容の正確性・完全性は保証しません。
- 利用時は利用者の責任でライセンス要件および各種規約を確認してください。
