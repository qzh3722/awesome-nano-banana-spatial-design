<div align="center">

![Awesome Nano Banana 空间设计Banner](./assets/images/banner.jpg)

# Awesome Nano Banana 空间设计

> 为空间设计师打造的 Gemini 3 Pro Image 专业提示词库
 
<!-- 语言切换 -->
[English](./README.md) | **简体中文**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## 🎯 快速导航

**跳转到工作流阶段：**  
[🎨 概念构思](#-概念构思) • [📐 空间规划](#-空间规划) • [🔧 技术转视觉](#-技术转视觉) • [🎨 材质软装](#-材质软装) • [🖼️ 场景渲染](#%EF%B8%8F-场景渲染) • [⚙️ 专项应用](#%EF%B8%8F-专项应用)

> **📌 免责声明**：本案例库中使用的所有图片仅用于教育和研究目的。输入图片来自公开的建筑图纸或专门为演示创建。本仓库不主张对引用图片的所有权，所有图片在非商业教育目的下按合理使用原则使用。

---

## 🎨 概念构思
*从零到创意方案*

**本阶段案例：**  
[1.1 手绘草图转渲染](#) • [1.2 多风格方案对比](#) • [1.3 概念拼贴板](#)

---

## 📐 空间规划
*布局优化与动线设计*

**本阶段案例:**  
[▶ 2.1 CAD平面图转彩色平面图](#21-cad平面图转彩色平面图) • [2.2 家具布局方案对比](#) • [2.3 流线分析](#)

---

### 2.1 CAD平面图转彩色平面图

将技术性的CAD平面图转换为带真实家具和清晰房间标签的照片级彩色俯视图，用于客户演示。

#### 输入：CAD平面图

![CAD平面图输入](./assets/cases/2.1-cad-to-topview/input.jpg)

---

#### 输出：自然语言提示词

![自然语言输出](./assets/cases/2.1-cad-to-topview/output-natural-cn.jpg)

**提示词：**
```
将提供的CAD平面图转换为照片级真实的彩色俯视图，用于客户演示。添加真实家具、清晰的房间标签，以及适合每个空间的材质地面。使用柔和的自然光照,保持建筑准确性。

房间标签语言：所有房间标签必须使用中文。

重要：严格遵循输入的平面图。不要添加原CAD图中没有的任何物品。不要删减或遗漏原图中出现的任何物品。保持准确的房间数量、家具位置和空间布局。
```

---

#### 输出：JSON结构化提示词

![JSON提示词输出](./assets/cases/2.1-cad-to-topview/output-json-cn.jpg)

**详细JSON提示词：**

> **为什么使用JSON?** JSON擅长定义**结构化关系、验证规则和约束**,这是自然语言无法精确表达的。重点不在于重复尺寸（这些都是估计值），而在于**在关键处强制精确性**:计数、独立性、类型和禁止项。

**🔧 新CAD图纸的JSON生成器：**

有一张新的CAD平面图？我们创建了一个**可复用的JSON生成器**来自动化JSON创建过程。这个元提示词模板可以分析任何CAD图纸（住宅、商业或公共空间），并按照我们的格式生成标准化的JSON提示词。

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
    "label_language": "chinese"
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

---

## 🔧 技术转视觉
*CAD/图纸转照片级可视化*

**本阶段案例：**  
[3.1 立面图转街景渲染](#) • [3.2 剖面图转室内透视](#)

---

## 🎨 材质软装
*材质细化与成本控制*

**本阶段案例：**  
[4.1 材料方案对比](#) • [4.2 材料降级替换](#)

---

## 🖼️ 场景渲染
*最终演示级效果图*

**本阶段案例：**  
[5.1 多角度室内渲染](#) • [5.2 日景夜景对比](#)

---

## ⚙️ 专项应用
*特殊场景与高级功能*

**本阶段案例：**  
[6.1 多语言导视标识](#) • [6.2 四季变化](#) • [6.3 现场问题快速方案](#)

---

## 📚 资源

- 📖 [CASE_TEMPLATE.md](./CASE_TEMPLATE.md) - 新案例创建模板
- 🤝 [CONTRIBUTING.md](./CONTRIBUTING.md) - 贡献指南

---

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

---

<div align="center">

**用❤️为设计师打造**

基于 **Gemini 3 Pro Image** 技术

</div>
