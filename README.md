<div align="center">

![Awesome Nano Banana Spatial Design Banner](./assets/images/banner.jpg)

# Awesome Nano Banana Spatial Design

> Professional Prompt Library for Spatial Designers using Gemini 3 Pro Image
 
<!-- Language Switch -->
**English** | [简体中文](./README.zh-CN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## 🎯 Quick Navigation

**Jump to Workflow Stage:**  
[🎨 Concept Ideation](#-concept-ideation) • [📐 Space Planning](#-space-planning) • [🔧 Technical to Visual](#-technical-to-visual) • [🎨 Material & Styling](#-material--styling) • [🖼️ Scene Rendering](#%EF%B8%8F-scene-rendering) • [⚙️ Specialized Tasks](#%EF%B8%8F-specialized-tasks)

> **📌 Disclaimer**: All images used in this case library are for educational and research purposes only. Input images are from public architectural drawings or created specifically for demonstration. This repository claims no ownership of referenced images; all images are used under fair use principles for non-commercial educational purposes.

---
## 🎨 Concept Ideation
*From Zero to Creative Concept*

**Cases in this stage:**  
[1.1 Auto-Furnish Floor Plan](#11-auto-furnish-floor-plan) • [1.2 3D Storefront Render](#12-3d-storefront-render)

### 1.1 Auto-Furnish Floor Plan

#### Input

![Input Image](./assets/cases/1.1-auto-furnish-plan/input.jpg)

#### Output

![Output Image](./assets/cases/1.1-auto-furnish-plan/output.jpg)

**Prompt:**
```
Using the uploaded floor plan as the base image, arrange furniture and soft furnishings in each space according to the functional room labels indicated by the text annotations in the original drawing. Maintain all wall structures, door locations, window positions, and architectural elements exactly as shown without any modifications to the building configuration. Do not add any new walls or partitions to the layout. Preserve the black and white line drawing style and monochromatic palette throughout the composition. Remove all text annotations and labels from the final output, showing only the architectural elements and newly added furniture arrangements.
```

---

### 1.2 3D Storefront Render

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Ultra-realistic 3D render of a cute, miniature [BRAND NAME] storefront building.
```

---

## 📐 Space Planning
*Layout Optimization & Circulation Design*

**Cases in this stage:**  
[2.1 Colored Floor Plan](#21-colored-floor-plan) • [2.2 Landscape Zoning Map](#22-landscape-zoning-map) • [2.3 Urban Fabric Stylization](#23-urban-fabric-stylization) • [2.4 Office Desk Layout](#24-office-desk-layout)

### 2.1 Colored Floor Plan


Convert technical CAD floor plans into photorealistic colored top views with real furniture and clear room labels for client presentations.

#### Input: CAD Floor Plan

![CAD Floor Plan Input](./assets/cases/2.1-cad-to-topview/input.jpg)

---

#### Output: Natural Language Prompt

![Natural Language Output](./assets/cases/2.1-cad-to-topview/output-natural-cn.jpg)

**Room Labeling:**
- You MUST label **every** space in the floor plan (e.g., "Living Room", "Bedroom 2", "Storage").
- If the original CAD drawing contains text or labels, **you MUST completely remove them** and replace them with new, clear, professional labels.
- Do not overlay new labels on top of old ones.

**Output Requirements:**
- **View**: Orthographic top-down view.
- **Style**: Photorealistic, natural lighting.

**Prompt:**
```
Convert the provided CAD floor plan into a photorealistic colored top view for client presentation. Add real furniture, clear room labels, and appropriate flooring materials for each space. Use soft natural lighting and maintain architectural accuracy.

Room Label Language: All room labels must be in English.

IMPORTANT: Strictly follow the input floor plan. Do not add any items not present in the original CAD. Do not remove or omit any items present in the original. Maintain accurate room count, furniture placement, and spatial layout.
```

---

#### Output: JSON Structured Prompt

![JSON Prompt Output](./assets/cases/2.1-cad-to-topview/output-json-cn.jpg)

**Detailed JSON Prompt:**

> **Why JSON?** JSON excels at defining **structured relationships, validation rules, and constraints** that natural language cannot express precisely. The focus is not on repeating dimensions (which are estimates), but on **enforcing precision where it matters**: counts, independence, types, and prohibitions.

**🔧 JSON Generator for New CAD Drawings:**

Have a new CAD floor plan? We created a **Reusable JSON Generator** to automate the JSON creation process. This meta-prompt template can analyze any CAD drawing (residential, commercial, or public space) and generate a standardized JSON prompt in our format.

**How to Use:**
1. Upload your CAD floor plan to Vision AI (e.g., Gemini Pro Vision, GPT-4 Vision, Claude 3.5 Sonnet)
2. Copy and paste the JSON Generator Prompt Template (see below)
3. AI will systematically scan your floor plan and output a complete JSON prompt
4. Review and use the generated JSON for visualization tasks

**Benefits:**
- ✅ Ensures complete room coverage (no missed spaces)
- ✅ Automates unique naming standards
- ✅ Applies constraint-oriented approach
- ✅ Reduces manual analysis errors
- ✅ Works for residential, commercial, and public spaces

<details>
<summary>📋 Click to View JSON Generator Prompt Template</summary>

Copy the entire prompt and use it with your CAD floor plan:

```markdown
# CAD Floor Plan JSON Prompt Generator

> **Purpose**: Analyze uploaded CAD floor plans and generate standardized JSON prompts.

## Vision AI Instructions

You are a professional architectural analyst. **Exhaustively analyze** the uploaded CAD floor plan and generate a structured JSON prompt for converting it into a photorealistic colored top view.

### 1. Complete Spatial Analysis

Execute the following scanning procedures in order:

#### A. Grid Scan Method
- Divide the floor plan into a 3x3 grid
- Systematically scan each grid cell
- Identify all enclosed or semi-enclosed spaces

#### B. Wall Tracing Method
- Trace clockwise along the perimeter walls
- Identify every space enclosed by walls
- Include small rooms (storage, closets, powder rooms)

#### C. Functional Space Checklist (Universal)
Verify you have identified all applicable categories:

**For ANY Space Type:**
- [ ] Primary Function Areas
- [ ] Service/Support Areas (Kitchen, Bathroom, Utility)
- [ ] Storage Spaces (Wardrobes, Closets, Storage Rooms)
- [ ] Circulation Spaces (Entrance, Lobby, Hallway, Stairs)
- [ ] Utility/MEP Spaces (Equipment Room, Server Room)
- [ ] Outdoor/Semi-outdoor Spaces (Balcony, Terrace, Courtyard)

**Space Type Examples:**
- Residential: Living Room, Bedroom, Bathroom
- Commercial: Workstation, Office, Meeting Room, Pantry
- Retail: Sales Area, Fitting Room, Stockroom
- Hospitality: Guest Room, Lobby, Restaurant, Gym
- Public: Waiting Area, Reception, Restroom, Exhibition Hall

#### D. Built-in Element Checklist
- [ ] Floor Fixtures
- [ ] Wall Fixtures (Upper Cabinets)
- [ ] Architectural Niches (Walk-in Closets)
- [ ] Sanitary Ware

### 2. Room Naming Standards

**Unique Naming Rule**: Rooms of the same type MUST have unique numbers:
- ✅ Correct: "Bedroom 2", "Bedroom 3", "Storage 1"
- ❌ Incorrect: "Bedroom", "Bedroom" (Duplicate)

### 3. Key Rules

1. **No Estimated Dimensions**: Do not include dimensions like "120x60cm"
2. **No Color Codes**: Do not include codes like "#D4B896"
3. **Focus on Constraints**: Use `independence_rule`, `COUNT_CRITICAL`, `separation_rule`
4. **Task Field**: Must explicitly mention "uploaded"

### 4. Output Format

Provide:
1. Brief Analysis Summary (Total rooms, categories)
2. Complete JSON Prompt in a code block

Use the JSON structure specification below.

**Now analyze the uploaded CAD and generate the JSON prompt.**
```

</details>

<details>
<summary>Click to Expand Full JSON Specification</summary>

```json
{
  "task": "Convert uploaded CAD floor plan to photorealistic colored top view",
  "input_specification": {
    "source": "uploaded CAD drawing",
    "constraint": "Must use uploaded image as sole spatial reference",
    "prohibition": "Do not generate alternative layouts",
    "verification": "Output layout must match input exactly"
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
      "rendering_rule": "Show as built-in space with opening, not standalone cabinet",
      "DO_NOT_render_as": [
        "wardrobe",
        "cabinet",
        "armoire",
        "furniture"
      ]
    },
    {
      "feature_id": "kitchen_upper_cabinets",
      "location": "kitchen",
      "category": "ARCHITECTURAL_not_furniture",
      "rendering_rule": "Wall-mounted upper cabinets visible in top view"
    }
  ],
  "rooms": [
    {
      "id": "living_room",
      "label": "Living Room",
      "flooring_material": "Light Oak Wood",
      "furniture_list": [
        {
          "item": "Sectional Sofa",
          "configuration": "L-shaped",
          "quantity": 1
        },
        {
          "item": "Chaise Lounge",
          "quantity": 1,
          "independence_rule": "Must be separate from sectional sofa",
          "placement_rule": "Angled placement",
          "CRITICAL": "Distinct independent angled piece"
        },
        {
          "item": "Coffee Table",
          "quantity": 1,
          "material": "Wood"
        },
        {
          "item": "Round Ottomans",
          "quantity": 2,
          "shape": "Round",
          "independence_rule": "Distinct from coffee table",
          "COUNT_CRITICAL": "Exactly 2 independent round pieces visible"
        },
        {
          "item": "TV Stand",
          "quantity": 1,
          "material": "Wood"
        },
        {
          "item": "Rug",
          "quantity": 1
        }
      ]
    },
    {
      "id": "dining_area",
      "label": "Dining Room",
      "flooring_material": "Tile",
      "furniture_list": [
        {
          "item": "Dining Table",
          "quantity": 1,
          "seating_capacity": 8,
          "material": "Wood"
        },
        {
          "item": "Dining Chairs",
          "quantity": 8,
          "arrangement": "4 on each long side",
          "COUNT_CRITICAL": "Exactly 8 chairs all visible"
        }
      ]
    },
    {
      "id": "kitchen",
      "label": "Kitchen",
      "flooring_material": "Tile",
      "furniture_list": [
        {
          "item": "Kitchen Island",
          "quantity": 1,
          "countertop_material": "White Quartz"
        },
        {
          "item": "Bar Stools",
          "quantity": 4,
          "placement": "Along island",
          "COUNT_CRITICAL": "Exactly 4 stools at island"
        }
      ],
      "fixtures": [
        {
          "item": "Sink",
          "quantity": 1,
          "type": "Undermount"
        },
        {
          "item": "Stovetop",
          "quantity": 1
        }
      ]
    },
    {
      "id": "master_bedroom",
      "label": "Master Bedroom",
      "flooring_material": "Wood",
      "furniture_list": [
        {
          "item": "Bed",
          "type": "King Size",
          "quantity": 1
        },
        {
          "item": "Nightstands",
          "quantity": 2,
          "placement": "Symmetrical on both sides",
          "COUNT_CRITICAL": "Exactly 2, one on each side"
        },
        {
          "item": "Bench",
          "quantity": 1,
          "location": "End of bed"
        }
      ],
      "architectural_reference": "Includes Walk-in Closet"
    },
    {
      "id": "bedroom_2",
      "label": "Bedroom 2",
      "flooring_material": "Wood",
      "furniture_list": [
        {
          "item": "Single Bed",
          "quantity": 1
        },
        {
          "item": "Desk",
          "quantity": 1
        },
        {
          "item": "Desk Chair",
          "quantity": 1
        },
        {
          "item": "Wardrobe",
          "quantity": 1,
          "type": "Freestanding Furniture"
        }
      ]
    },
    {
      "id": "master_bathroom",
      "label": "Master Bath",
      "flooring_material": "Marble Tile",
      "fixtures": [
        {
          "item": "Bathtub",
          "quantity": 1
        },
        {
          "item": "Shower Stall",
          "quantity": 1,
          "separation_rule": "Separate from bathtub",
          "CRITICAL": "Two independent fixtures: Shower AND Bathtub"
        },
        {
          "item": "Toilet",
          "quantity": 1
        },
        {
          "item": "Vanity Sink",
          "sink_count": 2,
          "type": "Double Vanity",
          "COUNT_CRITICAL": "Exactly 2 sinks"
        }
      ],
      "total_fixture_verification": 4
    },
    {
      "id": "secondary_bathroom",
      "label": "Bath 2",
      "flooring_material": "Tile",
      "fixtures": [
        {
          "item": "Shower Stall",
          "quantity": 1,
          "NO_BATHTUB": true,
          "CRITICAL": "Shower ONLY, absolutely NO bathtub"
        },
        {
          "item": "Toilet",
          "quantity": 1
        },
        {
          "item": "Vanity Sink",
          "sink_count": 1,
          "type": "Single Vanity",
          "COUNT_CRITICAL": "Exactly 1 sink"
        }
      ],
      "total_fixture_verification": 3
    },
    {
      "id": "entrance",
      "label": "Entrance",
      "flooring_material": "Tile",
      "furniture_list": [],
      "usage_note": "Circulation space, minimal or no furniture"
    },
    {
      "id": "storage_1",
      "label": "Storage 1",
      "flooring_material": "Tile",
      "furniture_list": [],
      "usage": "Storage"
    },
    {
      "id": "powder_room",
      "label": "Powder Room",
      "flooring_material": "Tile",
      "fixtures": [
        {
          "item": "Toilet",
          "quantity": 1
        },
        {
          "item": "Vanity Sink",
          "sink_count": 1,
          "type": "Small Single"
        }
      ],
      "note": "Guest Restroom"
    },
    {
      "id": "bathroom_1",
      "label": "Bath 1",
      "flooring_material": "Tile",
      "fixtures": [
        {
          "item": "Shower Stall",
          "quantity": 1
        },
        {
          "item": "Toilet",
          "quantity": 1
        },
        {
          "item": "Vanity Sink",
          "sink_count": 1,
          "type": "Single"
        }
      ]
    },
    {
      "id": "bedroom_3",
      "label": "Bedroom 3",
      "flooring_material": "Wood",
      "furniture_list": [
        {
          "item": "Single Bed",
          "quantity": 1
        },
        {
          "item": "Desk",
          "quantity": 1
        },
        {
          "item": "Desk Chair",
          "quantity": 1
        },
        {
          "item": "Wardrobe",
          "quantity": 1,
          "type": "Freestanding"
        }
      ]
    },
    {
      "id": "ensuite_bathroom",
      "label": "Ensuite",
      "flooring_material": "Tile",
      "fixtures": [
        {
          "item": "Shower Stall",
          "quantity": 1,
          "NO_BATHTUB": true
        },
        {
          "item": "Toilet",
          "quantity": 1
        },
        {
          "item": "Vanity Sink",
          "sink_count": 1,
          "type": "Single"
        }
      ],
      "note": "Private bath for Bedroom 3"
    },
    {
      "id": "storage_2",
      "label": "Storage 2",
      "flooring_material": "Tile",
      "furniture_list": [],
      "usage": "Storage"
    }
  ],
  "empty_spaces": [
    {
      "id": "balcony",
      "label": "Balcony",
      "flooring_material": "Decking",
      "furniture_list": [],
      "plants": [],
      "decorative_items": [],
      "CRITICAL_CONSTRAINT": "Must remain completely empty",
      "absolute_prohibition": [
        "NO_furniture",
        "NO_plants",
        "NO_pots",
        "NO_decor",
        "NO_items"
      ],
      "rendering_rule": "Show flooring only, nothing else"
    }
  ],
  "strict_constraints": {
    "count_accuracy": {
      "dining_chairs": {
        "exact": 8,
        "verification": "Count all 8 visible"
      },
      "bar_stools": {
        "exact": 4,
        "verification": "All 4 at island"
      },
      "round_ottomans": {
        "exact": 2,
        "verification": "Two distinct pieces"
      },
      "bedside_tables": {
        "exact": 2,
        "verification": "One on each side"
      },
      "master_bath_sinks": {
        "exact": 2,
        "verification": "Double vanity"
      },
      "secondary_bath_sinks": {
        "exact": 1,
        "verification": "Single vanity only"
      }
    },
    "independence_requirements": [
      {
        "item": "Chaise Lounge",
        "must_be_separate_from": "Sectional Sofa",
        "visual_proof": "Distinct angled piece"
      },
      {
        "item": "Round Ottomans",
        "must_be_separate_from": "Coffee Table",
        "visual_proof": "Two independent round shapes"
      },
      {
        "item": "Master Shower",
        "must_be_separate_from": "Bathtub",
        "visual_proof": "Two separate fixtures"
      }
    ],
    "categorical_distinctions": {
      "walk_in_closet": "Architectural Feature",
      "bedroom_wardrobes": "Furniture",
      "kitchen_upper_cabinets": "Architectural Feature"
    },
    "fixture_clarity": {
      "master_bathroom": "Has BOTH Bathtub AND Shower",
      "secondary_bathroom": "Shower ONLY, NO Bathtub",
      "ensuite_bathroom": "Shower ONLY, NO Bathtub"
    },
    "prohibition_list": {
      "no_added_decorative_items": [
        "Plants",
        "Vases",
        "Art",
        "Sculptures",
        "Pillows",
        "Table settings",
        "Books",
        "Accessories"
      ],
      "empty_space_enforcement": {
        "balcony": "Absolutely NO items allowed",
        "entrance": "Minimal or empty"
      }
    },
    "rendering_validation": {
      "no_added_items_rule": "Strictly render ONLY items corresponding to CAD symbols",
      "no_removed_items_rule": "All CAD elements must appear",
      "no_merged_elements_rule": "Independent items remain independent",
      "no_hallucinated_features_rule": "Do not invent architectural elements"
    }
  },
  "verification_checklist": {
    "room_count": 15,
    "furniture_count": 28,
    "fixture_count": 7,
    "architectural_features": 2,
    "empty_spaces": 2,
    "mandatory_verifications": [
      "Walk-in Closet as architectural feature",
      "Kitchen Upper Cabinets visible",
      "Balcony completely empty",
      "Chaise Lounge independent and angled",
      "2 Ottomans independent and visible",
      "4 Bar Stools at island",
      "8 Dining Chairs present",
      "2 Nightstands symmetrical",
      "Master Bath has separate Shower and Tub",
      "Master Bath has 2 sinks",
      "Bath 2 has Shower ONLY",
      "Bath 2 has 1 sink",
      "Ensuite has Shower ONLY"
    ]
  }
}
```

</details>

---

#### 💡 Tips

- **Iterative Generation**: Natural language prompts work best iteratively. Generate 2-3 variations, pick the best one, and refine details with simple image editing tools (Photoshop, Figma, Canva). This hybrid workflow often beats trying to perfect everything in a single prompt.
- **Check JSON Completeness**: Ensure all rooms from the CAD are included in the JSON before submitting. Missing furniture (like ottomans or chaise) will not appear in the output.
- **Material Consistency**: Keep flooring materials consistent across connected spaces (e.g., Kitchen + Dining + Entrance) for visual flow.
- **Label Clarity**: JSON prompts yield more precise text rendering. If natural language labels are unclear, use the JSON specification.
- **Style Variations**: To change the design style, modify:
  - Furniture materials (e.g., `"Linen Fabric"` → `"Leather"`)
  - Flooring colors (e.g., `"#D4B896"` → Darker/Lighter shades)
  - Overall atmosphere (`"Modern Residential"` → `"Luxury"`, `"Minimalist"`)

---
### 2.2 Landscape Zoning Map

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Site analysis diagram. Overlay color-coded zones on the site plan: Green for 'Public Park', Blue for 'Water Feature', Yellow for 'Residential'. Use hatch patterns and legends. Vector graphic style.
```

---

### 2.3 Urban Fabric Stylization

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Urban figure-ground diagram (Noli map). Render all buildings as solid black masses and all streets/open spaces as pure white. High contrast, abstract map style. Remove all vegetation and cars.
```

---

### 2.4 Office Desk Layout

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Open plan office interior. Rows of modern white desks with ergonomic black chairs. Separate the rows with planter boxes containing snake plants. Busy professional atmosphere, daytime.
```

---

## 🔧 Technical to Visual
*Technical Drawings to Visualization*

**Cases in this stage:**  
[3.1 Joinery Internal View](#31-joinery-internal-view) • [3.2 Complete Ensemble Deconstruction](#32-complete-ensemble-deconstruction) • [3.3 Lifestyle & Contextual Items](#33-lifestyle--contextual-items) • [3.4 Expression & Detail Sheet](#34-expression--detail-sheet) • [3.5 Central Subject Image](#35-central-subject-image) • [3.6 Complete Ensemble Deconstruction](#36-complete-ensemble-deconstruction) • [3.7 Lifestyle and Environmental Factors](#37-lifestyle-and-environmental-factors) • [3.8 Expression and Detail Sheet](#38-expression-and-detail-sheet) • [3.9 Floor Plan to Axonometric](#39-floor-plan-to-axonometric) • [3.10 Section to Section Perspective](#310-section-to-section-perspective) • [3.11 Exploded Axonometric](#311-exploded-axonometric) • [3.12 Sketch to Massing Model](#312-sketch-to-massing-model) • [3.13 Structural Analysis Diagram](#313-structural-analysis-diagram) • [3.14 HVAC](#314-hvac) • [3.15 Vertical Circulation](#315-vertical-circulation) • [3.16 3D Detail Callout](#316-3d-detail-callout) • [3.17 MEP X-Ray](#317-mep-x-ray) • [3.18 Construction Layers](#318-construction-layers) • [3.19 Accessibility Diagram](#319-accessibility-diagram) • [3.20 Sustainability Diagram](#320-sustainability-diagram) • [3.21 Aerial to Site Plan](#321-aerial-to-site-plan) • [3.22 3D Print Preview](#322-3d-print-preview) • [3.23 Structure Reference](#323-structure-reference) • [3.24 Iterative Process](#324-iterative-process) • [3.25 Using Text Capabilities for Annotation](#325-using-text-capabilities-for-annotation) • [3.26 Glass Railing Detail](#326-glass-railing-detail) • [3.27 "Structure Reference" is the Core](#327-structure-reference-is-the-core) • [3.28 Using "Inpainting" for Minimally Invasive Surgery](#328-using-inpainting-for-minimally-invasive-surgery) • [3.29 The Magic of Text Rendering](#329-the-magic-of-text-rendering) • [3.30 Multimodal Blending](#330-multimodal-blending) • [3.31 Main Image](#331-main-image) • [3.32 Small Image](#332-small-image) • [3.33 Small Image](#333-small-image) • [3.34 Small Image](#334-small-image)

### 3.1 Joinery Internal View

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Open view of a bespoke wardrobe. Show the internal layout: hanging rails, drawers with glass fronts, and LED strip lighting in the shelves. Finish: Dark grey melamine. Perspective view.
```

---

### 3.2 Complete Ensemble Deconstruction

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.3 Lifestyle & Contextual Items

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.4 Expression & Detail Sheet

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.5 Central Subject Image

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.6 Complete Ensemble Deconstruction

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.7 Lifestyle and Environmental Factors

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.8 Expression and Detail Sheet

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.9 Floor Plan to Axonometric

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Transform this 2D floor plan into a 3D isometric architectural drawing. Extrude the walls to a consistent height. Apply a 'clay render' style with soft ambient occlusion shadows. Keep the layout exactly as shown in the plan. Highlight circulation paths in soft blue.
```

---

### 3.10 Section to Section Perspective

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Architectural section perspective based on this line drawing. Render the cut surfaces (walls/slabs) in solid jet black (Poché). Render the interior spaces with photorealistic materials: concrete ceiling, oak flooring. Add depth and atmospheric lighting entering from the windows. 4K resolution.
```

---

### 3.11 Exploded Axonometric

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Exploded axonometric diagram of the building structure. Separate the layers vertically: foundation at the bottom, structural grid in the middle, and roof skin at the top. Style: Technical illustration, clean white background, thin linework, pastel color coding for each layer.
```

---

### 3.12 Sketch to Massing Model

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Convert this loose architectural sketch into a clean, geometric white massing model. Straighten the lines and correct the perspective. Render in a 'studio lighting' setup with sharp shadows to define the volumes. Abstract minimalism.
```

---

### 3.13 Structural Analysis Diagram

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Structural diagram. Make the non-structural walls transparent/ghosted. Highlight the columns and main beams in solid red. Show the load-bearing logic. X-ray architectural style.
```

---

### 3.14 HVAC

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Reflected ceiling plan visualization. Overlay 3D semi-transparent blue ducts showing the HVAC system. Distinguish supply diffusers (arrows out) and return vents. Maintain the layout of the lights.
```

---

### 3.15 Vertical Circulation

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Sectional circulation diagram. Highlight staircases and elevator shafts in glowing orange. Add arrows indicating upward movement. Dark background blueprint style.
```

---

### 3.16 3D Detail Callout

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Photorealistic 3D cutaway of a curtain wall detail based on this drawing. Show the layers: aluminum mullion, double glazing, rubber gasket, and insulation. Macro photography style, sharp focus on the joint.
```

---

### 3.17 MEP X-Ray

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Technical visualization. A bathroom wall rendered with 50% transparency. Reveal the copper plumbing pipes and PVC drainage pipes inside the wall cavity. Educational diagram style.
```

---

### 3.18 Construction Layers

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Layered floor construction diagram. Peel back the layers to show: 1. Concrete slab, 2. Acoustic mat, 3. Underfloor heating pipes, 4. Screed, 5. Timber finish. Label each layer.
```

---

### 3.19 Accessibility Diagram

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Accessibility analysis overlay on floor plan. Show 1.5m diameter turning circles in red dashed lines in bathrooms and hallways. Highlight wheelchair ramps in blue. Technical annotation style.
```

---

### 3.20 Sustainability Diagram

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Sustainability concept section. Show blue arrows for natural ventilation airflow through windows. Show yellow arrows for sunlight shading. Add icons for 'Solar Panels' on the roof. Educational style.
```

---

### 3.21 Aerial to Site Plan

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Convert this aerial drone photo into a flat architectural site plan diagram. Flatten the perspective to 2D top-down. Simplify trees to circles and buildings to solid shapes. Desaturated colors.
```

---

### 3.22 3D Print Preview

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Render this building model as a 3D printed object. Material: White PLA plastic with visible layer lines. Sitting on a wooden table. Depth of field blurring the background.
```

---

### 3.23 Structure Reference

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.24 Iterative Process

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.25 Using Text Capabilities for Annotation

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.26 Glass Railing Detail

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.27 "Structure Reference" is the Core

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.28 Using "Inpainting" for Minimally Invasive Surgery

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.29 The Magic of Text Rendering

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.30 Multimodal Blending

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.31 Main Image

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.32 Small Image

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.33 Small Image

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

### 3.34 Small Image

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

---

## 🎨 Material & Styling
*Materials & Styling*

**Cases in this stage:**  
[4.1 材质板转 3D 渲染](#41-材质板转-3d-渲染) • [4.2 定制柜体内部结构](#42-定制柜体内部结构) • [4.3 砖石铺贴纹理研究](#43-砖石铺贴纹理研究) • [4.4 灯光照度可视化](#44-灯光照度可视化) • [4.5 软装布艺褶皱模拟](#45-软装布艺褶皱模拟) • [4.6 异形家具曲面分析](#46-异形家具曲面分析) • [4.7 老旧材质做旧模拟](#47-老旧材质做旧模拟) • [4.8 艺术品/挂画替换](#48-艺术品挂画替换)

### 4.1 材质板转 3D 渲染

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Interior rendering of a living room using the materials from the reference image. Apply the boucle fabric to the sofa, the walnut wood to the cabinets, and the terrazzo sample to the floor. Maintain accurate texture scaling.
```

---

### 4.2 定制柜体内部结构

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Open view of a bespoke wardrobe. Show the internal layout: hanging rails, drawers with glass fronts, and LED strip lighting in the shelves. Finish: Dark grey melamine. Perspective view.
```

---

### 4.3 砖石铺贴纹理研究

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Close-up texture study of a brick wall. Arrange the bricks in a 'vertical stack bond' pattern. Bricks should be handmade terracotta with irregular edges and thick mortar joints.
```

---

### 4.4 灯光照度可视化

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Lighting visualization. A textured stone wall lit by three recessed spotlights from above. Show the realistic 'scallop' shape of the light beams and the texture relief created by grazing light.
```

---

### 4.5 软装布艺褶皱模拟

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Close-up of heavy velvet curtains pooling on a wooden floor. Show realistic fabric folds, weight, and light sheen. Color: Deep emerald green.
```

---

### 4.6 异形家具曲面分析

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Studio render of a parametric curved bench. Material: Glossy white fiberglass. Use 'zebra stripe' reflection mapping to highlight the curvature continuity.
```

---

### 4.7 老旧材质做旧模拟

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Material aging simulation. Show a copper facade panel with realistic green patina (verdigris) streaming down from the top edges, simulating 10 years of weather exposure.
```

---

### 4.8 艺术品/挂画替换

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Replace the painting on the wall with a large-scale abstract expressionist artwork in blue and gold tones. Add a frame that matches the furniture wood.
```

---

## 🖼️ Scene Rendering
*Scene Rendering*

**Cases in this stage:**  
[5.1 日夜光环境转换](#51-日夜光环境转换) • [5.2 餐厅灯光氛围模拟](#52-餐厅灯光氛围模拟) • [5.3 酒店客房标准间](#53-酒店客房标准间) • [5.4 咖啡馆氛围板](#54-咖啡馆氛围板) • [5.5 漫游关键帧生成](#55-漫游关键帧生成) • [5.6 配景人物植入](#56-配景人物植入) • [5.7 风格一致性检查](#57-风格一致性检查)

### 5.1 日夜光环境转换

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Turn this daylight photo into a night scene. Dark blue sky. Turn on the interior lights (3000K warm white). Add exterior uplighting to the trees.
```

---

### 5.2 餐厅灯光氛围模拟

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Fine dining restaurant interior. Moody, low-key lighting. Tables illuminated by focused pin-spots, leaving the surrounding areas in shadow. Velvet booth seating. Candlelight on tables.
```

---

### 5.3 酒店客房标准间

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Luxury hotel room interior. King size bed with crisp white linens and a beige throw. Floor-to-ceiling window with shear curtains. Warm bedside lamps on. Symmetrical composition.
```

---

### 5.4 咖啡馆氛围板

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Rustic coffee shop interior. Exposed brick walls, reclaimed wood tables, industrial pendant lights. Steam rising from a coffee cup in the foreground. Warm, inviting, morning light.
```

---

### 5.5 漫游关键帧生成

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Cinematic storyboard keyframes for architectural walkthrough. Frame 1: Wide shot of building exterior at dawn. Frame 2: Close up of hand opening the door. Frame 3: Eye- level view of the sunlit lobby. Consistent color grading.
```

---

### 5.6 配景人物植入

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Populate this plaza render with diverse groups of people. People walking, sitting on benches, talking. Motion blur on walking figures. Ensure shadows match the sun direction of the scene.
```

---

### 5.7 风格一致性检查

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Apply the color grading and lighting style of Reference Image A to Reference Image B. Make them look like they belong to the same photography set. Keep the content of Image B unchanged.
```

---

## ⚙️ Specialized Tasks
*Specialized Tasks*

**Cases in this stage:**  
[6.1 保留家具换硬装](#61-保留家具换硬装) • [6.2 清空房间](#62-清空房间) • [6.3 虚拟软装](#63-虚拟软装) • [6.4 厨房翻新：换门板不换布局](#64-厨房翻新换门板不换布局) • [6.5 窗外景观替换](#65-窗外景观替换) • [6.6 建筑立面改造](#66-建筑立面改造) • [6.7 增加绿植氛围](#67-增加绿植氛围) • [6.8 季节/天气变换](#68-季节天气变换) • [6.9 门头招牌设计](#69-门头招牌设计) • [6.10 货架陈列生成](#610-货架陈列生成) • [6.11 展台设计方案](#611-展台设计方案) • [6.12 品牌快闪店](#612-品牌快闪店) • [6.13 导视系统模拟](#613-导视系统模拟) • [6.14 橱窗陈列设计](#614-橱窗陈列设计) • [6.15 概念推演过程图](#615-概念推演过程图) • [6.16 渲染图转水彩手绘](#616-渲染图转水彩手绘) • [6.17 汇报排版生成](#617-汇报排版生成) • [6.18 入口对景树](#618-入口对景树)

### 6.1 保留家具换硬装

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Renovation visualization. Change the wall color to sage green and the floor to herringbone parquet. Constraint: Keep the existing sofa, coffee table, and rug exactly as they are in the photo. Do not move them.
```

---

### 6.2 清空房间

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Real estate photo editing. Remove all furniture, boxes, and clutter from this room. Show the clean, empty space with bare walls and flooring. Auto-fill the floor texture where furniture was removed.
```

---

### 6.3 虚拟软装

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Virtual staging. Furnish this empty bedroom with a Queen-sized bed, two nightstands, and a wardrobe. Style: Modern Minimalist. Ensure furniture perspective aligns with the room's vanishing points.
```

---

### 6.4 厨房翻新：换门板不换布局

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Kitchen facelift. Replace the oak cabinet doors with matte navy blue flat-panel doors. Change countertop to white marble. Keep the kitchen layout, appliances, and sink position exactly unchanged.
```

---

### 6.5 窗外景观替换

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
View substitution. Replace the white window background with a cityscape at twilight. Add realistic blue reflections of the city lights onto the interior floor.
```

---

### 6.6 建筑立面改造

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Building exterior renovation. Replace the red brick facade with sleek silver aluminum composite panels. Keep the window openings and building shape structurally identical.
```

---

### 6.7 增加绿植氛围

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Add lush indoor plants to this office lobby. Place tall Ficus trees in the corners and hanging planters from the ceiling beams. Natural, vibrant atmosphere.
```

---

### 6.8 季节/天气变换

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Change season to Winter. Cover the garden ground with snow. Trees should be bare branches. Add warm light glow coming from the house windows. Cozy winter evening.
```

---

### 6.9 门头招牌设计

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Retail storefront render. Place a 3D neon sign reading 'URBAN CAFE' above the entrance. Font style: Retro script. Color: Bright pink. Show realistic glow reflection on the glass window.
```

---

### 6.10 货架陈列生成

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Supermarket shelves visualization. Fill the shelves with neatly arranged cereal boxes and colorful packaging. Ensure distinct, non-repetitive product designs. bright, even lighting.
```

---

### 6.11 展台设计方案

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
3x3 meter exhibition booth design. Minimalist white style with a central reception counter. Large LED screen on the back wall displaying a abstract blue wave pattern. Spotlights on the counter.
```

---

### 6.12 品牌快闪店

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Pop-up store design in a mall atrium. A cylindrical structure made of translucent polycarbonate sheets. Glowing from within with purple light. Branding text 'FUTURE TECH' on the top header.
```

---

### 6.13 导视系统模拟

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Hospital corridor interior. Apply clear vinyl wayfinding graphics to the floor: A blue line with text 'Radiology' and a red line with text 'Emergency'. Perspective adjusted to match the floor plane.
```

---

### 6.14 橱窗陈列设计

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Fashion boutique window display. Two mannequins wearing avant-garde silver jackets. Background: Abstract geometric shapes suspended in air. Lighting: Dramatic purple and teal spotlights.
```

---

### 6.15 概念推演过程图

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Architectural concept diagram series. Three steps: 1. A simple cube. 2. The cube sliced diagonally. 3. The final form with terraced gardens. Style: Simple white isometric blocks with blue arrows showing the transformation.
```

---

### 6.16 渲染图转水彩手绘

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Convert this photorealistic building render into a loose watercolor sketch. Soft washes of color, pencil outlines, bleeding edges. Artistic, hand-drawn feel. Reduce detail.
```

---

### 6.17 汇报排版生成

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```
Architectural presentation board layout. Arrange the provided render (top), floor plan (bottom left), and material palette (bottom right) on a clean white background. Add a title 'PROJECT HORIZON' in minimalist sans-serif font.
```

---

### 6.18 入口对景树

#### Input

![Input Image](./assets/placeholders/input.jpg)

#### Output

![Output Image](./assets/placeholders/output.jpg)

**Prompt:**
```

```

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
