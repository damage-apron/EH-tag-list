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

此目录用于存放 hitomiViewer 的标签翻译数据集。

- 主要数据: [src/data.jsonc](../../../src/data.jsonc)
- 目的: 分发和管理扩展功能使用的词典数据

## 数据格式

- 格式: JSONC (带注释的 JSON)
- 根键示例: `tag`, `seriesTag`, `characterTag`
- 部分键为按上下文解析，使用包含 `default` 与 `series` 的对象

JSONC 可能无法被标准 JSON 解析器直接读取。
如需严格 JSON，请先去除注释。

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
