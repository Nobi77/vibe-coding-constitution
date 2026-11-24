# 开发全流程（一张图看懂）

```
用户意图
  ↓ 规划 Agent 确认目标与范围
事实文档（Docs/，新产品建骨架，老产品查现状）
  ↓
SPEC 起草（draft）→ 用户/规划批准（approved，验收标准冻结）
  ↓
开发 Agent 拉功能分支实现（in-progress）＋自测
  ↓
测试 Agent 按验收标准独立验证 → verified（不通过退回开发）
  ↓
审查 Agent 过清单 → 合并回 main → main 复测
  ↓
同步更新受影响的事实文档 → SPEC 置 done
  ↓
推送 GitHub 备份 → 按宪法第九章四栏汇报
```

## 每一步的产出物

| 步骤 | 产出 | 存放 |
|---|---|---|
| 规划 | 事实文档 / SPEC | 项目 `Docs/`、`specs/` |
| 开发 | 代码＋自测记录 | 功能分支、PR 描述 |
| 测试 | 验证结论＋证据 | SPEC 文末 |
| 审查 | 审查记录 | PR 评论 |
| 收尾 | 更新后的事实文档、CHANGELOG 一行 | 项目仓库 |

## 新项目启动清单

- [ ] 建仓库并初始化 `main`，推送 GitHub（可见性按宪法第六章第 5 条定）
- [ ] 建 `Docs/`（按 Docs/README.md 清单）、`specs/`、`.gitignore`、`.env.example`
- [ ] 把本宪法以链接或副本形式放入项目（副本须注明以总仓为准）
- [ ] 在总仓 `registry/PROJECTS.md` 登记一行
- [ ] 写第一份事实文档（总览）与第一份 SPEC
