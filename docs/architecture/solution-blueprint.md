# 解决方案蓝图

## 1. 解决方案建议

```text
Sql_note_v4.sln
src/
  SqlNote.App/
  SqlNote.Protocol/
  SqlNote.Data/
  SqlNote.Metadata/
  SqlNote.Editor/
  SqlNote.Features/
tests/
  SqlNote.App.Tests/
  SqlNote.Protocol.Tests/
  SqlNote.Data.Tests/
  SqlNote.Metadata.Tests/
  SqlNote.Editor.Tests/
  SqlNote.Features.Tests/
docs/
```

## 2. 项目职责

### SqlNote.App
- WinUI 3 主程序壳
- Host / DI / 启动
- 主窗体
- 多子窗口工作区宿主
- 主题接线

### SqlNote.Protocol
- 异步 SQL 执行协议
- 远端接口封装
- 错误模型
- 结果响应解析
- 取消 / 重试 / 状态轮询

### SqlNote.Data
- SQLite
- Migration
- 笔记、版本、活动流、工作区快照等仓储
- 本地状态持久化

### SqlNote.Metadata
- 元数据缓存
- 元数据刷新
- DDL 获取
- 联想数据查询

### SqlNote.Editor
- 编辑器宿主
- SQL 语义上下文分析
- 联想引擎
- 执行块识别
- 错误定位
- 结果区模型

### SqlNote.Features
- Routine Workbench
- 笔记管理中心
- 图标系统
- 主题管理服务
- 备份 / 恢复
- 后续云同步等扩展

## 3. 核心 ViewModel 建议

- AppShellViewModel
- WorkspaceHostViewModel
- SqlDocumentWindowViewModel
- ResultWorkspaceViewModel
- ObjectBrowserViewModel
- NoteManagerViewModel
- RoutineWorkbenchViewModel
- ThemeSettingsViewModel

## 4. 核心服务建议

- IThemeService
- IDocumentWindowManager
- IExecutionCoordinator
- ISqlContextAnalyzer
- ISuggestionService
- IMetadataRefreshService
- IRoutineVersionService
- INoteIconService
- INoteManagerService
- IWorkspaceSnapshotService

## 5. 明确的架构原则

- 主窗体只负责编排，不负责核心业务。
- 编辑器语义分析与联想 UI 分离。
- 结果控件只有一套实现。
- 例程版本与普通笔记版本分开。
- 图标生成是独立服务，不要散落到 UI 控件里。
- 主题切换必须通过统一服务管理，不得各处自行判断深浅色。
