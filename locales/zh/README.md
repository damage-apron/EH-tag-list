# hitomiViewer dataset (中文本地化)

此文件通过 AI 翻译生成，可能存在不准确之处。
如与日文原文不一致，请以日文原文为准。

---

## 语言与本地化

- 本地化文档统一放在 `locales` 目录下。
- 翻译使用了 AI 辅助。
- 本地化文档仅供参考。如有不一致，请以日文原文为准。

### 各语言 README

- 日文(原文): [README.md](../../../README.md)
- English (localized): [locales/en/README.md](../en/README.md)
- 中文(本地化): [locales/zh/README.md](README.md)
- 한국어(로컬라이즈): [locales/ko/README.md](../ko/README.md)

## 概要

此目录用于存放 hitomiViewer 的标签翻译数据。

- 目的: 分发和管理扩展功能使用的词典数据

## 文件结构

| 文件 | 内容 |
|------|------|
| [src/data1.jsonc](../../../src/data1.jsonc) | 简单的一对一翻译数据（原文件） |
| [src/data2.jsonc](../../../src/data2.jsonc) | 依赖上下文的翻译数据（原文件） |
| [dist/data1.json](../../../dist/data1.json) | 用于分发的压缩 JSON（无注释） |
| [dist/data2.json](../../../dist/data2.json) | 用于分发的压缩 JSON（无注释） |

## 数据格式

两个文件均使用 JSONC（带注释的 JSON）格式。

### 根键

| 键 | 内容 |
|----|------|
| `tag` | 一般标签 |
| `seriesTag` | 作品・系列标签 |
| `characterTag` | 角色标签 |
| `artistTag` | 作者标签 |
| `circleTag` | 社团・团体标签 |

### data1：简单字符串映射

标签名称可唯一翻译时使用：

```jsonc
"uncensored": "検閲なし"
```

### data2：依赖上下文的对象

同名标签在不同作品中有不同译名时使用。
`default` 为未匹配到任何作品时的默认译名，`series` 为以作品名为键的译名映射：

```jsonc
"robin": {
  "default": "ロビン",
  "series": {
    "batman": "ロビン",
    "fire emblem awakening": "ルフレ"
  }
}
```

### 注释行（data2）

```jsonc
// 10101
"robin": { ... }
```

行首数字注释为 EH (e-hentai) 标签 ID，仅用于编辑参考，无数据含义。

### 注意

JSONC 无法被标准 JSON 解析器直接读取。使用前请先去除注释和末尾逗号。

## 许可证与注明

本数据集参考了 EHWiki 的公开信息。
EHWiki 说明其内容在未特别注明时，按 GNU Free Documentation License 1.2+ 提供。

- 参考: <https://ehwiki.org/wiki/EHWiki:About>
- 参考: <https://ehwiki.org/wiki/EHWiki:Copyrights>

本仓库中的数据集按 GNU Free Documentation License 1.2 or later (GFDL-1.2-or-later) 分发。

- 许可证全文(原文): [LICENSE](../../../LICENSE)
- 署名与来源说明(日文原文): [NOTICE.md](../../../NOTICE.md)
- 署名与来源说明(中文本地化): [locales/zh/NOTICE.md](NOTICE.md)

## 免责声明

- 本数据集为个人用途整理，不提供任何形式的保证。
- 使用前请由使用者自行确认适用的许可条款及相关规则。
