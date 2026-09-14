# zeleCommands

个人 Claude Code Commands 集合（slash command，使用 `$ARGUMENTS`、`!` 执行等 command 语法）。

每个 command 一个文件夹，内含命令文件 `<name>.md` 与说明 `README.md`。

## Commands 列表

| Command | 说明 | 来源 |
|---------|------|------|
| [ultracode](./ultracode/) | 多智能体编排器，通过多 agent 并行协作完成复杂任务 | 原创 |
| [branchnew](./branchnew/) | Fork 当前 Claude Code session 到 iTerm 新 split pane | Fork from [limin112/branchnew](https://github.com/limin112/branchnew) |

## 安装

拷贝对应文件夹里的 `<name>.md` 到本地 commands 目录即可：

```bash
cp ultracode/ultracode.md ~/.claude/commands/
```

> **clarify 已迁移**：它需要携带脚本与资源（PlantUML 渲染、HTML 生成），而 command 是单个 `.md`、放不下附属文件——`commands/` 下的子目录是**命名空间**（`/cmd:sub`），不是附属文件目录。所以 clarify 已升级为 skill，移到 [zeleSkills](https://github.com/zelehuangdog-source/zeleSkills) 仓库。
>
> 其余 Skills 同样见 [zeleSkills](https://github.com/zelehuangdog-source/zeleSkills)。
