# branchnew · Fork 当前会话到新的 split pane

把当前 agent 会话（Claude Code / Grok）fork 到当前终端的新分屏（右侧），当前 pane 保持不动。

## 用途

- 执行本地 `branchnew` 可执行文件，将当前会话 fork 一份到右侧新分屏，两边共享同一份上下文。
- 命令本身只做两件事：触发 fork、用一行话告知用户新分屏已打开。

## 用法

```
/branchnew [name]
```

`name` 为可选的 fork 名称（仅 Claude Code 生效：grok 没有 `--name`，fork 出来的会话无名）。

## 后端差异

`branchnew` 按当前终端自动选后端，能力不一样：

| 终端 | 行为 | 备注 |
| --- | --- | --- |
| tmux | 真正的 split pane | 最可靠，走 `tmux split-window` + `send-keys` |
| Warp | 真正的 split pane | 走 CMD-D 分屏 + 剪贴板粘贴命令；**需要给终端授予「辅助功能」权限**，且执行时 Warp 会被抬到前台 |
| iTerm2 | 真正的 split pane | 走 iTerm 自己的 AppleScript `write text`，不抢焦点 |
| Apple Terminal | 开新窗口（无法分屏） | 退化为新窗口 |

## 依赖

- 本地 `branchnew` 可执行文件（在 PATH 中）
- tmux / Warp / iTerm2 任一（按上表）
- Warp 后端额外需要「系统设置 → 隐私与安全性 → 辅助功能」里授权终端

## 安装

```bash
cp branchnew.md ~/.claude/commands/
```

## 来源

Fork from [limin112/branchnew](https://github.com/limin112/branchnew)。
