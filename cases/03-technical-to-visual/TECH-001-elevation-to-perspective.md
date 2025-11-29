# Building Elevation to 3D Perspective / 立面图转三维透视

## 效果预览 / Preview

> Convert flat architectural elevation drawings into realistic 3D perspective views with accurate materials and lighting.
>
> 将平面建筑立面图转换为真实的三维透视视图，包含准确的材质和光照。

![Elevation to 3D Example](../../assets/images/TECH-001-output-placeholder.jpg)
*2D elevation drawing → Photorealistic 3D street view / 二维立面图 → 照片级三维街景*

---

## 提示词 / Prompt

### 中文版

```
基于此二维立面图生成三维透视建筑效果图。

技术转换要求:
- 将平面立面图拉伸为真实的三维透视视图
- 视角: {视角} (例如: "街道人视角/蛙眼仰视")
- 严格保持立面图中的窗洞位置、比例和排列

材质应用:
- 外墙材质: {外墙材质} (例如: "红砖，深灰缝")
- 窗框材质: {窗框} (例如: "深色铝合金框")
- 屋顶材质: {屋顶} (例如: "深灰色沥青瓦")
- 基座材质: {基座} (例如: "花岗岩")

环境设置:
- 天空: {天空} (例如: "晴朗蓝天，少量白云")
- 照明: {照明} (例如: "下午3点侧光，长阴影")
- 周边环境: {环境} (例如: "城市街道，人行道，行人")
- 季节: {季节} (例如: "春季，绿树")

技术要求:
- 为窗洞添加真实的阴影以显示深度
- 材质纹理比例准确(砖块尺寸标准)
- 照片级建筑摄影质量
- 焦距: 24mm广角镜头

最终图像应适合作为建筑方案的街景效果图展示。
```

### English Version

```
Generate a 3D perspective architectural rendering based on this 2D elevation drawing.

Technical Conversion Requirements:
- Extrude the flat elevation into a realistic 3D perspective view
- Viewpoint: {VIEWPOINT} (e.g., "street-level eye view / worm's eye view")
- Strictly maintain window positions, proportions, and arrangements from elevation

Material Application:
- Facade Material: {FACADE_MATERIAL} (e.g., "red brick with deep grey mortar joints")
- Window Frames: {WINDOW_FRAMES} (e.g., "dark aluminum frames")
- Roof Material: {ROOF_MATERIAL} (e.g., "dark grey asphalt shingles")
- Base Material: {BASE_MATERIAL} (e.g., "granite")

Environmental Settings:
- Sky: {SKY} (e.g., "clear blue sky with light clouds")
- Lighting: {LIGHTING} (e.g., "3 PM side lighting with long shadows")
- Context: {CONTEXT} (e.g., "urban street, sidewalk, pedestrians")
- Season: {SEASON} (e.g., "spring with green trees")

Technical Requirements:
- Add realistic drop shadows to window reveals to show depth
- Accurate material texture scaling (standard brick dimensions)
- Photorealistic architectural photography quality
- Focal length: 24mm wide-angle lens

The final image should be suitable as a street view rendering for architectural proposals.
```

---

## Tips / 使用技巧

### 中文

- **结构参考强度**: 使用Structure Reference强度0.9-1.0严格遵循立面图线条
- **材质尺寸**: 明确"标准砖尺寸240×115mm"比"砖墙"效果更真实
- **阴影一致性**: 指定"下午3点侧光"确保阴影方向与窗洞深度一致
- **透视修正**: 如果首次生成透视变形，使用"修正透视使垂直线平行"进行二次优化

### English

- **Structure Reference Strength**: Use 0.9-1.0 strength to strictly follow elevation linework
- **Material Dimensions**: Specifying "standard brick 240×115mm" works better than just "brick wall"
- **Shadow Consistency**: Specify "3 PM side lighting" to ensure shadow direction matches window depth
- **Perspective Correction**: If initial generation has distortion, use "correct perspective to make vertical lines parallel" for refinement

---

## 标签 / Tags

`#技术转可视化` `#立面图` `#CAD转渲染` `#建筑效果图` `#透视生成`

`#technical-to-visual` `#elevation-drawing` `#CAD-to-render` `#architectural-rendering` `#perspective-generation`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
