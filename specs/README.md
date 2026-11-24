# specs 文件夹规范

本文件夹放单次开发任务的 SPEC（需求规格说明书）与模板。

## 命名与编号

- 文件名：`SPEC-xxxx-简述.md`，xxxx 为四位序号，在**单个项目内**从 0001 起顺延，不跨项目共用编号，不复用已取消的编号。
- 一个 SPEC 只装一个任务；任务变大到需要拆分时，新开 SPEC 并互相引用（在模板「关联 SPEC」栏填写）。

## 生命周期与状态写入责任

`draft → approved → in-progress → verified → done`，异常状态：`blocked`（遇阻待裁决，注明卡点）、`cancelled`（取消，注明原因）。

| 状态 | 由谁置位 | 依据 |
|---|---|---|
| draft | 规划 Agent | 起草完成 |
| approved | 用户或被授权的规划 Agent（批准权边界见宪法第四章） | 验收标准冻结，记批准人与日期 |
| in-progress | 开发 Agent | 开工时置位（仅许改状态栏） |
| verified | 测试 Agent | 按验收标准逐条验证通过，证据绑定功能分支 commit SHA；分支有新提交或 rebase 后自动失效 |
| done | 收尾人（规划 Agent 或项目负责人） | 合并后走 docs 提交置位，并确认受影响事实文档已同步 |

各角色只许改 SPEC 的状态栏与本角色的证据区；正文变更走升版本流程（见宪法第四章）。

## 归档

done / cancelled 的 SPEC 保留在本文件夹（或项目自定的 `specs/archive/`），不删除，作为日后追溯依据。
