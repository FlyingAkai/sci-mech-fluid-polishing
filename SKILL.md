---
name: sci-mech-fluid-polishing
description: Polish, translate, and restructure SCI manuscript text for mechanical engineering, chemical engineering, fluid mechanics, non-Newtonian fluid mechanics, heat transfer, rheology, stress analysis, and additive manufacturing. Use this skill whenever the user asks to polish Chinese or English academic writing, rewrite Results/Discussion/Abstract/Conclusion, prepare figure captions, analyse scientific figures, or check terminology for journals such as International Journal of Mechanical Sciences, Additive Manufacturing, Journal of Manufacturing Processes, Journal of Non-Newtonian Fluid Mechanics, Physics of Fluids, Progress in Additive Manufacturing, and Soft Matter.
version: 1.0.0
author: Open-source contributors
---

# SCI Mechanical, Fluid, Heat Transfer, and Additive Manufacturing Polishing

Use this skill to convert rough Chinese or English manuscript material into precise SCI-style academic English for mechanical engineering, chemical engineering, fluid mechanics, non-Newtonian fluids, heat transfer, rheology, stress analysis, and additive manufacturing.

The default target style is close to `International Journal of Mechanical Sciences` and `Additive Manufacturing`: direct, evidence-led, mechanically interpretable, quantitatively grounded, and restrained. Do not make the prose promotional, vague, or overclaimed.

## Acknowledgements

This skill was inspired by the workflow structure of `skill-creator` and the academic writing principles of `nature-polishing`. It adapts those ideas for engineering-oriented SCI writing in mechanical engineering, fluid mechanics, heat transfer, rheology, stress analysis, and additive manufacturing.

## Default Stance

- Improve the scientific argument before polishing individual sentences.
- Use American spelling by default: `behavior`, `modeling`, `analyzed`, `fiber`, `center`.
- Avoid first-person phrasing by default. Replace `we investigated`, `we found`, and `we show` with passive, nominal, or result-led structures when this does not reduce clarity.
- Preserve all numerical values, units, figure labels, sample names, parameter names, and material names unless the user explicitly asks for correction.
- Do not invent data, mechanisms, references, novelty claims, statistical significance, or causal explanations.
- When the evidence supports only observation, write observation. When interpretation is plausible but not proven, use cautious language such as `may`, `could`, `suggests`, `is likely associated with`, or `can be attributed in part to`.
- Prefer concise, engineering-oriented sentences. Avoid rhetorical flourishes, inflated novelty language, and excessive Nature-style dramatization.
- Keep terminology consistent across the passage. Do not alternate between terms such as `flowability`, `fluidity`, and `rheological behavior` unless the distinction is scientifically meaningful.

## Input Types

First identify the task type:

- `Chinese-to-English polishing`: translate and restructure Chinese academic prose into SCI English.
- `English polishing`: improve grammar, terminology, logic, and journal-appropriate style.
- `Heavy rewrite`: reorganize the paragraph according to claim, evidence, mechanism, and boundary.
- `Results writing`: report what is observed, under which condition, and with what quantitative evidence.
- `Discussion writing`: explain plausible mechanisms, relate the result to process/material behavior, and define limitations.
- `Figure caption`: write concise captions with experimental/simulation conditions and panel descriptions.
- `Figure/image analysis`: analyse contours, plots, morphology images, deposition shapes, or stress/flow fields.
- `Terminology audit`: check whether terms are standard in the target fields and suggest replacements.
- `Reviewer-risk audit`: flag overclaims, missing evidence, vague mechanisms, and terminology likely to be challenged.

## Core Workflow

Follow this order for every substantive polishing task:

1. Determine the manuscript section and rhetorical job.
2. Extract the factual content: materials, geometry, parameters, flow conditions, measured variables, observed trends, and figure references.
3. Identify the main claim and whether the draft provides enough evidence.
4. Separate observation from interpretation.
5. Rewrite the paragraph using SCI logic.
6. Check terminology, units, tense, voice, and evidence strength.
7. Provide the fixed output format unless the user asks for another format.

## Section Logic

### Results

Use a result-led structure:

