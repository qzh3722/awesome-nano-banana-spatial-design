# [I-001] Furniture Layout Generation from Room Dimensions / 根据房间尺寸生成家具布局

**Category**: Interior Design
**Subcategory**: Space Planning & Layout
**Difficulty**: Beginner
**Thinking Mode**: Optional (Recommended for complex spaces)

---

## 🎯 Problem Statement / 痛点描述

### English
Interior designers often need to quickly visualize furniture arrangements for client presentations, especially in early design phases. Creating multiple layout options in CAD or 3D software is time-consuming. This prompt generates photorealistic top-down furniture layouts based on room dimensions and functional requirements, allowing rapid iteration and client feedback.

**When to use this:**
- Initial space planning for residential or commercial projects
- Testing multiple furniture arrangement options
- Client presentations showing different layout possibilities
- Quick feasibility studies for existing spaces

### 中文
室内设计师经常需要快速可视化家具布置以供客户演示，特别是在早期设计阶段。在CAD或3D软件中创建多个布局方案非常耗时。此提示词基于房间尺寸和功能需求生成照片级俯视家具布局图，允许快速迭代和客户反馈。

**使用场景：**
- 住宅或商业项目的初始空间规划
- 测试多种家具布置方案
- 向客户展示不同布局可能性
- 对现有空间进行快速可行性研究

---

## 📝 Prompt Template / 提示词模板

### English Version
```
Create a photorealistic top-down view of a furniture layout for the following space:

Room Specifications:
- Room Type: {ROOM_TYPE} (e.g., "living room", "bedroom", "home office")
- Dimensions: {LENGTH} x {WIDTH} meters / {LENGTH} x {WIDTH} feet
- Ceiling Height: {HEIGHT} meters / {HEIGHT} feet
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
- Maintain clear circulation paths (minimum 80cm / 32" width)
- Show flooring texture and area rugs
- Add small details like plants, books, or decorative items

The result should be presentation-quality with photorealistic materials and professional styling.
```

### 中文版本
```
为以下空间创建照片级俯视家具布局图：

房间规格：
- 房间类型：{房间类型}（例如："客厅"、"卧室"、"家庭办公室"）
- 尺寸：{长度} x {宽度} 米
- 层高：{高度} 米
- 窗户：{窗户描述}（例如："北墙一扇大窗，2.5米宽"）
- 门：{门描述}（例如："东墙入口门，向内开"）

功能需求：
- 主要功能：{主要用途}（例如："娱乐和放松"、"工作和学习"）
- 所需座位数：{座位数量}
- 储物需求：{储物要求}
- 特殊要求：{特殊需求}（例如："需要放钢琴的空间"、"宠物友好"）

设计风格：
- 风格：{室内风格}（例如："现代简约"、"中世纪现代"、"工业风"）
- 色彩方案：{色彩方案}
- 材质偏好：{材质}

需要包含的家具：
{家具列表}
（例如："一张三人沙发、两把单人椅、茶几、边几、落地灯、电视柜、书架"）

技术要求：
- 以完美的俯视正交视图显示空间
- 包含真实阴影和光照
- 确保家具比例正确，与房间大小相称
- 保持清晰的动线（最小80厘米宽）
- 显示地板纹理和地毯
- 添加植物、书籍或装饰品等小细节

结果应为演示级质量，具有照片级真实材质和专业软装。
```

---

## ⚙️ Key Parameters / 关键参数

| Parameter | Value | Notes |
|-----------|-------|-------|
| **aspect_ratio** | Match room proportions | Use `16:9` for wider rooms, `1:1` for square rooms |
| **thinking_mode** | `On` (Recommended) | Helps calculate proper furniture scale and spacing |
| **guidance_scale** | `10-12` | Ensures furniture placement follows spatial logic |
| **seed** | `[Optional]` | Save to generate variations with same layout |
| **reference_image** | `Optional` | Upload room photo or sketch for context |

### Reference Image Guidance / 参考图使用指南

**Optional - When to use reference images:**
- You have an existing room photo and want to redesign the layout
- You have a rough sketch of preferred furniture placement
- You want to maintain specific architectural features (fireplace, built-ins)

**What to upload:**
- Current room photo (any angle)
- Hand-drawn layout sketch
- Inspiration images showing desired furniture style

**How the model will use it:**
The model will extract room proportions, window/door locations, and architectural features while generating new furniture arrangements.

---

## 🖼️ Example Output / 示例结果

### Output Example 1: Modern Living Room / 现代客厅

