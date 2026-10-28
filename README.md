# 麦集 MacNest

Mac 好应用，常用常新。基于 Homebrew Cask 的 macOS 应用发现与管理工具。

此仓库仅用于二进制发布、使用说明与问题反馈，不包含应用源码。

## 下载与安装

当前版本 0.5.0，支持 macOS 14+、Apple Silicon（不支持 Intel）。
从 [Releases](https://github.com/drugnotes/MacNest/releases) 下载 `MacNest-0.5.0-arm64.zip`，解压后拖入应用程序目录。

通过 Homebrew 安装：

```sh
brew tap drugnotes/tap
brew install --cask drugnotes/tap/macnest
```

更新：`brew update && brew upgrade --cask drugnotes/tap/macnest`。
卸载：`brew uninstall --cask drugnotes/tap/macnest`（不清理用户配置或备份）。

当前为 ad-hoc 签名、未经 Apple 公证的预览版，macOS 可能阻止首次启动。Homebrew 不绕过系统安全检查。
已有手动安装副本时先退出应用，再通过 Finder 保留或移走旧副本，避免安装冲突；不要使用覆盖参数强制替换。
本应用无后台自动更新机制。

## 校验

将 ZIP 和 SHA256SUMS.txt 下载至同一目录，执行 `shasum -a 256 -c SHA256SUMS.txt`。
GitHub 自动生成的 Source code 压缩包只包含本公开仓库的说明文件，不是应用安装包。

## 源码与许可

应用闭源分发，此仓库未授予应用源码或二进制的开源许可。
Homebrew 是独立项目，本应用并非其官方客户端。
