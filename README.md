# X 内容工作室

一个用于中文 X/Twitter 内容创作的 Agent Skill，支持推文、线程、X Articles 和 Article 引流短文。

## 能做什么

- 根据目标读者和写作目的确定选题、角度与结构。
- 调研和核查事实，保留来源、证据缺口与不确定性。
- 起草或修改中文内容，保留用户指定的标题、表达和语气。
- 按任务需要进行独立审稿，设计封面或插图。

这份 Skill 用于明确的 X 内容任务。发布内容需要用户另外授权。

## 安装与使用

把整个仓库放入支持 Agent Skills 的工具的技能目录，文件夹命名为 `x-content-studio`。请保留 `references/` 等子目录，以便读取配套指导。

在 Codex 中，可以将它放到 `~/.codex/skills/x-content-studio`，然后在支持技能调用的对话中使用：

```text
使用 $x-content-studio，把下面的素材写成 3 条中文 X 线程。
受众是刚接触 AI 工作流的产品经理。保留原文的不确定性，
不要把假设示例写成我的亲身经历。
```

也可以指定修改范围：

```text
使用 $x-content-studio，只改顺这条文案，保留标题和我的用词。
不要扩写，只给一个版本。
```

联网调研、图片生成与多智能体协作取决于运行工具提供的能力。配套指导中列出的专门角色由运行环境提供；角色不可用时，可以交给可用智能体或直接完成任务。

## 文件说明

| 文件 | 用途 |
| --- | --- |
| [SKILL.md](SKILL.md) | 技能入口与核心工作规则 |
| [agents/openai.yaml](agents/openai.yaml) | Codex 展示名称与默认提示词 |
| [references/human-voice.md](references/human-voice.md) | 写作语气与保留个人表达 |
| [references/content-decisions.md](references/content-decisions.md) | 内容角度与编辑判断 |
| [references/editorial-modes.md](references/editorial-modes.md) | Article、引流短文及配图指导 |
| [references/agent-workflow.md](references/agent-workflow.md) | 按需委派研究、写作与审稿 |
| [evals/evals.json](evals/evals.json) | 保留语气和证据边界的评测案例 |

## 来源与许可

部分写作指导改编自 [human-writing](https://github.com/KKKKhazix/human-writing)。相关署名与 MIT 许可保留在 [references/human-writing-LICENSE.txt](references/human-writing-LICENSE.txt)，该许可文件标明的是上游改编内容的来源与许可。
