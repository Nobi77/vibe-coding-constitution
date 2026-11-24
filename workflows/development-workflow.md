# 开发全流程（一张图看懂）

```
用户意图
↓ 规划 Agent 确认目标与范围
事实文档（项目仓 Docs/，按分级建齐必备文档）
↓
SPEC 起草（draft）→ 批准（approved，验收标准冻结，记批准人）
↓
开发 Agent 置 in-progress → 功能分支实现＋自测（含既有测试回归）
↓
测试 Agent 在干净上下文按验收标准验证，绑定 commit SHA → verified
（分支有新提交或 rebase 后 verified 自动失效，须重验）
↓
功能分支内同步更新受影响的事实文档 → 审查 Agent 过清单
↓
合并回 main → main 跑冒烟测试（失败立即 git revert）
↓
收尾 docs 提交：SPEC 置 done＋证据落位 → 推送 GitHub 备份
↓
按宪法第九章四栏模板汇报
```

## 每一步的产出物

| 步骤 | 产出 | 存放 |
|---|---|---|
| 规划 | 事实文档 / SPEC | 项目仓 `Docs/`、`specs/` |
| 开发 | 代码＋自测记录 | 功能分支、PR 描述 |
| 测试 | 验证结论＋证据（绑定 commit SHA） | PR 描述，收尾时落入 SPEC 文末 |
| 审查 | 审查记录 | PR 评论 |
| 收尾 | SPEC 置 done、更新后的事实文档、CHANGELOG 一行 | 项目仓 docs 提交 |

## 新项目启动清单

- [] 建项目仓库并初始化 `main`，推送 GitHub（可见性按宪法第六章定；公开仓加 LICENSE）
- [] 建 `Docs/`（按分级表建必备文档）、`specs/`、`.gitignore`、`.env.example`
- [] 宪法以链接引用总仓为准；如放副本，副本顶部注明总仓来源版本号
- [] 在总仓 `registry/PROJECTS.md` 登记一行（注意：登记在总仓，文档建在项目仓，两者别混）
- [] 按分级写齐必备事实文档，第一份 SPEC 经批准后再开工
