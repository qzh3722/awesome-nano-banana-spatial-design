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
[1.1 Hand Sketch to Rendering](#) • [1.2 Multi-Style Concept Comparison](#) • [1.3 Mood Board Generation](#) • [Wardrobe Deconstruction](#wardrobe-deconstruction) • [3D Storefront Render](#3d-storefront-render)



---

## 📐 Space Planning
*Layout optimization & circulation design*

**Cases in this stage:**  
[▶ 2.1 CAD Floor Plan to Colored Floor Plan](#21-cad-floor-plan-to-colored-floor-plan) • [2.2 Furniture Layout Variations](#) • [2.3 Circulation Analysis](#) • [Colored Floor Plan](#colored-floor-plan) • [Landscape Zoning Map](#landscape-zoning-map) • [Urban Fabric Stylization](#urban-fabric-stylization) • [Office Desk Layout](#office-desk-layout)

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
[3.1 Elevation to Street View](#) • [3.2 Section to Interior Perspective](#) • [**Central Subject Image:**](#**central-subject-image:**) • [Photorealistic Product Shots](#photorealistic-product-shots) • [**Lifestyle & Contextual Items:**](#**lifestyle-&-contextual-items:**) • [**Expression & Detail Sheet:**](#**expression-&-detail-sheet:**) • [** 中心主题图像:**](#**-中心主题图像:**) • [** 完整整体解构（照片级产品照片） :**](#**-完整整体解构（照片级产品照片）-:**) • [** 生活方式和环境因素:**](#**-生活方式和环境因素:**) • [** 表达式和详细信息表:**](#**-表达式和详细信息表:**) • [Floor Plan to Axonometric](#floor-plan-to-axonometric) • [Section to Section Perspective](#section-to-section-perspective) • [Exploded Axonometric](#exploded-axonometric) • [Sketch to Massing Model](#sketch-to-massing-model) • [Structural Analysis Diagram](#structural-analysis-diagram) • [HVAC](#hvac) • [Vertical Circulation](#vertical-circulation) • [3D Detail Callout](#3d-detail-callout) • [MEP X-Ray](#mep-x-ray) • [Construction Layers](#construction-layers) • [Accessibility Diagram](#accessibility-diagram) • [Sustainability Diagram](#sustainability-diagram) • [Aerial to Site Plan](#aerial-to-site-plan) • [3D Print Preview](#3d-print-preview) • [Structure Reference](#structure-reference) • [Iterative Process](#iterative-process) • [利用文本能力做标注： Nano Banana Pro 的文本能力很强，可以直接在](#利用文本能力做标注：-nano-banana-pro-的文本能力很强，可以直接在) • [玻璃栏杆节点](#玻璃栏杆节点) • ["Structure Reference" 是核心中的核心：](#"structure-reference"-是核心中的核心：) • [利用"Inpainting"进行微创手术：](#利用"inpainting"进行微创手术：) • [文本渲染的妙用：](#文本渲染的妙用：) • [Multimodal Blending](#multimodal-blending) • [Top](#top) • [Bottom Left](#bottom-left) • [Bottom Middle](#bottom-middle) • [Bottom Right](#bottom-right)















---

## 🎨 Material & Styling
*Material refinement & cost optimization*

**Cases in this stage:**  
[4.1 Material Scheme Comparison](#) • [4.2 Material Downgrade for Budget](#) • [Moodboard to Render](#moodboard-to-render) • [Joinery Internal View](#joinery-internal-view) • [Pattern Generation](#pattern-generation) • [Lighting Falloff](#lighting-falloff) • [Fabric Physics](#fabric-physics) • [Curved Surface Analysis](#curved-surface-analysis) • [Weathering Simulation](#weathering-simulation) • [Art Staging](#art-staging)









---

## 🖼️ Scene Rendering
*Final presentation quality renders*

**Cases in this stage:**  
[5.1 Multi-Angle Interior](#) • [5.2 Day/Night Lighting](#) • [Day to Night](#day-to-night) • [Restaurant Ambiance](#restaurant-ambiance) • [Hotel Room Visualization](#hotel-room-visualization) • [Cafe Mood Visualization](#cafe-mood-visualization) • [Walkthrough Keyframes](#walkthrough-keyframes) • [Entourage Population](#entourage-population) • [Style Consistency Check](#style-consistency-check)








---

## ⚙️ Specialized Tasks
*Special use cases & advanced features*

**Cases in this stage:**  
[6.1 Multilingual Signage](#) • [6.2 Seasonal Variations](#) • [6.3 On-Site Quick Solutions](#) • [Keep Furniture, Change Room](#keep-furniture,-change-room) • [Declutter / Empty Room](#declutter--empty-room) • [Virtual Staging](#virtual-staging) • [Kitchen Facelift](#kitchen-facelift) • [View Replacement](#view-replacement) • [Facade Cladding Swap](#facade-cladding-swap) • [Biophilic Injection](#biophilic-injection) • [Seasonal Variation](#seasonal-variation) • [Storefront Signage](#storefront-signage) • [Visual Merchandising](#visual-merchandising) • [Exhibition Booth](#exhibition-booth) • [Pop-up Store](#pop-up-store) • [Wayfinding Mockup](#wayfinding-mockup) • [Window Display](#window-display) • [Concept Diagram Sequence](#concept-diagram-sequence) • [Render to Watercolor](#render-to-watercolor) • [Presentation Board Layout](#presentation-board-layout) • [入口对景树](#入口对景树)


















---


### Keep Furniture, Change Room

**Prompt:**
```
Renovation visualization. Change the wall color to sage green and the floor to herringbone parquet. Constraint: Keep the existing sofa, coffee table, and rug exactly as they are in the photo. Do not move them.
```

---

### Declutter / Empty Room

**Prompt:**
```
Real estate photo editing. Remove all furniture, boxes, and clutter from this room. Show the clean, empty space with bare walls and flooring. Auto-fill the floor texture where furniture was removed.
```

---

### Virtual Staging

**Prompt:**
```
Virtual staging. Furnish this empty bedroom with a Queen-sized bed, two nightstands, and a wardrobe. Style: Modern Minimalist. Ensure furniture perspective aligns with the room's vanishing points.
```

---

### Kitchen Facelift

**Prompt:**
```
Kitchen facelift. Replace the oak cabinet doors with matte navy blue flat-panel doors. Change countertop to white marble. Keep the kitchen layout, appliances, and sink position exactly unchanged.
```

---

### View Replacement

**Prompt:**
```
View substitution. Replace the white window background with a cityscape at twilight. Add realistic blue reflections of the city lights onto the interior floor.
```

---

### Facade Cladding Swap

**Prompt:**
```
Building exterior renovation. Replace the red brick facade with sleek silver aluminum composite panels. Keep the window openings and building shape structurally identical.
```

---

### Biophilic Injection

**Prompt:**
```
Add lush indoor plants to this office lobby. Place tall Ficus trees in the corners and hanging planters from the ceiling beams. Natural, vibrant atmosphere.
```

---

### Seasonal Variation

**Prompt:**
```
Change season to Winter. Cover the garden ground with snow. Trees should be bare branches. Add warm light glow coming from the house windows. Cozy winter evening.
```

---

### Storefront Signage

**Prompt:**
```
Retail storefront render. Place a 3D neon sign reading 'URBAN CAFE' above the entrance. Font style: Retro script. Color: Bright pink. Show realistic glow reflection on the glass window.
```

---

### Visual Merchandising

**Prompt:**
```
Supermarket shelves visualization. Fill the shelves with neatly arranged cereal boxes and colorful packaging. Ensure distinct, non-repetitive product designs. bright, even lighting.
```

---

### Exhibition Booth

**Prompt:**
```
3x3 meter exhibition booth design. Minimalist white style with a central reception counter. Large LED screen on the back wall displaying a abstract blue wave pattern. Spotlights on the counter.
```

---

### Pop-up Store

**Prompt:**
```
Pop-up store design in a mall atrium. A cylindrical structure made of translucent polycarbonate sheets. Glowing from within with purple light. Branding text 'FUTURE TECH' on the top header.
```

---

### Wayfinding Mockup

**Prompt:**
```
Hospital corridor interior. Apply clear vinyl wayfinding graphics to the floor: A blue line with text 'Radiology' and a red line with text 'Emergency'. Perspective adjusted to match the floor plane.
```

---

### Window Display

**Prompt:**
```
Fashion boutique window display. Two mannequins wearing avant-garde silver jackets. Background: Abstract geometric shapes suspended in air. Lighting: Dramatic purple and teal spotlights.
```

---

### Concept Diagram Sequence

**Prompt:**
```
Architectural concept diagram series. Three steps: 1. A simple cube. 2. The cube sliced diagonally. 3. The final form with terraced gardens. Style: Simple white isometric blocks with blue arrows showing the transformation.
```

---

### Render to Watercolor

**Prompt:**
```
Convert this photorealistic building render into a loose watercolor sketch. Soft washes of color, pencil outlines, bleeding edges. Artistic, hand-drawn feel. Reduce detail.
```

---

### Presentation Board Layout

**Prompt:**
```
Architectural presentation board layout. Arrange the provided render (top), floor plan (bottom left), and material palette (bottom right) on a clean white background. Add a title 'PROJECT HORIZON' in minimalist sans-serif font.
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
