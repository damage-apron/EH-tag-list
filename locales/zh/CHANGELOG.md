# 变更记录 (Changelog, 中文本地化)

此文件通过 AI 翻译生成，可能存在不准确之处。
如与日文原文不一致，请以日文原文为准。

---

跳转到语言区段: [各语言 CHANGELOG](#各语言-changelog)

## [1.1.2] - 2026-03-26

修复本地化文档中的相对路径。

### Changed

- 修正指向日文原文链接的目录层级（上溯3层 -> 上溯2层）
- 修正本地化 README 中 `src` / `dist` / `LICENSE` / `NOTICE` 链接的层级
- 重新检查各本地化 README/CHANGELOG/NOTICE 的相对路径并消除不一致

## [1.1.1] - 2026-03-26

调整本地化文档中的语言链接标签。

### Changed

- 统一语言链接的显示规则
- 在各本地化文档中，仅“日文(原文)”与当前文档语言使用文档语言表记
- 其余语言链接改为各自语言的原生表记

## [1.1.0] - 2026-03-24

标签名称整理和扩展。

### Changed

- 整理标签名称：将「creatorTag」改为「artistTag」，将「groupTag」改为「circleTag」
- 添加了新的翻译数据

### Removed

- 删除了部分条目
- 修改了部分条目

## [1.0.0] - 2026-03-14

首次公开发布。

### Added

- 创建用于数据集发布的文档 (README, LICENSE, NOTICE, CHANGELOG)
- 同捆 GNU Free Documentation License 1.2 or later (GFDL-1.2-or-later) 全文并整理来源信息
- 新增本地化文档 (English, 中文, 한국어)
- 统一文档结构 (语言区段、跳转链接、Markdown 分节、翻译免责声明)

## 各语言 CHANGELOG

- 日文(原文): [CHANGELOG.md](../../CHANGELOG.md)
- English (localized): [locales/en/CHANGELOG.md](../en/CHANGELOG.md)
- 中文(本地化): [locales/zh/CHANGELOG.md](CHANGELOG.md)
- 한국어(로컬라이즈): [locales/ko/CHANGELOG.md](../ko/CHANGELOG.md)
