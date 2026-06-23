# Example: Figure Analysis

## Prompt

```text
Use sci-mech-fluid-polishing to analyse a velocity contour and write Results and Discussion text. The figure shows that the high-velocity region is concentrated near the nozzle centerline, while the velocity decreases near the wall. At higher inlet velocity, the wall-adjacent shear region becomes more pronounced.
```

## Expected Behavior

The assistant should:

- identify direct observations
- propose cautious mechanisms
- write SCI-style Results text
- optionally write Discussion text
- avoid claiming unprovided quantitative values
- flag reviewer risks

## Example Output Sketch

```markdown
**Key Observations**
- The high-velocity region is concentrated near the nozzle centerline.
- The velocity decreases toward the wall.
- The wall-adjacent shear region becomes more pronounced at higher inlet velocity.

**Possible Mechanism**
- The near-wall velocity reduction may reflect the no-slip boundary condition and increased viscous resistance.
- The intensified wall-adjacent shear region is consistent with stronger velocity gradients at higher inlet velocity.

**SCI-style Results Text**
The velocity contour shows a centerline-dominated flow profile, with lower velocities near the nozzle wall. As the inlet velocity increased, the near-wall shear region became more pronounced, indicating a stronger radial velocity gradient under high-flow-rate conditions.

**Optional Discussion Text**
This behavior may be attributed to the combined effect of wall confinement and viscous resistance. The stronger near-wall velocity gradient at higher inlet velocity suggests that deformation was increasingly localized in the wall-adjacent region.

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| velocity contour | velocity contour | 高 | 保留 | 避免 speed cloud map |
| shear region | wall-adjacent shear region | 高 | 明确空间位置 | 避免 vague high-shear wording |

**审稿人风险检查**
- If available, the maximum velocity and shear-rate values should be added to strengthen the result.
```
