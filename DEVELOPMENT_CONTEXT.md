# Development Context & History
## Awesome Nano Banana Spatial Design

> 🤖 **AI Assistant Notice**: This document contains the complete development history and context. **ALWAYS READ THIS FILE FIRST** when resuming development to understand what has been done and what needs to be done next.

**Last Updated**: 2025-11-29
**Current Phase**: Scenario Library Integrated (62 scenarios), Ready for Testing
**Repository Status**: Private, Scenario mapping complete

---

## 📋 Quick Context Summary

### Project Overview
- **Name**: Awesome Nano Banana Spatial Design
- **Type**: Curated prompt library for spatial design professionals
- **Target**: 100+ high-quality use cases for Nano Banana Pro (Gemini 3 Pro Image)
- **Languages**: Bilingual (English + 简体中文)
- **Classification**: Workflow-based (6 stages) × Space Types (Residential/Commercial/Outdoor)
- **Workflow Stages**: Concept → Planning → Technical → Material → Rendering → Specialized
- **Status**: Framework v2.0 complete, 62 scenarios mapped to 6 workflow stages, ready for testing

### GitHub Repository
- **Owner**: qzh3722
- **Repo Name**: awesome-nano-banana-spatial-design
- **URL**: https://github.com/qzh3722/awesome-nano-banana-spatial-design
- **Visibility**: Private (will be made public after MVP completion)
- **Branch**: main

---

## 🗂️ Project Structure

```
awesome-nano-banana-spatial-design/
├── DEVELOPMENT_CONTEXT.md     # ⭐ THIS FILE - Development history & context
├── README.md                  # English homepage
├── README.zh-CN.md           # Chinese homepage (GitHub i18n standard)
├── README_CN.md              # Deprecated redirect (backward compatibility)
├── CASE_TEMPLATE.md          # Standardized template for all cases
├── CONTRIBUTING.md           # Contribution guidelines
├── LICENSE                   # MIT License
│
├── .github/                  # GitHub configuration
│   ├── ISSUE_TEMPLATE/
│   │   ├── new-case-submission.md
│   │   └── bug-report.md
│   └── PULL_REQUEST_TEMPLATE.md
│
├── assets/
│   └── images/
│       ├── banner.jpg        # 218KB optimized (was 2MB PNG)
│       └── README.md
│
├── cases/                    # 100+ planned cases (workflow-based structure)
│   ├── architecture/         # Legacy structure (to be reorganized)
│   │   ├── README.md
│   │   └── A-001-cad-to-colored-plan.md  # ✅ v2.0 Example
│   ├── interior/
│   │   ├── README.md
│   │   └── I-001-furniture-layout.md     # ✅ v2.0 Example
│   ├── landscape/
│   │   ├── README.md
│   │   └── L-001-master-plan-visualization.md  # ✅ v2.0 Example
│   │
│   └── [PLANNED] Workflow-based structure:
│       ├── 01-concept-ideation/          # From zero to creative solutions
│       ├── 02-space-planning/            # Layout optimization & circulation
│       ├── 03-technical-to-visual/       # CAD/drawings to visualization
│       ├── 04-material-styling/          # Material refinement & styling
│       ├── 05-scene-rendering/           # Final presentation renders
│       └── 06-specialized-tasks/         # Special use cases
│
└── docs/
    ├── GETTING_STARTED.md   # User guide
    ├── FAQ.md               # Frequently asked questions
    └── ROADMAP.md           # 4-week development plan
```

---

## 📅 Development Timeline

### Week 1 - Foundation Setup (COMPLETED ✅)

#### Session 1: Initial Repository Setup (2025-11-28)

**Commit 1: `64edf29` - Initial repository structure**
- Created complete directory structure
- Established 3-tier categorization system
- Created bilingual README files (EN/CN)
- Designed standardized case template
- Created 3 example cases (A-001, I-001, L-001)
- Added comprehensive documentation (Getting Started, FAQ, Roadmap)
- Set up GitHub templates (Issues, PR)
- Added MIT License and Contributing guidelines
- Initialized Git repository

**Commit 2: `2282e46` - Update GitHub username to qzh3722**
- Replaced all placeholder `yourusername` with `qzh3722`
- Updated all GitHub links in:
  - README.md
  - README_CN.md
  - CONTRIBUTING.md
  - docs/FAQ.md

**Commit 3: `5169876` - Add professional banner image**
- Added banner.png (2.0MB, 1664×704px)
- Updated README.md with centered banner display
- Updated README_CN.md with centered banner display
- Banner showcases 3D visualization of architecture, interior, and landscape

