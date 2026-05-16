# 项目总结报告

> 由小组全员协作编辑，每周补充内容，最终在 W8 定稿。

## 1. 基本信息

- 项目名称：校园活动报名与签到管理系统
- 课程：软件项目管理实验（软工23级）
- 学院：计算机学院
- 指导教师：佟强
- 报告版本：V0.1（初稿框架）
- 最后更新：2026-04-29

## 2. 小组成员与分工

| 姓名 | 学号 | 角色 | 主要负责 | 工时占比 |
| ---- | ---- | ---- | -------- | -------- |
| TBD  | TBD  | 组长 | 整体协调、进度、风险 | TBD |
| TBD  | TBD  | 成员 | 需求与 WBS           | TBD |
| TBD  | TBD  | 成员 | 设计与开发           | TBD |
| TBD  | TBD  | 成员 | 测试与配置管理       | TBD |

## 3. 项目目标完成情况

> 对照 `requirements.md` 中的功能需求逐条勾选。

- [ ] FR-01 活动信息管理
- [ ] FR-02 学生报名
- [ ] FR-03 报名审核
- [ ] FR-04 签到管理
- [ ] FR-05 统计与导出
- [ ] FR-06 系统维护

## 4. 项目管理过程回顾

### 4.1 进度执行情况

| 里程碑 | 计划时间 | 实际时间 | 偏差   | 说明 |
| ------ | -------- | -------- | ------ | ---- |
| M1     | W1 末    | TBD      | TBD    | TBD  |
| M2     | W3 末    | TBD      | TBD    | TBD  |
| M3     | W5 末    | TBD      | TBD    | TBD  |
| M4     | W6 末    | TBD      | TBD    | TBD  |
| M5     | W7 末    | TBD      | TBD    | TBD  |
| M6     | W8 末    | TBD      | TBD    | TBD  |

### 4.2 风险事件回顾

| 风险         | 是否发生 | 应对效果 | 备注 |
| ------------ | -------- | -------- | ---- |
| 需求频繁变化 | TBD      | TBD      | TBD  |
| 主线开发滞后 | TBD      | TBD      | TBD  |
| 仓库结构混乱 | TBD      | TBD      | TBD  |

### 4.3 配置管理执行情况

- 分支策略执行情况：TBD
- 提交规范执行情况：TBD
- PR 评审执行情况：TBD

### 4.4 冲突演练（Git Conflict Drill）

> 对应课程要求"制造并解决一次冲突"。演练用文件：[`docs/conflict.md`](conflict.md)。
> 本组共 3 名成员，采用**双人双分支真实协作**方式（不使用单人模拟）。

#### 4.4.1 冲突产生原因

- 成员 A：廖鹏懿，分支 `feat/conflict-liao`，将 `docs/conflict.md` 第 1 节 "后端：Spring Boot" 改为 `后端：Node.js`。
- 成员 B：吴珂，分支 `feat/conflict-wu`，将同一行改为 `后端：Django`。
- 二人在不同分支上修改了同一文件的同一行；先合 A 后合 B 时由 Git 报告冲突。
- 冲突类型：`CONFLICT (content): Merge conflict in docs/conflict.md`。

#### 4.4.2 处理方式

1. 项目经理谢凯博先在 `main` 上合入 `feat/conflict-liao`（顺利合并）。
2. 再合入 `feat/conflict-wu` 时触发冲突，`git status` 标记 `docs/conflict.md` 为 `both modified`。
3. 手工编辑 `docs/conflict.md`，删除全部 `<<<<<<<` `=======` `>>>>>>>` 标记。
4. 经组会讨论后，最终决定保留为：`后端：TBD（待最终评审决定）`（或填入实际定稿值）。
5. 执行 `git add docs/conflict.md` → `git commit`（生成 merge commit）→ `git push`。

#### 4.4.3 最终结果

- `main` 分支保留双方独立提交 + 一条解决冲突的 merge commit，提交历史完整可追溯。
- `docs/conflict.md` 中"后端"一行为讨论后的最终值，无残留冲突标记。
- `git log --oneline --graph --all` 输出可见分叉与合并节点。

#### 4.4.4 提交记录证据

```text
（在此粘贴 git log --oneline --graph --all 的实际输出）

例：
*   abc1234 (HEAD -> main) Merge branch 'feat/conflict-wu' into main
|\
| * def5678 (origin/feat/conflict-wu, feat/conflict-wu) docs(conflict): 后端候选改为 Django
* | ghi9012 (origin/feat/conflict-liao, feat/conflict-liao) docs(conflict): 后端候选改为 Node.js
|/
* jkl3456 docs: 新增 conflict.md 用于冲突演练
```

#### 4.4.5 经验总结

- 同一文件同一行的并行修改一定要靠"先沟通、后合并"避免；不可避免时必须手工解决而不是简单选边。
- 解决冲突的提交不应再夹带其它无关改动，便于后续审查。

## 5. 主要交付物

- [ ] 项目仓库与目录结构
- [ ] WBS 文档：[docs/WBS.md](WBS.md)
- [ ] 简化进度计划：[docs/schedule.md](schedule.md)
- [ ] 配置管理文档：[docs/config-management.md](config-management.md)
- [ ] 需求说明：[docs/requirements.md](requirements.md)
- [ ] 冲突演练记录：本文件 §4.4，演练文件 [docs/conflict.md](conflict.md)
- [ ] 总结报告：[docs/summary-report.md](summary-report.md)

## 6. 经验与教训

### 6.1 做得好的地方

- TBD

### 6.2 改进点

- TBD

### 6.3 对后续课程 / 工作的建议

- TBD

## 7. 个人贡献说明

> 每位成员各自填写一段 200–400 字的个人小结。

- 成员 A：TBD
- 成员 B：TBD
- 成员 C：TBD
- 成员 D：TBD

## 8. 附录

- 关键评审会议纪要
- 关键 PR 列表
- 关键 issue 列表
