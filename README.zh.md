# newtype Lite

面向 Codex 的轻量内容团队工作流，以单个 Skill 的方式提供。

[English](README.md)

## newtype Lite 是什么？

newtype Lite 是一个自包含的 Skill，用来把 newtype 的部分内容工作流带进 Codex，但不需要完整的 newtype OS 运行时。

它可以让 Codex 以轻量内容团队路由器的方式处理：

- 内容策划与 brief 梳理
- 研究与资料整理
- 分析、比较与综合判断
- 文章、报告、帖子、脚本、newsletter 写作
- 草稿编辑、重构与润色
- 事实核查
- 从用户提供的材料中提取结构化信息
- 归档可复用的知识摘要

newtype Lite 适合想在 Codex 里使用 newtype 方法层，但不想部署完整系统的用户。

## Lite 版和 newtype OS 的区别

newtype Lite 不是 newtype OS 的替代品。

| 能力 | newtype Lite | newtype OS |
| --- | --- | --- |
| 交付方式 | Codex Skill | 完整 CLI 产品 |
| 运行时 | 使用当前 Codex 会话 | 独立 newtype 运行时 |
| Agent | 通过方法包模拟流程 | 完整多 Agent 工作流 |
| 后台任务 | 不包含 | 按产品能力支持 |
| 知识工作流 | 轻量摘要 | 完整项目工作流 |
| 适合场景 | 在 Codex 内快速处理内容任务 | 完整 newtype 体验 |

如果想获得完整体验，包括整合版 CLI、更完整的工作流编排和完整产品能力，建议部署或安装 newtype OS。

## 工作方式

这个 Skill 使用 `SKILL.md` 作为路由入口。根据任务类型，它只加载 `references/` 目录中需要的方法包：

- `workflow.md`：端到端内容生产
- `interviewer.md`：澄清想法、补全 brief
- `researcher.md`：资料研究与来源整理
- `analyst.md`：比较、诊断、分析和综合判断
- `writer.md`：写作与成稿
- `editor.md`：编辑、重构和润色
- `fact-checker.md`：事实核查
- `extractor.md`：从原始材料中提取信息
- `archivist.md`：沉淀可复用知识卡片

这样既保持轻量，也保留 newtype 的核心方法：先 brief 后写作，先来源后断言，先结构后文字，先核查后确信。

## 安装

把它安装为 Codex Skill：

```bash
mkdir -p ~/.codex/skills/newtype-lite
cp -R SKILL.md references ~/.codex/skills/newtype-lite/
```

然后重启 Codex，或重新加载 Skill 环境。

## 使用方式

在 Codex 中提出内容任务，并按需提到 newtype Lite：

```text
用 newtype Lite 帮我把这些笔记整理成一篇可发布文章。
```

```text
Use newtype Lite to research this topic and draft a newsletter.
```

简单任务通常只会加载一个方法包；复杂任务会按阶段推进，例如先澄清 brief，再研究、分析、写作、编辑和核查。

## 仓库结构

```text
.
├── SKILL.md
└── references/
    ├── analyst.md
    ├── archivist.md
    ├── editor.md
    ├── extractor.md
    ├── fact-checker.md
    ├── interviewer.md
    ├── researcher.md
    ├── workflow.md
    └── writer.md
```

## 和 newtype OS 的关系

newtype Lite 把 newtype OS 中的轻量内容工作流思路打包成 Skill-only 形态。它适合需要便携、无运行时的内容团队方法时使用。

如果需要生产级使用、完整编排能力和完整 newtype 产品体验，请使用 newtype OS。
