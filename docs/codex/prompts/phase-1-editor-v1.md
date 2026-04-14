# Phase 1 提示词：SQL 编辑器 v1 与主题联动

> 建议：**新开一个线程**。
> 开始前先阅读：
> - `/AGENTS.md`
> - `/docs/codex/codex-context-min.md`
> - `/docs/product/project-brief.md`
> - `/docs/architecture/solution-blueprint.md`
> - `/docs/acceptance/phase-acceptance.md`

## 本轮目标

在已经可启动的 WinUI 3 工程骨架上，完成 SQL 编辑器 v1 的最小闭环。

## 本轮范围

1. 在内部子窗口中放入 SQL 编辑器宿主
2. 支持基础文本编辑
3. 支持查找替换基础入口
4. 支持块执行识别的最小版本
5. 支持底部结果/消息区域骨架
6. 保证主题切换后编辑器区域视觉正常

## 明确不做

- 不要开始完整联想引擎
- 不要开始完整元数据刷新
- 不要开始 routine 工作台主体
- 不要加入右侧辅助区

## 验收重点

- 内部子窗口中可以正常编辑 SQL
- 至少能创建多个独立 SQL 子窗口
- 底部结果区骨架已经存在
- 主题切换后编辑器容器、窗口容器、底部区域没有明显破坏
- 编译通过
