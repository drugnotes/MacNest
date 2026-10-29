# 麦集 MacNest

Mac 好应用，常用常新。原生 macOS 应用发现与管理工具，基于 Homebrew Cask。

本仓库仅提供应用下载、使用说明与问题反馈，不包含应用源码。

## 下载

**最新版本：[0.6.0（build 7）](https://github.com/drugnotes/MacNest/releases/tag/v0.6.0)**

- [下载 MacNest-0.6.0-universal.zip](https://github.com/drugnotes/MacNest/releases/download/v0.6.0/MacNest-0.6.0-universal.zip)
- [下载 SHA256SUMS.txt](https://github.com/drugnotes/MacNest/releases/download/v0.6.0/SHA256SUMS.txt)

要求 macOS 14 或更新版本。应用为 Apple Silicon 与 Intel 通用二进制；Intel 尚未实机验收。

0.6.0 已使用 Developer ID 签名并通过 Apple 公证，发布包已通过严格签名、公证票据与 Gatekeeper 检查。

将两个附件下载到同一目录，在终端执行：

```sh
shasum -a 256 -c SHA256SUMS.txt
```

解压 ZIP，将 MacNest.app 拖入“应用程序”。替换旧副本前请等待应用任务结束并退出。GitHub 自动生成的 Source code 归档不是应用安装包。

## 功能

- 侧栏搜索、精选专题、用途分类和 30 天安装榜。
- 查看、安装、更新与卸载 Homebrew Cask 应用，操作日志集中展示。
- 将匹配的本机应用转换为 Homebrew 管理：先备份，再安装，失败尝试恢复。
- 全部转换按顺序执行；失败恢复成功则继续，无法恢复则停止并汇总结果。
- 玻璃质感应用图标与原生界面，新系统采用可用的 Liquid Glass，旧系统使用系统材质回退。

榜单按 Homebrew Cask 30 天安装事件次数排序，不是独立用户数。应用每日自动检查并在启动或唤醒时补刷，数据新鲜度取决于上游统计。

## 使用说明

安装和管理功能需要本机 Homebrew。需要管理员权限的原应用可能无法自动转换，请按应用提示处理；转换前先退出待转换应用并保留备份。部分应用可能需要重新登录或激活。

应用没有后台自动更新机制，可从 Releases 下载新版。

### Homebrew 安装渠道

现有第三方 tap 尚未同步 0.6.0；需要最新版请使用上方 Release 下载，勿将 tap 版本视为本次新版。

```sh
brew tap drugnotes/tap
brew trust --cask drugnotes/tap/macnest
brew install --cask drugnotes/tap/macnest
```

Homebrew 安装不会绕过系统安全检查；已有手动安装副本时请先自行保留或移走旧副本，避免路径冲突。

## 反馈与许可

请通过 [Issues](https://github.com/drugnotes/MacNest/issues) 提交问题，分享日志前移除个人信息和凭据。

应用闭源分发，本仓库未授予应用源码或二进制的开源许可。Homebrew 为独立项目，MacNest 并非其官方客户端。
