# Git 工作流程

## 分支模型

- `main`：唯一主分支，永远可运行。禁止直接提交，禁止强推。
- 功能分支：从最新 `main` 拉出，命名：
  - `feat/SPEC-xxxx-简述` 新功能
  - `fix/简述` 修复
  - `docs/简述` 纯文档
  - `chore/简述` 杂项维护

## 标准流程

1. `git checkout main && git pull` 确保本地 main 最新。
2. `git checkout -b feat/SPEC-xxxx-简述` 开工。
3. 开发中勤提交，一次提交只做一件事；提交信息：`<type>: <说明> (SPEC-xxxx)`。
4. 完工自测后推送功能分支，发起 Pull Request，附 SPEC 链接与自测证据。
5. 测试 Agent 验证通过＋审查 Agent 过清单后，合并回 `main`（优先 Squash 或 Merge commit，项目内统一一种并记入该项目事实文档）。
6. 合并后在 `main` 复跑关键测试，确认无误后删除功能分支。
7. 推送远端 GitHub 备份（位于 Nobi77 名下；可见性按宪法第六章第 5 条：普通项目可公开，商业化 / 涉隐私项目私有）。

## 冲突与回滚

- 合并冲突由功能分支一方解决：把最新 `main` 合入功能分支、解决、复测，再走合并。
- `main` 合并后出问题：优先 `git revert` 该合并提交，不改写已推送的历史。
- 每次发版打 tag：`v主.次.修订`，并在 CHANGELOG 记一行。

## 禁止

- 强推任何已共享分支；把密钥或 `.env` 提交进仓；一个 PR 夹带多个 SPEC 的改动。
