# [A-001] CAD Floor Plan to Photorealistic Colored Top View / CAD平面图转彩色鸟瞰图

**Category**: Architecture
**Subcategory**: CAD to Visualization
**Difficulty**: Beginner
**Thinking Mode**: Optional (Recommended for complex layouts)

---

## 🎯 Problem Statement / 痛点描述

### English
Clients and stakeholders often struggle to understand black-and-white CAD floor plans. Traditional methods require manual rendering in software like Photoshop or SketchUp, which is time-consuming. This prompt transforms technical CAD drawings into photorealistic colored top-down views with furniture, materials, and realistic lighting—perfect for client presentations and early-stage design reviews.

**When to use this:**
- Client presentations for residential or commercial projects
- Quick design review meetings
- Marketing materials for real estate
- Portfolio pieces showing before/after workflow

### 中文
客户和利益相关者往往难以理解黑白CAD平面图。传统方法需要在Photoshop或SketchUp等软件中手动渲染，非常耗时。此提示词将技术CAD图纸转换为带有家具、材质和真实光照的照片级彩色俯视图——非常适合客户演示和早期设计评审。

**使用场景：**
- 住宅或商业项目的客户演示
- 快速设计评审会议
- 房地产营销材料
- 展示前后工作流程的作品集

---

## 📝 Prompt Template / 提示词模板

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

### 中文版本
```
将上传的CAD平面图转换为照片级俯视建筑可视化图。

设计规格：
- 风格：{室内风格}（例如："现代简约"、"斯堪的纳维亚"、"传统"）
- 空间类型：{空间类型}（例如："住宅公寓"、"办公套间"、"零售店"）
- 主要房间：{房间列表}（例如："客厅、厨房、2间卧室、1间浴室"）

视觉要求：
- 显示每个空间适当的所有家具和固定装置
- 应用真实材质：{材质偏好}（例如："白橡木地板、大理石台面、亚麻软包"）
- 光照：自然日光从窗户照射进来，带有柔和阴影
- 添加细节：地毯、植物、装饰物品
- 保持CAD平面图的精确空间比例和墙体位置

技术细节：
- 视角：完美的俯视正交视图
- 渲染质量：照片级真实感，材质纹理准确
- 色彩方案：{色彩方案}（例如："暖色调中性色加大地色系"、"冷灰和蓝色"）

最终图像应看起来像适合客户演示的专业建筑渲染图。
```

---

## ⚙️ Key Parameters / 关键参数

| Parameter | Value | Notes |
|-----------|-------|-------|
| **aspect_ratio** | `1:1` or `4:3` | Match your CAD plan proportions |
| **thinking_mode** | `On` (Recommended) | Helps maintain spatial accuracy and proportions |
| **guidance_scale** | `10-12` | Higher values ensure closer adherence to CAD layout |
| **seed** | `[Optional]` | Save seed for variations with same layout |
| **reference_image** | `Required` | See guidance below |

### Reference Image Guidance / 参考图使用指南

**What to upload:**
- A clean, high-contrast black-and-white CAD floor plan
- Export as PNG or JPG with at least 1500px on the longest side
- Ensure walls are clearly defined (thick black lines work best)
- Remove unnecessary annotation layers and dimensions if too cluttered

**Preparation tips:**
- Use a white background with black line work
- Hide unnecessary layers (grids, dimensions, technical notes)
- Ensure door swings and windows are visible
- If the plan is complex, consider processing one floor at a time

**How the model will use it:**
The model will:
1. Detect the room boundaries and wall positions
2. Understand spatial relationships and proportions
3. Place furniture according to room function
4. Apply materials while respecting the original layout

---

## 🖼️ Example Output / 示例结果

### Input / 输入

![Input Example](../../assets/images/A-001-input-example.jpg)
*Example: Black-and-white CAD floor plan of a 2-bedroom apartment (100 sq m)*

### Output / 输出

![Output Example](../../assets/images/A-001-output-example.jpg)
*Generated photorealistic top-down view with modern Scandinavian styling, white oak floors, and natural lighting*

