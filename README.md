# Chinese Grill Me

一个为中文使用者设计的 Codex Skill，通过持续、校准强度的结构化访谈，压力测试并完善编程产品构思、功能方案、技术决策与开发提示词。

当前版本：`v1.0.0`  
Skill 调用名：`$grill-me-chinese`

> 中文优先版本。当前只承诺支持 ChatGPT 桌面端中的 Codex、Codex CLI 和 Codex IDE 扩展。

## 安装

### 使用 Skill Installer

在 Codex 中输入：

```text
$skill-installer 请从 https://github.com/mamadoesnotloveu/grill-me-chinese 安装仓库根目录的 Skill，并命名为 grill-me-chinese。
```

安装完成后，在下一轮对话中调用：

```text
$grill-me-chinese 帮我压力测试这个编程产品构思：……
```

### 手动安装

将整个仓库下载或克隆到个人 Skill 目录，并确保最终结构为：

```text
~/.agents/skills/grill-me-chinese/
├── SKILL.md
├── agents/
└── references/
```

如果你的 Codex 环境使用 `~/.codex/skills` 作为个人 Skill 目录，也可以安装到：

```text
~/.codex/skills/grill-me-chinese/
```

安装后如果没有立即出现，请重新启动 Codex。

## 为什么选择 Chinese Grill Me？

### 中文原生，而非英文提示词的直接翻译

有别于以英文逻辑为基础再进行翻译的同类方案，Chinese Grill Me 原生使用中文组织提问、建议和分析，输出自然、准确的简体中文，并持续维护关键中英文术语的一致性。这能减少生硬翻译、词不达意和术语漂移，让中文使用者更准确地讨论产品与技术决策。

### 每个问题都提供可反驳的思考起点

Chinese Grill Me 采用“问题＋建议答案＋为什么重要”的固定结构，不会只把问题抛给使用者。建议答案会明确关键假设，并在存在多个合理方向时给出选项和推荐理由，帮助使用者更快理解权衡、修正观点并形成自己的决定。

### 可根据使用者和讨论阶段调整访谈方式

与固定语气、固定难度的提问清单不同，Chinese Grill Me 支持调节知识水平、压力强度和讨论重点。你可以要求它面向入门者补充背景，也可以切换到专家级、高压审查，或聚焦产品与技术中的某一侧，从而获得适合当前能力和目标的挑战。

### Skill 本身免费且开放

Chinese Grill Me 采用 MIT 许可证。个人使用者可以免费下载、使用和修改，无需支付本 Skill 的授权费用；开发者和组织也可以按照许可证要求复制、修改、再发布或用于商业项目。

> Chinese Grill Me 本身免费，但运行它所使用的 Codex、模型、网络服务或其他第三方平台可能有各自的订阅、用量和费用规则。

## 常用指令

| 指令 | 作用 |
|---|---|
| `继续烤` | 沿当前最关键的未决问题继续；不表示接受上一条建议答案。 |
| `深入这个问题` | 暂不切换主题，继续深挖当前问题及其关键分支。 |
| `阶段总结` | 分别整理用户已确认、助手建议、模型推断、待确认项及其他状态。 |
| `还有多远` | 根据已完成维度和剩余关键分支报告进展，不编造完成百分比。 |
| `换个方向` | 比较新旧方向，识别仍然有效、已经失效和需要重新审查的决定。 |
| `温和一点` / `更严格` | 调整后续访谈的压力强度，同时保留已有结论。 |
| `聚焦产品` / `聚焦技术` | 将后续问题集中在产品决策或技术方案。 |
| `暂停` | 生成可供新对话恢复的状态摘要，然后停止访谈。 |
| `出炉` | 校对决策状态，并生成最终产品方案、风险与下一步。 |
| `只生成开发提示词` | 根据已确认结论生成 Codex 开发提示词，不开始实施。 |

## 重要行为边界

- 助手给出的建议答案默认只是“助手建议、未确认”。
- `继续烤`、`下一题`或沉默不代表使用者接受建议。
- 只有使用者明确确认的内容才能进入硬需求。
- Skill 默认只进行对话和分析，不会自行联网、读写文件或开始开发。

## 维护范围

本项目采用有限维护模式。欢迎通过 GitHub Issues 报告缺陷，但不承诺响应时间、持续功能开发或永久兼容所有 Codex 版本。

## License

MIT License。详见 [LICENSE](LICENSE)。

---

## English

Chinese Grill Me is a Chinese-native Codex Skill for pressure-testing and refining programming product ideas, feature proposals, technical decisions, and development prompts through an adaptive, structured interview.

Version: `v1.0.0`  
Invocation: `$grill-me-chinese`

> This is a Chinese-first release. Compatibility is currently promised only for Codex in the ChatGPT desktop app, Codex CLI, and the Codex IDE extension.

### Install with Skill Installer

Enter the following in Codex:

```text
$skill-installer Install the Skill at the root of https://github.com/mamadoesnotloveu/grill-me-chinese and name it grill-me-chinese.
```

Then invoke it in a new turn:

```text
$grill-me-chinese Pressure-test this programming product idea in Chinese: ...
```

### Why Chinese Grill Me?

#### Chinese-native reasoning instead of translated English prompts

Unlike similar approaches built around English-language reasoning and then translated into Chinese, Chinese Grill Me is designed natively for Chinese conversations. It produces natural and precise Simplified Chinese while maintaining consistent mappings between important Chinese and English terms. This reduces awkward phrasing, mistranslation, and terminology drift.

#### Every question comes with a concrete starting point

Chinese Grill Me follows a consistent “Question + Suggested Answer + Why It Matters” structure instead of leaving users with an open-ended question alone. Suggested answers identify their assumptions and provide meaningful options when several directions are viable, helping users understand trade-offs and reach their own decisions more efficiently.

#### An interview style that adapts to the user and the situation

Unlike a fixed questionnaire, Chinese Grill Me can adjust its knowledge level, pressure intensity, and area of focus. It can explain essential background for beginners, switch to expert-level or high-pressure scrutiny, and focus on either product or technical decisions.

#### Free and openly licensed

Chinese Grill Me is released under the MIT License. Individuals may download, use, and modify the Skill without paying a licensing fee. Developers and organizations may also copy, modify, redistribute, and use it commercially, subject to the license terms.

> The Skill itself is free. Codex, AI models, network services, or other third-party platforms used to run it may have separate subscription, usage, or pricing requirements.

### Common commands

The commands remain in Chinese because this is a Chinese-first Skill:

| Command | What it does |
|---|---|
| `继续烤` | Continues with the most important unresolved question. It does not accept the previous suggestion. |
| `深入这个问题` | Keeps exploring the current issue and its critical branches. |
| `阶段总结` | Separately summarizes confirmed decisions, suggestions, inferences, and unresolved items. |
| `还有多远` | Reports progress without inventing a completion percentage. |
| `换个方向` | Compares the old and new directions and identifies decisions that require review. |
| `温和一点` / `更严格` | Adjusts the pressure level without discarding existing conclusions. |
| `聚焦产品` / `聚焦技术` | Focuses subsequent questions on product or technical decisions. |
| `暂停` | Produces a resumable state summary and stops the interview. |
| `出炉` | Audits decision state and produces the final plan, risks, and next actions. |
| `只生成开发提示词` | Generates a Codex-ready development prompt without starting implementation. |

### Maintenance

This project follows a limited-maintenance model. Bug reports are welcome through GitHub Issues, but no response time, ongoing feature development, or permanent compatibility with every Codex version is guaranteed.

### License

MIT License. See [LICENSE](LICENSE).
