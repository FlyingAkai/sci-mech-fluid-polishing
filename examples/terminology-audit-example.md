# Example: Terminology Audit

## Prompt

```text
Use sci-mech-fluid-polishing to check whether these terms are suitable for a manuscript on extrusion-based 3D printing of non-Newtonian fluids:

- Newton fluid
- speed field
- stress cloud map
- fluidity
- heat transfer capability
```

## Expected Behavior

The assistant should:

- identify nonstandard or context-sensitive terms
- suggest field-appropriate replacements
- explain risks in Chinese
- mention that Google Scholar count verification requires explicit web search

## Example Output Sketch

```markdown
**Polished Version**
The following terms should be revised before use in an SCI manuscript on extrusion-based 3D printing of non-Newtonian fluids.

**中文解释**
这些表达中有几项属于中文直译或非标准工程表达，容易被审稿人认为术语不规范。建议改为流体力学、传热学和增材制造领域更常用的术语。

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| Newton fluid | Newtonian fluid | 高 | 使用标准术语 | Newton fluid 不规范 |
| speed field | velocity field | 高 | 用于流场描述 | speed field 不够标准 |
| stress cloud map | stress contour / stress distribution | 高 | 取决于图类型 | cloud map 是中文直译 |
| fluidity | flowability / rheological behavior / extrudability | 需看语境 | 打印浆料常用 flowability 或 extrudability | fluidity 可能过宽泛 |
| heat transfer capability | heat transfer performance / thermal transport performance | 中-高 | 按实验指标选择 | capability 可能过泛 |

**审稿人风险检查**
- 建议根据具体图、实验指标和材料体系选择最终术语。
- 若需要验证术语是否有超过 10,000 条 Google Scholar 结果，需要单独联网检索。
```
