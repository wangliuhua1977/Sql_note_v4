# Codex 最小上下文

请先阅读：
- `/AGENTS.md`
- `/docs/product/project-brief.md`
- `/docs/architecture/solution-blueprint.md`
- `/docs/acceptance/phase-acceptance.md`
- 当前阶段对应的 `/docs/codex/prompts/*.md`

## 项目一句话
Sql_note_v4 是一个基于 .NET 10 + WinUI 3 的 PostgreSQL-only 桌面 SQL Notebook / SQL Client，主交互是单主窗体内多个编辑子窗口。

## 当前最高优先级
1. SQL 编辑器与联想引擎
2. 函数/存储过程工作台
3. 笔记管理中心
4. 独特笔记图标系统
5. 主题管理与切换

## 当前明确约束
- 保留内部多子窗口模式
- 去掉 Hive 区分
- 不做右侧任务/日志/Inspector
- 主题系统必须从第一阶段就接入
- 不得把核心逻辑塞回窗口类
- 一次只做一个阶段目标

## 本轮如果没有特别说明
默认只做当前阶段最小闭环，不抢跑后续功能。
