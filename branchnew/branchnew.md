---
description: Fork the current agent session (Claude Code / Grok) into a new split pane to the right
argument-hint: [name]
allowed-tools: Bash(branchnew *)
---
!`branchnew $ARGUMENTS`

上面那行在 Claude Code 里会被执行、并替换成命令输出；Grok 不执行这种内联 bash，会把命令原样留在这里。所以按你实际看到的内容分流：

- 看到的是执行结果（或一段输出）→ 说明已经跑过了，直接用**一行话**告诉用户 fork 已打开。
- 看到的仍是「!\`branchnew …\`」这种字面命令 → 用你的 shell 工具执行反引号里的那条命令（`$ARGUMENTS` 此刻已被替换成实际参数），再用**一行话**告诉用户 fork 已打开。

除上面这一步和最后那一行告知，不要做任何别的事。
