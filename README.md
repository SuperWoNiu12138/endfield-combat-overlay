# 管理员终端

终末地战斗浮窗。在自己摆放的位置显示干员终结技充能、连携冷却、技能按钮和技力，支持拖动、缩放、透明度和多套布局。还可以给每支队伍写好排轴（出手顺序），战斗中浮窗跟着提示下一步该按什么。

通过 Windows Graphics Capture 捕获游戏窗口并识别 HUD，不注入游戏、不读取游戏进程内存、不抓包。游戏切到后台、最小化或关闭时，停止截图并隐藏浮窗。

本仓库只用来发布安装包和使用说明，程序本身不开源。

## 下载和使用

1. 打开 [GitHub 最新发布](https://github.com/SuperWoNiu12138/endfield-combat-overlay/releases/latest)，下载 Assets 中以 `x64-setup.exe` 结尾的安装包。GitHub 慢的话，到 [CNB 镜像](https://cnb.cool/feifeifox-toolbox/endfield-combat-overlay/-/releases) 下载同一个安装包。附带的「Source code」只有这份说明，不用下载。
2. 双击安装包完成安装，再从开始菜单启动「管理员终端」，出现管理员权限提示时选择「是」。无需安装开发工具。
3. 打开终末地并切回游戏，浮窗会跟随游戏窗口显示。
4. 按 `Ctrl+F9` 进入编辑模式，调整位置、大小和透明度，再按一次锁定。

程序常驻系统托盘，可以从托盘打开设置或退出。没进游戏时看不到浮窗属于正常情况；也可以按 `Ctrl+F9` 进入编辑模式预览布局。

| 默认快捷键 | 操作 |
| --- | --- |
| `Ctrl+F9` | 编辑 / 锁定布局 |
| `Ctrl+F10` | 隐藏 / 显示浮窗 |
| `Ctrl+F11` | 切换布局方案 |
| `Ctrl+F12` | 单独隐藏 / 显示排轴 |

快捷键可以在设置里修改。程序会自动检查新版本，有新版本时托盘菜单里会出现「更新到 vX」，点一下就会下载安装。布局保存在 `%APPDATA%\endfield-overlay\config.json`。

每个发布都附有 `SHA256SUMS.txt`，可以用 `certutil -hashfile 安装包.exe SHA256` 核对下载的安装包是否完整。

## 支持范围

- Windows x64，使用系统的 WebView2 运行时。
- 支持 16:9 和 16:10 游戏画面；21:9 和自定义游戏内 UI 缩放尚不支持。
- HUD 被菜单、过场动画或特效遮挡时，识别可能暂时不可用。

## 反馈

遇到问题请在 [Issues](https://github.com/SuperWoNiu12138/endfield-combat-overlay/issues) 里说明游戏分辨率、是否全屏，最好附一张战斗画面截图。

## 许可

免费提供给个人使用，保留所有权利，详见 [LICENSE](LICENSE)。本程序与终末地的开发商和发行商无关。
