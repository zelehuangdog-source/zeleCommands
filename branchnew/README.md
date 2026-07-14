# branchnew · Fork session 到新 split pane

把当前 Claude Code session fork 到 iTerm 右侧的新 split pane。

## 用途

- 执行本地 `branchnew` 可执行文件，将当前会话 fork 一份到 iTerm 右侧新分屏。
- 命令本身只做一件事：触发 fork 并用一行话告知用户新分屏已打开。

## 用法

```
/branchnew [name]
```

`name` 为可选的 fork 名称。

## 依赖

- iTerm2
- 本地 `branchnew` 可执行文件（在 PATH 中）

## 安装

```bash
cp branchnew.md ~/.claude/commands/
```

## 来源

Fork from [limin112/branchnew](https://github.com/limin112/branchnew)。
