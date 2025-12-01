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
        "label_language": "english"
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
            "flooring_material": "tile_matching_kitchen",
            "furniture_list": [],
            "usage_note": "circulation_space_minimal_or_empty"
        },
        {
            "id": "storage_1",
            "label": "STORAGE 1",
            "flooring_material": "tile_matching_dining",
            "furniture_list": [],
            "usage": "storage_utility"
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
            "label": "EN-SUITE BATHROOM",
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
            "note": "attached_to_bedroom_3"
        },
        {
            "id": "storage_2",
            "label": "STORAGE 2",
            "flooring_material": "ceramic_tile",
            "furniture_list": [],
            "usage": "storage_utility"
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
                "NO_any_items"
            ],
            "rendering_rule": "show_ONLY_flooring_surface"
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
                "verification": "both_distinguishable"
            },
            "bedside_tables": {
                "exact": 2,
                "verification": "one_each_side"
            },
            "master_bath_sinks": {
                "exact": 2,
                "verification": "double_vanity"
            },
            "secondary_bath_sinks": {
                "exact": 1,
                "verification": "single_only"
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
                "visual_proof": "two_separate_circular_forms"
            },
            {
                "item": "master_bath_shower",
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
            "master_bathroom": "has_BOTH_bathtub_AND_separate_shower",
            "secondary_bathroom": "has_shower_ONLY_absolutely_NO_bathtub",
            "ensuite_bathroom": "has_shower_ONLY_NO_bathtub"
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
                "entrance": "minimal_or_empty_only"
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
            "2_ottomans_both_distinct_and_visible",
            "4_bar_stools_all_at_island",
            "8_dining_chairs_all_present",
            "2_bedside_tables_symmetrical",
            "master_bath_both_shower_AND_tub_separate",
            "master_bath_2_sinks_verified",
            "secondary_bath_shower_only_NO_tub_confirmed",
            "secondary_bath_1_sink_only_verified",
            "ensuite_bath_shower_only_NO_tub"
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

---

## 🔧 Technical to Visual
*CAD/drawings to photorealistic visualization*

**Cases in this stage:**  
[3.1 Elevation to Street View](#) • [3.2 Section to Interior Perspective](#)

---

## 🎨 Material & Styling
*Material refinement & cost optimization*

**Cases in this stage:**  
[4.1 Material Scheme Comparison](#) • [4.2 Material Downgrade for Budget](#)

---

## 🖼️ Scene Rendering
*Final presentation quality renders*

**Cases in this stage:**  
[5.1 Multi-Angle Interior](#) • [5.2 Day/Night Lighting](#)

---

## ⚙️ Specialized Tasks
*Special use cases & advanced features*

**Cases in this stage:**  
[6.1 Multilingual Signage](#) • [6.2 Seasonal Variations](#) • [6.3 On-Site Quick Solutions](#)

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
