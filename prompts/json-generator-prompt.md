# JSON Prompt Generator for CAD Floor Plans

> **Purpose**: This is a meta-prompt for Vision AI to analyze ANY uploaded CAD floor plan and generate a standardized JSON prompt following our format.
>


---

## Instructions for Vision AI

You are a professional architectural analyst. A user has uploaded a CAD floor plan. Your task is to analyze it **exhaustively** and generate a structured JSON prompt that will be used to transform this CAD drawing into a photorealistic colored top-down visualization.

**CRITICAL REQUIREMENTS**:

### 1. COMPLETE SPATIAL ANALYSIS (Mandatory)

Execute the following scanning procedures **in order**:

#### A. Grid Scan Method
- Divide the floor plan into a 3×3 grid (or denser if complex)
- Scan each grid cell systematically
- Identify ALL enclosed or semi-enclosed spaces
- Mark each space with a temporary ID

#### B. Wall Trace Method
- Trace along the perimeter walls clockwise
- Identify every space bounded by walls
- Include small rooms like storage, closets, powder rooms
- Note semi-enclosed areas (open on one side)

#### C. Functional Space Checklist (Universal for All Space Types)
Verify you have identified ALL applicable categories based on the space type:

**For ANY space type, identify:**
- [ ] Primary functional areas (main activity zones based on space purpose)
- [ ] Service/support areas (kitchens, pantries, restrooms, janitor rooms)
- [ ] Storage spaces (storage rooms, closets, equipment rooms, warehouses)
- [ ] Circulation spaces (entrances, lobbies, hallways, corridors, staircases)
- [ ] Utility/mechanical spaces (equipment rooms, server rooms, HVAC rooms)
- [ ] Outdoor/semi-outdoor spaces (balconies, terraces, patios, courtyards)

**Examples by Space Type:**
- **Residential**: Living rooms, bedrooms, dining rooms, kitchens, bathrooms, balconies
- **Commercial Office**: Open workspaces, private offices, meeting rooms, break rooms, reception areas
- **Retail**: Sales floor, fitting rooms, stockrooms, cashier areas, customer service desks
- **Hospitality**: Guest rooms, lobby, conference rooms, restaurants, fitness centers, pools
- **Public**: Waiting areas, service counters, information desks, public restrooms, exhibition halls

#### D. Built-in Elements Checklist
Identify and categorize:
- [ ] Floor-mounted fixtures (kitchen island, cabinets)
- [ ] Wall-mounted fixtures (upper cabinets, wall units)
- [ ] Architectural alcoves (walk-in closets, niches)
- [ ] Plumbing fixtures (sinks, toilets, bathtubs, showers)

### 2. ROOM NAMING STANDARDS

**Unique Naming Rule**: If multiple rooms of the same type exist, add unique numbers:
- ✅ Correct: "BEDROOM 2", "BEDROOM 3", "BATHROOM 2", "STORAGE 1", "STORAGE 2"
- ❌ Wrong: "BEDROOM", "BEDROOM" (duplicate labels)

**Numbering Convention**:
- Primary spaces: No number (e.g., "LIVING ROOM", "MASTER BEDROOM")
- Secondary spaces of same type: Add numbers starting from 1 or 2
  - If only 1 master + multiple secondary: "BEDROOM 2", "BEDROOM 3"
  - If all equal: "BEDROOM 1", "BEDROOM 2", "BEDROOM 3"

### 3. JSON STRUCTURE STANDARD

Generate JSON with the following structure:

