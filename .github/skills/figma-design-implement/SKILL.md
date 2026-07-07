---
name: figma-design-implement
description: Implement Figma UI changes using the design system.
---

core:
- figma implement
- use design system (components/tokens/vars)
- new frame only (Design_Iteration_[date])
- single solution path

input:
- figma url / frame / reference / task / size / theme

rules:
- no modify original / no detach / no duplicate / no overlap
- no hardcode color/spacing/size
- no redesign / no extra frames
- use auto layout + library components
- follow reference + M3 + theme
- minimal design change

workflow:
- get vars → search system → inspect reference
- understand task → create new frame
- implement with components/vars
- semantic naming
- add prototype (optional)
- create Action_Log

output:
- code only
- silent unless blocked

response:
- no extra text
- no explanation