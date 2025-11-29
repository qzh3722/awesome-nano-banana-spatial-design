# Kitchen Cabinet Material Swap / 厨房橱柜材质更换

## 效果预览 / Preview

> Quickly test different material combinations for existing spaces without changing layout or structure.
>
> 在不改变布局或结构的情况下，快速测试现有空间的不同材质组合。

![Material Swap Example](../../assets/images/MAT-001-output-placeholder.jpg)
*Oak cabinets → Matte navy blue cabinets, same layout / 橡木橱柜 → 哑光海军蓝橱柜，相同布局*

---

## 提示词 / Prompt

### 中文版

```
在保持厨房布局完全不变的情况下，更换橱柜材质和颜色。

材质更换规格:
- 橱柜门板: 将 {原材质} 更换为 {新材质}
  例如: "将橡木凸起面板门更换为哑光海军蓝平板门"
- 台面: 将 {原台面} 更换为 {新台面}
  例如: "将层压板台面更换为白色大理石台面"
- 五金件: 将 {原五金} 更换为 {新五金}
  例如: "将镀铬拉手更换为拉丝黄铜拉手"
- 墙面: {墙面变化} (可选)
  例如: "背景墙更换为白色地铁瓷砖"

严格约束条件:
- **保持厨房布局、电器位置和水槽位置完全不变**
- **保持相机角度和光照不变**
- **仅更改指定的材质和颜色**
- **保持空间尺寸和比例**

技术要求:
- 真实的材质纹理(木纹/哑光漆面/大理石纹路)
- 准确的光照反射(哑光vs光泽)
- 五金件的真实金属质感
- 照片级真实感

结果应像专业的材质方案对比图，方便客户选择。
```

### English Version

```
Replace kitchen cabinet materials and colors while keeping the layout completely unchanged.

Material Replacement Specifications:
- Cabinet Doors: Replace {ORIGINAL_MATERIAL} with {NEW_MATERIAL}
  e.g., "Replace raised-panel oak doors with flat-panel matte navy blue doors"
- Countertop: Replace {ORIGINAL_COUNTER} with {NEW_COUNTER}
  e.g., "Replace laminate countertop with white marble countertop"
- Hardware: Replace {ORIGINAL_HARDWARE} with {NEW_HARDWARE}
  e.g., "Replace chrome pulls with brushed brass pulls"
- Backsplash: {BACKSPLASH_CHANGE} (optional)
  e.g., "Change to white subway tile backsplash"

Strict Constraints:
- **Keep kitchen layout, appliance positions, and sink position exactly unchanged**
- **Maintain camera angle and lighting**
- **Only change specified materials and colors**
- **Preserve spatial dimensions and proportions**

Technical Requirements:
- Realistic material textures (wood grain/matte finish/marble veining)
- Accurate lighting reflections (matte vs glossy)
- Realistic metal finish on hardware
- Photorealistic quality

The result should look like a professional material comparison for client selection.
```

---

## Tips / 使用技巧

### 中文

- **结构锁定**: 上传原图作为Structure Reference(强度0.8-1.0)确保布局不变
- **材质对照表**: 明确列出"橱柜门→海军蓝"、"台面→白色大理石"的一一对应关系
- **光泽度控制**: "哑光漆面"vs"高光烤漆"会产生完全不同的视觉效果，需明确指定
- **多方案对比**: 生成3-4种色彩方案(如海军蓝、鼠尾草绿、木色、白色)供客户选择

### English

- **Structure Locking**: Upload original image as Structure Reference (strength 0.8-1.0) to preserve layout
- **Material Mapping Table**: Clearly list one-to-one mappings like "cabinet doors→navy blue", "countertop→white marble"
- **Finish Control**: "Matte finish" vs "high-gloss lacquer" creates completely different visual effects - must specify clearly
- **Multiple Options**: Generate 3-4 color schemes (navy blue, sage green, wood tone, white) for client selection

---

## 标签 / Tags

`#材质软装` `#材质更换` `#厨房设计` `#方案对比` `#客户选择`

`#material-styling` `#material-swap` `#kitchen-design` `#option-comparison` `#client-selection`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