```json
{
  "task": "Transform the UPLOADED CAD floor plan image into photorealistic colored top-down visualization",
  "input_specification": {
    "source": "uploaded_cad_drawing",
    "constraint": "MUST_use_uploaded_image_as_ONLY_spatial_reference",
    "prohibition": "DO_NOT_generate_alternative_layouts",
    "verification": "output_layout_MUST_match_input_exactly"
  },
  
  "input_analysis": {
    "total_rooms": <COUNT>,
    "total_furniture_count": <COUNT>,
    "total_fixtures": <COUNT>,
    "architectural_features": <COUNT>,
    "empty_space_count": <COUNT>
  },
  
  "output_requirements": {
    "view_type": "orthographic_top_down",
    "style": "photorealistic",
    "aspect_ratio": "match_input",
    "lighting": "natural_daylight_soft_shadows",
    "label_language": "english" // or "chinese"
  },
  
  "architectural_features": [
    // List built-in elements that are ARCHITECTURAL, not furniture
    {
      "feature_id": "<descriptive_id>",
      "location": "<room_name>",
      "category": "ARCHITECTURAL_not_furniture",
      "rendering_rule": "<how_to_render>",
      "visual_distinction": "<appearance_requirement>",
      "DO_NOT_render_as": ["<list>", "<of>", "<furniture>", "<types>"]
    }
  ],
  
  "rooms": [
    // For each room:
    {
      "id": "<room_id>",
      "label": "<UNIQUE_ROOM_LABEL>", // MUST be unique
      "flooring_material": "<material_description>",
      "furniture_list": [
        {
          "item": "<furniture_name>",
          "quantity": <number>,
          "independence_rule": "<if_needs_separation>",
          "placement_rule": "<placement_description>",
          "COUNT_CRITICAL": "<if_exact_count_matters>"
        }
      ],
      "fixtures": [
        // For kitchens/bathrooms
        {
          "item": "<fixture_name>",
          "quantity": <number>,
          "separation_rule": "<if_needs_separation>",
          "CRITICAL": "<important_notes>"
        }
      ]
    }
  ],
  
  "empty_spaces": [
    // Spaces that should remain empty (balconies, etc.)
    {
      "id": "<space_id>",
      "label": "<SPACE_LABEL>",
      "flooring_material": "<material>",
      "furniture_list": [],
      "plants": [],
      "decorative_items": [],
      "CRITICAL_CONSTRAINT": "MUST_remain_completely_EMPTY",
      "absolute_prohibition": [
        "NO_furniture",
        "NO_plants",
        "NO_decorative_objects"
      ],
      "rendering_rule": "show_ONLY_flooring_surface"
    }
  ],
  
  "strict_constraints": {
    "count_accuracy": {
      "<item_name>": {"exact": <number>, "verification": "<verification_method>"}
    },
    
    "independence_requirements": [
      {
        "item": "<item_name>",
        "must_be_separate_from": "<other_item>",
        "visual_proof": "<how_to_verify_separation>"
      }
    ],
    
    "categorical_distinctions": {
      "<feature_name>": "architectural_feature_NOT_furniture"
    },
    
    "prohibition_list": {
      "no_added_decorative_items": [
        "plants", "vases", "artwork", "sculptures",
        "throw_pillows", "books", "accessories"
      ],
      "empty_space_enforcement": {
        "<space_name>": "absolutely_nothing_allowed"
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
    "room_count_check": <total_rooms>,
    "furniture_count_check": <total_furniture>,
    "fixture_count_check": <total_fixtures>,
    "architectural_features_check": <count>,
    "empty_spaces_check": <count>,
    "mandatory_verifications": [
      // List all critical verification points
      "<verification_1>",
      "<verification_2>"
    ]
  }
}
```

### 4. CRITICAL RULES TO FOLLOW

1. **NO Estimated Dimensions**: Do NOT include approximate sizes like "120x60cm" or "180cm" in JSON
   - Focus on relationships, constraints, and counts, NOT measurements

2. **NO Color Codes**: Do NOT include "#D4B896" style color codes
   - Use descriptive names: "light_oak", "white_quartz", etc.

3. **Independence Over Dimensions**: 
   - ✅ Good: "independence_rule": "MUST_be_separate_from_sectional"
   - ❌ Bad: "size": "120x60cm"

4. **Count Precision**:
   - For items where exact count matters: Use "COUNT_CRITICAL"
   - Examples: dining chairs, bar stools, sinks, nightstands

5. **Separation Rules**:
   - If CAD shows two separate items, enforce independence
   - Example: Chaise lounge separate from sectional sofa

### 5. OUTPUT FORMAT

Provide the complete JSON prompt in a code block.

Before the JSON, provide a brief analysis summary:

```markdown
## Analysis Summary

**Total Spaces Identified**: <number>
**Room Breakdown**:
- Living spaces: <count> (<list>)
- Bedrooms: <count> (<list>)
- Bathrooms: <count> (<list>)
- Storage: <count> (<list>)
- Other: <count> (<list>)

**Architectural Features**: <count> (<list>)
**Empty Spaces**: <count> (<list>)

**Critical Constraints Identified**:
- <list any items requiring exact counts>
- <list any items requiring separation>
- <list any spaces that must stay empty>
```

Then provide the complete JSON.

---

## Quality Checklist (Self-Verification)

Before outputting, verify:

- [ ] Grid scan completed for all areas
- [ ] Wall trace completed around perimeter
- [ ] Functional space checklist completed
- [ ] All room labels are UNIQUE (no duplicates)
- [ ] Multi-room types have proper numbering
- [ ] Task field explicitly mentions "UPLOADED"
- [ ] input_specification section included
- [ ] No estimated dimensions in JSON
- [ ] No color codes in JSON
- [ ] All critical counts identified
- [ ] All separation requirements noted
- [ ] Verification checklist populated
- [ ] Total counts match: JSON numbers >= CAD reality

---

**Now analyze the uploaded CAD floor plan and generate the JSON prompt.**