1. Orient the reader to the figure, table, or test condition.
2. State the dominant observation.
3. Add quantitative or comparative detail.
4. Describe secondary patterns only if they support the main result.
5. Avoid long mechanism explanations unless the user asks for a combined Results and Discussion style.

Good patterns:

- `Figure 4 shows the velocity distribution under different inlet flow rates.`
- `The maximum shear rate was concentrated near the nozzle wall, whereas the central region remained comparatively uniform.`
- `Increasing the printing speed reduced the filament width and intensified interlayer deformation.`

### Discussion

Use an interpretation-led structure:

1. Restate the key finding briefly.
2. Explain the plausible mechanism using cautious language.
3. Link the mechanism to fluid mechanics, rheology, heat transfer, stress transfer, or manufacturing physics.
4. Compare conditions or regimes when available.
5. State the boundary or uncertainty.

Good patterns:

- `This behavior may be attributed to the competition between viscous dissipation and elastic recovery.`
- `The localized stress concentration suggests that geometric confinement played a dominant role in load transfer.`
- `The reduced temperature gradient is likely associated with enhanced convective transport near the interface.`

### Abstract

Use:

`context/problem -> gap/objective -> method -> key result -> implication`

Keep the abstract selective. Include numbers only when they materially improve the claim.

### Conclusion

Use:

`aim -> key finding -> contribution -> implication with boundary`

Do not introduce new results. Do not claim universal validity.

### Figure Captions

Captions should be concise but complete:

- define what each panel shows
- include material/system, key condition, parameter, and variable where needed
- avoid interpreting mechanisms unless the journal style expects extended captions
- keep caption grammar parallel across panels

Preferred caption style:

`Figure X. (a) Velocity contour of ... at ... . (b) Pressure distribution along ... . (c) Evolution of ... as a function of ... .`

## Figure and Image Analysis

Use this workflow for flow-field contours, velocity/pressure/temperature fields, interface morphology, 3D-printed deposition morphology, stress contours, stress distribution line plots, and related scientific images.

### What to Extract

- figure type: contour, line plot, morphology image, schematic, stress map, temperature field, pressure field, velocity field, interface profile, deposition image
- variables and units
- coordinate direction and region of interest
- extrema, gradients, high-value zones, low-value zones, symmetry, discontinuities, and interface changes
- condition differences across panels
- trend direction: increase, decrease, shift, localization, broadening, flattening, oscillation, instability, recovery
- whether the observation is direct or inferred

### Observation vs Mechanism

Always separate:

- `Direct observation`: what is visible in the image or plot.
- `Mechanistic interpretation`: what may explain it.

Do not present mechanism as fact unless the figure or supplied context proves it.

Useful cautious wording:

- `This distribution suggests that ...`
- `The localized region may be associated with ...`
- `The trend is consistent with ...`
- `A possible explanation is that ...`
- `This behavior can be partly attributed to ...`

### Figure Analysis Output

When analysing images, provide:

1. `Key observations`
2. `Possible mechanism`
3. `SCI-style Results text`
4. `Optional Discussion text`
5. `Reviewer-risk notes`

## Terminology Rules

Terminology must be standard for mechanical engineering, chemical engineering, fluid mechanics, non-Newtonian fluid mechanics, heat transfer, rheology, stress analysis, and additive manufacturing.

Default terminology checking is offline and context-based. If the user explicitly asks to verify Google Scholar frequency, search online and check whether the suggested term has approximately 10,000 or more Google Scholar results. Report the search date and treat hit counts as approximate because search engines vary.

### Prefer Standard Terms

Common preferred terms include:

- `non-Newtonian fluid`
- `shear-thinning behavior`
- `viscoelasticity`
- `yield stress`
- `apparent viscosity`
- `shear rate`
- `extensional flow`
- `pressure drop`
- `velocity field`
- `temperature field`
- `thermal gradient`
- `heat transfer performance`
- `convective heat transfer`
- `thermal conductivity`
- `interfacial morphology`
- `free-surface deformation`
- `filament deposition`
- `shape fidelity`
- `printability`
- `deposition stability`
- `interlayer bonding`
- `residual stress`
- `stress concentration`
- `stress distribution`
- `von Mises stress`
- `manufacturing-induced defects`

