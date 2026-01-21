<div align="center">

![Awesome Nano Banana 空间设计Banner](./assets/images/banner.jpg)

# Awesome Nano Banana 空间设计

一个面向**空间设计师**的实战场景 AI 提示词库
 
<!-- 语言切换 -->
[English](./README.md) | **简体中文**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

本仓库**不是“魔法提示词”集合**。  
它记录的是 **AI 提示词在真实空间设计工作流中的实际应用** —— 从早期概念构思到平面图自动化，再到高级渲染定制。

本仓库中的所有提示词：
- 面向**真实设计场景**设计
- 按**设计场景和阶段**组织
- 旨在被**修改、组合和调整**，而非盲目复制

本项目作为开放的、不断演进的参考文档发布给空间设计社区。

> 📖 **初次访问？** 查看 [开始使用](./Start-Here.zh-CN.md) 找到适合你经验水平的入口。

---

## 🎯 快速导航 <a id="目录"></a>

**跳转到工作流阶段：**  
[🎨 概念构思](#concept) • [📐 空间规划](#planning) • [🔧 技术转视觉](#technical) • [🎨 材质软装](#material) • [🖼️ 场景渲染](#rendering) • [⚙️ 专项应用](#special)

> **📌 免责声明**：本案例库中使用的所有图片仅用于教育和研究目的。输入图片来自公开的建筑图纸或专门为演示创建。本仓库不主张对引用图片的所有权，所有图片在非商业教育目的下按合理使用原则使用。

---
<a id="concept"></a>

## 🎨 概念构思
*从零到创意方案*

**本阶段案例：**  
[1.1 自动布置平面图](#11-自动布置平面图-auto-furnish-floor-plan) • [1.2 平地起高楼](#12-平地起高楼-building-from-scratch) • [1.3 迷你建筑模型](#13-迷你建筑模型-miniature-building-model) • [1.4 生成式设计推演](#14-生成式设计推演-generative-design-process) • [1.5 手绘草图转照片级可视化](#15-手绘草图转照片级可视化-sketch-to-photorealistic-visualization) • [1.6 CAD 布局规划](#16-cad-布局规划-cad-layout-planning)

### 1.1 自动布置平面图 (Auto-Furnish Floor Plan)

#### 输入

![输入图片](./assets/cases/1.1-auto-furnish-plan/input.jpg)

#### 输出

![输出图片](./assets/cases/1.1-auto-furnish-plan/output.jpg)

**提示词：**
```
使用上传的平面图作为底图，根据原始图纸中文本标注指示的功能房间标签，在每个空间中布置家具和软装。严格保持所有墙体结构、门的位置、窗户位置和建筑元素与所示完全一致，不对建筑配置做任何修改。不要在布局中添加任何新的墙壁或隔断。在整个构图中保留黑白线条画风格和单色调。从最终输出中移除所有文本注释和标签，仅显示建筑元素和新添加的家具布置。
```

> **💡 提示**：如果对生成的图片要进行修改，请一个空间一个空间修改，不要同时提出多个空间的修改意见，否则结果可能不理想。

[↑ 回到顶部](#目录)

---

### 1.2 平地起高楼 (Building from Scratch)

#### 输入

*仅文字描述 / Text Description Only*

#### 输出

![输出图片](./assets/cases/1.2-building-from-scratch/output.jpg)

**提示词：**
```
生成一栋约300平方米的两层现代别墅的建筑透视渲染图。建筑应采用L形平面布局，并带有一个朝南的庭院。主要材料包括清水混凝土墙和大幅面玻璃系统。一楼包含开放式起居区，可直接通往室外露台，而二楼则容纳私人睡眠区。平屋顶带有深远的挑檐以控制日照。极简装饰，强调水平线条和材料的真实性。
```

#### 💡 技巧：如何从零开始描述别墅

当从零开始描述别墅（没有上传参考图）时，您应该为 Gemini Image Pro 提供遵循以下框架的结构化描述：

**核心要素：**
1.  **可视化类型**：首先，指定您想要生成的可视化类型。说明您是需要建筑渲染图、轴测投影图、立面图、透视图还是平面图表现。这确立了 Gemini 应遵循的技术绘图惯例。
2.  **基本参数**：其次，定义基本的建筑参数。描述建筑体量、层数、总占地尺寸（如果相关）以及主要的空间组织。例如，您可以指定一个带有中央庭院布局的两层别墅，或者一个具有明显公共和私密翼楼的L形平面。
3.  **关键特征**：第三，确定定义别墅特征的关键建筑特征。这可能包括屋顶配置、窗户样式、外表面的材料表现、入口位置和处理方式，或与周围场地条件的关系。
4.  **功能要求**：第四，指定对您的设计意图至关重要的任何功能要求或空间关系。指出内部空间应如何与外部区域联系，主要流线应发生在哪里，或者建筑应如何根据日照或景观进行朝向。

**应避免的内容：**
不要提供每一个设计细节、材料规格或装饰元素的详尽清单，除非这些对您的概念真正至关重要。允许 Gemini Image Pro 通过专业惯例来解决次要细节。当功能和技术参数足以说明问题时，不要用复杂的描述性语言过度规定审美特质。

[↑ 回到顶部](#目录)

---

### 1.3 迷你建筑模型 (Miniature Building Model)

#### 输入

![输入图片](./assets/cases/1.3-miniature-building-model/input.jpg)

#### 输出

![输出图片](./assets/cases/1.3-miniature-building-model/output.jpg)

**提示词：**
```
超写实3D渲染，可爱的迷你[上传图片]建筑。
```

[↑ 回到顶部](#目录)

---

### 1.4 生成式设计推演

#### 输入

![输入图片](./assets/cases/1.4-generative-design-process/input.jpg)

#### 输出

![输出图片](./assets/cases/1.4-generative-design-process/output.jpg)

**提示词：**
```
使用上传的建筑图像作为最终设计成果，生成一个概念图序列，以包含四个连续阶段的 2x2 网格布局展示生成式设计过程。分析上传图像中所示建筑的形式特征，然后反向推导，说明从简单的几何体块到最终形式的概念演变。阶段 1（左上）应显示作为简单几何体积的初始主要体块。阶段 2（右上）应显示第一次主要的形式转换，例如减法操作或体积调整。阶段 3（左下）应显示次要的细化，包括额外的切割、扭曲或清晰度处理。阶段 4（右下）应显示与上传图像匹配的最终建筑形式。将每个阶段呈现为清晰的三维图解，演示设计如何通过连续的形式操作从基本体积演变为完整的建筑配置。
```

[↑ 回到顶部](#目录)

---

### 1.5 手绘草图转照片级可视化

#### 输入

![输入图片](./assets/cases/1.5-sketch-to-photo/input.jpg)

#### 输出

![输出图片](./assets/cases/1.5-sketch-to-photo/output.jpg)
*输出：建筑可视化*

#### 示例 2：室内设计

![输入图片室内](./assets/cases/1.5-sketch-to-photo/input-interior.jpg)
*输入：室内草图*

![输出图片室内](./assets/cases/1.5-sketch-to-photo/output-interior.jpg)
*输出：室内可视化*

**提示词：**
```
使用上传的手绘草图作为设计源，将图纸转换为照片级可视化，同时忠实地保留原始草图中表达的设计意图。严格保持草图中指示的空间配置、比例关系、视角和设计元素的排列。解读草图线条和注释以理解预期的空间布局，然后将其转化为具有适当材质、纹理、光照和照片级渲染质量的逼真三维空间。保持所有构图决策、元素放置和空间关系与原始草图一致，仅添加实现照片级质量所需的材质真实感和光照细节，而不改变基本设计概念。
```

[↑ 回到顶部](#目录)

---

### 1.6 CAD 布局规划

#### 输入

![输入图片](./assets/cases/1.6-cad-layout-planning/input.jpg)

#### 输出

![输出图片](./assets/cases/1.6-cad-layout-planning/output.jpg)

**提示词：**
```
使用上传的显示原始建成状态的 CAD 平面图，保留所有现有的建筑结构，包括外墙、承重墙、所有门洞（特别是入口门）和所有窗户位置，完全按照显示的内容，不做任何修改。入口门作为功能布局规划的主要定位点：紧邻入口的空间应为公共/生活区域。根据此入口位置和现有结构配置，分析空间潜力，并在适当位置添加非承重隔墙，根据住宅设计标准创建合理的房间划分。确立空间划分后，根据确定的功能和住宅室内的典型布局惯例，在每个定义的空间内布置家具和固定装置。平面图边界内的所有内部区域必须分配明确的功能用途并进行适当布置——不应有未定义或空置的空间。将结果呈现为完整的平面图，以专业的 CAD 绘图风格显示新的隔墙布局和家具布置，具有适当的线宽和图形惯例，确保所有原始结构元素和开口保持不变。
```


[↑ 回到顶部](#目录)

---

<a id="planning"></a>

## 📐 空间规划
*布局优化与流线设计*

**本阶段案例：**  
[2.1 彩色平面图](#21-彩色平面图-colored-floor-plan) • [2.2 景观分区图](#22-景观分区图-landscape-zoning-map) • [2.3 城市肌理风格化](#23-城市肌理风格化-urban-fabric-stylization) • [2.4 总平面图转照片级鸟瞰](#24-总平面图转照片级鸟瞰) • [2.5 办公室布局规划](#25-办公室布局规划)

### 2.1 彩色平面图 (Colored Floor Plan)

#### 输入：CAD平面图

![CAD平面图输入](./assets/cases/2.1-cad-to-topview/input.jpg)

[↑ 回到顶部](#目录)

---

#### 输出：自然语言提示词

![自然语言输出](./assets/cases/2.1-cad-to-topview/output-natural-cn.jpg)

**房间标注：**
- 必须标注平面图中的**每一个**空间（例如："客厅"、"次卧室1"、"储藏间"）。
- 如果原始CAD图纸包含文字或标注，**必须完全移除**，并用新的、清晰的、专业的标签替换。
- 不要将新标签覆盖在旧标签上。

**输出要求：**
- **视图**：正交俯视图。
- **风格**：照片级真实感，自然光照。

**提示词：**
```
将提供的CAD平面图转换为照片级真实的彩色俯视图，用于客户演示。添加真实家具、清晰的房间标签，以及适合每个空间的材质地面。使用柔和的自然光照,保持建筑准确性。

房间标签语言：所有房间标签必须使用中文。

重要：严格遵循输入的平面图。不要添加原CAD图中没有的任何物品。不要删减或遗漏原图中出现的任何物品。保持准确的房间数量、家具位置和空间布局。
```

[↑ 回到顶部](#目录)

---

#### 输出：JSON结构化提示词

![JSON提示词输出](./assets/cases/2.1-cad-to-topview/output-json-cn.jpg)

**详细JSON提示词：**

> **为什么使用JSON?** JSON擅长定义**结构化关系、验证规则和约束**,这是自然语言无法精确表达的。重点不在于重复尺寸（这些都是估计值），而在于**在关键处强制精确性**:计数、独立性、类型和禁止项。

**🔧 新CAD图纸的JSON生成器：**

一张新的CAD平面图？我们创建了一个**可复用的JSON生成器**来自动化JSON创建过程。这个元提示词模板可以分析任何CAD图纸（住宅、商业或公共空间），并按照我们的格式生成标准化的JSON提示词。

**如何使用：**
1. 将您的CAD平面图上传到Vision AI（如Gemini Pro Vision, GPT-4 Vision, Claude 3.5 Sonnet）
2. 复制并粘贴JSON生成器提示词模板（见下文）
3. AI将系统地扫描您的平面图并输出完整的JSON提示词
4. 审查并使用生成的JSON进行可视化任务

**优势：**
- ✅ 确保完整的房间覆盖（无遗漏空间）
- ✅ 自动执行唯一命名标准
- ✅ 应用约束导向的方法
- ✅ 减少人工分析错误
- ✅ 适用于住宅、商业和公共空间

<details>
<summary>📋 点击查看JSON生成器提示词模板</summary>

复制整个提示词并与您的CAD平面图一起使用：

```markdown
# CAD平面图JSON提示词生成器

> **用途**: 分析上传的CAD平面图并生成标准化的JSON提示词。

## Vision AI指令

你是一位专业的建筑分析师。**详尽分析**上传的CAD平面图，并生成一个结构化的JSON提示词，用于将其转换为照片级真实的彩色俯视图。

### 1. 完整空间分析

按顺序执行以下扫描程序：

#### A. 网格扫描法
- 将平面图划分为3×3网格
- 系统性扫描每个网格单元
- 识别所有封闭或半封闭空间

#### B. 墙体追踪法
- 沿外围墙体顺时针追踪
- 识别每个被墙体围合的空间
- 包括小房间（储藏间、衣帽间、客卫）

#### C. 功能空间检查单（通用）
验证你已识别所有适用类别：

**对于任何空间类型：**
- [ ] 主要功能区
- [ ] 服务/支持区（厨房、卫生间、清洁间）
- [ ] 储藏空间（衣柜、设备间、仓库）
- [ ] 流线空间（入口、大堂、走廊、楼梯）
- [ ] 公用/机电空间（设备间、机房）
- [ ] 室外/半室外空间（阳台、露台、庭院）

**空间类型示例：**
- 住宅：客厅、卧室、卫生间
- 商业：工位、办公室、会议室、茶水间
- 零售：销售区、试衣间、库房
- 酒店：客房、大堂、餐厅、健身房
- 公共：等候区、服务台、卫生间、展厅

#### D. 内置元素检查单
- [ ] 地面固定装置
- [ ] 墙面固定装置（吊柜）
- [ ] 建筑凹槽（步入式衣帽间）
- [ ] 洁具

### 2. 房间命名标准

**唯一命名规则**: 同类型房间必须有唯一编号：
- ✅ 正确："次卧室1"、"次卧室2"、"储藏间1"
- ❌ 错误："次卧室"、"次卧室"（重复）

### 3. 关键规则

1. **禁止估计尺寸**: 不要包含"120x60cm"等尺寸
2. **禁止颜色代码**: 不要包含"#D4B896"等代码
3. **专注于约束**: 使用 `independence_rule`, `COUNT_CRITICAL`, `separation_rule`
4. **Task字段**: 必须明确提到"上传的"

### 4. 输出格式

提供：
1. 简要分析摘要（总房间数、类别）
2. 代码块中的完整JSON提示词

使用下方的JSON结构规范。

**现在分析上传的CAD并生成JSON提示词。**
```

</details>

<details>
<summary>点击展开完整JSON规格</summary>

```json
{
  "task": "将上传的CAD平面图转换为照片级真实的彩色俯视图",
  "input_specification": {
    "source": "上传的CAD图纸",
    "constraint": "必须使用上传的图片作为唯一空间参考",
    "prohibition": "禁止生成替代布局",
    "verification": "输出布局必须精确匹配输入"
  },
  "project_type": "residential_apartment",
  "input_analysis": {
    "total_rooms": 15,
    "total_furniture_count": 28,
    "total_fixtures": 7,
    "architectural_features": 2,
    "empty_spaces": 2
  },
  "output_requirements": {
    "view_type": "orthographic_top_down",
    "style": "photorealistic",
    "aspect_ratio": "match_input",
    "lighting": "natural_daylight_soft_shadows",
    "label_language": "chinese",
    "labeling_policy": {
      "coverage": "ALL_defined_spaces_MUST_be_labeled",
      "existing_text": "REMOVE_original_CAD_text_and_REPLACE_with_new_labels",
      "style": "clear_sans_serif_text_centered_in_room"
    }
  },
  "architectural_features": [
    {
      "feature_id": "walk_in_closet",
      "location": "master_bedroom",
      "category": "ARCHITECTURAL_not_furniture",
      "rendering_rule": "显示为带开口的嵌入式空间,不是独立柜体",
      "DO_NOT_render_as": [
        "衣柜",
        "柜子",
        "大衣柜",
        "衣柜家具"
      ]
    },
    {
      "feature_id": "kitchen_upper_cabinets",
      "location": "kitchen",
      "category": "ARCHITECTURAL_not_furniture",
      "rendering_rule": "墙面安装的吊柜,俯视图中可见"
    }
  ],
  "rooms": [
    {
      "id": "living_room",
      "label": "客厅",
      "flooring_material": "浅色橡木地板",
      "furniture_list": [
        {
          "item": "转角沙发",
          "configuration": "L型",
          "quantity": 1
        },
        {
          "item": "贵妃椅",
          "quantity": 1,
          "independence_rule": "必须与转角沙发分离",
          "placement_rule": "倾斜摆放",
          "CRITICAL": "明显独立的倾斜件"
        },
        {
          "item": "茶几",
          "quantity": 1,
          "material": "木质"
        },
        {
          "item": "圆形矮凳",
          "quantity": 2,
          "shape": "圆形",
          "independence_rule": "与茶几区分",
          "COUNT_CRITICAL": "精确2个_独立圆形件_都可见"
        },
        {
          "item": "电视柜",
          "quantity": 1,
          "material": "木质"
        },
        {
          "item": "地毯",
          "quantity": 1
        }
      ]
    },
    {
      "id": "dining_area",
      "label": "餐厅",
      "flooring_material": "瓷砖",
      "furniture_list": [
        {
          "item": "餐桌",
          "quantity": 1,
          "seating_capacity": 8,
          "material": "木质"
        },
        {
          "item": "餐椅",
          "quantity": 8,
          "arrangement": "长边各4把",
          "COUNT_CRITICAL": "精确8把椅子_全部可见"
        }
      ]
    },
    {
      "id": "kitchen",
      "label": "厨房",
      "flooring_material": "瓷砖_与餐厅匹配",
      "furniture_list": [
        {
          "item": "厨房岛台",
          "quantity": 1,
          "countertop_material": "白色石英石"
        },
        {
          "item": "吧台椅",
          "quantity": 4,
          "placement": "沿岛台",
          "COUNT_CRITICAL": "精确4把_全在岛台"
        }
      ],
      "fixtures": [
        {
          "item": "水槽",
          "quantity": 1,
          "type": "台下盆"
        },
        {
          "item": "灶台",
          "quantity": 1
        }
      ]
    },
    {
      "id": "master_bedroom",
      "label": "主卧室",
      "flooring_material": "木地板_与客厅匹配",
      "furniture_list": [
        {
          "item": "床",
          "type": "大床",
          "quantity": 1
        },
        {
          "item": "床头柜",
          "quantity": 2,
          "placement": "对称置于床两侧",
          "COUNT_CRITICAL": "精确2个_两侧各1"
        },
        {
          "item": "座椅",
          "quantity": 1,
          "location": "床尾"
        }
      ],
      "architectural_reference": "包含步入式衣帽间"
    },
    {
      "id": "bedroom_2",
      "label": "次卧室1",
      "flooring_material": "木地板_与客厅匹配",
      "furniture_list": [
        {
          "item": "单人床",
          "quantity": 1
        },
        {
          "item": "书桌",
          "quantity": 1
        },
        {
          "item": "书桌椅",
          "quantity": 1
        },
        {
          "item": "衣柜",
          "quantity": 1,
          "type": "独立式家具_非建筑"
        }
      ]
    },
    {
      "id": "master_bathroom",
      "label": "主卫生间",
      "flooring_material": "大理石纹瓷砖",
      "fixtures": [
        {
          "item": "浴缸",
          "quantity": 1
        },
        {
          "item": "淋浴房",
          "quantity": 1,
          "separation_rule": "与浴缸分离_不组合",
          "CRITICAL": "两个独立洁具_淋浴和浴缸"
        },
        {
          "item": "马桶",
          "quantity": 1
        },
        {
          "item": "洗手台",
          "sink_count": 2,
          "type": "双盆台",
          "COUNT_CRITICAL": "精确2个洗手盆"
        }
      ],
      "total_fixture_verification": 4
    },
    {
      "id": "secondary_bathroom",
      "label": "卫生间2",
      "flooring_material": "瓷砖",
      "fixtures": [
        {
          "item": "淋浴间",
          "quantity": 1,
          "NO_BATHTUB": true,
          "CRITICAL": "仅淋浴_此卫生间绝对没有浴缸"
        },
        {
          "item": "马桶",
          "quantity": 1
        },
        {
          "item": "洗手台",
          "sink_count": 1,
          "type": "单盆",
          "COUNT_CRITICAL": "精确1个洗手盆_不是2个"
        }
      ],
      "total_fixture_verification": 3
    },
    {
      "id": "entrance",
      "label": "玄关",
      "flooring_material": "瓷砖_与厨房匹配",
      "furniture_list": [],
      "usage_note": "流线空间_极少或无家具"
    },
    {
      "id": "storage_1",
      "label": "储藏间1",
      "flooring_material": "瓷砖_与餐厅匹配",
      "furniture_list": [],
      "usage": "储藏功能"
    },
    {
      "id": "powder_room",
      "label": "客卫",
      "flooring_material": "瓷砖",
      "fixtures": [
        {
          "item": "马桶",
          "quantity": 1
        },
        {
          "item": "洗手台",
          "sink_count": 1,
          "type": "小型单盆"
        }
      ],
      "note": "访客卫生间"
    },
    {
      "id": "bathroom_1",
      "label": "卫生间1",
      "flooring_material": "瓷砖",
      "fixtures": [
        {
          "item": "淋浴间",
          "quantity": 1
        },
        {
          "item": "马桶",
          "quantity": 1
        },
        {
          "item": "洗手台",
          "sink_count": 1,
          "type": "单盆"
        }
      ]
    },
    {
      "id": "bedroom_3",
      "label": "次卧室2",
      "flooring_material": "木地板_与客厅匹配",
      "furniture_list": [
        {
          "item": "单人床",
          "quantity": 1
        },
        {
          "item": "书桌",
          "quantity": 1
        },
        {
          "item": "书桌椅",
          "quantity": 1
        },
        {
          "item": "衣柜",
          "quantity": 1,
          "type": "独立式"
        }
      ]
    },
    {
      "id": "ensuite_bathroom",
      "label": "次卫",
      "flooring_material": "瓷砖",
      "fixtures": [
        {
          "item": "淋浴间",
          "quantity": 1,
          "NO_BATHTUB": true
        },
        {
          "item": "马桶",
          "quantity": 1
        },
        {
          "item": "洗手台",
          "sink_count": 1,
          "type": "单盆"
        }
      ],
      "note": "次卧室2的私人卫生间"
    },
    {
      "id": "storage_2",
      "label": "储藏间2",
      "flooring_material": "瓷砖",
      "furniture_list": [],
      "usage": "储藏功能"
    }
  ],
  "empty_spaces": [
    {
      "id": "balcony",
      "label": "阳台",
      "flooring_material": "复合地板",
      "furniture_list": [],
      "plants": [],
      "decorative_items": [],
      "CRITICAL_CONSTRAINT": "必须保持完全空置",
      "absolute_prohibition": [
        "禁止_家具",
        "禁止_植物",
        "禁止_花盆",
        "禁止_装饰物品",
        "禁止_任何物品"
      ],
      "rendering_rule": "仅显示地面_其他什么都不要"
    }
  ],
  "strict_constraints": {
    "count_accuracy": {
      "dining_chairs": {
        "exact": 8,
        "verification": "清点全部8把可见"
      },
      "bar_stools": {
        "exact": 4,
        "verification": "全部4把在岛台"
      },
      "round_ottomans": {
        "exact": 2,
        "verification": "两个可区分"
      },
      "bedside_tables": {
        "exact": 2,
        "verification": "两侧各一"
      },
      "master_bath_sinks": {
        "exact": 2,
        "verification": "双台盆"
      },
      "secondary_bath_sinks": {
        "exact": 1,
        "verification": "仅单盆"
      }
    },
    "independence_requirements": [
      {
        "item": "贵妃椅",
        "must_be_separate_from": "转角沙发",
        "visual_proof": "明显独立的倾斜件"
      },
      {
        "item": "圆形矮凳",
        "must_be_separate_from": "茶几",
        "visual_proof": "两个独立圆形"
      },
      {
        "item": "主卫淋浴",
        "must_be_separate_from": "浴缸",
        "visual_proof": "两个独立洁具_不组合"
      }
    ],
    "categorical_distinctions": {
      "walk_in_closet": "建筑特征_非家具",
      "bedroom_wardrobes": "家具_非建筑",
      "kitchen_upper_cabinets": "建筑_非家具"
    },
    "fixture_clarity": {
      "master_bathroom": "同时有_浴缸和独立淋浴",
      "secondary_bathroom": "仅淋浴_绝对没有浴缸",
      "ensuite_bathroom": "仅淋浴_没有浴缸"
    },
    "prohibition_list": {
      "no_added_decorative_items": [
        "植物",
        "花瓶",
        "艺术品",
        "雕塑",
        "抱枕",
        "餐具摆设",
        "书籍",
        "配饰"
      ],
      "empty_space_enforcement": {
        "balcony": "绝对不允许任何物品",
        "entrance": "仅极少或空置"
      }
    },
    "rendering_validation": {
      "no_added_items_rule": "严格仅渲染CAD符号对应物品",
      "no_removed_items_rule": "所有CAD元素必须出现",
      "no_merged_elements_rule": "独立物品保持独立",
      "no_hallucinated_features_rule": "不臆造建筑元素"
    }
  },
  "verification_checklist": {
    "room_count": 15,
    "furniture_count": 28,
    "fixture_count": 7,
    "architectural_features": 2,
    "empty_spaces": 2,
    "mandatory_verifications": [
      "步入式衣帽间_作为建筑非家具",
      "厨房吊柜_可见",
      "阳台_完全空置已验证",
      "贵妃椅_独立且倾斜",
      "2个矮凳_都独立可见",
      "4把吧台椅_全在岛台",
      "8把餐椅_全部存在",
      "2个床头柜_对称",
      "主卫_淋浴和浴缸都有且独立",
      "主卫_2个洗手盆已验证",
      "次卫2_仅淋浴无浴缸已确认",
      "次卫2_仅1个洗手盆已验证",
      "次卫_仅淋浴无浴缸"
    ]
  }
}
```

</details>

[↑ 回到顶部](#目录)

---

#### 💡 使用技巧

- **推荐迭代生成**：自然语言提示词最适合迭代方式。先生成2-3个变体，选择最佳效果，再用简单的图像编辑工具（Photoshop、Figma、Canva）微调细节。这种混合工作流往往比试图用单个提示词完美化所有细节效果更好。
- **检查JSON完整性**：提交前确保CAD图中所有房间都包含在JSON内。遗漏的家具（如矮凳或贵妃椅）不会出现在输出中。
- **材质一致性**：保持连通空间的地面材质一致（如厨房+餐厅+玄关），视觉流畅。
- **房间标签清晰度**：JSON提示词产生更精确的文字渲染。如果自然语言标签不清晰，使用JSON规格。
- **风格变化**：要改变设计风格，修改：
  - 家具材质（如 `"亚麻布艺"` → `"皮革"`）
  - 地板颜色（如 `"#D4B896"` → 更深/更浅色调）
  - 整体氛围（`"现代住宅"` → `"奢华"`, `"极简"`）

[↑ 回到顶部](#目录)

---

### 2.2 景观分区图 (Landscape Zoning Map)

#### 输入

![输入图片](./assets/cases/2.2-landscape-zoning-map/input.jpg)

#### 输出

![输出图片](./assets/cases/2.2-landscape-zoning-map/output.jpg)

**提示词：**
```
场地分析图。在总平面图上叠加颜色编码的分区：绿色代表'公共公园'，蓝色代表'水景'，黄色代表'住宅区'。使用填充图案和图例。矢量图形风格。
```

[↑ 回到顶部](#目录)

---

### 2.3 城市肌理风格化 (Urban Fabric Stylization)

#### 输入

![输入图片](./assets/cases/2.3-urban-fabric-stylization/input.jpg)

#### 输出

![输出图片](./assets/cases/2.3-urban-fabric-stylization/output.jpg)

**提示词：**
```
城市图底关系图（诺利地图） 。将所有建筑渲染为实心黑色体块，所有街道/开放空间 渲染为纯白色。高对比度，抽象地图风格。移除所有植被和车辆。
```

[↑ 回到顶部](#目录)

---

### 2.4 总平面图转照片级鸟瞰

#### 阶段 1：清晨

![输入图片](./assets/cases/2.4-site-plan-to-aerial/input.jpg)
*输入：总平面图*

![输出图片](./assets/cases/2.4-site-plan-to-aerial/output.jpg)
*输出：清晨鸟瞰图*

**提示词：**
```
使用上传的总平面图作为源文件，生成一张照片级渲染图，展示该场地在现实中对普通观察者的外观。将平面视图转换为三维逼真可视化，使用真实世界的材质、纹理和自然光照渲染住宅建筑、水景和公共公园区域。将平面图中显示的等高线建模为实际的地形高程变化，在景观中创造可见的山丘、斜坡和地貌变化。将视点定位为直接位于场地中心上方的居中鸟瞰视角，仿佛是无人机从头顶拍摄的。应用适合清晨时分的低角度阳光光照条件，创造相应的阴影、温暖的光质和具有黎明照明特征的大气效果。将场景呈现为一张逼真的照片级图像，清晰地传达建成后的开发项目外观。
```

#### 阶段 2：夜间照明迭代

![输出图片夜间](./assets/cases/2.4-site-plan-to-aerial/output-night.jpg)
*输出：夜间照明效果*

**提示词：**
```
使用之前生成的清晨渲染图作为底图，将光照条件从清晨转换为夜间。移除自然日光照明，替换为夜间照明场景。添加适合场地元素的人工照明，包括透过窗户可见的室内建筑灯光、住宅结构的室外建筑照明、道路和公共公园区域的景观照明，以及水景的重点照明。保持所有空间配置、材质、纹理、地形和视角与当前图像完全一致，仅修改一天中的时间和相应的光照条件，以表现晚间照明效果。
```

#### 💡 技巧
*   **持续迭代：** Nano Banana Pro 支持持续迭代。您可以将上一次生成的输出直接用作下一步的输入，无需重新上传，从而实现逐步优化（例如：更改一天中的时间）。

[↑ 回到顶部](#目录)

---

### 2.5 办公室布局规划

#### 输入

![输入图片](./assets/cases/2.5-office-layout-planning/input.jpg)

#### 输出

![输出图片](./assets/cases/2.5-office-layout-planning/output.jpg)

**提示词：**
```
使用上传的显示原始建成状态的空白平面图，保留所有现有的建筑结构，包括外墙、承重墙、所有门洞和所有窗户位置，完全按照显示的内容，不做任何修改。设计一个符合工作场所设计人体工程学标准的完整办公室布局。空间规划必须包括以下所需的功能区域：总经理办公室，位于具有适当地位和隐私的位置；高级管理层的行政办公室；以及财务办公室，配置为相对封闭并与其他工作区域独立。在其余区域安排开放式工作站，遵循办公桌尺寸、通行间隙和工位之间视觉隐私的人体工程学间距标准。优化工作站布置，以创建高效的通行路径，最大限度地减少穿过工作区的交叉交通。指定并布置协作区域，其位置应支持团队互动而不干扰专注工作区。所有家具放置必须符合人体工程学原则，包括适当的桌子高度、椅子间隙和设备可及性。将结果呈现为完整的办公室平面图，以专业的建筑绘图风格显示封闭办公室的隔墙、工作站布局和所有家具布置，具有适当的线宽和图形惯例。
```

[↑ 回到顶部](#目录)

---

<a id="technical"></a>

## 🔧 技术转视觉
*从线稿到三维表现*

**本阶段案例：**  
[3.1 平面图转轴测图](#31-平面图转轴测图-plan-to-isometric) • [3.2 衣柜内部结构可视化](#32-衣柜内部结构可视化-wardrobe-interior)

### 3.1 平面图转轴测图 (Plan to Isometric)

![输入图片](./assets/cases/3.1-plan-to-isometric/input.jpg)
*输入：二维平面图*

![输出图片](./assets/cases/3.1-plan-to-isometric/output.jpg)
*输出：三维轴测图*

**提示词：**
```
将此二维平面图转换为三维等距建筑图。将墙壁拉伸至一致的高度。应用带有柔和环境光遮蔽阴影的"蓝图风格"。
```

#### 阶段 2：反向视角

![输出图片反向](./assets/cases/3.1-plan-to-isometric/output-reverse.jpg)
*输出：反向轴测视图*

**提示词：**
```
使用之前生成的三维轴测建筑图作为参考，创建一个从相反视角（绕垂直轴旋转180度）的新视图。保持相同的拉伸高度、渲染风格、环境光遮蔽阴影以及所有建筑元素与原图完全一致。仅改变相机视点，从反向视角展示建筑，揭示在第一视图中被隐藏的相反立面和空间关系。
```



#### 💡 技巧

**1. 风格变体 (Style Variations)**
将提示词中的 **'blueprint style'** 替换为：

*   **'wireframe style' (线框风格)**: 仅显示边缘线条,无表面填充,展示结构逻辑。
*   **'technical line drawing style' (技术线图风格)**: 精确的黑白线条绘制,不同线宽表示层级,类似施工图。
*   **'flat color blocking with ambient occlusion' (平面色块+环境光遮蔽)**: 每个体块用单一颜色填充,保留阴影深度感。
*   **'watercolor rendering style' (水彩渲染风格)**: 柔和的水彩质感,边缘略带晕染效果,艺术化表达。
*   **'hand-drawn sketch style with hatching' (手绘素描风格+阴影线)**: 模拟手工绘制,用平行线表示阴影和材质。
*   **'physical model photography style' (实体模型摄影风格)**: 模拟白色卡纸或木材制作的实体建筑模型。
*   **'ghost render with transparency' (半透明幽灵渲染)**: 外墙半透明,可透视内部空间布局。
*   **'material study render' (材质研究渲染)**: 精确显示不同材料(混凝土/木材/玻璃)的真实质感。
*   **'diagram style with color-coded functional zones' (图解风格+功能分区色标)**: 不同功能空间用不同颜色区分,带图例说明。
*   **'clay render style' (粘土渲染风格)**: 柔和的哑光表面，类似于粘土模型。

**2. 视角变体 (Viewpoint Variations)**

*   **90度 (侧面):** `"rotated 90 degrees clockwise/counterclockwise"`
*   **45度 (斜角):** `"rotated 45 degrees to show the adjacent corner perspective"`
*   **鸟瞰俯视:** `"from a higher bird's eye view angle looking down at 60 degrees"`

[↑ 回到顶部](#目录)

---

### 3.2 衣柜内部结构可视化 (Wardrobe Interior)

智能分析并展示关闭状态衣柜的内部收纳系统，支持迭代优化调整。

#### 阶段 1：内部结构展示

#### 输入：关闭状态的衣柜

![输入图片](./assets/cases/3.2-wardrobe-interior/input.jpg)

#### 输出：内部收纳结构展示

![输出图片1](./assets/cases/3.2-wardrobe-interior/output1.jpg)

**提示词：**
```
将此衣柜转换为内部结构展示图，遵循以下严格规则：

1. 结构保真：完全保留参考图片中的隔间、门板、抽屉的精确数量和位置。禁止更改、合并或增加任何分隔。

2. 展示内部：
   - 移除所有柜门以暴露内部储物空间
   - 将所有抽屉部分拉出以展示其内容物
   - 保持原始比例和对齐方式

3. 智能填充：用与衣柜风格相匹配的真实收纳物品（衣物、床品、配饰）填充展示的内部空间。

4. 一致性：保持与原图相同的相机角度、光照、房间环境和材质饰面。
```

#### 阶段 2：迭代优化

#### 输出：修改后布局（右上柜改为挂衣区）

![输出图片2](./assets/cases/3.2-wardrobe-interior/output2.jpg)

**提示词（基于 Output 1）：**
```
将右上柜改成衣架式，保持右下柜是抽屉不变。
```

#### 💡 技巧

**结构保真关键原则：**

| 指令 | 作用 |
|-----|------|
| `"完全保留精确数量"` | 防止 AI 自行修改分隔数量 |
| `"禁止更改、合并或增加"` | 明确禁止任何结构变更 |
| `"将所有抽屉部分拉出"` | 确保抽屉展示内部内容 |
| `"保持原始比例"` | 保持比例一致，便于对比 |

**迭代优化策略：**
本案例展示了**两阶段工作流**：
1. **阶段一**：在严格保持结构保真的前提下生成初始内部展示图
2. **阶段二**：使用简洁精确的指令进行针对性修改

[↑ 回到顶部](#目录)

---



<a id="material"></a>

## 🎨 材质软装
*材质与软装设计*

**本阶段案例：**  
[4.1 材质替换](#41-材质替换-material-swap) • [4.2 风格迁移](#42-风格迁移-style-transfer) • [4.3 家具替换](#43-家具替换-furniture-replacement) • [4.4 清空房间](#44-清空房间-declutter--empty-room) • [4.5 空房间自动布置](#45-空房间自动布置-auto-furnish-empty-room)

---

### 4.1 真实材质替换 (Realistic Material Replacement)

#### 输入

![材质样本](./assets/cases/4.1-material-swap/input-material.jpg)
*输入 1：材质样本*


![目标场景](./assets/cases/4.1-material-swap/input-scene.jpg)
*输入 2：目标场景*

#### 输出

![输出图片](./assets/cases/4.1-material-swap/output.jpg)
*输出：材质已替换*

**提示词：**
```
使用第一张上传的图片作为源材质样本，第二张上传的图片作为目标场景，将目标场景中的 [指定元素：地板/墙砖/墙漆/柜体表面/台面等] 替换为源样本中显示的材质图案和纹理。应用源材质时，保持目标场景现有的透视变形、光照条件、阴影、反射和表面几何形状。保持目标场景中的所有其他元素完全不变，包括家具摆放、空间配置、建筑特征以及任何未指定进行材质替换的元素。确保替换后的材质自然地响应场景的光照环境，并与周围表面无缝融合。
```

#### 💡 技巧

**上传顺序说明：**
1. **第一张图：** 材质样本照片（地板花色、瓷砖纹理、油漆色样、柜体表面处理等）
2. **第二张图：** 需要替换材质的实景效果照片

**填写参数说明：**
- `地板` / `flooring`
- `墙砖` / `wall tiles`
- `墙漆/墙面` / `wall paint/wall surface`
- `柜体表面/柜门` / `cabinet surfaces/cabinet doors`
- `台面` / `countertops`

[↑ 回到顶部](#目录)

---

### 4.2 风格迁移 (Style Transfer)

#### 输入

![风格参考](./assets/cases/4.2-style-transfer/input-style.jpg)
*输入 1：风格参考*

![目标场景](./assets/cases/4.2-style-transfer/input-scene.jpg)
*输入 2：目标场景*

#### 输出

![输出图片](./assets/cases/4.2-style-transfer/output.jpg)
*输出：风格迁移后*

**提示词：**
```
使用第一张上传的图片作为风格参考，第二张上传的图片作为目标空间场景，将参考图片的视觉风格特征迁移到目标场景。应用参考图片的美学特质，包括色彩搭配、色调关系、材质处理方式、光照氛围、纹理渲染风格和装饰语汇到目标场景，同时保持目标场景的空间配置、建筑结构、家具布局和功能组织。维持目标场景的透视、比例和空间关系完全不变。最终结果应体现目标空间通过参考风格的视觉语言和美学感受进行重新诠释。
```

[↑ 回到顶部](#目录)

---

#### 💡 技巧

**上传顺序说明：**
1. **第一张图：** 风格参考照片
2. **第二张图：** 目标空间场景照片

**风格迁移 vs 材质替换的区别：**
- **材质替换**：精确替换特定元素的表面材质
- **风格迁移**：改变整个场景的视觉美学和表达方式

[↑ 回到顶部](#目录)

---

### 4.3 家具替换 (Furniture Replacement)

#### 输入

![家具参考](./assets/cases/4.3-furniture-replacement/ref-furniture.jpg)
*输入 1：家具参考*

![目标场景](./assets/cases/4.3-furniture-replacement/target-scene.jpg)
*输入 2：目标场景*

#### 输出

![输出图片](./assets/cases/4.3-furniture-replacement/output.jpg)
*输出：家具替换后*

**提示词：**
```
使用第一张上传的图片作为家具参考，第二张上传的图片作为目标室内场景，将目标场景中的 [指定家具：沙发/茶几/床/餐桌/椅子/柜体/边几等] 替换为参考图片中显示的家具。将参考家具放置在与原家具相同的空间位置，匹配目标场景的透视角度和视点位置。适当缩放参考家具以适应空间环境，保持与周围元素的比例关系。将目标场景现有的光照条件、阴影和反射应用到新放置的家具上，确保自然融合。保持目标场景中的所有其他元素完全不变，包括墙面、地板、其他家具、装饰物品、建筑特征和空间配置。
```

[↑ 回到顶部](#目录)

---

### 4.4 清空房间 (Declutter / Empty Room)

#### 输入

![输入图片](./assets/cases/4.4-declutter-empty-room/input.jpg)

#### 输出

![输出图片](./assets/cases/4.4-declutter-empty-room/output.png)

**提示词：**
```
房地产照片编辑。移除房间内所有的家具、箱子和杂物。展示带有裸露墙壁和地面的干净空房间。自动填充移除家具后的地面纹理。
```

#### 💡 技巧

- 此提示词非常适合房地产挂牌展示，用于展示杂乱空间的潜力
- 在原始照片光线良好的情况下效果最佳
- AI 会尝试保留建筑特征（窗户、门、壁炉）
- 为获得最佳效果，确保原始照片有可见的地面和墙面区域作为参考

> ⚠️ **已知限制**：在本示例中，AI 错误地将左侧墙上的一个开口填平了。请始终检查 AI 结果的结构准确性。

[↑ 回到顶部](#目录)

---

### 4.5 空房间自动布置 (Auto-Furnish Empty Room)

> 将空房间转换为完全布置好的室内空间。一张输入照片，无限设计可能。

#### 输入

![空房间](./assets/cases/4.5-auto-furnish-empty-room/input.png)
*输入：空房间照片*

#### 输出示例

![男孩卧室](./assets/cases/4.5-auto-furnish-empty-room/output-boys-bedroom.jpg)
*示例1：10岁男孩卧室 - 蓝白色系，活泼俏皮*

![主卧](./assets/cases/4.5-auto-furnish-empty-room/output-master-bedroom.jpg)
*示例2：法式轻奢主卧 - 奶油色系*

![客厅](./assets/cases/4.5-auto-furnish-empty-room/output-living-room.jpg)
*示例3：现代客厅 - 整墙电视柜*

**提示词模板：**
```
根据我指定的风格重新设计这个房间。以专业室内设计师的身份，将这个空间彻底改造，如同从空壳开始设计。

关键要求 - 必须保持上传照片中的：
- 完全相同的相机角度和透视
- 相同的观看位置和视野范围
- 照片中显示的房间比例

可以修改的内容：
- 所有家具
- 墙面颜色/饰面/处理
- 天花板设计和处理
- 地面材料和颜色
- 窗帘处理（窗帘、百叶窗）
- 灯具照明
- 内置功能（搁架、壁炉装饰、柜体）
- 所有装饰元素

不允许的结构性改变：
- 不要添加、移除或移动窗户
- 不要添加、移除或移动门
- 不要改变墙体位置

运用专业设计原则。创造杂志级别的效果。

我想要的房间用途和风格：[指定房间类型、色彩方案和设计风格]
```

#### 💡 技巧

**如何编写有效的个性化指令：**

用以下要素构建你的需求：
1. **房间类型**：卧室、客厅、书房、餐厅
2. **色彩方案**：具体颜色（蓝白色系、奶油色、大地色系）
3. **设计风格**：现代、北欧、法式轻奢、工业风
4. **特殊功能**（可选）：电视墙、学习区、阅读角

**示例个性化指令：**
- `10岁男孩卧室：蓝白色系，活泼俏皮风格`
- `温馨主卧室，奶油色调，法式轻奢风格`
- `现代风格公寓客厅，配有整墙电视柜`

[↑ 回到顶部](#目录)

---

<a id="rendering"></a>

## 🖼️ 场景渲染
*最终渲染与效果图*

**本阶段案例：**  
[5.1 白模转照片级渲染](#51-白模转照片级渲染-clay-to-photorealistic) • [5.2 光影修复与强化](#52-光影修复与强化-lighting-enhancement) • [5.3 色调统一与色彩校正](#53-洗图2色调统一与色彩校正)

### 5.1 白模转照片级渲染 (Clay to Photorealistic)

将白模/灰模3D渲染图智能转换为照片级可视化效果，支持材质自动分配和风格控制。提供两种方式：**文字指定风格** 或 **图片参考风格**。

---

#### 方案 A：文字指定风格

*使用文字描述来定义目标风格和材质。*

**输入：**

![输入图片](./assets/cases/5.1-clay-to-render/input.jpg)
*白模/灰模渲染图*

**输出：**

![输出奶油色](./assets/cases/5.1-clay-to-render/output-cream.jpg)
*奶油色轻奢风*

**提示词：**
```
将此白模/灰模渲染图转换为照片级建筑可视化效果，遵循以下严格分析规则：

1. 几何保真：分析并完全保留输入模型的精确3D几何形状、透视角度、光照方向和空间比例。禁止修改任何建筑元素、家具形状或空间关系。

2. 智能材质分配：根据可见的形体和场景上下文，智能分配适当的材质：
   - 墙面 → [指定：如 白色肌理漆 / 清水混凝土 / 木饰面板]
   - 地面 → [指定：如 浅色橡木地板 / 大理石瓷砖 / 抛光混凝土]
   - 天花 → [指定：如 白色哑光 / 木梁结构 / 内嵌式造型]
   - 家具 → [指定：如 天然面料 / 皮革 / 混合材质]
   - 五金 → [指定：如 拉丝黄铜 / 哑光黑 / 镀铬]

3. 设计风格：[指定风格：如 现代简约 / 北欧 / 日式侘寂 / 工业loft / 法式轻奢]

4. 灯光氛围：应用能增强指定风格的照片级灯光。

5. 输出：高质量照片级室内渲染，保持与输入完全相同的相机角度和构图。
```

**常用风格关键词：**

| 风格 | 描述 |
|------|------|
| `现代简约` | 干净线条，中性色调 |
| `北欧` | 温暖木质，温馨氛围 |
| `日式侘寂` | 原始质感，大地色系 |
| `工业风` | 裸露砖墙，金属，混凝土 |
| `法式轻奢` | 奶油色调，优雅细节 |

---

#### 方案 B：图片参考风格

*使用现有室内照片作为风格参考。上传顺序：第一张 = 风格参考图，第二张 = 白模图。*

**输入 1 - 风格参考图：**

![风格参考](./assets/cases/5.1-clay-to-render/ref-dark-style.jpg)
*风格/材质参考图片*

**输入 2 - 白模图：**

![输入图片](./assets/cases/5.1-clay-to-render/input.jpg)
*白模/灰模渲染图（与方案 A 相同）*

**输出：**

![输出深色](./assets/cases/5.1-clay-to-render/output-dark.png)
*深色木质日式风（基于参考图生成）*

**提示词：**
```
使用第一张上传的图片作为风格/材质参考，第二张上传的图片作为白模/灰模源：

1. 几何来源：完全从白模（第二张图）提取所有3D几何形状、空间布局、家具摆放、相机角度和透视关系。禁止修改任何形状或位置。

2. 风格迁移：将参考图片（第一张图）的视觉风格、材质色板、配色方案、灯光氛围和设计语言应用到白模几何体上。

3. 材质映射：将风格参考中的材质智能映射到白模中的对应表面。

4. 照片级输出：生成最终渲染图，结合白模的精确空间结构与风格参考的美学质量。
```

[↑ 回到顶部](#目录)

---

### 5.2 光影修复与强化 (Lighting Enhancement)

增强室内渲染图的光照品质：强化灯具光晕、恢复暗部细节、优化光线衰减、提升空间层次。提供两种方法：**快速通用版**或**高级元提示词**（效果最佳）。

#### 输入

![输入图片](./assets/cases/5.2-lighting-enhancement/input.png)
*原始渲染图*

#### 输出

![输出图片](./assets/cases/5.2-lighting-enhancement/output.png)
*光影增强后（通用提示词）*

---

#### 方案 A：快速通用版

*适用于任何室内渲染图，无需修改。*

**提示词：**
```
增强这张室内渲染图的光照品质，同时严格保留所有几何形状、家具和设计元素：

自动光影分析与增强：
1. 分析所有可见光源，强化光晕并添加自然的光线扩散效果
2. 恢复暗部区域的细节同时保持画面深度
3. 应用真实的光线衰减——靠近光源的物体应明显更亮
4. 在天花板和墙面上添加微妙的环境光反射
5. 通过光影创建前景和背景之间清晰的明暗层次分离

严格保真：
- 保持精确的几何形状、颜色、材质和空间布局
- 不添加、移除或修改任何物体

输出：呈现自然且富有氛围感的专业摄影级灯光效果。
```

---

#### 方案 B：高级元提示词

*先让 AI 分析图片，再生成针对性提示词，效果最佳。*

![元提示词输出](./assets/cases/5.2-lighting-enhancement/output-meta.png)
*元提示词方案的最佳效果*

**第一步：** 使用元提示词生成定制化提示词：
```
分析这张室内渲染图，识别需要改进的具体光影问题：

第一步 - 诊断分析：
列出检测到的所有光影问题：
- 光源光晕质量（弱/强/自然）
- 阴影区域（过暗/细节丢失/可接受）
- 光线衰减（平淡/真实/过于戏剧化）
- 天花板亮度（过暗/平衡/过亮）
- 层次分离（平淡/适中/良好）
- 任何过曝或欠曝区域

第二步 - 生成定制提示词：
根据你的分析，生成一个针对性的光影增强提示词：
- 仅解决识别出的具体问题
- 优先解决影响最大的改进点
- 使用精确的技术语言
- 包含几何保真保护措施

输出格式：
## 检测到的光影问题：
[具体问题的要点列表]

## 定制增强提示词：
[针对此图片量身定制的可直接使用的提示词]
```

**第二步：** 复制 AI 生成的提示词，与图片一起使用。

> **💡 提示**：方案 B 可产生作品集/演示级别的最佳效果。


[↑ 回到顶部](#目录)

---

### 5.3 洗图2：色调统一与色彩校正
*Post-production 2: Tone Unification and Color Correction*

修复混合光照问题，统一色温，校正白平衡，同时保留原始细节。**三层提示词体系**适应不同用户需求。

#### 输入

![输入图片](./assets/cases/5.3-tone-unification/input.png)
*输入：混合光照（冷调窗光与暖调室内灯冲突）*

#### 输出选项A：快速修正（暖调方向）

![输出快速](./assets/cases/5.3-tone-unification/output-quick.png)
*AI 自动强化暖调氛围，同时消除色彩冲突*

#### 输出选项B：元提示词（中性方向）

![输出元提示词](./assets/cases/5.3-tone-unification/output-meta.png)
*用户指定的 4000K 中性白平衡，保留材质固有色*

---

#### Level 1：快速修正（AI 自动判断最佳色调）

适用场景：快速交图，让 AI 决定最佳调色方向。

```
使用上传的图片作为严格的参考底图。保持所有的家具、装饰、几何结构和细节完全不变。

首先分析这张渲染图的空间类型、设计风格和预期氛围。
然后识别当前色温的具体问题（如不协调的混合光照、局部色偏）。

重新渲染图像以统一光照色温，同时：
- 保留并强化原设计的氛围意图（如温馨住宅保持暖调，现代办公保持冷调）
- 仅消除不协调的色偏和混合光照冲突
- 确保最终色调既统一和谐，又能提升空间的设计表现力

不要将画面调成平庸的中性色调，而是调成最能展现本空间设计特色的色调。
```

---

#### Level 2：元提示词（AI 分析并生成定制指令）

适用场景：先理解色偏问题，再生成精准的修复方案。

**第一步：** 使用此元提示词分析图片：

```
你是一位专业的建筑可视化后期专家。请分析上传的渲染图，识别色温和白平衡的具体缺陷。
然后，根据你的分析编写一段**修改指令提示词**。

⚠️ **关键规则（Nano Banana Pro 专用）**：
1. **纯指令模式**：只写"要做什么修改"，禁止描述画面内容。
2. **光色分离**：明确区分"光照色温"和"物体固有色"。
   - ✅ 正确：中和画面中的冷色**光线**。
   - ❌ 错误：移除背景的蓝色（这会导致蓝色家具变色）。
3. **强制保真指令**：必须包含以下保护性指令：
   - "Do not alter the intrinsic color of any furniture or materials."
   - "Apply color correction ONLY to the lighting/atmosphere, NOT the objects."
```

**第二步：** 复制 AI 生成的提示词，与图片一起使用。

---

#### Level 3：手动精调（指定色温参数）

适用场景：专业后期师，已知明确需求。

```
使用上传的图片作为严格的参考底图。保持所有的家具、装饰、几何结构和细节完全不变。重新渲染图像以统一光照色温。消除原本混乱的混合光照，将整体色调统一为 [3000K / 4000K / 5000K / 6500K]。确保白平衡准确，色彩自然和谐。
```

| 色温值 | 名称 | 适用场景 |
|--------|------|----------|
| 2700K-3000K | 暖白光 | 卧室、餐厅、酒店 |
| 4000K | 自然白光 | 办公室、展厅、商业空间 |
| 5000K-6500K | 冷白光 | 医院、科技空间、展览馆 |

> **💡 提示**：先用 Level 1（快速修正），不满意再用 Level 2 了解问题，最后用 Level 3 精调。

[↑ 回到顶部](#目录)

---

### 5.4 日景转夜景
*Post-production 3: Atmospheric Lighting Change*

将日间建筑渲染图转换为具有定制照明效果的戏剧性夜景。

#### 输入

![输入图片](./assets/cases/5.4-day-to-night/input.jpg)

#### 输出

![输出图片](./assets/cases/5.4-day-to-night/output.png)

**提示词：**
```
现代当代别墅的写实夜景。建筑拥有大面积玻璃窗，散发出温暖诱人的室内光线(3000K)。深蓝色的暮光"蓝色时刻"天空，点缀着微弱的星星。室外花园照明照亮了景观。混凝土纹理可见但较暗。玻璃上以及可能在潮湿或抛光的地面上有室内灯光的反射。高对比度，电影感布光，建筑摄影风格。保持与输入图像完全一致的建筑结构和透视，仅改变光照和氛围为夜间。
```

> **💡 提示**：在提示词中使用 **"Blue Hour" (蓝色时刻)** 关键词，可以获得最迷人的夜空背景效果。

[↑ 回到顶部](#目录)

---


<a id="special"></a>

## ⚙️ 专项应用
*设计辅助与文档生成*

**本阶段案例：**  
[6.1 软装元素提取白板](#61-软装元素提取白板)

### 6.1 软装元素提取白板

从室内效果图中提取家具和装饰元素，生成专业的产品目录式白板 —— 非常适合采购清单和供应商询价。

#### 输入

![输入图片](./assets/cases/6.1-soft-furnishing-extraction/input.jpg)

#### 输出

![输出图片](./assets/cases/6.1-soft-furnishing-extraction/output.png)

**提示词：**
```
从这张室内效果图中提取家具和装饰元素。
创建一个高端产品目录风格的白板。

⚠️ 关键：禁止重复项目
- 每个独特物品只出现一次
- 例外：成对出现的物品（2盏配套台灯、2个床头柜）应同时展示

排除：
- 固定在墙上的柜子和搁架
- 固定的建筑元素
- 墙面板、地板、天花板

版式风格：
- 干净的白色背景
- 优雅的网格布局，间距充足
- 同类别物品尺寸一致
- 大件在上，小件在下

格式：
- 分类标题：家具 | 灯具 | 软装 | 装饰
- 顺序编号
- 正面视图

美学：高端室内设计目录，极简，精致。
```

> **💡 提示**：建议多次生成，选择最佳结果。小配件可能会遗漏，可单独请求补充提取。

[↑ 回到顶部](#目录)

---

## 📚 资源

- 📖 [CASE_TEMPLATE.md](./CASE_TEMPLATE.md) - 创建新案例的模板
- 🤝 [CONTRIBUTING.md](./CONTRIBUTING.md) - 如何贡献新案例

[↑ 回到顶部](#目录)

---

## 使用原则

本仓库鼓励学习、改编与协作。请注意：

- 本仓库中的 prompt 是**可用的工作模板**，而非万能解决方案
- AI 生成的内容应始终由专业设计师审核
- 强烈建议根据您的项目需求进行修改和调整

📖 **完整说明**：详见 [USAGE.zh-CN.md](./USAGE.zh-CN.md) 了解完整的使用原则和署名指南。

---

## 许可证

本项目采用 **知识共享署名 4.0 国际许可协议 (CC BY 4.0)** 进行许可。

您可以自由地共享和演绎本作品（包括商业目的），只需给出适当的署名。

有关完整的许可文本，请参阅[LICENSE](./LICENSE)或访问[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)。

## 联系方式 / Contact

维护者：[qzh3722@gmail.com](mailto:qzh3722@gmail.com)

[↑ 回到顶部](#目录)

---

<div align="center">

**Made with ❤️ for Designers**

Powered by **Gemini 3 Pro Image**

</div>
