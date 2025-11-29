# CAD Floor Plan to Photorealistic Top View / CAD平面图转彩色鸟瞰图

## 效果预览 / Preview

> Transform black-and-white CAD floor plans into photorealistic colored visualizations with furniture, materials, and realistic lighting.
>
> 将黑白CAD平面图转换为带有家具、材质和真实光照的照片级彩色可视化图。

![CAD to Realistic Plan Example](../../assets/images/A-001-output-example.jpg)
*Generated photorealistic top-down view with modern Scandinavian styling, white oak floors, and natural lighting / 生成的照片级俯视图,现代斯堪的纳维亚风格,白橡木地板,自然光照*

---

## 提示词 / Prompt

### 中文版

```
将上传的CAD平面图转换为照片级俯视建筑可视化图。

设计规格:
- 风格: {室内风格} (例如: "现代简约"、"斯堪的纳维亚"、"传统")
- 空间类型: {空间类型} (例如: "住宅公寓"、"办公套间"、"零售店")
- 主要房间: {房间列表} (例如: "客厅、厨房、2间卧室、1间浴室")

视觉要求:
- 显示每个空间适当的所有家具和固定装置
- 应用真实材质: {材质偏好} (例如: "白橡木地板、大理石台面、亚麻软包")
- 光照: 自然日光从窗户照射进来,带有柔和阴影
- 添加细节: 地毯、植物、装饰物品
- 保持CAD平面图的精确空间比例和墙体位置

技术细节:
- 视角: 完美的俯视正交视图
- 渲染质量: 照片级真实感,材质纹理准确
- 色彩方案: {色彩方案} (例如: "暖色调中性色加大地色系"、"冷灰和蓝色")

最终图像应看起来像适合客户演示的专业建筑渲染图。
```

### English Version

```
Transform the uploaded CAD floor plan into a photorealistic top-down architectural visualization.

Design Specifications:
- Style: {INTERIOR_STYLE} (e.g., "modern minimalist", "scandinavian", "traditional")
- Space Type: {SPACE_TYPE} (e.g., "residential apartment", "office suite", "retail store")
- Key Rooms: {ROOM_LIST} (e.g., "living room, kitchen, 2 bedrooms, 1 bathroom")

Visual Requirements:
- Show all furniture and fixtures appropriate for each space
- Apply realistic materials: {MATERIAL_PREFERENCES} (e.g., "white oak flooring, marble countertops, linen upholstery")
- Lighting: Natural daylight streaming through windows with soft shadows
- Add subtle details: area rugs, plants, decorative items
- Maintain the exact spatial proportions and wall positions from the CAD plan

Technical Details:
- Perspective: Perfect top-down orthographic view
- Render quality: Photorealistic with accurate material textures
- Color palette: {COLOR_SCHEME} (e.g., "warm neutrals with earth tones", "cool grays and blues")

The final image should look like a professional architectural rendering suitable for client presentation.
```

---

## Tips / 使用技巧

### 中文

- **材质具体化**: 不要说"木地板",而要指定"白橡木人字拼花"或"深色胡桃木木板"以获得更真实的效果
- **启用Thinking Mode**: 对于4个以上房间的复杂户型,启用Thinking Mode以帮助模型理解空间关系
- **风格一致性**: 参考具体的设计流派(如"日式极简"vs"斯堪的纳维亚温馨风")以获得连贯美学
- **多方案对比**: 通过更改色彩方案描述生成3-4个不同版本,快速提供客户选择

### English

- **Material Specificity**: Instead of "wood flooring," specify "white oak herringbone pattern" or "dark walnut planks" for better results
- **Enable Thinking Mode**: For complex layouts with 4+ rooms, enable Thinking Mode to help the model understand spatial relationships
- **Style Consistency**: Reference specific design movements (e.g., "Japanese minimalism" vs. "Scandinavian hygge") for coherent aesthetics
- **Multiple Options**: Generate 3-4 versions with different color schemes by changing the palette description for quick client comparisons

---

## 标签 / Tags

`#CAD转可视化` `#建筑设计` `#平面图渲染` `#技术转化` `#住宅设计`

`#CAD-to-visualization` `#architectural-design` `#floor-plan-rendering` `#technical-to-visual` `#residential-design`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
