# Vibe Coding Constitution

本仓库是陈灵王晓豪nobi 的 AI 编程约束总仓：所有用 Vibe Coding 方式开发的项目、脚本与工具，都遵循本仓的宪法、文档结构与 SPEC 流程。任何 Muse 账号 / 编程 Agent 接到编程任务时，先读本仓，再动手。

## 阅读顺序（任何 Agent 必读，不许跳步）

1. `CONSTITUTION.md` — 宪法正本：优先级、铁律、禁止事项
2. `Docs/README.md` — 文档分离与产品事实文档的组织规则
3. `specs/SPEC-template.md` — 单次开发任务的规格模板
4. `agents/` — 按自己的角色读对应文件（规划 / 开发 / 测试 / 审查）
5. `workflows/git-workflow.md` 与 `workflows/testing-gates.md` — 分支流程与测试门禁

一句话版入口在 `prompts/bootstrap-prompt.md`：把那段话粘贴给任何新 Agent，它就知道来本仓按规矩干活。

## 仓库结构

| 路径 | 职责 |
|---|---|
| `CONSTITUTION.md` | 约束正本，版本化管理，改动须走 CHANGELOG |
| `AGENTS.md` / `CLAUDE.md` | 给各类编程 Agent 的入口指针（内容以 CONSTITUTION 为准） |
| `Docs/` | 产品事实文档区：只放规划与事实，不放代码 |
| `specs/` | SPEC 模板与已立项的单次任务规格 |
| `agents/` | 规划 / 开发 / 测试 / 审查四种角色的工作规程 |
| `workflows/` | Git 流程、开发流程、测试门禁 |
| `registry/PROJECTS.md` | 全部项目的登记册（项目名、仓库、状态、入口） |
| `registry/CAPABILITIES.md` | 能力登记册：已沉淀的可复用能力及其调用方式 |
| `prompts/` | 可直接粘贴使用的启动提示词 |
| `projects/` | 小型脚本 / 工具的打包区（每个项目一个子目录，自带 Docs 与 specs） |

## 核心原则（详见 CONSTITUTION.md）

- 先文档，后代码；先 SPEC，后开发。
- 产品事实只有一个出处，冲突按宪法规定的优先级裁决。
- 开发与测试只认同一份 SPEC，验收标准在动手前写死。
- 主分支永远可用；一切改动走分支、过测试、再合并。
- 密钥、密码、Token 永不进仓。

## 版本

当前版本见 `VERSION` 文件，变更记录见 `CHANGELOG.md`。
