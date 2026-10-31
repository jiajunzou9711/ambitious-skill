# ambitious

把一个任务按「高度 / 深度 / 广度」升级成更有野心的版本：先出一张升级卡和改写后的 prompt，你确认后 agent 再执行，交付时附外部验收结果。

方法来自 Felix Rieseberg（Anthropic）的博客 [*How to be more ambitious: A tutorial for humans with models*](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/)（2026-10-13）。

*An agent skill that upgrades a task along Altitude / Depth / Range before executing it. Based on Felix Rieseberg's post above.*

## 用法

**Claude Code**：安装后在对话里输入 `/ambitious <你的任务>`。

```bash
mkdir -p ~/.claude/skills/ambitious && curl -fsSL https://raw.githubusercontent.com/jiajunzou9711/ambitious-skill/main/SKILL.md -o ~/.claude/skills/ambitious/SKILL.md
```

**Codex**：

```bash
mkdir -p ~/.codex/skills/ambitious && curl -fsSL https://raw.githubusercontent.com/jiajunzou9711/ambitious-skill/main/SKILL.md -o ~/.codex/skills/ambitious/SKILL.md
```

**其他能联网的 agent**：直接把下面这句粘贴进对话，后面接上你的任务。

```text
请先读取 https://raw.githubusercontent.com/jiajunzou9711/ambitious-skill/main/SKILL.md ，按其中的流程处理我接下来的任务：先出升级卡，等我确认再执行。我的任务是：
```

不能联网的 agent：打开 [SKILL.md](SKILL.md)，复制全文粘贴进对话即可。

## 它做什么

| 方向 | 卡片里写什么 |
|---|---|
| 高度 | 目标之后的目标：推进会上要做的决策，或把反复出现的任务改成持续流程 |
| 深度 | 专家会多做什么、最原始的材料、具体方法与工具（标可用性）、外部验收、要检验的假设 |
| 广度 | 把任务改写成动词，引入你想不到的领域和反方角色 |
| 目标 | 可测指标的「现状 → 目标」，与外部验收绑定 |

原则：更深，不更大；先出卡，后执行；不适用的方向直接写「不适用」。
