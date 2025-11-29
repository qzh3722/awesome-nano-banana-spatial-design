# Sketch to Photorealistic Render / 手绘草图转照片级渲染

## 效果预览 / Preview

> Transform loose architectural sketches into photorealistic visualizations while preserving design intent.
>
> 将松散的建筑草图转换为照片级可视化效果，同时保留设计意图。

![Sketch to Render Example](../../assets/images/CONCEPT-001-output-placeholder.jpg)
*Hand sketch → Photorealistic render of modern cultural center / 手绘草图 → 现代文化中心照片级渲染*

---

## 提示词 / Prompt

### 中文版

```
将这幅松散的手绘草图解读为现代文化中心建筑。

设计规格:
- 建筑风格: {风格描述} (例如: "现代主义"、"解构主义")
- 主要材质: {材质列表} (例如: "木模纹混凝土、无框玻璃")
- 场地环境: {环境描述} (例如: "雾蒙蒙的森林边缘")

技术要求:
- 保持草图中的精确比例和体量关系
- 补充合理的材质纹理和细节
- 添加真实的光照和阴影
- 场景氛围: {氛围描述} (例如: "柔和的漫射光线")
- 视角: 照片级建筑摄影风格

最终图像应展示专业的建筑效果图质量，同时忠实于原始草图的设计意图。
```

### English Version

```
Interpret this loose hand sketch as a modern cultural center building.

Design Specifications:
- Architectural Style: {STYLE_DESCRIPTION} (e.g., "modernist", "deconstructivist")
- Primary Materials: {MATERIAL_LIST} (e.g., "board-marked concrete, frameless glass")
- Site Context: {CONTEXT_DESCRIPTION} (e.g., "misty forest edge")

Technical Requirements:
- Preserve exact proportions and massing from sketch
- Add realistic material textures and details
- Include realistic lighting and shadows
- Atmosphere: {ATMOSPHERE_DESCRIPTION} (e.g., "soft diffused light")
- Perspective: Photorealistic architectural photography style

The final image should demonstrate professional rendering quality while remaining faithful to the original sketch's design intent.
```

---

## Tips / 使用技巧

### 中文

- **保持几何约束**: 使用Structure Reference功能(强度0.4-0.6)给予AI足够创作空间，同时保持核心造型
- **材质具体化**: 不要说"混凝土"，而要说"木模板纹理的清水混凝土"以获得更真实的效果
- **氛围描述**: 添加"黄金时刻逆光"或"阴天柔光"等描述可大幅提升渲染质量
- **迭代优化**: 第一次生成后，使用Inpainting修正细节(如窗框、入口)

### English

- **Maintain Geometric Constraints**: Use Structure Reference (strength 0.4-0.6) to give AI creative freedom while preserving core forms
- **Material Specificity**: Instead of "concrete," specify "board-formed exposed concrete" for better results
- **Atmosphere Description**: Adding "golden hour backlight" or "overcast soft light" significantly improves render quality
- **Iterative Refinement**: After first generation, use Inpainting to refine details (window frames, entrances)

---

## 标签 / Tags

`#概念构思` `#草图转渲染` `#建筑可视化` `#设计推敲` `#方案生成`

`#concept-ideation` `#sketch-to-render` `#architectural-visualization` `#design-development` `#schematic-design`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
