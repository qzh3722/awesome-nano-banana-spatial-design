# [L-001] Landscape Master Plan Visualization / 景观总平面图可视化

**Category**: Landscape
**Subcategory**: Site Planning & Hardscape
**Difficulty**: Intermediate
**Thinking Mode**: Optional (Recommended for complex sites)

---

## 🎯 Problem Statement / 痛点描述

### English
Landscape architects need to communicate site plans to clients who may not read technical drawings well. Traditional plan rendering is labor-intensive. This prompt converts landscape master plans (or descriptions) into beautiful top-down visualizations showing planting areas, hardscape, and spatial relationships—perfect for client presentations and design development.

**When to use this:**
- Client presentations for residential or commercial landscape projects
- Design development to visualize planting mass and material distribution
- Competition boards and portfolio pieces
- Community engagement and public presentations

### 中文
景观设计师需要向可能不太会读技术图纸的客户传达场地规划。传统的平面渲染图制作非常费时。此提示词将景观总平面图（或描述）转换为美丽的俯视可视化图，展示种植区、硬景和空间关系——非常适合客户演示和设计深化。

**使用场景：**
- 住宅或商业景观项目的客户演示
- 设计深化以可视化植物组团和材质分布
- 竞赛展板和作品集
- 社区参与和公众演示

---

## 📝 Prompt Template / 提示词模板

### English Version
```
Create a photorealistic top-down landscape master plan visualization for the following site:

Site Information:
- Project Type: {PROJECT_TYPE} (e.g., "residential backyard", "public park", "commercial plaza")
- Site Dimensions: {LENGTH} x {WIDTH} meters / {LENGTH} x {WIDTH} feet
- Climate Zone: {CLIMATE} (e.g., "temperate", "mediterranean", "tropical")
- Topography: {TERRAIN} (e.g., "flat", "gentle slope", "terraced")

Design Zones:
{ZONE_DESCRIPTIONS}
Example:
- Entry area (northeast): Paved forecourt with specimen trees
- Central lawn (center): Open grass area for recreation
- Seating garden (southwest): Intimate patio with perennial borders
- Woodland edge (northwest): Native shade planting

Hardscape Elements:
- Paving Materials: {PAVING} (e.g., "natural stone, gravel paths, wooden decking")
- Structures: {STRUCTURES} (e.g., "pergola, seating walls, water feature")
- Furnishings: {FURNISHINGS} (e.g., "benches, planters, outdoor lighting")

Planting Palette:
- Trees: {TREE_LIST} (e.g., "Japanese maple, flowering cherry, evergreen pines")
- Shrubs: {SHRUB_LIST} (e.g., "boxwood hedges, hydrangeas, ornamental grasses")
- Groundcover: {GROUNDCOVER} (e.g., "lawn, clover, perennial beds, mulch")
- Season: {SEASON} (Specify for accurate plant appearance)

Style and Character:
- Design Style: {LANDSCAPE_STYLE} (e.g., "naturalistic", "formal", "contemporary")
- Color Palette: {COLOR_SCHEME} (e.g., "green with white and purple flowers", "autumn tones")
- Maintenance Level: {MAINTENANCE} (e.g., "low-maintenance", "high-maintenance formal")

Technical Requirements:
- Perfect top-down orthographic view showing entire site
- Photorealistic textures for all materials
- Accurate plant sizes and groupings
- Soft shadows suggesting time of day
- Clear definition between zones
- Show surrounding context if relevant

The final image should convey the design intent clearly and be suitable for professional presentation.
```

### 中文版本
```
为以下场地创建照片级俯视景观总平面可视化图：

场地信息：
- 项目类型：{项目类型}（例如："住宅后院"、"公共公园"、"商业广场"）
- 场地尺寸：{长度} x {宽度} 米
- 气候区：{气候}（例如："温带"、"地中海"、"热带"）
- 地形：{地形}（例如："平坦"、"缓坡"、"台地"）

设计分区：
{分区描述}
示例：
- 入口区（东北）：铺装前院配景观树
- 中央草坪（中心）：开放草地供休闲活动
- 座位花园（西南）：私密露台配多年生植物边界
- 林缘区（西北）：本土耐阴植物

硬景元素：
- 铺装材料：{铺装}（例如："天然石材、碎石小径、木平台"）
- 构筑物：{构筑物}（例如："廊架、座墙、水景"）
- 设施：{设施}（例如："长凳、花器、户外照明"）

植物材料：
- 乔木：{乔木列表}（例如："日本枫树、樱花、常绿松树"）
- 灌木：{灌木列表}（例如："黄杨绿篱、绣球花、观赏草"）
- 地被：{地被}（例如："草坪、三叶草、多年生花境、覆盖物"）
- 季节：{季节}（指定以获得准确的植物外观）

风格和特征：
- 设计风格：{景观风格}（例如："自然式"、"规则式"、"当代"）
- 色彩方案：{色彩方案}（例如："绿色配白色和紫色花卉"、"秋季色调"）
- 养护水平：{养护}（例如："低养护"、"高养护规则式"）

技术要求：
- 完美俯视正交视图展示整个场地
- 所有材料的照片级纹理
- 准确的植物尺寸和组团
- 柔和阴影暗示时间
- 分区之间清晰界定
- 如相关则显示周边环境

最终图像应清晰传达设计意图，适合专业演示。
```

---

## ⚙️ Key Parameters / 关键参数

