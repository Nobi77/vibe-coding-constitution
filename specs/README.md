# specs 文件夹规范

本文件夹放单次开发任务的 SPEC（需求规格说明书）与模板。

## 命名与编号

- 文件名：`SPEC-xxxx-简述.md`，xxxx 为四位序号，从 0001 起全局顺延，不复用。
- 一个 SPEC 只装一个任务；任务变大到需要拆分时，新开 SPEC 并互相引用。

## 生命周期

`draft → approved → in-progress → verified → done`

- draft：规划 Agent 起草中，未批准前开发不得开工。
- approved：用户或规划 Agent 批准，验收标准冻结。
- in-progress：开发进行中；要改 SPEC 先升小版本号（如 v1.0 → v1.1）并在文末记录变更原因。
- verified：测试 Agent 按验收标准逐条验证通过，证据链接附在 SPEC 文末。
- done：已合并回 main，受影响的事实文档已同步更新。

## 归档

done 的 SPEC 保留在本文件夹（或项目自定的 `specs/archive/`），不删除，作为日后追溯依据。
