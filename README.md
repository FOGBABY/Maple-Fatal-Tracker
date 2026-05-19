# Maple Countdown

一个干净的 Windows 30 秒倒计时小工具：40x40 透明无边框窗口、置顶、可拖拽，不注入游戏、不读内存、不模拟输入。

把 `timer.png` 放在程序同目录下，程序会以 70% 透明度显示这张图片，并覆盖一层顺时针逐秒减少的阴影。

## 快捷键

- `Ctrl+Alt+F9`：启动 / 继续
- `Ctrl+Alt+F10`：暂停
- `Ctrl+Alt+F11`：重置到 30 秒
- 鼠标左键拖拽移动位置
- 鼠标右键关闭程序

## 构建

```powershell
go build -ldflags="-H windowsgui" -o "Simple Timer.exe" .
```

## 安全边界

本程序只使用普通 Win32 窗口、透明分层窗口和 `RegisterHotKey` 全局热键；没有使用 AutoHotkey、键鼠 hook、`SendInput`、模拟按键、读内存、DLL 注入或 DirectX 注入式 overlay。

没有任何同机程序可以承诺 100% 不触发游戏反作弊误判。如果账号安全优先，第二屏计时器仍然是最稳妥方案。
