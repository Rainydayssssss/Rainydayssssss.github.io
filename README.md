# Rainydayssssss.github.io

Rain 的网页应用与 Windows 程序发布站：<https://rainydayssssss.github.io/>

这个仓库只存放构建产物，源码在各自的私有仓库中，推送后由 GitHub Actions 自动发布到这里：

| 路径 / Release 标签 | 来源仓库 | 内容 |
| --- | --- | --- |
| `index.html` | 本仓库 | 门户首页（直接在这里修改） |
| `audiobook/` | `audiobook-reader` | 听书网页版（也是 iPhone 主屏幕应用） |
| `mystery/` | `mystery-archive` | 诡秘档案网页版（不含未授权公开的第三方模组） |
| `.well-known/assetlinks.json` | 本仓库 | 让听书安卓版直接打开 `audiobook/` 的配对链接；指纹要与安卓版签名密钥一致 |
| Release `audiobook-android` | `audiobook-reader` | 听书安卓版 `listen-books.apk` + `version.txt` |
| Release `stock-abnormal-monitor` | `stock-abnormal-monitor` | 股票异动监控 zip + `version.txt` |
| Release `media-transcriber` | `media-transcriber` | 影音转文字 zip + `version.txt` |
| Release `beijing-time-hotkey` | `beijing-time-hotkey` | 北京时间定时按键 zip + `version.txt` |
| Release `toolbox` | `rain-toolbox` | Rain 工具箱启动器 `RainToolbox.exe` + `version.txt` + 程序目录 `catalog.txt` |

`audiobook/`、`mystery/` 由对应仓库的工作流整体替换（旧的 `assets/` 文件保留，避免已打开的页面在发布后加载失败），不要手动修改。
