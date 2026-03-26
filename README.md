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

このディレクトリは、hitomiViewer 用のタグ翻訳データを格納しています。

このリポジトリは、ライセンス管理（GFDL 分離）のためにデータのみを切り出して公開する目的で運用しています。
データを利用する本体プログラムは別リポジトリで開発中です。

- 目的: 拡張機能で使用する翻訳辞書データの配布と管理

## ファイル構成

| ファイル | 内容 |
|---------|------|
| [src/data1.jsonc](src/data1.jsonc) | 単純な一対一対応の翻訳データ（原本） |
| [src/data2.jsonc](src/data2.jsonc) | 文脈依存の翻訳データ（原本） |
| [dist/data1.json](dist/data1.json) | data1 の配布用 JSON（コメント・改行なし） |
| [dist/data2.json](dist/data2.json) | data2 の配布用 JSON（コメント・改行なし） |

## データ形式

両ファイルとも形式は JSONC (コメント付き JSON) です。

### ルートキー

| キー | 内容 |
|------|------|
| `tag` | 一般タグ |
| `seriesTag` | 作品・シリーズタグ |
| `characterTag` | キャラクタータグ |
| `artistTag` | 作者タグ |
| `circleTag` | サークル・グループタグ |

### data1: 単純文字列マッピング

タグ名が文脈によらず一意に翻訳できる場合:

```jsonc
"uncensored": "検閲なし"
```

### data2: 文脈依存オブジェクト

同名タグが作品によって異なる訳語を持つ場合。
`default` はどの作品にも該当しない場合のフォールバック訳語、
`series` は作品名をキーとした個別訳語のマップ:

```jsonc
"robin": {
  "default": "ロビン",
  "series": {
    "batman": "ロビン",
    "fire emblem awakening": "ルフレ"
  }
}
```

### コメント行（data2）

```jsonc
// 10101
"robin": { ... }
```

行頭の数字コメントは EH (e-hentai) のタグ ID です。編集・照合時の管理用であり、データとしての意味はありません。

### 注意

JSONC は標準 JSON パーサでは読めません。利用時はコメントと末尾カンマを除去してから JSON として使用してください。

## 開発

データセットの変換・管理に使用する ツール・プログラムは以下で公開しています。

- **EH tag list generator**: <https://github.com/damage-apron/EH-tag-list-generator>

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
