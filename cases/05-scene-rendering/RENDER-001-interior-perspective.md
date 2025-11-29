# Interior Perspective Rendering / 室内空间透视渲染

## 效果预览 / Preview

> Create cinematic interior renderings with dramatic lighting and photorealistic materials for client presentations.
>
> 创建具有戏剧性照明和照片级材质的电影感室内渲染图，用于客户展示。

![Interior Rendering Example](../../assets/images/RENDER-001-output-placeholder.jpg)
*Luxury hotel lobby with dramatic afternoon sunlight / 奢华酒店大堂，午后戏剧性阳光*

---

## 提示词 / Prompt

### 中文版

```
为以下室内空间创建照片级透视渲染图:

空间设定:
- 空间类型: {空间类型} (例如: "精品酒店大堂"、"高级住宅客厅")
- 尺寸: {尺寸} (例如: "双层挑高，6米层高")
- 风格: {室内风格} (例如: "现代奢华"、"Wabi-Sabi侘寂")

材质方案:
- 地面: {地面材质} (例如: "抛光大理石，浅灰色带金色纹路")
- 墙面: {墙面材质} (例如: "深色胡桃木饰面板")
- 家具: {家具材质} (例如: "天鹅绒深绿色沙发、黄铜边几")
- 装饰: {装饰元素} (例如: "艺术吊灯、大型绿植、艺术画")

光照设置(关键):
- 时间: {时间} (例如: "下午4点")
- 光照类型: {光照} (例如: "侧光从大窗户射入")
- 氛围: {氛围} (例如: "戏剧性、忧郁、体积光束")
- 色温: {色温} (例如: "温暖的3000K室内灯+冷色系自然光对比")

构图设置:
- 视角: {视角} (例如: "人视角、略微仰视")
- 焦距: {焦距} (例如: "24mm广角镜头")
- 景深: {景深} (例如: "浅景深f/2.8，前景模糊")
- 取景: {取景} (例如: "对角线构图，强调空间深度")

技术要求:
- 照片级真实材质纹理
- 真实的光线追踪阴影和反射
- 细腻的光影过渡
- 4K分辨率输出
- 电影级色彩分级

最终图像应达到顶级建筑摄影和室内摄影杂志的发表水准。
```

### English Version

```
Create a photorealistic perspective rendering for the following interior space:

Space Settings:
- Space Type: {SPACE_TYPE} (e.g., "boutique hotel lobby", "high-end residential living room")
- Dimensions: {DIMENSIONS} (e.g., "double-height volume, 6m ceiling")
- Style: {INTERIOR_STYLE} (e.g., "modern luxury", "Wabi-Sabi")

Material Scheme:
- Flooring: {FLOORING_MATERIAL} (e.g., "polished marble, light grey with gold veining")
- Walls: {WALL_MATERIAL} (e.g., "dark walnut wood veneer panels")
- Furniture: {FURNITURE_MATERIAL} (e.g., "velvet deep green sofa, brass side tables")
- Decoration: {DECORATIVE_ELEMENTS} (e.g., "artistic chandelier, large plants, artwork")

Lighting Setup (Critical):
- Time: {TIME} (e.g., "4 PM afternoon")
- Lighting Type: {LIGHTING} (e.g., "side lighting streaming through large windows")
- Atmosphere: {ATMOSPHERE} (e.g., "dramatic, moody, volumetric light beams")
- Color Temperature: {COLOR_TEMP} (e.g., "warm 3000K interior lights + cool natural light contrast")

Composition Settings:
- Viewpoint: {VIEWPOINT} (e.g., "eye level, slightly looking up")
- Focal Length: {FOCAL_LENGTH} (e.g., "24mm wide-angle lens")
- Depth of Field: {DOF} (e.g., "shallow depth f/2.8, foreground blur")
- Framing: {FRAMING} (e.g., "diagonal composition emphasizing spatial depth")

Technical Requirements:
- Photorealistic material textures
- Realistic raytraced shadows and reflections
- Subtle light and shadow transitions
- 4K resolution output
- Cinematic color grading

The final image should meet publication standards of top architectural and interior photography magazines.
```

---

## Tips / 使用技巧

### 中文

- **光照是灵魂**: "戏剧性午后阳光束"比"明亮光线"产生的效果差异巨大，具体描述光照
- **体积光**: 添加"体积雾效果"或"光束中的灰尘粒子"可增强戏剧性
- **色温对比**: "暖光室内+冷光自然光"的对比可营造高级感
- **景深技巧**: 使用f/1.8-2.8浅景深模糊前景物体(如花瓶)，突出主体空间
- **分步骤**: 先生成基础渲染→调整光照→Inpainting添加装饰品

### English

- **Lighting is Soul**: "Dramatic afternoon sunbeams" produces vastly different results than "bright light" - describe lighting specifically
- **Volumetric Lighting**: Adding "volumetric fog effect" or "dust particles in light beams" enhances drama
- **Color Temperature Contrast**: "Warm interior + cool natural light" contrast creates premium feel
- **Depth of Field Trick**: Use f/1.8-2.8 shallow DoF to blur foreground objects (vases) and emphasize main space
- **Phased Approach**: Generate base render → adjust lighting → add decorations via Inpainting

---

## 标签 / Tags

`#场景渲染` `#室内效果图` `#照片级渲染` `#建筑摄影` `#电影级光照`

`#scene-rendering` `#interior-rendering` `#photorealistic-render` `#architectural-photography` `#cinematic-lighting`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
