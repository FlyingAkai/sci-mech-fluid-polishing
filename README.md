# sci-mech-fluid-polishing

## 中文介绍

`sci-mech-fluid-polishing` 是一个面向机械工程、化学工程、流体力学、非牛顿流体力学、传热学、应力分析与增材制造方向的 SCI 论文写作润色 skill。它用于将中文或英文稿件重写为更符合工程类 SCI 期刊风格的英文表达，并提供术语检查、图注撰写、图像结果分析和审稿人风险检查。

默认风格偏向 `International Journal of Mechanical Sciences` 与 `Additive Manufacturing`：表达直接、证据导向、机理清楚、工程解释充分，同时避免夸大结论或编造数据。

## English Overview

`sci-mech-fluid-polishing` is a Codex skill for SCI manuscript polishing in mechanical engineering, chemical engineering, fluid mechanics, non-Newtonian fluid mechanics, heat transfer, stress analysis, and additive manufacturing.

It supports Chinese-to-English polishing, English academic rewriting, figure-caption preparation, scientific image analysis, terminology auditing, and reviewer-risk checking. The default style is concise, engineering-oriented, evidence-led, and close to the writing conventions of `International Journal of Mechanical Sciences` and `Additive Manufacturing`.

## Features / 功能

- 中文初稿翻译为 SCI 英文并润色
- 英文段落的语法、用词、句式和逻辑优化
- Results、Discussion、Abstract、Conclusion 的重写和强化
- 图注撰写与图像结果分析
- 流场云图、速度场、压力场、温度场、应力云图、应力分布线图分析
- 界面形貌、3D 打印沉积形貌和层间变形分析
- 专业术语规范检查与替换建议
- 审稿人视角的风险检查，包括过度宣称、证据不足、术语不规范和逻辑跳跃

## Target Fields / 目标领域

- Mechanical engineering
- Chemical engineering
- Fluid mechanics
- Non-Newtonian fluid mechanics
- Rheology
- Heat transfer
- Stress analysis
- Additive manufacturing
- Direct ink writing and extrusion-based printing
- Interfacial morphology and free-surface deformation

## Reference Journal Style / 参考期刊风格

This skill is designed for engineering-oriented SCI writing and is especially aligned with the style of:

1. `International Journal of Mechanical Sciences`
2. `Journal of Manufacturing Processes`
3. `Journal of Non-Newtonian Fluid Mechanics`
4. `Progress in Additive Manufacturing`
5. `Physics of Fluids`
6. `Additive Manufacturing`
7. `Soft Matter`

The default priority is `International Journal of Mechanical Sciences` and `Additive Manufacturing`.

## Installation / 安装

Copy this folder into your Codex skills directory.

Windows example:

```text
C:\Users\<YourName>\.agents\skills\sci-mech-fluid-polishing
```

macOS or Linux example:

```text
~/.agents/skills/sci-mech-fluid-polishing
```

The required instruction file is:

```text
sci-mech-fluid-polishing/SKILL.md
```

## Quick Start / 快速使用

Example prompt:

```text
Use sci-mech-fluid-polishing to polish the following Results paragraph for Additive Manufacturing. Avoid first-person wording and check terminology.
```

中文示例：

```text
请用 sci-mech-fluid-polishing 润色下面这段 Results，偏 International Journal of Mechanical Sciences 风格，并给出术语检查表和审稿人风险检查。
```

图像分析示例：

```text
请基于 sci-mech-fluid-polishing 分析这张速度云图，并帮我写 Results 和 Discussion。
```

## Default Writing Rules / 默认写作规则

- Use American spelling, such as `behavior`, `modeling`, and `analyzed`.
- Avoid first-person wording where possible.
- Perform heavy rewriting when needed, but do not invent data, mechanisms, references, or conclusions.
- Separate direct observations from mechanistic interpretations.
- Use cautious wording for inferred mechanisms, such as `may`, `could`, `suggests`, and `is likely associated with`.
- Preserve numerical values, units, figure labels, parameter names, and material names unless correction is explicitly requested.
- Avoid promotional or unsupported wording such as `prove`, `excellent`, `perfect`, `unprecedented`, and `best`.

## Default Output Format / 默认输出格式

For polishing tasks:

```markdown
**Polished Version**
[SCI-style rewritten English text]

**中文解释**
[说明主要逻辑调整、语言优化、术语替换和保守化处理。]

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

**审稿人风险检查**
- [过度宣称、证据不足、术语不规范、逻辑跳跃等风险。]
```

For image-analysis tasks:

```markdown
**Key Observations**
- ...

**Possible Mechanism**
- ...

**SCI-style Results Text**
...

**Optional Discussion Text**
...

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

**审稿人风险检查**
- ...
```

## Terminology Checking / 术语检查

The skill performs offline, context-based terminology checking by default. It checks whether terms are suitable for mechanical engineering, fluid mechanics, non-Newtonian fluids, heat transfer, stress analysis, rheology, and additive manufacturing.

If the user explicitly asks for Google Scholar verification, the assistant should search online and report whether the suggested term has approximately 10,000 or more Google Scholar results. Search counts should be treated as approximate because they vary by date, region, and search engine behavior.

Common examples:

| Less preferred | Preferred | Reason |
|---|---|---|
| `Newton fluid` | `Newtonian fluid` | Standard fluid-mechanics term |
| `speed field` | `velocity field` | More standard in flow analysis |
| `stress cloud map` | `stress contour` / `stress distribution` | More standard in mechanics papers |
| `temperature cloud map` | `temperature contour` / `temperature field` | More standard in heat-transfer papers |
| `fluidity` | `flowability` / `rheological behavior` / `extrudability` | Depends on paste, rheology, or extrusion context |

## Examples / 示例

See the `examples/` directory:

- `examples/chinese-results-polishing.md`
- `examples/figure-analysis-example.md`
- `examples/terminology-audit-example.md`

## Evaluation Prompts / 测试提示词

See:

```text
evals/evals.json
```

These prompts are intended for qualitative testing of whether the skill triggers correctly and produces the expected sections.

## Acknowledgements / 致谢

This skill was inspired by the workflow structure of `skill-creator` and the academic writing principles of `nature-polishing`, then adapted for engineering-oriented SCI writing in mechanical engineering, fluid mechanics, heat transfer, rheology, stress analysis, and additive manufacturing.

## Limitations / 限制

- The skill must not fabricate data, citations, mechanisms, or novelty claims.
- Image-based mechanisms should be presented as interpretations unless directly supported by the supplied data.
- Google Scholar result counts are approximate and should not be treated as exact bibliometric evidence.
- The skill can improve writing and logic, but it cannot replace domain expert validation.

## License / 许可证

This project is released under the MIT License. See `LICENSE` for details.
