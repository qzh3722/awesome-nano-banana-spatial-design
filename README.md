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
[▶ 2.1 CAD Floor Plan to Client-Friendly View](#21-cad-floor-plan-to-client-friendly-view) • [2.2 Furniture Layout Variations](#) • [2.3 Circulation Analysis](#)

---

### 2.1 CAD Floor Plan to Client-Friendly View

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

<details>
<summary>Click to expand full JSON specification</summary>

```json
{
  "task": "cad_floor_plan_to_photorealistic_topview",
  "project_type": "residential_apartment",
  
  "input_summary": {
    "total_rooms": 9,
    "total_furniture_pieces": 28,
    "total_plumbing_fixtures": 7,
   "architectural_features_count": 1,
    "empty_spaces": ["balcony", "entrance"],
    "language": "english"
  },
  
  "output_requirements": {
    "view": "orthographic_top_down_90_degrees",
    "style": "photorealistic",
    "aspect_ratio": "match_input",
    "lighting": {
      "type": "natural_daylight",
      "time_of_day": "10:00_AM",
      "quality": "soft_diffused",
      "shadows": "subtle_for_depth"
    },
    "room_labels": {
      "language": "english",
      "style": "clean_sans_serif",
      "position": "centered_in_rooms"
    }
  },
  
  "architectural_features": [
    {
      "type": "walk_in_closet",
      "location": "master_bedroom_right_side",
      "rendering_requirement": "Show as built-in architectural space, NOT as freestanding wardrobe furniture",
      "DO_NOT_render_as": "freestanding_wardrobe_cabinet"
    }
  ],
  
  "rooms": [
    {
      "id": "living_room",
      "label": "LIVING ROOM",
      "flooring": {"material": "engineered_wood", "species": "light_oak", "color": "#D4B896"},
      "furniture": [
        {"item": "sectional_sofa", "type": "L_shaped", "quantity": 1, "color": "#C8B8A8"},
        {"item": "chaise_lounge", "quantity": 1, "independence": "SEPARATE_piece_NOT_attached_to_sectional", "placement": "angled_near_window_corner"},
        {"item": "coffee_table", "quantity": 1, "size": "120x60cm", "material": "walnut_wood"},
        {"item": "round_ottomans", "quantity": 2, "shape": "circular", "CRITICAL": "Exact count = 2, both must be distinguishable"},
        {"item": "tv_console", "quantity": 1, "length": "180cm", "material": "walnut_wood"},
        {"item": "area_rug", "quantity": 1, "size": "200x300cm"}
      ]
    },
    {
      "id": "dining_area",
      "label": "DINING AREA",
      "flooring": {"material": "porcelain_tile", "size": "60x60cm", "color": "#E8DCC8"},
      "furniture": [
        {"item": "dining_table", "quantity": 1, "size": "180x90cm", "seating_capacity": 8},
        {"item": "dining_chairs", "quantity": 8, "CRITICAL": "Must show exactly 8 chairs, 4 per long side"}
      ]
    },
    {
      "id": "kitchen",
      "label": "KITCHEN",
      "flooring": {"material": "porcelain_tile", "same_as": "dining_area"},
      "furniture": [
        {"item": "kitchen_island", "quantity": 1, "countertop": "white_quartz"},
        {"item": "bar_stools", "quantity": 4, "CRITICAL": "Must show exactly 4 bar stools at island"}
      ],
      "fixtures": [
        {"item": "sink", "type": "undermount"},
        {"item": "cooktop", "burners": 4}
      ]
    },
    {
      "id": "master_bedroom",
      "label": "MASTER BEDROOM",
      "flooring": {"material": "engineered_wood", "same_as": "living_room"},
      "furniture": [
        {"item": "bed", "type": "queen_or_king", "quantity": 1},
        {"item": "bedside_tables", "quantity": 2, "CRITICAL": "Must show exactly 2 nightstands, one on each side"},
        {"item": "bench_or_chair", "quantity": 1}
      ],
      "architectural_feature_reference": "walk_in_closet_see_architectural_features_section"
    },
    {
      "id": "bedroom_2",
      "label": "BEDROOM 2",
     "flooring": {"material": "engineered_wood", "same_as": "living_room"},
      "furniture": [
        {"item": "single_bed", "quantity": 1, "size": "120x200cm"},
        {"item": "desk", "quantity": 1, "size": "120x60cm"},
        {"item": "desk_chair", "quantity": 1},
        {"item": "wardrobe", "quantity": 1, "color": "white"}
      ]
    },
    {
      "id": "master_bathroom",
      "label": "MASTER BATHROOM",
      "flooring": {"material": "porcelain_tile", "style": "marble_look", "color": "#F5F5F5"},
      "fixtures": [
        {"item": "bathtub", "quantity": 1, "type": "alcove_or_freestanding"},
        {"item": "shower_enclosure", "quantity": 1, "separate_from_bathtub": true, "CRITICAL": "SEPARATE shower, not combined with bathtub"},
        {"item": "toilet", "quantity": 1},
        {"item": "vanity", "type": "double_vanity", "sinks": 2, "CRITICAL": "Must have exactly 2 sinks"}
      ],
      "total_fixture_count": 4
    },
    {
      "id": "secondary_bathroom",
      "label": "BATHROOM",
      "flooring": {"material": "porcelain_tile", "color": "#F0F0F0"},
      "fixtures": [
        {"item": "shower_stall", "quantity": 1, "NO_BATHTUB": true, "CRITICAL": "SHOWER ONLY, absolutely NO bathtub"},
        {"item": "toilet", "quantity": 1},
        {"item": "vanity", "type": "single_sink", "sinks": 1}
      ],
      "total_fixture_count": 3
    },
    {
      "id": "entrance",
      "label": "ENTRANCE",
      "flooring": {"material": "porcelain_tile", "same_as": "kitchen"},
      "furniture": []
    }
  ],
  
  "empty_spaces": [
    {
      "id": "balcony",
      "label": "BALCONY",
      "flooring": {"material": "composite_decking", "color": "#8B8B8B"},
      "furniture": [],
      "plants": [],
      "decorative_items": [],
      "CRITICAL_CONSTRAINT": "Balcony MUST remain completely EMPTY",
      "rendering_requirement": "Show only flooring, NO furniture, NO plants, NO objects"
    }
  ],
  
  "strict_constraints": {
    "no_added_items": true,
    "no_decorative_accessories": ["plants", "vases", "artwork", "throw_pillows", "table_settings"],
    "empty_spaces_enforcement": {"balcony": "must_remain_empty"},
    "exact_counts_required": {
      "dining_chairs": 8,
      "bar_stools": 4,
      "round_ottomans": 2,
      "bedside_tables": 2,
      "master_bath_sinks": 2,
      "secondary_bath_sinks": 1
    },
    "independence_enforced": [
      "chaise_lounge_separate_from_sectional",
      "ottomans_distinct_from_coffee_table",
      "master_bath_shower_separate_from_bathtub"
    ],
    "architectural_vs_furniture": {"walk_in_closet": "architectural_space_not_furniture"},
    "fixture_clarity": {
      "master_bathroom": "has_both_bathtub_and_separate_shower",
      "secondary_bathroom": "has_shower_only_no_bathtub"
    }
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