**Prompt used for this example:**
```
Transform the uploaded CAD floor plan into a photorealistic top-down architectural visualization.

Design Specifications:
- Style: Modern Scandinavian with minimalist aesthetic
- Space Type: Residential apartment (2-bedroom, 100 sq m)
- Key Rooms: Open living/dining room, kitchen, 2 bedrooms, 1 bathroom, entrance hall

Visual Requirements:
- Show all furniture: Sofa, dining table with 4 chairs, double beds, minimalist kitchen island
- Apply realistic materials: White oak herringbone flooring, white matte kitchen cabinets, marble bathroom surfaces, light gray linen upholstery
- Lighting: Soft natural daylight from windows creating gentle shadows
- Add subtle details: Green plants in living areas, area rugs under dining and living zones, minimal artwork
- Maintain the exact spatial proportions and wall positions from the CAD plan

Technical Details:
- Perspective: Perfect top-down orthographic view
- Render quality: Photorealistic with accurate wood grain and fabric textures
- Color palette: Warm neutrals with white, light gray, natural wood tones, and green accents from plants

The final image should look like a professional architectural rendering suitable for client presentation.
```

---

## 💡 Tips & Variations / 使用技巧与变体

### English

1. **Material Specificity**: Instead of "wood flooring," specify "white oak herringbone pattern" or "dark walnut planks" for better results
2. **Furniture Scale**: If furniture appears too large/small, add phrases like "appropriately scaled furniture for human use"
3. **Lighting Control**: Specify time of day ("morning light," "golden hour") for different shadow qualities
4. **Style Consistency**: Reference specific design movements (e.g., "Japanese minimalism" vs. "Scandinavian hygge") for coherent aesthetics
5. **Complex Layouts**: For apartments with 4+ rooms, enable Thinking Mode to help the model understand spatial relationships

**Variations:**
- **Commercial spaces**: Replace residential furniture with desks, conference tables, reception areas
- **Multiple options**: Generate 3-4 versions with different color schemes by changing the palette description
- **Seasonal context**: Add "winter scene with warm interior lighting" or "summer with bright natural light"

### 中文

1. **材质具体性**: 不要说"木地板"，而要指定"白橡木人字拼花"或"深色胡桃木木板"以获得更好效果
2. **家具比例**: 如果家具显得过大/过小，添加"适合人类使用的比例正确的家具"等短语
3. **光照控制**: 指定一天中的时间（"晨光"、"黄金时刻"）以获得不同的阴影质量
4. **风格一致性**: 参考具体的设计流派（如"日式极简"vs"斯堪的纳维亚温馨风"）以获得连贯美学
5. **复杂布局**: 对于4个以上房间的公寓，启用思考模式以帮助模型理解空间关系

**变体：**
- **商业空间**: 用办公桌、会议桌、接待区替换住宅家具
- **多个方案**: 通过更改色彩方案描述生成3-4个不同版本
- **季节背景**: 添加"冬季场景配温暖室内照明"或"夏季配明亮自然光"

---

## 🔗 Related Cases / 相关案例

- [A-002: Elevation to 3D Render](./A-002-elevation-to-render.md) - Convert facade drawings to realistic views
- [I-001: Space Planning Layout](../interior/I-001-space-planning.md) - Generate furniture layouts from scratch
- [A-007: Sketch to Presentation](./A-007-sketch-to-presentation.md) - Similar workflow for hand sketches

---

## 📊 Quality Checklist / 质量检查清单

Before publishing this case:

- [x] Problem statement is clear and relatable
- [x] Prompt is complete with all necessary placeholders
- [x] Parameters are tested and optimal
- [ ] Example output is high-quality (minimum 1920px width) - *Placeholder images to be added*
- [x] Both English and Chinese versions are complete
- [x] Reference image guidance is clear
- [x] Tips are practical and tested
- [x] Related cases are linked

---

**Last Updated**: 2025-11-28
**Contributor**: Project Maintainer
**Version**: 1.0