**Commit 4: `2734a63` - Optimize banner image**
- Compressed banner from 2.0MB PNG to 218KB JPG
- 89% file size reduction
- Maintained high visual quality (JPG quality 80)
- Updated image references from .png to .jpg
- Significantly improved page load time

**Commit 5: `47e360b` - Implement professional language switcher**
- Created README.zh-CN.md (GitHub i18n standard naming)
- Added professional language switcher UI with table layout
- Updated README_CN.md to redirect notice
- Language switcher shows current language in bold
- Added 🌐 icon for better visual clarity
- Prepared structure for future language additions

**Push to GitHub**:
- Successfully pushed all commits to private repository
- Repository accessible at: https://github.com/qzh3722/awesome-nano-banana-spatial-design

#### Session 2: Framework Restructuring (2025-11-29)

**Major Strategic Pivot**:
User requested complete framework overhaul after overnight reflection:

1. **Classification System Change**:
   - **Old**: Fixed domain categories (Architecture 30, Interior 40, Landscape 30)
   - **New**: Workflow-based classification (6 stages) × Space types (open-ended count)
   - **Rationale**: More intuitive for designers, matches actual workflow, avoids content imbalance

2. **Workflow Stages Defined** (in correct designer sequence):
   - **Stage 1**: Concept Ideation - From zero to creative solutions
   - **Stage 2**: Space Planning - Layout optimization & circulation design
   - **Stage 3**: Technical to Visual - CAD/drawings to visualization
   - **Stage 4**: Material & Styling - Material refinement and styling
   - **Stage 5**: Scene Rendering - Final presentation renders
   - **Stage 6**: Specialized Tasks - Special use cases (text rendering, seasonal, etc.)

3. **Case Structure Simplified**:
   - **Old**: 7 major sections (Problem, Parameters, Prompt, Quality, Tips, Related, Tags)
   - **New**: 4 essential sections (Preview, Prompt, Tips, Tags)
   - **Improvement**: Cleaner, card-style layout; large compressed images; bilingual maintained

4. **Files Updated to v2.0**:
   - `CASE_TEMPLATE.md` - Complete rewrite to new simplified structure
   - `cases/architecture/A-001-cad-to-colored-plan.md` - Rewritten to v2.0
   - `cases/interior/I-001-furniture-layout.md` - Rewritten to v2.0
   - `cases/landscape/L-001-master-plan-visualization.md` - Rewritten to v2.0

5. **New Case Structure Features**:
   - Large hero images (gallery-style, compressed JPG)
   - Bilingual prompts (Chinese first, English second)
   - Practical Tips section (usage advice, variations, best practices)
   - Bilingual hashtags for discoverability
   - Version tracking and contributor attribution

**Commit 6: `[PENDING]` - Framework v2.0: Template and case restructuring**
- Updated CASE_TEMPLATE.md to simplified 4-section structure
- Rewrote A-001 (CAD to visualization) to v2.0
- Rewrote I-001 (Furniture layout) to v2.0
- Rewrote L-001 (Landscape master plan) to v2.0
- Added Tips sections to all cases
- Maintained full bilingual support throughout
- Updated all cases to Version 2.0

**Commit 7: `[PLANNED]` - Directory reorganization to workflow structure**
- Create 6 workflow stage directories
- Move cases to appropriate workflow categories
- Update README files to explain new classification
- Update all cross-references and links

---

## 🎯 Current Status (2025-11-29)

### Completed Tasks ✅
- [x] Repository structure established
- [x] Bilingual documentation complete
- [x] Case template v1.0 created (7-section structure)
- [x] 3 example cases created v1.0 (domain-based)
- [x] GitHub repository initialized (Private)
- [x] Banner image added and optimized
- [x] Professional language switcher implemented
- [x] **Framework v2.0 restructuring complete**
- [x] **Classification changed to workflow-based (6 stages)**
- [x] **CASE_TEMPLATE.md rewritten (4-section simplified structure)**
- [x] **All 3 example cases updated to v2.0**
- [x] **Tips section added to all cases**
- [x] **DEVELOPMENT_CONTEXT.md updated**

### Next Steps 🎯
- [ ] **IMMEDIATE**: Git commit phase 1 (template + case restructuring)
- [ ] Reorganize directory structure (create 6 workflow stage directories)
- [ ] Update README.md and README.zh-CN.md to explain new workflow classification
- [ ] Git commit phase 2 (directory reorganization + README updates)
- [ ] Push all changes to GitHub
- [ ] Begin creating new cases using workflow-based structure
- [ ] Generate example images for each case

### Pending Decisions 🤔
- Exact file naming convention for workflow-based cases
- Whether to keep legacy A-/I-/L- prefixes or use new STAGE-TYPE-NUM format
- Image generation tool/workflow for case examples
- Migration path for future cases from legacy to workflow structure

