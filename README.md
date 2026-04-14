# Sql_note_v4

Sql_note_v4 是一个从 0 开始重写的 Windows 桌面 SQL Notebook / PostgreSQL 客户端。

## 目标

- 主窗体内多子窗口 SQL 编辑体验
- PostgreSQL-only
- 强联想 SQL 编辑器
- 函数 / 存储过程工作台
- 笔记管理中心
- 独特笔记图标系统
- WinUI 3 主题管理与切换

## 当前状态

本仓库按阶段开发。开始编码前请先阅读：

1. `AGENTS.md`
2. `docs/product/project-brief.md`
3. `docs/architecture/solution-blueprint.md`
4. `docs/acceptance/phase-acceptance.md`
5. `docs/codex/codex-context-min.md`
6. 对应阶段的 `docs/codex/prompts/*.md`

## 开发规则

- 先立规约，再动代码。
- 每轮只做一个明确阶段目标。
- 每轮都必须编译并给出验证结果。
- 不得把主逻辑重新塞回窗口类。

## 推荐首轮顺序

- 初始化解决方案与项目骨架
- 建立主题系统基础
- 建立多子窗口工作区骨架
- 保证空壳可编译、可启动