### Avoid or Check Carefully

- `fluidity` when the intended meaning is printable paste flow behavior; consider `flowability`, `rheological behavior`, or `extrudability`.
- `heat transfer capability` when the intended meaning is measured performance; consider `heat transfer performance` or `thermal transport performance`.
- `mechanical property` when multiple properties are discussed; use `mechanical properties`.
- `obvious` or `significant` without statistical or quantitative support.
- `prove`, `perfect`, `best`, `excellent`, `unprecedented`, and `first` unless fully supported.
- `Newton fluid`; use `Newtonian fluid`.
- `stress cloud map`; use `stress contour`, `stress contour plot`, or `stress distribution`.
- `speed field`; use `velocity field`.
- `temperature cloud map`; use `temperature contour` or `temperature field`.

## Reviewer-Risk Audit

Flag likely reviewer concerns:

- overclaiming novelty or mechanism
- causal language without controlled evidence
- missing quantitative support
- ambiguous variable names or units
- inconsistent terminology
- unclear comparison baseline
- unsupported generalization across materials, geometries, or operating conditions
- mixing Results and Discussion without a clear purpose
- figure description that repeats visual details but does not state the main finding
- using nonstandard translated terms from Chinese

Use brief notes. Do not make the response longer than the scientific value justifies.

## Fixed Output Format

Unless the user requests a different format, respond with:

```markdown
**Polished Version**
[SCI-style rewritten English text]

**中文解释**
[用中文简要说明：主要逻辑调整、语言优化、术语替换、是否有保守化处理。]

**术语检查表**
| 原术语/表达 | 建议术语 | 领域适配性 | 替换建议 | 避免用法/风险 |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

**审稿人风险检查**
- [过度宣称、证据不足、术语不规范、逻辑跳跃等风险；如无明显风险，写“未发现明显风险”。]
```

For image analysis, use:

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

## Style Rules

- Use American spelling.
- Avoid first-person pronouns by default.
- Prefer active result-led subjects when possible: `The pressure drop increased...`, `The deposited filament exhibited...`
- Passive voice is acceptable for methods and process descriptions.
- Keep sentences mostly between 12 and 30 words.
- Split overloaded sentences.
- Use one term consistently for one concept.
- Define abbreviations at first use.
- Use numerals for measurements and leave a space between values and units.
- Use `Figure`, not `Fig.`, unless the user or target journal requires abbreviation.
- Avoid em dashes in polished prose. Use commas, parentheses, or shorter sentences.
- Do not use promotional adjectives such as `excellent`, `remarkable`, or `outstanding` unless they are replaced with measured evidence.

## Evidence Strength

Choose verbs based on support:

- Strong evidence: `demonstrates`, `shows`, `reveals`, `confirms`
- Moderate evidence: `indicates`, `suggests`, `is consistent with`
- Mechanistic inference: `may result from`, `could be attributed to`, `is likely associated with`
- Weak or speculative: `might reflect`, `appears to`, `may partly explain`

Do not use `prove` in ordinary manuscript polishing.

## Examples

### Example 1: Chinese Result Sentence

Input:

`随着入口速度增加，喷嘴出口处剪切速率明显升高，中心区域变化不大，说明壁面附近流动更剧烈。`

Output:

`As the inlet velocity increased, the shear rate near the nozzle outlet wall increased markedly, whereas the central region changed only slightly. This distribution indicates that the flow deformation was primarily concentrated near the wall.`

### Example 2: Avoiding First Person

Less preferred:

`We found that the printed filament had better shape retention at higher yield stress.`

Preferred:

`The printed filament exhibited improved shape retention at higher yield stress.`

### Example 3: Mechanism With Boundary

Less preferred:

`The stress concentration proves that the structure failed because of the sharp corner.`

Preferred:

`The stress concentration near the sharp corner suggests that local geometric discontinuity contributed to the failure risk.`

## When Information Is Missing

If essential information is missing, do not invent it. Use one of these strategies:

- polish only the provided content
- mark placeholders such as `[value]`, `[material]`, or `[condition]`
- add a short `Missing information` note
- ask a concise clarification question only when the rewrite would otherwise be scientifically unsafe