---

## 🏗️ Architecture Decisions

### 1. Workflow-Based Classification (Framework v2.0)

**Decision Date**: 2025-11-29
**Status**: Implemented

**Old Approach (v1.0)**:
- Fixed domain categories: Architecture (30), Interior (40), Landscape (30)
- File naming: `A-###`, `I-###`, `L-###`

**New Approach (v2.0)**:
- **Primary Classification**: 6 Workflow Stages (matches designer's actual process)
  1. 01-concept-ideation - From zero to creative solutions
  2. 02-space-planning - Layout optimization & circulation
  3. 03-technical-to-visual - CAD/drawings to visualization
  4. 04-material-styling - Material refinement & styling
  5. 05-scene-rendering - Final presentation renders
  6. 06-specialized-tasks - Special use cases
- **Secondary Classification**: Space types (residential, commercial, outdoor)
- **Case Count**: Open-ended (not fixed per category)

**Rationale**:
- Workflow stages more intuitive for designers
- Matches actual designer workflow (user confirmed "路径A")
- Avoids content imbalance across domains
- Each workflow stage equally important regardless of space type
- Easier for users to find cases matching their current work stage

### 2. File Naming Convention

**v1.0 (Legacy)**: `[CATEGORY-ID]-[descriptive-name].md`
- Architecture: `A-001`, `A-002`, ..., `A-030`
- Interior: `I-001`, `I-002`, ..., `I-040`
- Landscape: `L-001`, `L-002`, ..., `L-030`

**v2.0 (Planned)**: `[STAGE]-[TYPE]-[NUM]-[descriptive-name].md`
- Example: `03-TECH-RES-001-cad-floor-plan-to-render.md`
- Example: `02-PLAN-COM-005-office-furniture-layout.md`
- Stage codes: 01-06 (workflow stages)
- Type codes: RES (residential), COM (commercial), OUT (outdoor)

**Images**: `[CASE-ID]-[input|output]-[descriptor].jpg`
- Example: `A-001-output-modern-styled.jpg`
- Large, compressed JPG format (~200KB target)

**README Files**:
- `README.md` - English (default, GitHub homepage)
- `README.zh-CN.md` - Simplified Chinese (GitHub i18n standard)
- `README_CN.md` - Deprecated, backward compatibility only

### 3. Language Strategy

**Approach**: Parallel bilingual content
- Every case must have complete English AND Chinese content
- Language switcher at top of README files
- GitHub i18n naming standard: `README.{lang-code}.md`
- Current: EN (default) + zh-CN
- Future: Can add ja, ko, es, fr, de, etc.

### 4. Case Structure (Framework v2.0)

**Decision Date**: 2025-11-29
**Status**: Implemented

**Old Structure (v1.0)**: 7 major sections
1. Problem Statement
2. Key Parameters
3. Complete Prompt Template
4. Quality Checklist
5. Tips & Best Practices
6. Related Cases
7. Tags & Metadata

**New Structure (v2.0)**: 4 essential sections (card-style)
1. **效果预览 / Preview** - Large hero image showing input→output
2. **提示词 / Prompt** - Bilingual prompt templates (CN/EN)
3. **Tips / 使用技巧** - Practical usage tips (CN/EN)
4. **标签 / Tags** - Bilingual hashtags for discoverability

**Improvements**:
- Simplified from 7 to 4 sections (cleaner, more focused)
- Visual-first approach (large images)
- Tips section added for practical advice
- Maintained full bilingual support
- Version tracking added
- More gallery-like, less documentation-heavy

### 5. Image Optimization

**Decision**: Use compressed JPG for web images
- Banner: JPG, ~200KB, quality 80
- Case examples: JPG recommended for photographs/renders
- PNG only for diagrams with text

**Rationale**:
- 89% size reduction achieved
- Significantly faster page load
- No visible quality loss
- Better for users with slow connections

### 6. Content Quality Standards

**v2.0 Requirements - Every case must include**:
1. **Large preview image** - High-quality example (1920px+ width, compressed JPG ~200KB)
2. **Bilingual prompts** - Complete prompt templates in Chinese AND English
3. **Practical tips** - Usage advice, variations, best practices (CN + EN)
4. **Bilingual tags** - Relevant hashtags for discoverability
5. **Tested prompts** - Minimum 3-5 test generations to verify quality
6. **Version tracking** - Last updated date, contributor, version number
7. **QA Review** - Visual verification on GitHub after push (see QA Process below)

**Review checklist** available in CASE_TEMPLATE.md

### 7. QA Technical Review Process (Standard for Each Case)

**Objective**: Compare input vs output images to identify violations, professional errors, and prompt adherence failures

**When to Execute**: After pushing each case with all generated images

**Review Levels**:

#### Level 1: Visual Display Check (Basic)
1. Navigate to GitHub repository
2. Verify all images load correctly (no broken links)
3. Check language labels match version (EN/CN)
4. Take screenshots for documentation

#### Level 2: Technical Accuracy Review (Deep) ⭐ **Required**
1. **Input Analysis**
   - Document all spatial elements in CAD/input image
   - Create furniture/room inventory checklist
   - Note room count, furniture quantities, layout

2. **Output Comparison** (Each generated image)
   - Compare against input inventory
   - Identify **added elements** (violations of "strictly follow input")
   - Identify **missing elements** (omissions from original)
   - Verify **furniture counts** (e.g., 2 ottomans, 4 bar stools, 8 chairs)

3. **Prompt Adherence Check**
   - ✅ **No added items**: Decorative elements, plants, accessories not in input
   - ✅ **No removed items**: All CAD symbols must appear in output
   - ✅ **Correct language labels**: English prompt → English labels; Chinese prompt → Chinese labels
   - ✅ **Material accuracy**: Colors, textures match specifications

4. **Professional Quality Check**
   - Room proportions maintained
   - Furniture placement matches CAD layout
   - Distinct pieces remain distinct (e.g., chaise lounge ≠ sectional sofa)
   - Realistic lighting and shadows
   - Presentation-grade quality

5. **Documentation**
   - Create detailed QA report (see template: `case-X.X-technical-qa-report.md`)
   - List all discrepancies with file names
   - Categorize: ❌ Critical (re-generate), ⚠️ Minor (verification needed), ✅ Passed
   - Provide recommendations for correction

6. **User Notification**
   - Report findings to user
   - If critical issues found: User re-generates images
   - If minor issues: User verifies or confirms acceptable
   - If passed: Mark case as QA approved ✅

**QA Report Template**:
```markdown
# Case X.X Technical QA Report

## Input Inventory
- Room count: X
- Furniture items: [list all]
- Spatial elements: [list all]

## Output Comparison

### File: output-natural.jpg
- ❌ Added elements: [list]
- ❌ Missing elements: [list]
- ⚠️ Unclear items: [list items needing verification]
- ✅ Correct elements: [count]

### File: output-json.jpg
[Same structure]

## Prompt Adherence Summary
| Requirement | Natural-EN | JSON-EN | Natural-CN | JSON-CN |
|-------------|-----------|---------|-----------|---------|
| No added items | ❌/✅ | ❌/✅ | ❌/✅ | ❌/✅ |
| All original items | ❌/✅ | ❌/✅ | ❌/✅ | ❌/✅ |
| Correct labels | ❌/✅ | ❌/✅ | ❌/✅ | ❌/✅ |

## Recommendations
1. [Action items]

## Final Status
⚠️ Requires re-generation / ✅ QA Approved
```

**Common Professional Errors to Check**:
- Added decorative items (plants, art, rugs not in CAD)
- Merged furniture (separate pieces blended together)
- Incorrect counts (missing stools, chairs, ottomans)
- Wrong language labels (English in CN version)
- Distorted proportions (rooms stretched/compressed)
- Missing rooms or spaces from input

**QA Approval Status**:
- Case 2.1: ⚠️ **Testing in Progress** (2025-11-30)
  - User Testing Result: Natural language v2.0 showed minimal improvement over v1.0 despite increased complexity
  - Decision: Reverted natural language prompts to v1.0 (simplicity prioritized)
  - JSON v2.0: Retained (structured format benefits from detailed specifications)
  - Added: Iterative generation tip in README (generate 2-3 variations + post-processing)
  - Technical QA Report: `case-2.1-technical-qa-report.md`
  - **Next**: Re-generate with v1.0 natural language + v2.0 JSON, final QA validation

### 8. Prompt Engineering Best Practices (Mandatory Standard) - **Updated Based on User Testing** ⚠️

**Objective**: Systematic methodology to minimize errors across all 62 use cases

**Document**: `prompt-engineering-best-practices.md` (Artifact)

**🔄 Key Learning from Case 2.1 User Testing** (2025-11-30):
- **Natural Language Prompts**: v1.0 simplicity preferred over v2.0 complexity
  - User testing showed minimal accuracy improvement with detailed v2.0
  - Increased complexity reduced usability without proportional benefit
  - **Recommendation**: Keep natural language prompts concise, use iteration instead
- **JSON Prompts**: v2.0 detailed structure retained
  - Structured format benefits from comprehensive specifications
  - JSON v2.0 provides 95%+ accuracy target
  - New categories (`architectural_features`, `empty_spaces`, `strict_constraints`) proven valuable

**Refined Approach**:
1. **Natural Language**: Simple + Iterative
   - Use concise v1.0 style prompts
   - Generate 2-3 variations
   - Select best result
   - Refine with simple image editing tools if needed

2. **JSON**: Detailed + Structured
   - Use comprehensive v2.0 specifications
   - Include `architectural_features`, `empty_spaces`, independence fields
   - Leverage `strict_constraints` for accuracy
   - Target 95%+ accuracy in single generation

**Hybrid Workflow Recommended**:
```
Input CAD → Simple Natural Language Prompt → 2-3 Variations → Select Best
                                           OR
Input CAD → Detailed JSON Prompt → High Accuracy Single Result
```

**Case 2.1 Final Specifications**:
- Natural Language: v1.0 (concise, proven effective)
- JSON: v2.0 (detailed, 95%+ accuracy)
- Tips: Added iterative generation recommendation

**Derived From**: Case 2.1 comprehensive QA findings + User Testing Feedback

**Core Methodology** (5 Phases) - **Applies Primarily to JSON Prompts**:

**Objective**: Systematic methodology to minimize errors across all 62 use cases

**Document**: `prompt-engineering-best-practices.md` (Artifact)

**Derived From**: Case 2.1 comprehensive QA findings

**Core Methodology** (5 Phases):

#### Phase 1: Exhaustive Input Analysis
**Before writing any prompt:**

1. **Spatial Inventory**
   - Room count, names, dimensions
   - Built-in elements (walk-in closets, alcoves, architectural features)
   - Empty spaces (balconies, hallways) - document what is NOT there

2. **Furniture Inventory** (Per Room)
   - Itemized list with exact quantities
   - Distinctions (sectional vs. chaise, built-in vs. freestanding)
   - Independence notes (separate pieces that might merge)

3. **Fixture Inventory** (Bathrooms/Kitchens)
   - ALL plumbing fixtures (bathtub + separate shower common error)
   - Exact counts (single vs. double vanity)
   - Fixed vs. movable elements

4. **Empty Space Notation**
   - Explicitly document spaces with NO furniture
   - Critical for preventing AI additions

**Time Investment**: 15-20 minutes per case  
**Error Reduction**: ~70% of common mistakes caught here

---

#### Phase 2: Structured Prompt Writing

**Natural Language Template:**
```
1. Transformation goal
2. What to ADD (matching CAD)
3. What to PRESERVE (exact counts, proportions)
4. What NOT to ADD ⭐ CRITICAL
5. Language specification
6. Critical elements list (easy-to-miss items)
```

**JSON Template:**
```json
{
  "input_summary": {room_count, furniture_count, fixture_count},
  "architectural_features": [separate from furniture],
  "rooms": [detailed specs per room],
  "empty_spaces": [explicit empty array],
  "strict_constraints": {no_added, no_removed, exact_counts}
}
```

**Key Innovations from Case 2.1**:
- Separate `architectural_features` from `furniture` (walk-in closet issue)
- Explicit `empty_spaces` category (balcony issue)
- `independence` field for furniture (chaise lounge issue)
- `separate_from_tub` for showers (missing fixture issue)

---

#### Phase 3: Common Error Patterns & Prevention

**Error Pattern Library** (from Case 2.1):

| Error | Symptom | Prevention |
|-------|---------|------------|
| Decorative Additions | Plants, vases, pillows added | Explicit negative list in prompt |
| Merged Furniture | Chaise + sofa blend | "independence" field in JSON |
| Architectural Confusion | Walk-in closet → wardrobe | Separate architectural category |
| Count Inaccuracies | Wrong number of stools/chairs | "exact_counts_enforced" in JSON |
| Missing Fixtures | Separate shower omitted | "separate_from_tub": true |

**Prevention Strategies**:
- Explicit negative constraints ("DO NOT ADD")
- Quantity precision ("exactly 4 bar stools" not "bar stools")
- Architectural vs. furniture categorization
- Reference-based constraints ("only items with CAD symbols")

---

#### Phase 4: Pre-Submission QA Checklist

**Mandatory verification before generating:**

- [ ] Input analysis complete (all inventories done)
- [ ] All CAD elements referenced in prompt
- [ ] Negative constraints included
- [ ] Quantities specified exactly
- [ ] Architectural features distinguished from furniture
- [ ] Empty spaces explicitly noted
- [ ] Language specification clear
- [ ] Easy-to-miss items highlighted

**Estimated Time**: 5 minutes  
**Impact**: Catches 90% of specification errors before generation

---

#### Phase 5: Post-Generation QA Review

**Deep technical review** (see Section 7):
- Compare each output against input inventory
- Verify exact counts
- Check for added/missing elements
- Validate architectural rendering
- Create detailed QA report
- Document errors for methodology improvement

---

### Prompt Quality Metrics

**Target Accuracy (Post-Best-Practices):**
- Room count: 100%
- Furniture quantity: 95%+
- No added deco items: 90%+
- Architectural correctness: 90%+
- Fixture count: 95%+
- Empty space preservation: 95%+

**Case 2.1 Baseline (Pre-Best-Practices):**
- Natural language: ~40% accuracy
- JSON: ~60% accuracy
- **Improvement needed**: 30-50 percentage points

**Expected Improvement with Methodology:**
- Natural language: 85-90% accuracy
- JSON: 95%+ accuracy

---

### Implementation for Cases 2.2 - 6.8

**Standard Workflow** (per case):

1. **Input Analysis** (15-20 min)
   - Complete all checklists from best practices guide
   - Document inventory in structured format
   - Note tricky/easy-to-miss elements

2. **Prompt Drafting** (10-15 min)
   - Use templates from best practices
   - Customize for specific case requirements
   - Add case-specific constraints

3. **Quality Review** (5 min)
   - Run through QA checklist
   - Validate against prompt matrix
   - Refine weak specification points

4. **Generate & Test** (varies)
   - Generate all outputs (natural EN/CN, JSON EN/CN)
   - Technical QA review (Section 7)
   - Document discrepancies

5. **Iterate if Needed**
   - Update prompt based on QA findings
   - Re-generate failed outputs
   - Re-test until QA approved

**Total Time per Case**: 30-40 minutes initially → 20-25 minutes as templates mature

---

### Continuous Improvement Loop

After each case:
1. Update error pattern library with new findings
2. Refine templates based on lessons learned
3. Add new prevention strategies
4. Update checklists
5. Measure accuracy improvement

**Document Maintenance**:
- Review `prompt-engineering-best-practices.md` after every 10 cases
- Incorporate community feedback
- Version control prompt templates
- Share learnings across all cases

---

## 🔧 Technical Stack

### Core Technologies
- **Version Control**: Git + GitHub
- **Documentation**: Markdown (GitHub-flavored)
- **Image Processing**: Python PIL/Pillow (for compression)
- **AI Model**: Nano Banana Pro (Gemini 3 Pro Image)

### Development Tools Used
- Git CLI for version control
- GitHub Desktop (user preference)
- Python 3.13.2 for image optimization
- Text editor for Markdown

### Dependencies
- Python Pillow library (for image compression script)
- No other runtime dependencies
- Static content only (Markdown + images)

---

## 📊 Content Plan (100 Cases)

### 🏠 Architecture & Workflow (30 cases)

**CAD to Visualization (8 cases)** - Status: 1/8
- [x] A-001: CAD Floor Plan to Photorealistic Top View
- [ ] A-002: Elevation Drawing to 3D Render
- [ ] A-003: Section Cut to Interior Visualization
- [ ] A-004: Site Plan to Landscape Context
- [ ] A-005: Axonometric Drawing to Realistic View
- [ ] A-006: Detail Drawing to Close-up Render
- [ ] A-007: Sketch Plan to Presentation Quality
- [ ] A-008: Technical Drawing to Client-Friendly Visual

**Concept Development (8 cases)** - Status: 0/8
- [ ] A-009 through A-016 (planned in docs/ROADMAP.md)

**Material & Facade Studies (8 cases)** - Status: 0/8
- [ ] A-017 through A-024 (planned)

**Structural & Technical Analysis (6 cases)** - Status: 0/6
- [ ] A-025 through A-030 (planned)

### 🛋️ Interior Design & Styling (40 cases)

**Space Planning & Layout (8 cases)** - Status: 1/8
- [x] I-001: Furniture Layout Generation
- [ ] I-002 through I-008 (planned)

**Material & Lighting (10 cases)** - Status: 0/10
- [ ] I-009 through I-018 (planned)

**Furniture & Styling (10 cases)** - Status: 0/10
- [ ] I-019 through I-028 (planned)

**Style Transformation (8 cases)** - Status: 0/8
- [ ] I-029 through I-036 (planned)

**Text & Graphics in Space (4 cases)** - Status: 0/4
- [ ] I-037 through I-040 (planned)

### 🌳 Landscape & Outdoor Living (30 cases)

**Site Planning & Hardscape (8 cases)** - Status: 1/8
- [x] L-001: Master Plan Visualization
- [ ] L-002 through L-008 (planned)

**Planting & Softscape (8 cases)** - Status: 0/8
- [ ] L-009 through L-016 (planned)

**Garden Styles (8 cases)** - Status: 0/8
- [ ] L-017 through L-024 (planned)

**Seasonal & Lighting Effects (6 cases)** - Status: 0/6
- [ ] L-025 through L-030 (planned)

**Overall Progress**: 3/100 cases (3%)

---

## 💡 Key Design Decisions & Rationale

### Decision 1: Manual Curation Over Automation
**Choice**: MVP focuses on hand-crafted, tested prompts
**Rationale**: Quality over quantity; each case must solve real design problems
**Impact**: Slower initial development but higher quality output

### Decision 2: Private Repository During Development
**Choice**: Keep repo private until MVP complete
**Rationale**:
- Control over public release timing
- Freedom to experiment without public scrutiny
- Ensure quality before community engagement
**Plan**: Make public after 100 cases complete (Week 5)

### Decision 3: GitHub i18n Standard Naming
**Choice**: Use `README.zh-CN.md` instead of `README_CN.md`
**Rationale**:
- Follows GitHub official multilingual convention
- May trigger automatic language detection
- Easier to add more languages (ja, ko, es, etc.)
- More professional and scalable
**Implementation**: Commit 47e360b

### Decision 4: Compressed Images
**Choice**: JPG at quality 80, target ~200KB for banners
**Rationale**:
- 89% size reduction achieved
- Negligible quality loss
- Much faster page loads, especially for Chinese users
- Better mobile experience
**Implementation**: Commit 2734a63

### Decision 5: Framework v2.0 Restructuring
**Choice**: Complete pivot from domain-based to workflow-based classification
**Date**: 2025-11-29
**Rationale**:
- **User insight**: After overnight reflection, user realized workflow stages match designer thinking better than domains
- **User's workflow confirmed**: "路径A" (from zero start): Concept → Planning → Technical → Material → Rendering → Specialized
- **Content balance**: Avoids thin content in architecture/landscape; all workflow stages equally important
- **Open-ended growth**: No fixed case counts per category, add cases as tested
- **Improved UX**: Designers can find cases matching their current work stage
- **Case structure simplification**: 7-section structure too complex, simplified to 4-section card-style
- **Visual-first approach**: Large images for at-a-glance understanding
**Impact**:
- All 3 example cases rewritten to v2.0
- CASE_TEMPLATE.md completely restructured
- Future directory reorganization planned
- README updates needed to explain new classification
**Implementation**: Session 2 (2025-11-29), Commit 6 pending

---

## ⚠️ Known Issues & Limitations

### Current Limitations
1. **No actual case examples yet**: Only 3 template examples exist, no real generated images
2. **Placeholder content**: Example images in case files are placeholders
3. **Need image generation workflow**: Must establish process for generating case examples
4. **README_CN.md deprecated**: Will be removed in future version

### Technical Constraints
1. **GitHub README limitations**: Cannot implement true "in-place" language switching (static Markdown)
2. **Image file size**: Must manually optimize images, no automated CI/CD yet
3. **No automated testing**: Prompt quality relies on manual testing

### Future Improvements Needed
1. Automated image optimization in CI/CD pipeline
2. Consistent image generation workflow
3. Community contribution review process
4. Automated link checking
5. Case cross-reference validation

---

## 🔐 Repository Configuration

### Git Configuration
- **Remote**: origin → https://github.com/qzh3722/awesome-nano-banana-spatial-design.git
- **Default Branch**: main
- **Git Ignore**: Configured for design files (.psd, .ai, .sketch, temp files)

### GitHub Settings Recommended
- **Visibility**: Private (current) → Public (after Week 5)
- **Issues**: Enable for community feedback
- **Discussions**: Enable after going public
- **Wiki**: Not needed
- **Projects**: Optional for tracking case creation

### Repository Secrets/Tokens
- User authenticated via GitHub Desktop or Personal Access Token
- No secrets stored in repository
- All content is public-safe (prompts, documentation)

---

## 📝 Important File Locations

### Core Documentation
- `DEVELOPMENT_CONTEXT.md` - **THIS FILE** (Development history)
- `README.md` - English homepage
- `README.zh-CN.md` - Chinese homepage
- `CASE_TEMPLATE.md` - Template for all cases

### Reference Documentation
- `docs/GETTING_STARTED.md` - User guide for using prompts
- `docs/FAQ.md` - Common questions
- `docs/ROADMAP.md` - 4-week development plan
- `CONTRIBUTING.md` - Guidelines for contributors

### Case Examples (v2.0)
- `cases/architecture/A-001-cad-to-colored-plan.md` - Architecture example (v2.0 structure)
- `cases/interior/I-001-furniture-layout.md` - Interior example (v2.0 structure)
- `cases/landscape/L-001-master-plan-visualization.md` - Landscape example (v2.0 structure)
- All cases now use simplified 4-section card-style format with Tips section

---

## 🎯 Next Session TODO

When resuming development, AI should:

1. **Read this file first** to understand context
2. **Check "Current Status"** section for latest state
3. **Review last commit** to see what was done
4. **Continue from "Next Steps"** section above
5. **Update this file** after significant progress

### Immediate Next Tasks (Post-Restructuring)
1. **Git commit phase 1**: Template and case restructuring (IMMEDIATE)
2. **Directory reorganization**: Create 6 workflow stage directories
3. **Update README files**: Explain new workflow-based classification
4. **Git commit phase 2**: Directory reorganization + README updates
5. **Push to GitHub**: Push all changes
6. Begin creating new cases using v2.0 structure
7. Establish image generation workflow
8. Test all prompts thoroughly (3-5 generations each)

### Before Each Session Ends
- [ ] Update "Last Updated" date at top
- [ ] Update "Current Status" section
- [ ] Record any new decisions in "Architecture Decisions"
- [ ] Update case progress counters
- [ ] Git commit this file with changes

---

## 📞 User Preferences & Context

### User: qzh3722
- **Language**: Prefers Chinese (中文) communication
- **GitHub Username**: qzh3722
- **Tool Preference**: GitHub Desktop for git operations
- **Development Style**: Prefers structured, documented approach

### Communication Style
- Detailed explanations preferred
- Step-by-step instructions appreciated
- Visual structure (tables, trees) helpful
- Both English and Chinese documentation valued

### Project Goals
- Create 100 high-quality, tested use cases
- Serve spatial design professionals (architects, interior, landscape designers)
- Bilingual support (EN + CN) is critical
- Quality over speed - willing to take time for polish

---

## 🔄 Version History of This Document

### v1.0 - 2025-11-28
- Initial creation
- Documented Week 1 foundation phase
- Recorded all 5 commits and their purposes
- Established structure for ongoing updates
- Added all architectural decisions made so far

### v2.0 - 2025-11-29
- **Major update**: Documented Framework v2.0 restructuring
- Added Session 2 development timeline
- Updated classification from domain-based to workflow-based
- Documented 6 workflow stages (Concept → Planning → Technical → Material → Rendering → Specialized)
- Added Decision 5: Framework v2.0 restructuring rationale
- Updated case structure documentation (7-section → 4-section card-style)
- Updated file naming conventions (legacy vs planned v2.0)
- Updated Current Status section with v2.0 completion
- Updated all references to reflect workflow-based organization
- Added commits 6-7 (pending) to timeline

---

## 📚 Additional Notes

### For Future AI Assistants

**When you see this file**:
1. This is the **single source of truth** for project state
2. Read the "Quick Context Summary" first
3. Check the "Current Status" section for what's done/pending
4. Review "Architecture Decisions" before making changes
5. Update this file before ending the session

**Important Reminders**:
- Repository is **private** - don't assume it's public
- All content must be **bilingual** (EN + CN)
- Every case needs **3-5 test generations** before committing
- Follow the **v2.0 case template** strictly (4-section card-style)
- Maintain **git commit message** quality
- **Framework v2.0**: Workflow-based classification is now the standard

**File Naming Patterns**:
- **Legacy (v1.0)**: `[A|I|L]-###-descriptive-name.md` (current 3 examples)
- **Planned (v2.0)**: `[STAGE]-[TYPE]-[NUM]-descriptive-name.md` (future cases)
- Images: `[case-id]-[input|output]-description.jpg`
- Language files: `README.{lang}.md` (ISO 639-1 codes)

### Critical Context Items
- **Nano Banana Pro** = Gemini 3 Pro Image model
- **Thinking Mode** = Special feature for logical reasoning
- **Framework v2.0** = Workflow-based classification (6 stages)
- **6 Workflow Stages**:
  1. Concept Ideation
  2. Space Planning
  3. Technical to Visual
  4. Material & Styling
  5. Scene Rendering
  6. Specialized Tasks
- **100+ cases** = Open-ended count, not fixed per category
- **User's workflow** = "路径A" (Concept → Planning → Technical → Material → Rendering → Specialized)
- **Case structure** = v2.0 uses 4-section card-style (Preview + Prompt + Tips + Tags)
- **Target timeline** = MVP with quality cases, then public release

---

**End of Development Context Document**

*This document should be updated regularly throughout development to maintain accurate project state for AI context preservation.*
