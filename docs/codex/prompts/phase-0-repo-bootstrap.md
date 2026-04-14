# Phase 0 提示词：仓库规约与工程起步

> 建议：**新开一个线程**。
> 开始前先阅读：
> - `/AGENTS.md`
> - `/docs/codex/codex-context-min.md`
> - `/docs/product/project-brief.md`
> - `/docs/architecture/solution-blueprint.md`
> - `/docs/acceptance/phase-acceptance.md`

你现在要在空仓库中完成 **Phase 0 + Phase 1 的工程起步部分**，但不要抢跑实现后续复杂功能。

## 本轮目标

1. 创建 WinUI 3 + .NET 10 解决方案骨架
2. 按分层建立项目目录与项目引用关系
3. 建立最基础的 Host / DI 启动结构
4. 建立主题系统骨架（Follow System / Light / Dark）
5. 建立主窗体和内部多子窗口工作区骨架
6. 保证应用可编译、可启动

## 必须遵守

- 不要实现 Hive 分支
- 不要实现右侧任务/日志/Inspector
- 不要把业务逻辑直接写死在窗口 code-behind
- 不要开始写完整 SQL 编辑器、联想引擎、routine 工作台，只搭骨架
- 不要把所有阶段一起做完

## 建议产出

### 解决方案与项目
- `Sql_note_v4.sln`
- `src/SqlNote.App`
- `src/SqlNote.Protocol`
- `src/SqlNote.Data`
- `src/SqlNote.Metadata`
- `src/SqlNote.Editor`
- `src/SqlNote.Features`
- 至少 1 个基础测试项目

### App 层
- `App.xaml`
- `App.xaml.cs`
- `Program.cs`（如需要）
- `Hosting/AppHostBuilder.cs`
- `Windows/MainWindow.xaml`
- `ViewModels/AppShellViewModel.cs`
- `ViewModels/WorkspaceHostViewModel.cs`

### 主题系统骨架
- `IThemeService`
- `ThemeService`
- `ThemeMode` 枚举或模型
- 主题持久化接口
- 主题切换命令

### 多子窗口工作区骨架
- `IDocumentWindowManager`
- `DocumentWindowManager`
- `SqlDocumentWindowViewModel`
- 示例子窗口创建命令
- 主窗体内可新建并显示至少一个子窗口容器

## 验证要求

必须执行并反馈：
1. `dotnet restore`
2. `dotnet build`
3. 应用启动验证
4. 至少一次主题切换验证
5. 至少一次新建内部子窗口验证

## 输出要求

最后必须给出：
- 修改文件列表
- 项目结构说明
- 编译结果
- 运行结果
- 尚未实现项
- 下一轮建议（应聚焦 SQL 编辑器 v1）
