# LyricDrop

一款极简的 macOS 菜单栏 LRC 歌词播放器。常驻菜单栏，实时显示当前歌词，支持桌面悬浮歌词和卡拉 OK 模式。

## 截图

<table>
  <tr>
    <td width="50%" align="center" valign="top">
      <img src="docs/screenshots/1.png" alt="menu bar panel" /><br/>
      <b>菜单栏面板</b><br/>
      <sub>完整播放器 UI、进度条、倍速控制、歌词列表都在菜单栏弹出面板里。</sub>
    </td>
    <td width="50%" align="center" valign="top">
      <img src="docs/screenshots/2.png" alt="desktop lyrics and settings" /><br/>
      <b>桌面悬浮歌词 &amp; 外观设置</b><br/>
      <sub>多种主题渐变、字体、字号、显示模式（水平扫过 / 逐字滚动 / 水平滚动）和显示行数可调；下方即为卡拉 OK 模式的逐字染色效果。</sub>
    </td>
  </tr>
</table>

## 功能

- **菜单栏常驻**：无 Dock 图标，占用空间极小，菜单栏实时渲染当前歌词
- **本地音频 + LRC**：支持 `mp3`/`wav`/`aiff`/`aac`/`m4a`/`flac`/`ogg`/`wma`，拖拽即可加载
- **从 URL 加载**：支持直接从网络地址加载音频
- **桌面悬浮歌词**：可随意拖动到屏幕任何位置，支持锁定/解锁
- **丰富的外观设置**：内置霓虹 / 日落 / 海洋 / 森林 / 雪夜 / 樱花等主题渐变；字体、字号、显示行数（1/3/5/7 行）、窗口宽度可调
- **三种显示模式**：水平扫过 / 逐字滚动 / 水平滚动
- **卡拉 OK 模式**：歌词逐字渐变染色
- **完整播放控制**：播放/暂停/停止、±5 秒快进快退、进度拖动、循环播放
- **倍速播放**：0.5× / 0.75× / 1× / 1.25× / 1.5× / 2×
- **歌词时间校准**：±0.5 秒步进调整，点击归零
- **歌词列表**：可滚动预览全部歌词，点击任意行跳转到该时间点
- **音量控制**：独立音量滑块 + 一键静音

## 系统要求

- macOS 15.7 或更新版本

## 安装

1. 从 [Releases](https://github.com/ninetyeights/LyricDrop/releases) 页面下载最新的 `LyricDrop.dmg`
2. 打开 DMG，把 `LyricDrop.app` 拖到 Applications 文件夹
3. 首次启动时若提示"无法打开"，在 **系统设置 → 隐私与安全性** 中点击"仍要打开"；或在终端执行：
   ```sh
   xattr -cr /Applications/LyricDrop.app
   ```

## 使用

1. 启动后在菜单栏会出现一个文字图标，点击打开面板
2. 点击 **Open Audio** 加载音频文件，点击 **Open LRC** 加载同名歌词文件（或直接拖入）
3. 点击播放按钮开始播放，菜单栏会实时显示当前歌词
4. 点击 **文字气泡** 图标切换桌面悬浮歌词；拖动悬浮窗到任意位置，点击锁图标锁定
5. 点击 **画笔** 图标切换卡拉 OK 模式

## LRC 格式支持

标准 LRC 时间戳格式：

```
[00:12.34]第一行歌词
[00:15.67]第二行歌词
[ti:歌曲名]
[ar:歌手]
[al:专辑]
```

同时支持逐字 LRC（Enhanced LRC）用于卡拉 OK 模式。

## 从源码构建

需要 Xcode 15+ 和 macOS 15.7 SDK。

```sh
git clone https://github.com/ninetyeights/LyricDrop.git
cd LyricDrop
xcodebuild -project LyricDrop.xcodeproj \
           -scheme LyricDrop \
           -configuration Release \
           build
```

## License

MIT
