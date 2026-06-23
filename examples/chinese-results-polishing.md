# Example: Chinese Results Polishing

## Prompt

```text
请用 sci-mech-fluid-polishing 润色下面这段 Results，偏 Additive Manufacturing 风格。要求不保留第一人称，给出润色版、中文解释、术语检查表和审稿人风险检查。

随着入口速度增加，喷嘴出口处剪切速率明显升高，中心区域变化不大，说明壁面附近流动更剧烈。同时，沉积丝材的宽度逐渐减小，层间变形更加明显。
```

## Expected Behavior

The assistant should:

- rewrite the Chinese content into polished SCI English
- use American spelling
- avoid first-person wording
- separate observation from mechanism
- avoid unsupported claims
- provide a terminology table
- flag whether quantitative evidence is missing

## Example Output Sketch

```markdown
**Polished Version**
As the inlet velocity increased, the shear rate near the nozzle outlet wall increased markedly, whereas the central region changed only slightly. This distribution indicates that flow deformation was primarily concentrated near the wall. The deposited filament width also decreased gradually, accompanied by more pronounced interlayer deformation.

**中文解释**
该版本将原句重组为“速度变化-剪切率分布-沉积形貌变化”的结果逻辑，并避免使用第一人称。最后一句保留为结果描述，没有进一步扩展为未经证明的机理解释。

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| 剪切速率 | shear rate | 高 | 保留该术语 | 避免写成 shearing speed |
| 沉积丝材 | deposited filament | 高 | 用于挤出式打印语境 | 避免与 fiber 混用 |

**审稿人风险检查**
- “明显升高”和“逐渐减小”最好补充定量数值或图号支持。
```
