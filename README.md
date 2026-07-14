# zeleCommands

个人 Claude Code Commands 集合（slash command，使用 `$ARGUMENTS`、`!` 执行等 command 语法）。

每个 command 一个文件夹，内含命令文件 `<name>.md` 与说明 `README.md`。

## Commands 列表

| Command | 说明 | 来源 |
|---------|------|------|
| [clarify](./clarify/) | 需求澄清器，动手之前系统性收集需求细节，消除歧义 | 原创 |
| [ultracode](./ultracode/) | 多智能体编排器，通过多 agent 并行协作完成复杂任务 | 原创 |
| [branchnew](./branchnew/) | Fork 当前 Claude Code session 到 iTerm 新 split pane | Fork from [limin112/branchnew](https://github.com/limin112/branchnew) |

## 安装

拷贝对应文件夹里的 `<name>.md` 到本地 commands 目录即可：

```bash
cp clarify/clarify.md ~/.claude/commands/
```

> Skills 见独立仓库 [zeleSkills](https://github.com/zelehuangdog-source/zeleSkills)。