| Parameter | Value | Notes |
|-----------|-------|-------|
| **aspect_ratio** | Match site proportions | Often `16:9` or `4:3` for rectangular sites |
| **thinking_mode** | `On` (Recommended) | Helps organize complex spatial relationships |
| **guidance_scale** | `10-12` | Ensures accurate zone placement |
| **seed** | `[Optional]` | For generating seasonal variations |
| **reference_image** | `Recommended` | Upload CAD plan, sketch, or site photo |

### Reference Image Guidance / 参考图使用指南

**Recommended - What to upload:**
- CAD landscape plan (line drawing)
- Hand-drawn site plan sketch
- Aerial site photo showing existing conditions
- Inspiration images for desired plant character

**Preparation tips:**
- For CAD plans: Export with clear zone boundaries and labels
- For sketches: Use clear line work showing major elements
- For site photos: Drone or high-angle views work best

**How the model will use it:**
The model will extract site boundaries, spatial proportions, and major design zones while adding realistic materials and planting.

---

## 🖼️ Example Output / 示例结果

### Output Example: Residential Garden / 住宅花园

![Output Example](../../assets/images/L-001-output-residential.jpg)
*200 sq m residential garden with naturalistic planting, stone paths, and central lawn - Summer visualization*

**Prompt used:**
```
Create a photorealistic top-down landscape master plan visualization for the following site:

Site Information:
- Project Type: Residential backyard garden
- Site Dimensions: 15m x 13m (approximately 200 sq m)
- Climate Zone: Temperate (similar to UK or Pacific Northwest)
- Topography: Mostly flat with slight slope away from house

Design Zones:
- Patio area (adjacent to house, south side): Natural stone paving, outdoor dining area
- Perennial border (east side): Curved border with layered planting, 2m depth
- Central lawn (center): Kidney-shaped open grass area for family activities
- Woodland garden (north side): Shade-loving plants under existing mature trees
- Vegetable garden (west corner): Raised beds with organized rows
- Gravel path: Meandering path connecting all zones

Hardscape Elements:
- Paving Materials: Irregular natural limestone for patio, decomposed granite for paths
- Structures: Simple wooden pergola over part of patio (3m x 3m), low stone seating wall
- Furnishings: Wooden dining table and chairs on patio, scattered stone boulders as natural seating

Planting Palette:
- Trees: Existing mature oak tree (northwest), one new flowering cherry (east)
- Shrubs: Hydrangeas, lavender, rosemary, boxwood edging along paths
- Perennials: Salvia, echinacea, rudbeckia, ornamental grasses (miscanthus, pennisetum)
- Groundcover: Lawn in center, mulch in beds, creeping thyme between stepping stones
- Season: Mid-summer (peak bloom)

Style and Character:
- Design Style: Naturalistic English garden with relaxed planting
- Color Palette: Predominantly green with purple, pink, and yellow flowering accents
- Maintenance Level: Medium - requires seasonal pruning and deadheading

Technical Requirements:
- Perfect top-down orthographic view showing entire garden
- Photorealistic textures for stone, gravel, wood, lawn, and plant materials
- Show plants at mature size with natural, flowing forms
- Soft shadows suggesting afternoon summer light
- Clear visual distinction between lawn, paths, and planted areas
- Show part of house facade at bottom edge for context

The final image should convey a lush, lived-in garden character suitable for client presentation.
```

---

## 💡 Tips & Variations / 使用技巧与变体

### English

1. **Seasonal Specificity**: Always specify season. "Early spring" gives different results than "mid-summer bloom"
2. **Plant Maturity**: Mention "show plants at mature size" or "2 years after planting" for realistic expectations
3. **Zone Clarity**: Use directional references (north, south) or relative positions (near house, far corner) for clear organization
4. **Material Detail**: Specific material names ("bluestone" vs "stone") give more accurate results
5. **Complex Topography**: For sloped sites, enable Thinking Mode and describe level changes clearly

**Variations:**
- **Seasonal series**: Generate the same plan in spring, summer, fall, winter by changing season parameter
- **Before/After**: Create existing conditions vs. proposed design views
- **Public spaces**: Scale up for parks or plazas with larger tree groupings and open lawns
- **Rooftop gardens**: Add "elevated planters and lightweight materials" for rooftop contexts

### 中文

1. **季节特定性**: 始终指定季节。"早春"与"盛夏花期"会给出不同结果
2. **植物成熟度**: 提及"显示植物成熟尺寸"或"种植2年后"以获得现实预期
3. **分区清晰度**: 使用方位参考（北、南）或相对位置（靠近房屋、远角）以实现清晰组织
4. **材料细节**: 具体材料名称（"青石板"vs"石材"）提供更准确结果
5. **复杂地形**: 对于坡地，启用思考模式并清楚描述高差变化

**变体：**
- **季节系列**: 通过更改季节参数生成同一方案的春夏秋冬版本
- **前后对比**: 创建现状与设计方案视图
- **公共空间**: 放大为公园或广场，使用更大的乔木组团和开放草坪
- **屋顶花园**: 添加"升高种植池和轻质材料"用于屋顶环境

---

## 🔗 Related Cases / 相关案例

- [L-009: Planting Plan Generation](./L-009-planting-plan.md) - Focus on detailed plant composition
- [L-025: Four Seasons Comparison](./L-025-four-seasons.md) - Visualize seasonal changes
- [A-001: CAD to Colored Plan](../architecture/A-001-cad-to-colored-plan.md) - Similar workflow for architectural plans

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
