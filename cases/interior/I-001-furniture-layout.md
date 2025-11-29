# Furniture Layout Generation from Room Dimensions / 根据房间尺寸生成家具布局

## 效果预览 / Preview

> Generate photorealistic top-down furniture layouts based on room dimensions and functional requirements, perfect for rapid design iteration.
>
> 基于房间尺寸和功能需求生成照片级俯视家具布局图,非常适合快速设计迭代。

![Furniture Layout Example](../../assets/images/I-001-output-modern.jpg)
*20 sq m living room with modern minimalist furniture, neutral color palette / 20平方米客厅,现代简约家具,中性色调*

---

## 提示词 / Prompt

### 中文版

```
为以下空间创建照片级俯视家具布局图:

房间规格:
- 房间类型: {房间类型} (例如: "客厅"、"卧室"、"家庭办公室")
- 尺寸: {长度} x {宽度} 米
- 层高: {高度} 米
- 窗户: {窗户描述} (例如: "北墙一扇大窗,2.5米宽")
- 门: {门描述} (例如: "东墙入口门,向内开")

功能需求:
- 主要功能: {主要用途} (例如: "娱乐和放松"、"工作和学习")
- 所需座位数: {座位数量}
- 储物需求: {储物要求}
- 特殊要求: {特殊需求} (例如: "需要放钢琴的空间"、"宠物友好")

设计风格:
- 风格: {室内风格} (例如: "现代简约"、"中世纪现代"、"工业风")
- 色彩方案: {色彩方案}
- 材质偏好: {材质}

需要包含的家具:
{家具列表}
(例如: "一张三人沙发、两把单人椅、茶几、边几、落地灯、电视柜、书架")

技术要求:
- 以完美的俯视正交视图显示空间
- 包含真实阴影和光照
- 确保家具比例正确,与房间大小相称
- 保持清晰的动线(最小80厘米宽)
- 显示地板纹理和地毯
- 添加植物、书籍或装饰品等小细节

结果应为演示级质量,具有照片级真实材质和专业软装。
```

### English Version

```
Create a photorealistic top-down view of a furniture layout for the following space:

Room Specifications:
- Room Type: {ROOM_TYPE} (e.g., "living room", "bedroom", "home office")
- Dimensions: {LENGTH} x {WIDTH} meters
- Ceiling Height: {HEIGHT} meters
- Windows: {WINDOW_DESCRIPTION} (e.g., "One large window on the north wall, 2.5m wide")
- Doors: {DOOR_DESCRIPTION} (e.g., "Entry door on east wall, opens inward")

Functional Requirements:
- Primary Function: {PRIMARY_USE} (e.g., "entertaining and relaxation", "work and study")
- Number of Seats Required: {SEATING_COUNT}
- Storage Needs: {STORAGE_REQUIREMENTS}
- Special Requirements: {SPECIAL_NEEDS} (e.g., "space for a piano", "pet-friendly")

Design Style:
- Style: {INTERIOR_STYLE} (e.g., "modern minimalist", "mid-century modern", "industrial")
- Color Palette: {COLOR_SCHEME}
- Material Preferences: {MATERIALS}

Furniture to Include:
{FURNITURE_LIST}
(e.g., "One 3-seater sofa, two armchairs, coffee table, side table, floor lamp, media console, bookshelf")

Technical Requirements:
- Show the space from a perfect top-down orthographic view
- Include realistic shadows and lighting
- Ensure furniture is properly scaled and proportional to room size
- Maintain clear circulation paths (minimum 80cm width)
- Show flooring texture and area rugs
- Add small details like plants, books, or decorative items

The result should be presentation-quality with photorealistic materials and professional styling.
```

---

## Tips / 使用技巧

### 中文

- **尺度准确性**: 始终提供具体尺寸。添加"确保家具符合标准人体尺度"有助于防止过大的物件
- **启用Thinking Mode**: 对于复杂空间或L型房间,启用Thinking Mode并提供详细尺寸描述
- **动线逻辑**: 提及最小通道宽度(舒适行走需80厘米)以确保实用的布局
- **多方案测试**: 通过更改家具列表或布置描述生成3-4个变体(如"对称布局"vs"不对称休闲组合")

### English

- **Scale Accuracy**: Always provide specific dimensions. Adding "ensure furniture fits standard human scale" helps prevent oversized pieces
- **Enable Thinking Mode**: For complex spaces or L-shaped rooms, enable Thinking Mode and provide detailed dimension descriptions
- **Circulation Logic**: Mention minimum pathway widths (80cm for comfortable walking) to ensure practical layouts
- **Multiple Options**: Generate 3-4 variations by changing furniture list or arrangement description (e.g., "symmetrical layout" vs "asymmetrical casual grouping")

---

## 标签 / Tags

`#空间规划` `#家具布局` `#室内设计` `#平面布局` `#住宅设计`

`#space-planning` `#furniture-layout` `#interior-design` `#floor-planning` `#residential-design`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
