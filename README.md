<div align="center">

![Awesome Nano Banana Spatial Design Banner](./assets/images/banner.jpg)

# Awesome Nano Banana Spatial Design

> Professional prompts for spatial designers powered by Gemini 3 Pro Image
 
<!-- Language Switcher -->
**English** | [简体中文](./README.zh-CN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## 🎯 Quick Navigation

**Jump to Workflow Stage:**  
[🎨 Concept Ideation](#-concept-ideation) • [📐 Space Planning](#-space-planning) • [🔧 Technical to Visual](#-technical-to-visual) • [🎨 Material & Styling](#-material--styling) • [🖼️ Scene Rendering](#-scene-rendering) • [⚙️ Specialized Tasks](#%EF%B8%8F-specialized-tasks)

> **📌 Disclaimer**: All images used in case examples are for educational and research purposes only. Input images are sourced from publicly available architectural drawings or created specifically for demonstration. This repository does not claim ownership of referenced images and they are used under fair use principles for non-commercial educational purposes.

---

## 🎨 Concept Ideation
*From zero to creative concepts*

**Cases in this stage:**  
[1.1 Hand Sketch to Rendering](#) • [1.2 Multi-Style Concept Comparison](#) • [1.3 Mood Board Generation](#)

### [Intro] 城市俯视等距 3D 卡通微缩场景

**Prompt:**
```
Present a clear, 45° top-down isometric miniature 3D cartoon scene of [CITY], featuring its most iconic landmarks and architectural elements. Use soft, refined textures with realistic PBR materials and gentle, lifelike lighting and shadows. Integrate the current weather conditions directly into the city environment to create an immersive atmospheric mood. Use a clean, minimalistic composition with a soft, solid-colored background.
```

---

### [Intro] PS5 的技术蓝图

**Prompt:**
```
A two-panel technical blueprint diagram in clean monochrome line-art, matching the exact layout of the provided PlayStation 1 schematic. On the left side, draw a full, intact Sony PlayStation 5 console in precise thin line-art on a white background. On the right side, draw a highly detailed, vertically exploded-view diagram of the PS5 showing each
```

---

---

## 📐 Space Planning
*Layout optimization & circulation design*

**Cases in this stage:**  
[▶ 2.1 CAD Floor Plan to Colored Floor Plan](#21-cad-floor-plan-to-colored-floor-plan) • [2.2 Furniture Layout Variations](#) • [2.3 Circulation Analysis](#)

---

### 2.1 CAD Floor Plan to Colored Floor Plan

Convert technical CAD floor plans into photorealistic colored top-down visualizations with realistic furniture and clear room labels for client presentation.

#### Input: CAD Floor Plan

![CAD Floor Plan Input](./assets/cases/2.1-cad-to-topview/input.jpg)

---

#### Output: Natural Language Prompt

![Natural Language Output](./assets/cases/2.1-cad-to-topview/output-natural.jpg)

**Prompt:**
```
Transform the provided CAD floor plan into a photorealistic colored top-down visualization for client presentation. Add realistic furniture, clear room labels, and material-appropriate flooring for each space. Use soft natural lighting and maintain architectural accuracy.

Room Label Language: All room labels must be in ENGLISH.

IMPORTANT: Strictly follow the input floor plan. Do not add any items that are not shown in the original CAD drawing. Do not remove or omit any items that appear in the original plan. Maintain exact room count, furniture placement, and spatial layout as provided.
```

---

#### Output: JSON-Structured Prompt

![JSON Prompt Output](./assets/cases/2.1-cad-to-topview/output-json.jpg)

**Detailed JSON Prompt:**

> **Why use JSON?** JSON excels at defining **structural relationships, validation rules, and constraints** that natural language cannot precisely express. It's not about repeating dimensions (which are estimates anyway), but about enforcing **exactness where it matters**: counts, separations, types, and prohibitions.

**🔧 JSON Generator for New CAD Drawings:**

Got a new CAD floor plan? We've created a **Reusable JSON Generator** to automate the JSON creation process. This meta-prompt template analyzes ANY CAD drawing (residential, commercial, or public space) and generates a standardized JSON prompt following our format.

**How to use:**
1. Upload your CAD floor plan to a Vision AI (e.g., Gemini Pro Vision, GPT-4 Vision, Claude 3.5 Sonnet)
2. Copy and paste the JSON Generator Prompt Template (see below)
3. The AI will systematically scan your floor plan and output a complete JSON prompt
4. Review and use the generated JSON for your visualization task

**Benefits:**
- ✅ Ensures complete room coverage (no missed spaces)
- ✅ Enforces unique naming standards automatically
- ✅ Applies constraint-oriented approach
- ✅ Reduces manual analysis errors
- ✅ Works for residential, commercial, and public spaces

<details>
<summary>📋 Click to view JSON Generator Prompt Template</summary>

Copy this entire prompt and use it with your CAD floor plan image:

```markdown
# JSON Prompt Generator for CAD Floor Plans

> **Purpose**: Analyze the UPLOADED CAD floor plan and generate a standardized JSON prompt.

## Instructions for Vision AI

You are a professional architectural analyst. Analyze the uploaded CAD floor plan **exhaustively** and generate a structured JSON prompt for transforming it into a photorealistic colored top-down visualization.

### 1. COMPLETE SPATIAL ANALYSIS

Execute these scanning procedures in order:

#### A. Grid Scan Method
- Divide the floor plan into a 3×3 grid
- Scan each grid cell systematically
- Identify ALL enclosed or semi-enclosed spaces

#### B. Wall Trace Method
- Trace along perimeter walls clockwise
- Identify every space bounded by walls
- Include small rooms (storage, closets, powder rooms)

#### C. Functional Space Checklist (Universal)
Verify you have identified ALL applicable categories:

**For ANY space type:**
- [ ] Primary functional areas
- [ ] Service/support areas (kitchens, restrooms, janitor rooms)
- [ ] Storage spaces (closets, equipment rooms, warehouses)
- [ ] Circulation spaces (entrances, lobbies, hallways, staircases)
- [ ] Utility/mechanical spaces (equipment rooms, server rooms)
- [ ] Outdoor/semi-outdoor spaces (balconies, terraces, courtyards)

**Space Type Examples:**
- Residential: Living rooms, bedrooms, bathrooms
- Commercial: Workspaces, offices, meeting rooms, break rooms
- Retail: Sales floor, fitting rooms, stockrooms
- Hospitality: Guest rooms, lobby, restaurants, fitness centers
- Public: Waiting areas, service counters, restrooms, exhibition halls

#### D. Built-in Elements Checklist
- [ ] Floor-mounted fixtures
- [ ] Wall-mounted fixtures (upper cabinets)
- [ ] Architectural alcoves (walk-in closets)
- [ ] Plumbing fixtures

### 2. ROOM NAMING STANDARDS

**Unique Naming Rule**: Multiple rooms of same type MUST have unique numbers:
- ✅ Correct: "BEDROOM 2", "BEDROOM 3", "STORAGE 1", "STORAGE 2"
- ❌ Wrong: "BEDROOM", "BEDROOM" (duplicates)

### 3. CRITICAL RULES

1. **NO Estimated Dimensions**: Do NOT include sizes like "120x60cm"
2. **NO Color Codes**: Do NOT include "#D4B896" style codes
3. **Focus on Constraints**: Use `independence_rule`, `COUNT_CRITICAL`, `separation_rule`
4. **Task Field**: MUST explicitly mention "UPLOADED"

### 4. OUTPUT FORMAT

Provide:
1. Brief analysis summary (total rooms, categories)
2. Complete JSON prompt in code block

Use the JSON structure from the main specification below.

**Now analyze the uploaded CAD and generate the JSON prompt.**
```

</details>

<details>
<summary>Click to expand full JSON specification</summary>

```json
{
    "task": "Transform the UPLOADED CAD floor plan image into photorealistic colored top-down visualization",
    "input_specification": {
        "source": "uploaded_cad_drawing",
        "constraint": "MUST_use_uploaded_image_as_ONLY_spatial_reference",
        "prohibition": "DO_NOT_generate_alternative_layouts",
        "verification": "output_layout_MUST_match_input_exactly"
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
        "label_language": "english",
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
            "rendering_rule": "Show as built-in space with opening, NOT as freestanding cabinet",
            "DO_NOT_render_as": [
                "wardrobe",
                "cabinet",
                "armoire",
                "closet_furniture"
            ]
        },
        {
            "feature_id": "kitchen_upper_cabinets",
            "location": "kitchen",
            "category": "ARCHITECTURAL_not_furniture",
            "rendering_rule": "Wall-mounted overhead cabinetry visible in top view"
        }
    ],
    "rooms": [
        {
            "id": "living_room",
            "label": "LIVING ROOM",
            "flooring_material": "light_oak_wood",
            "furniture_list": [
                {
                    "item": "sectional_sofa",
                    "configuration": "L_shaped",
                    "quantity": 1
                },
                {
                    "item": "chaise_lounge",
                    "quantity": 1,
                    "independence_rule": "MUST_be_separate_from_sectional",
                    "placement_rule": "angled_placement",
                    "CRITICAL": "Clearly_distinct_angled_piece"
                },
                {
                    "item": "coffee_table",
                    "quantity": 1,
                    "material": "wood"
                },
                {
                    "item": "round_ottomans",
                    "quantity": 2,
                    "shape": "circular",
                    "independence_rule": "distinct_from_coffee_table",
                    "COUNT_CRITICAL": "EXACTLY_2_separate_circular_pieces_both_visible"
                },
                {
                    "item": "tv_console",
                    "quantity": 1,
                    "material": "wood"
                },
                {
                    "item": "area_rug",
                    "quantity": 1
                }
            ]
        },
        {
            "id": "dining_area",
            "label": "DINING AREA",
            "flooring_material": "ceramic_tile",
            "furniture_list": [
                {
                    "item": "dining_table",
                    "quantity": 1,
                    "seating_capacity": 8,
                    "material": "wood"
                },
                {
                    "item": "dining_chairs",
                    "quantity": 8,
                    "arrangement": "4_per_long_side",
                    "COUNT_CRITICAL": "EXACTLY_8_chairs_all_visible"
                }
            ]
        },
        {
            "id": "kitchen",
            "label": "KITCHEN",
            "flooring_material": "ceramic_tile_matching_dining",
            "furniture_list": [
                {
                    "item": "kitchen_island",
                    "quantity": 1,
                    "countertop_material": "white_quartz"
                },
                {
                    "item": "bar_stools",
                    "quantity": 4,
                    "placement": "along_island",
                    "COUNT_CRITICAL": "EXACTLY_4_stools_all_at_island"
                }
            ],
            "fixtures": [
                {
                    "item": "sink",
                    "quantity": 1,
                    "type": "undermount"
                },
                {
                    "item": "cooktop",
                    "quantity": 1
                }
            ]
        },
        {
            "id": "master_bedroom",
            "label": "MASTER BEDROOM",
            "flooring_material": "wood_matching_living_room",
            "furniture_list": [
                {
                    "item": "bed",
                    "type": "queen_or_king",
                    "quantity": 1
                },
                {
                    "item": "bedside_tables",
                    "quantity": 2,
                    "placement": "symmetrically_flanking_bed",
                    "COUNT_CRITICAL": "EXACTLY_2_one_each_side"
                },
                {
                    "item": "seating",
                    "quantity": 1,
                    "location": "foot_of_bed"
                }
            ],
            "architectural_reference": "includes_walk_in_closet"
        },
        {
            "id": "bedroom_2",
            "label": "BEDROOM 2",
            "flooring_material": "wood_matching_living_room",
            "furniture_list": [
                {
                    "item": "single_bed",
                    "quantity": 1
                },
                {
                    "item": "desk",
                    "quantity": 1
                },
                {
                    "item": "desk_chair",
                    "quantity": 1
                },
                {
                    "item": "wardrobe",
                    "quantity": 1,
                    "type": "standalone_furniture_not_architectural"
                }
            ]
        },
        {
            "id": "master_bathroom",
            "label": "MASTER BATHROOM",
            "flooring_material": "marble_look_tile",
            "fixtures": [
                {
                    "item": "bathtub",
                    "quantity": 1
                },
                {
                    "item": "shower_enclosure",
                    "quantity": 1,
                    "separation_rule": "SEPARATE_from_bathtub_NOT_combined",
                    "CRITICAL": "Two_distinct_fixtures_shower_AND_tub"
                },
                {
                    "item": "toilet",
                    "quantity": 1
                },
                {
                    "item": "vanity",
                    "sink_count": 2,
                    "type": "double_sink",
                    "COUNT_CRITICAL": "EXACTLY_2_sinks"
                }
            ],
            "total_fixture_verification": 4
        },
        {
            "id": "secondary_bathroom",
            "label": "BATHROOM 2",
            "flooring_material": "ceramic_tile",
            "fixtures": [
                {
                    "item": "shower_stall",
                    "quantity": 1,
                    "NO_BATHTUB": true,
                    "CRITICAL": "SHOWER_ONLY_absolutely_NO_bathtub"
                },
                {
                    "item": "toilet",
                    "quantity": 1
                },
                {
                    "item": "vanity",
                    "sink_count": 1,
                    "type": "single_sink",
                    "COUNT_CRITICAL": "EXACTLY_1_sink_NOT_2"
                }
            ],
            "total_fixture_verification": 3
        },
        {
            "id": "entrance",
            "label": "ENTRANCE",
            "flooring_material": "ceramic_tile_matching_kitchen",
            "furniture_list": [],
            "usage_note": "circulation_space_minimal_furniture"
        },
        {
            "id": "storage_1",
            "label": "STORAGE 1",
            "flooring_material": "ceramic_tile_matching_dining",
            "furniture_list": [],
            "usage": "storage"
        },
        {
            "id": "powder_room",
            "label": "POWDER ROOM",
            "flooring_material": "ceramic_tile",
            "fixtures": [
                {
                    "item": "toilet",
                    "quantity": 1
                },
                {
                    "item": "vanity",
                    "sink_count": 1,
                    "type": "small_single_sink"
                }
            ],
            "note": "guest_bathroom"
        },
        {
            "id": "bathroom_1",
            "label": "BATHROOM 1",
            "flooring_material": "ceramic_tile",
            "fixtures": [
                {
                    "item": "shower_stall",
                    "quantity": 1
                },
                {
                    "item": "toilet",
                    "quantity": 1
                },
                {
                    "item": "vanity",
                    "sink_count": 1,
                    "type": "single_sink"
                }
            ]
        },
        {
            "id": "bedroom_3",
            "label": "BEDROOM 3",
            "flooring_material": "wood_matching_living_room",
            "furniture_list": [
                {
                    "item": "single_bed",
                    "quantity": 1
                },
                {
                    "item": "desk",
                    "quantity": 1
                },
                {
                    "item": "desk_chair",
                    "quantity": 1
                },
                {
                    "item": "wardrobe",
                    "quantity": 1,
                    "type": "standalone"
                }
            ]
        },
        {
            "id": "ensuite_bathroom",
            "label": "EN-SUITE",
            "flooring_material": "ceramic_tile",
            "fixtures": [
                {
                    "item": "shower_stall",
                    "quantity": 1,
                    "NO_BATHTUB": true
                },
                {
                    "item": "toilet",
                    "quantity": 1
                },
                {
                    "item": "vanity",
                    "sink_count": 1,
                    "type": "single_sink"
                }
            ],
            "note": "private_bathroom_for_bedroom_3"
        },
        {
            "id": "storage_2",
            "label": "STORAGE 2",
            "flooring_material": "ceramic_tile",
            "furniture_list": [],
            "usage": "storage"
        }
    ],
    "empty_spaces": [
        {
            "id": "balcony",
            "label": "BALCONY",
            "flooring_material": "composite_decking",
            "furniture_list": [],
            "plants": [],
            "decorative_items": [],
            "CRITICAL_CONSTRAINT": "MUST_remain_completely_EMPTY",
            "absolute_prohibition": [
                "NO_furniture",
                "NO_plants",
                "NO_planters",
                "NO_decorative_objects",
                "NO_items_whatsoever"
            ],
            "rendering_rule": "show_ONLY_flooring_surface_nothing_else"
        }
    ],
    "strict_constraints": {
        "count_accuracy": {
            "dining_chairs": {
                "exact": 8,
                "verification": "count_all_8_visible"
            },
            "bar_stools": {
                "exact": 4,
                "verification": "all_4_at_island"
            },
            "round_ottomans": {
                "exact": 2,
                "verification": "two_distinct_pieces"
            },
            "bedside_tables": {
                "exact": 2,
                "verification": "one_on_each_side"
            },
            "master_bath_sinks": {
                "exact": 2,
                "verification": "double_vanity"
            },
            "secondary_bath_sinks": {
                "exact": 1,
                "verification": "single_vanity"
            }
        },
        "independence_requirements": [
            {
                "item": "chaise_lounge",
                "must_be_separate_from": "sectional_sofa",
                "visual_proof": "clearly_distinct_angled_piece"
            },
            {
                "item": "round_ottomans",
                "must_be_separate_from": "coffee_table",
                "visual_proof": "two_separate_circular_items"
            },
            {
                "item": "master_shower",
                "must_be_separate_from": "bathtub",
                "visual_proof": "two_distinct_fixtures_not_combined"
            }
        ],
        "categorical_distinctions": {
            "walk_in_closet": "architectural_feature_NOT_furniture",
            "bedroom_wardrobes": "furniture_NOT_architectural",
            "kitchen_upper_cabinets": "architectural_NOT_furniture"
        },
        "fixture_clarity": {
            "master_bathroom": "has_BOTH_tub_AND_separate_shower",
            "secondary_bathroom": "SHOWER_ONLY_absolutely_NO_bathtub",
            "ensuite_bathroom": "SHOWER_ONLY_no_bathtub"
        },
        "prohibition_list": {
            "no_added_decorative_items": [
                "plants",
                "vases",
                "artwork",
                "sculptures",
                "throw_pillows",
                "table_settings",
                "books",
                "accessories"
            ],
            "empty_space_enforcement": {
                "balcony": "absolutely_nothing_allowed",
                "entrance": "minimal_or_empty"
            }
        },
        "rendering_validation": {
            "no_added_items_rule": "strictly_only_items_with_CAD_symbols",
            "no_removed_items_rule": "all_CAD_elements_must_appear",
            "no_merged_elements_rule": "separate_items_stay_separate",
            "no_hallucinated_features_rule": "no_invented_architectural_elements"
        }
    },
    "verification_checklist": {
        "room_count": 15,
        "furniture_count": 28,
        "fixture_count": 7,
        "architectural_features": 2,
        "empty_spaces": 2,
        "mandatory_verifications": [
            "walk_in_closet_as_architectural_not_furniture",
            "kitchen_upper_cabinets_visible",
            "balcony_completely_empty_verified",
            "chaise_lounge_separate_and_angled",
            "2_ottomans_distinct_and_visible",
            "4_bar_stools_at_island",
            "8_dining_chairs_present",
            "2_bedside_tables_symmetrical",
            "master_bath_has_separate_shower_and_tub",
            "master_bath_has_2_sinks",
            "secondary_bath_has_shower_only_no_tub",
            "secondary_bath_has_1_sink",
            "ensuite_has_shower_only"
        ]
    }
}
```

</details>

---

#### 💡 Tips

- **Iterative Generation Recommended**: Natural language prompts work best with an iterative approach. Generate 2-3 variations first, select the best one, then use simple image editing tools (Photoshop, Figma, Canva) to refine minor details if needed. This hybrid workflow often produces better results than trying to perfect everything in a single prompt.
- **Verify JSON Completeness**: Before submitting, ensure all rooms from your CAD plan are included in the JSON. Missing furniture (like ottomans or chaise lounges) will not appear in the output.
- **Material Consistency**: Keep the same flooring material for connected spaces (e.g., kitchen + dining + entrance) for visual flow.
- **Room Label Clarity**: JSON prompt produces more precise text rendering. If labels are unclear with natural language, use the JSON specification.
- **Style Variations**: To change design styles, modify:
  - Furniture materials (e.g., `"linen_fabric"` → `"leather"`)
  - Flooring colors (e.g., `"#D4B896"` → darker/lighter tones)
  - Overall atmosphere (`"modern_residential"` → `"luxury"`, `"minimalist"`)

### 05. 彩色平面图生成 (Colored Floor Plan)

**Prompt:**
```
Rendered architectural floor plan (top view). Fill the bedrooms with wood texture, bathrooms with tile texture, and living areas with carpet. Add subtle drop shadows to furniture to show depth. Style: High-end real estate marketing brochure, flat lighting.
```

---

### 08. 景观分区分析图 (Landscape Zoning Map)

**Prompt:**
```
Site analysis diagram. Overlay color-coded zones on the site plan: Green for 'Public Park', Blue for 'Water Feature', Yellow for 'Residential'. Use hatch patterns and legends. Vector graphic style.
```

---

### 09. 城市肌理底图风格化 (Urban Fabric Stylization)

**Prompt:**
```
Urban figure-ground diagram (Noli map). Render all buildings as solid black masses and all streets/open spaces as pure white. High contrast, abstract map style. Remove all vegetation and cars.
```

---

### 34. 办公位布局优化 (Office Desk Layout)

**Prompt:**
```
Open plan office interior. Rows of modern white desks with ergonomic black chairs. Separate the rows with planter boxes containing snake plants. Busy professional atmosphere, daytime.
```

---

---

## 🔧 Technical to Visual
*CAD/drawings to photorealistic visualization*

**Cases in this stage:**  
[3.1 Elevation to Street View](#) • [3.2 Section to Interior Perspective](#)

### 01. 平面图转轴测图 (Floor Plan to Axonometric)

**Prompt:**
```
Transform this 2D floor plan into a 3D isometric architectural drawing. Extrude the walls to a consistent height. Apply a 'clay render' style with soft ambient occlusion shadows. Keep the layout exactly as shown in the plan. Highlight circulation paths in soft blue.
```

---

### 02. 剖面图转剖透视 (Section to Section Perspective)

**Prompt:**
```
Architectural section perspective based on this line drawing. Render the cut surfaces (walls/slabs) in solid jet black (Poché). Render the interior spaces with photorealistic materials: concrete ceiling, oak flooring. Add depth and atmospheric lighting entering from the windows. 4K resolution.
```

---

### 03. 爆炸轴测图生成 (Exploded Axonometric)

**Prompt:**
```
Exploded axonometric diagram of the building structure. Separate the layers vertically: foundation at the bottom, structural grid in the middle, and roof skin at the top. Style: Technical illustration, clean white background, thin linework, pastel color coding for each layer.
```

---

### 04. 手绘草图转体块推敲 (Sketch to Massing Model)

**Prompt:**
```
Convert this loose architectural sketch into a clean, geometric white massing model. Straighten the lines and correct the perspective. Render in a 'studio lighting' setup with sharp shadows to define the volumes. Abstract minimalism.
```

---

### 06. 结构系统分析图 (Structural Analysis Diagram)

**Prompt:**
```
Structural diagram. Make the non-structural walls transparent/ghosted. Highlight the columns and main beams in solid red. Show the load-bearing logic. X-ray architectural style.
```

---

### 07. 暖通空调(HVAC)布局可视化 (HVAC Overlay)

**Prompt:**
```
Reflected ceiling plan visualization. Overlay 3D semi-transparent blue ducts showing the HVAC system. Distinguish supply diffusers (arrows out) and return vents. Maintain the layout of the lights.
```

---

### 10. 垂直交通流线图 (Vertical Circulation)

**Prompt:**
```
Sectional circulation diagram. Highlight staircases and elevator shafts in glowing orange. Add arrows indicating upward movement. Dark background blueprint style.
```

---

### 12. 构造节点三维剖切 (3D Detail Callout)

**Prompt:**
```
Photorealistic 3D cutaway of a curtain wall detail based on this drawing. Show the layers: aluminum mullion, double glazing, rubber gasket, and insulation. Macro photography style, sharp focus on the joint.
```

---

### 17. 隐蔽工程透视 (MEP X-Ray)

**Prompt:**
```
Technical visualization. A bathroom wall rendered with 50% transparency. Reveal the copper plumbing pipes and PVC drainage pipes inside the wall cavity. Educational diagram style.
```

---

### 18. 施工工艺分层示意 (Construction Layers)

**Prompt:**
```
Layered floor construction diagram. Peel back the layers to show: 1. Concrete slab, 2. Acoustic mat, 3. Underfloor heating pipes, 4. Screed, 5. Timber finish. Label each layer.
```

---

### 46. 无障碍分析图 (Accessibility Diagram)

**Prompt:**
```
Accessibility analysis overlay on floor plan. Show 1.5m diameter turning circles in red dashed lines in bathrooms and hallways. Highlight wheelchair ramps in blue. Technical annotation style.
```

---

### 47. 可持续设计图解 (Sustainability Diagram)

**Prompt:**
```
Sustainability concept section. Show blue arrows for natural ventilation airflow through windows. Show yellow arrows for sunlight shading. Add icons for 'Solar Panels' on the roof. Educational style.
```

---

### 48. 鸟瞰图转总平面 (Aerial to Site Plan)

**Prompt:**
```
Convert this aerial drone photo into a flat architectural site plan diagram. Flatten the perspective to 2D top-down. Simplify trees to circles and buildings to solid shapes. Desaturated colors.
```

---

### 49. 3D 打印预览图 (3D Print Preview)

**Prompt:**
```
Render this building model as a 3D printed object. Material: White PLA plastic with visible layer lines. Sitting on a wooden table. Depth of field blurring the background.
```

---

---

## 🎨 Material & Styling
*Material refinement & cost optimization*

**Cases in this stage:**  
[4.1 Material Scheme Comparison](#) • [4.2 Material Downgrade for Budget](#)

### 11. 材质板转 3D 渲染 (Moodboard to Render)

**Prompt:**
```
Interior rendering of a living room using the materials from the reference image. Apply the boucle fabric to the sofa, the walnut wood to the cabinets, and the terrazzo sample to the floor. Maintain accurate texture scaling.
```

---

### 13. 定制柜体内部结构 (Joinery Internal View)

**Prompt:**
```
Open view of a bespoke wardrobe. Show the internal layout: hanging rails, drawers with glass fronts, and LED strip lighting in the shelves. Finish: Dark grey melamine. Perspective view.
```

---

### 14. 砖石铺贴纹理研究 (Pattern Generation)

**Prompt:**
```
Close-up texture study of a brick wall. Arrange the bricks in a 'vertical stack bond' pattern. Bricks should be handmade terracotta with irregular edges and thick mortar joints.
```

---

### 15. 灯光照度可视化 (Lighting Falloff)

**Prompt:**
```
Lighting visualization. A textured stone wall lit by three recessed spotlights from above. Show the realistic 'scallop' shape of the light beams and the texture relief created by grazing light.
```

---

### 16. 软装布艺褶皱模拟 (Fabric Physics)

**Prompt:**
```
Close-up of heavy velvet curtains pooling on a wooden floor. Show realistic fabric folds, weight, and light sheen. Color: Deep emerald green.
```

---

### 19. 异形家具曲面分析 (Curved Surface Analysis)

**Prompt:**
```
Studio render of a parametric curved bench. Material: Glossy white fiberglass. Use 'zebra stripe' reflection mapping to highlight the curvature continuity.
```

---

### 20. 老旧材质做旧模拟 (Weathering Simulation)

**Prompt:**
```
Material aging simulation. Show a copper facade panel with realistic green patina (verdigris) streaming down from the top edges, simulating 10 years of weather exposure.
```

---

### 30. 艺术品/挂画替换 (Art Staging)

**Prompt:**
```
Replace the painting on the wall with a large-scale abstract expressionist artwork in blue and gold tones. Add a frame that matches the furniture wood.
```

---

---

## 🖼️ Scene Rendering
*Final presentation quality renders*

**Cases in this stage:**  
[5.1 Multi-Angle Interior](#) • [5.2 Day/Night Lighting](#)

### 29. 日夜光环境转换 (Day to Night)

**Prompt:**
```
Turn this daylight photo into a night scene. Dark blue sky. Turn on the interior lights (3000K warm white). Add exterior uplighting to the trees.
```

---

### 35. 餐厅灯光氛围模拟 (Restaurant Ambiance)

**Prompt:**
```
Fine dining restaurant interior. Moody, low-key lighting. Tables illuminated by focused pin-spots, leaving the surrounding areas in shadow. Velvet booth seating. Candlelight on tables.
```

---

### 37. 酒店客房标准间 (Hotel Room Visualization)

**Prompt:**
```
Luxury hotel room interior. King size bed with crisp white linens and a beige throw. Floor-to-ceiling window with shear curtains. Warm bedside lamps on. Symmetrical composition.
```

---

### 40. 咖啡馆氛围板 (Cafe Mood Visualization)

**Prompt:**
```
Rustic coffee shop interior. Exposed brick walls, reclaimed wood tables, industrial pendant lights. Steam rising from a coffee cup in the foreground. Warm, inviting, morning light.
```

---

### 44. 漫游关键帧生成 (Walkthrough Keyframes)

**Prompt:**
```
Cinematic storyboard keyframes for architectural walkthrough. Frame 1: Wide shot of building exterior at dawn. Frame 2: Close up of hand opening the door. Frame 3: Eye- level view of the sunlit lobby. Consistent color grading.
```

---

### 45. 配景人物植入 (Entourage Population)

**Prompt:**
```
Populate this plaza render with diverse groups of people. People walking, sitting on benches, talking. Motion blur on walking figures. Ensure shadows match the sun direction of the scene.
```

---

### 50. 风格一致性检查 (Style Consistency Check)

**Prompt:**
```
Apply the color grading and lighting style of Reference Image A to Reference Image B. Make them look like they belong to the same photography set. Keep the content of Image B unchanged.
```

---

---

## ⚙️ Specialized Tasks
*Special use cases & advanced features*

**Cases in this stage:**  
[6.1 Multilingual Signage](#) • [6.2 Seasonal Variations](#) • [6.3 On-Site Quick Solutions](#)

### 21. 保留家具换硬装 (Keep Furniture, Change Room)

**Prompt:**
```
Renovation visualization. Change the wall color to sage green and the floor to herringbone parquet. Constraint: Keep the existing sofa, coffee table, and rug exactly as they are in the photo. Do not move them.
```

---

### 22. 清空房间 (Declutter / Empty Room)

**Prompt:**
```
Real estate photo editing. Remove all furniture, boxes, and clutter from this room. Show the clean, empty space with bare walls and flooring. Auto-fill the floor texture where furniture was removed.
```

---

### 23. 虚拟软装 (Virtual Staging)

**Prompt:**
```
Virtual staging. Furnish this empty bedroom with a Queen-sized bed, two nightstands, and a wardrobe. Style: Modern Minimalist. Ensure furniture perspective aligns with the room's vanishing points.
```

---

### 24. 厨房翻新：换门板不换布局 (Kitchen Facelift)

**Prompt:**
```
Kitchen facelift. Replace the oak cabinet doors with matte navy blue flat-panel doors. Change countertop to white marble. Keep the kitchen layout, appliances, and sink position exactly unchanged.
```

---

### 25. 窗外景观替换 (View Replacement)

**Prompt:**
```
View substitution. Replace the white window background with a cityscape at twilight. Add realistic blue reflections of the city lights onto the interior floor.
```

---

### 26. 建筑立面改造 (Facade Cladding Swap)

**Prompt:**
```
Building exterior renovation. Replace the red brick facade with sleek silver aluminum composite panels. Keep the window openings and building shape structurally identical.
```

---

### 27. 增加绿植氛围 (Biophilic Injection)

**Prompt:**
```
Add lush indoor plants to this office lobby. Place tall Ficus trees in the corners and hanging planters from the ceiling beams. Natural, vibrant atmosphere.
```

---

### 28. 季节/天气变换 (Seasonal Variation)

**Prompt:**
```
Change season to Winter. Cover the garden ground with snow. Trees should be bare branches. Add warm light glow coming from the house windows. Cozy winter evening.
```

---

### 31. 门头招牌设计 (Storefront Signage)

**Prompt:**
```
Retail storefront render. Place a 3D neon sign reading 'URBAN CAFE' above the entrance. Font style: Retro script. Color: Bright pink. Show realistic glow reflection on the glass window.
```

---

### 32. 货架陈列生成 (Visual Merchandising)

**Prompt:**
```
Supermarket shelves visualization. Fill the shelves with neatly arranged cereal boxes and colorful packaging. Ensure distinct, non-repetitive product designs. bright, even lighting.
```

---

### 33. 展台设计方案 (Exhibition Booth)

**Prompt:**
```
3x3 meter exhibition booth design. Minimalist white style with a central reception counter. Large LED screen on the back wall displaying a abstract blue wave pattern. Spotlights on the counter.
```

---

### 36. 品牌快闪店 (Pop-up Store)

**Prompt:**
```
Pop-up store design in a mall atrium. A cylindrical structure made of translucent polycarbonate sheets. Glowing from within with purple light. Branding text 'FUTURE TECH' on the top header.
```

---

### 38. 导视系统模拟 (Wayfinding Mockup)

**Prompt:**
```
Hospital corridor interior. Apply clear vinyl wayfinding graphics to the floor: A blue line with text 'Radiology' and a red line with text 'Emergency'. Perspective adjusted to match the floor plane.
```

---

### 39. 橱窗陈列设计 (Window Display)

**Prompt:**
```
Fashion boutique window display. Two mannequins wearing avant-garde silver jackets. Background: Abstract geometric shapes suspended in air. Lighting: Dramatic purple and teal spotlights.
```

---

### 41. 概念推演过程图 (Concept Diagram Sequence)

**Prompt:**
```
Architectural concept diagram series. Three steps: 1. A simple cube. 2. The cube sliced diagonally. 3. The final form with terraced gardens. Style: Simple white isometric blocks with blue arrows showing the transformation.
```

---

### 42. 渲染图转水彩手绘 (Render to Watercolor)

**Prompt:**
```
Convert this photorealistic building render into a loose watercolor sketch. Soft washes of color, pencil outlines, bleeding edges. Artistic, hand-drawn feel. Reduce detail.
```

---

### 43. 汇报排版生成 (Presentation Board Layout)

**Prompt:**
```
Architectural presentation board layout. Arrange the provided render (top), floor plan (bottom left), and material palette (bottom right) on a clean white background. Add a title 'PROJECT HORIZON' in minimalist sans-serif font.
```

---

---

## 📚 Resources

- 📖 [CASE_TEMPLATE.md](./CASE_TEMPLATE.md) - Template for creating new use cases
- 🤝 [CONTRIBUTING.md](./CONTRIBUTING.md) - How to contribute new cases

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for Designers**

Powered by **Gemini 3 Pro Image**

</div>