![Output Example 1](../../assets/images/I-001-output-modern.jpg)
*20 sq m living room with modern minimalist furniture, neutral color palette*

**Prompt used:**
```
Create a photorealistic top-down view of a furniture layout for the following space:

Room Specifications:
- Room Type: Living room
- Dimensions: 5m x 4m (20 sq m)
- Ceiling Height: 2.8m
- Windows: One large window on the north wall, 2.5m wide, floor-to-ceiling
- Doors: Entry door on east wall, opens inward

Functional Requirements:
- Primary Function: Entertaining guests and daily relaxation
- Number of Seats Required: 5-6 people
- Storage Needs: Media storage, some book display
- Special Requirements: TV viewing area, good conversation layout

Design Style:
- Style: Modern minimalist with Scandinavian influence
- Color Palette: Warm neutrals - white walls, light gray sofa, natural wood accents, black metal details
- Material Preferences: Light oak wood, linen fabrics, matte black metal, white marble accents

Furniture to Include:
- One 3-seater sofa in light gray linen (2.2m length)
- Two modern armchairs in complementary gray tone
- Round coffee table in white marble and brass (90cm diameter)
- Wooden side table
- Low media console in light oak (1.8m length)
- One floor lamp with black metal frame
- Small bookshelf or floating shelves

Technical Requirements:
- Show the space from a perfect top-down orthographic view
- Include realistic shadows from natural window light
- Ensure furniture is properly scaled and proportional to room size
- Maintain clear circulation paths (minimum 80cm width)
- Show light oak herringbone flooring with a natural jute area rug under the seating area
- Add small details like green plants, art books on coffee table, a throw blanket on sofa

The result should be presentation-quality with photorealistic materials and professional styling.
```

---

## 💡 Tips & Variations / 使用技巧与变体

### English

1. **Scale Accuracy**: Always provide specific dimensions. Adding "ensure furniture fits standard human scale" helps prevent oversized pieces
2. **Circulation Logic**: Mention minimum pathway widths (80cm for comfortable walking) to ensure practical layouts
3. **Focal Points**: Specify "arrange furniture to face {focal point}" (e.g., window, fireplace, TV) for intentional layouts
4. **Multiple Options**: Generate 3-4 variations by changing furniture list or arrangement description (e.g., "symmetrical layout" vs "asymmetrical casual grouping")
5. **Complex Spaces**: For L-shaped or irregular rooms, enable Thinking Mode and provide detailed dimension descriptions

**Variations:**
- **Open plan spaces**: Define zones by describing "living zone in the west area, dining zone in the east"
- **Small spaces**: Add "space-saving furniture" and "multi-functional pieces" to descriptions
- **Commercial**: Replace residential furniture with office desks, waiting area seating, or retail fixtures

### 中文

1. **尺度准确性**: 始终提供具体尺寸。添加"确保家具符合标准人体尺度"有助于防止过大的物件
2. **动线逻辑**: 提及最小通道宽度（舒适行走需80厘米）以确保实用的布局
3. **视觉焦点**: 指定"将家具布置面向{焦点}"（如窗户、壁炉、电视）以实现有意图的布局
4. **多个方案**: 通过更改家具列表或布置描述生成3-4个变体（如"对称布局"vs"不对称休闲组合"）
5. **复杂空间**: 对于L型或不规则房间，启用思考模式并提供详细尺寸描述

**变体：**
- **开放式空间**: 通过描述"西侧为客厅区，东侧为餐厅区"来定义分区
- **小空间**: 在描述中添加"节省空间的家具"和"多功能家具"
- **商业空间**: 用办公桌、等候区座椅或零售固定装置替换住宅家具

---

## 🔗 Related Cases / 相关案例

- [A-001: CAD to Colored Plan](../architecture/A-001-cad-to-colored-plan.md) - If you have an existing CAD plan
- [I-002: Open Plan Zoning](./I-002-open-plan-zoning.md) - For multi-functional open spaces
- [I-019: Style Mood Board to 3D](./I-019-style-mood-board.md) - Visualize a specific style direction

---

## 📊 Quality Checklist / 质量检查清单

- [x] Problem statement is clear and relatable
- [x] Prompt is complete with all necessary placeholders
- [x] Parameters are tested and optimal
- [ ] Example output is high-quality (minimum 1920px width) - *Placeholder to be added*
- [x] Both English and Chinese versions are complete
- [x] Reference image guidance is clear
- [x] Tips are practical and tested
- [x] Related cases are linked

---

**Last Updated**: 2025-11-28
**Contributor**: Project Maintainer
**Version**: 1.0
