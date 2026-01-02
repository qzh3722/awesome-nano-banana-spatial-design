# Case 5.1: Clay/White Model to Photorealistic Render / 白模转照片级渲染 `[Original]`

> **Scene Rendering.**
>
> Transform clay/white 3D model renders into photorealistic visualizations with intelligent material assignment and style control.
>
> **场景渲染。**
>
> 将白模/灰模3D渲染图智能转换为照片级可视化效果，支持材质自动分配和风格控制。

#### Input: Clay/White Model Render

![Input Image](../../assets/cases/5.1-clay-to-render/input.jpg)

---

## Style Variation Examples / 风格变体示例

#### Output 1: Cream Luxury Style (奶油色轻奢风)

![Output Cream](../../assets/cases/5.1-clay-to-render/output-cream.jpg)

#### Output 2: Dark Wood Japanese Style (深色木质日式风)

![Output Dark](../../assets/cases/5.1-clay-to-render/output-dark.png)

---

## 📝 Prompt / 提示词

### Option A: Text-Specified Style (单图+文字指定风格)

**English:**
```markdown
Transform this clay/white model render into a photorealistic architectural visualization with the following STRICT analysis rules:

1. GEOMETRY PRESERVATION: Analyze and preserve the EXACT 3D geometry, perspective, lighting direction, and spatial proportions from the input model. Do NOT modify any architectural elements, furniture shapes, or spatial relationships.

2. INTELLIGENT MATERIAL ASSIGNMENT: Based on the visible forms and context, intelligently assign appropriate materials:
   - Wall surfaces → [specify: e.g., white textured paint / exposed concrete / wood paneling]
   - Flooring → [specify: e.g., light oak hardwood / marble tile / polished concrete]
   - Ceiling → [specify: e.g., white matte / wood beams / recessed panels]
   - Furniture → [specify: e.g., natural fabrics / leather / mixed materials]
   - Fixtures → [specify: e.g., brushed brass / matte black / chrome]

3. DESIGN STYLE: [specify style: e.g., Modern Minimalist / Scandinavian / Japanese Wabi-Sabi / Industrial Loft / French Luxury]

4. LIGHTING & ATMOSPHERE: Apply photorealistic lighting that enhances the specified style. Add natural window light, ambient reflections, and subtle shadows for depth.

5. OUTPUT: High-quality photorealistic interior render, maintaining the exact camera angle and composition of the input.
```

**中文:**
```markdown
将此白模/灰模渲染图转换为照片级建筑可视化效果，遵循以下严格分析规则：

1. 几何保真：分析并完全保留输入模型的精确3D几何形状、透视角度、光照方向和空间比例。禁止修改任何建筑元素、家具形状或空间关系。

2. 智能材质分配：根据可见的形体和场景上下文，智能分配适当的材质：
   - 墙面 → [指定：如 白色肌理漆 / 清水混凝土 / 木饰面板]
   - 地面 → [指定：如 浅色橡木地板 / 大理石瓷砖 / 抛光混凝土]
   - 天花 → [指定：如 白色哑光 / 木梁结构 / 内嵌式造型]
   - 家具 → [指定：如 天然面料 / 皮革 / 混合材质]
   - 五金 → [指定：如 拉丝黄铜 / 哑光黑 / 镀铬]

3. 设计风格：[指定风格：如 现代简约 / 北欧 / 日式侘寂 / 工业loft / 法式轻奢]

4. 灯光氛围：应用能增强指定风格的照片级灯光。添加自然窗光、环境反射和柔和阴影以增加深度感。

5. 输出：高质量照片级室内渲染，保持与输入完全相同的相机角度和构图。
```

---

### Option B: Image Reference Style (双图输入，图片参考风格)

**English:**
```markdown
Using the FIRST uploaded image as the style/material reference and the SECOND uploaded image as the clay/white model source:

1. GEOMETRY SOURCE: Extract ALL 3D geometry, spatial layout, furniture placement, camera angle, and perspective EXCLUSIVELY from the clay model (second image). Do NOT modify any shapes or positions.

2. STYLE TRANSFER: Apply the visual style, material palette, color scheme, lighting atmosphere, and design language from the reference image (first image) to the clay model geometry.

3. MATERIAL MAPPING: Intelligently map materials from the style reference to corresponding surfaces in the clay model:
   - Match wall treatments to similar wall surfaces
   - Apply flooring materials to floor areas
   - Transfer furniture textures to equivalent furniture forms
   - Adapt lighting mood and color temperature

4. PHOTOREALISTIC OUTPUT: Generate a final render that combines:
   - The EXACT spatial structure of the clay model
   - The aesthetic quality of the style reference
   - Professional-grade lighting and material rendering

Maintain strict fidelity to the clay model's geometry while achieving the visual atmosphere of the reference.
```

**中文:**
```markdown
使用第一张上传的图片作为风格/材质参考，第二张上传的图片作为白模/灰模源：

1. 几何来源：完全从白模（第二张图）提取所有3D几何形状、空间布局、家具摆放、相机角度和透视关系。禁止修改任何形状或位置。

2. 风格迁移：将参考图片（第一张图）的视觉风格、材质色板、配色方案、灯光氛围和设计语言应用到白模几何体上。

3. 材质映射：将风格参考中的材质智能映射到白模中的对应表面：
   - 将墙面处理匹配到相似的墙面
   - 将地面材质应用到地面区域
   - 将家具纹理转移到对应的家具形体
   - 适配灯光氛围和色温

4. 照片级输出：生成最终渲染图，结合：
   - 白模的精确空间结构
   - 风格参考的美学质量
   - 专业级的灯光和材质渲染

在实现参考图的视觉氛围同时，严格保持对白模几何形状的忠实度。
```

---

## 💡 Tips / 技巧

### Common Style Keywords / 常用风格关键词

| English | 中文 | Description |
|---------|------|-------------|
| `Modern Minimalist` | 现代简约 | Clean lines, neutral palette, uncluttered |
| `Scandinavian` | 北欧 | Warm wood tones, hygge atmosphere, light |
| `Japanese Wabi-Sabi` | 日式侘寂 | Raw textures, muted earth tones, imperfection |
| `Industrial Loft` | 工业风 | Exposed brick, metal, concrete |
| `French Light Luxury` | 法式轻奢 | Cream palette, elegant details, refined |

### Best Practices / 最佳实践

1. **Geometry Fidelity**: The prompt emphasizes preserving exact geometry - this prevents AI from "improving" or modifying your design
2. **Material Placeholders**: Replace `[specify]` with your actual requirements for precise control
3. **Style Iteration**: Use the same clay model with different style specifications for quick design iterations

## 🏷️ Tags
`#scene-rendering` `#clay-model` `#photorealistic` `#material-assignment` `#style-control`
`#场景渲染` `#白模` `#照片级渲染` `#材质分配` `#风格控制`
