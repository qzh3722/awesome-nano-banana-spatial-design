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

<details>
<summary>点击展开完整JSON规格</summary>

```json
{
  "task": "cad_floor_plan_to_photorealistic_topview",
  "input_analysis": {
    "total_rooms": 9,
    "total_furniture_count": 28,
    "total_fixtures": 7,
    "architectural_features": 1,
    "empty_space_count": 2
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
      "feature_id": "walk_in_closet_master",
      "location": "master_bedroom",
      "category": "ARCHITECTURAL_not_furniture",
      "rendering_rule": "显示为带开口的嵌入式空间,不是独立柜体",
      "visual_distinction": "必须呈现为房间延伸,而非家具",
      "DO_NOT_render_as": ["衣柜", "柜子", "大衣柜", "衣柜家具"]
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
          "placement_rule": "靠窗倾斜摆放",
          "visual_distinction_required": "明显独立的家具"
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
          "COUNT_CRITICAL": "精确2个_独立件_都可见"
        },
        {
          "item": "电视柜",
          "quantity": 1
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
          "seating_capacity": 8
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
        {"item": "水槽", "quantity": 1, "type": "台下盆"},
        {"item": "灶台", "quantity": 1}
      ]
    },
    {
      "id": "master_bedroom",
      "label": "主卧室",
      "flooring_material": "木地板_与客厅匹配",
      "furniture_list": [
        {"item": "床", "type": "大床", "quantity": 1},
        {
          "item": "床头柜",
          "quantity": 2,
          "placement": "对称置于床两侧",
          "COUNT_CRITICAL": "精确2个_两侧各1"
        },
        {"item": "座椅", "quantity": 1, "location": "床尾"}
      ],
      "architectural_reference": "包含步入式衣帽间_见建筑特征"
    },
    {
      "id": "bedroom_2",
      "label": "次卧室1",
      "flooring_material": "木地板_与客厅匹配",
      "furniture_list": [
        {"item": "单人床", "quantity": 1},
        {"item": "书桌", "quantity": 1},
        {"item": "书桌椅", "quantity": 1},
        {"item": "衣柜", "quantity": 1, "type": "独立式家具_非建筑"}
      ]
    },
    {
      "id": "master_bathroom",
      "label": "主卫生间",
      "flooring_material": "大理石纹瓷砖",
      "fixtures": [
        {"item": "浴缸", "quantity": 1},
        {
          "item": "淋浴房",
          "quantity": 1,
          "separation_rule": "与浴缸分离_不组合",
          "CRITICAL": "两个独立洁具_淋浴和浴缸",
          "visual_requirement": "明显可区分的独立单元"
        },
        {"item": "马桶", "quantity": 1},
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
        {"item": "马桶", "quantity": 1},
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
      "dining_chairs": {"exact": 8, "verification": "清点全部8把可见"},
      "bar_stools": {"exact": 4, "verification": "全部4把在岛台"},
      "round_ottomans": {"exact": 2, "verification": "两个可区分"},
      "bedside_tables": {"exact": 2, "verification": "两侧各一"},
      "master_bath_sinks": {"exact": 2, "verification": "双台盆"},
      "secondary_bath_sinks": {"exact": 1, "verification": "仅单盆"}
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
      "bedroom_2_wardrobe": "家具_非建筑"
    },
    
    "fixture_clarity": {
      "master_bathroom": "同时有_浴缸和独立淋浴",
      "secondary_bathroom": "仅淋浴_绝对没有浴缸"
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
    "room_count_check": 9,
    "furniture_count_check": 28,
    "fixture_count_check": 7,
    "architectural_features_check": 1,
    "empty_spaces_check": 2,
    "mandatory_verifications": [
      "步入式衣帽间_作为建筑非家具",
      "阳台_完全空置已验证",
      "贵妃椅_独立且倾斜",
      "2个矮凳_都独立可见",
      "4把吧台椅_全在岛台",
      "8把餐椅_全部存在",
      "2个床头柜_对称",
      "主卫_淋浴和浴缸都有且独立",
      "主卫_2个洗手盆已验证",
      "次卫_仅淋浴无浴缸已确认",
      "次卫_仅1个洗手盆已验证"
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
