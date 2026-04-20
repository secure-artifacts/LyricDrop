# LyricDrop 1.0.0

首个公开版本。

## 核心功能

- **菜单栏常驻**：无 Dock 图标，菜单栏实时显示当前歌词
- **本地音频 + LRC**：mp3 / wav / aiff / aac / m4a / flac / ogg / wma，支持拖拽
- **从 URL 加载**音频
- **桌面悬浮歌词**：可拖动 / 锁定，6 种主题渐变（霓虹 / 日落 / 海洋 / 森林 / 雪夜 / 樱花）
- **三种显示模式**：水平扫过 / 逐字滚动 / 水平滚动
- **卡拉 OK 模式**：歌词逐字渐变染色
- **完整播放控制**：播放 / 暂停 / 停止、±5 秒跳转、进度拖动、循环
- **倍速播放**：0.5× / 0.75× / 1× / 1.25× / 1.5× / 2×
- **歌词时间校准**：±0.5 秒步进，点击归零

## 安装

下载 `LyricDrop-1.0.0.dmg`，打开后把 `LyricDrop.app` 拖到 `Applications` 文件夹。

首次启动若提示"无法打开"，在 **系统设置 → 隐私与安全性** 中点"仍要打开"，或终端执行：

```sh
xattr -cr /Applications/LyricDrop.app
```

## 系统要求

macOS 15.7 或更新版本（Intel 和 Apple Silicon 均支持）。

## Build Provenance

本次 DMG 由 GitHub Actions 构建并自动签发 build provenance attestation。可通过以下命令验证：

```sh
gh attestation verify LyricDrop-1.0.0.dmg --repo secure-artifacts/LyricDrop
```
