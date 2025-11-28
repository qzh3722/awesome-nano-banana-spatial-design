# Getting Started with Awesome Nano Banana Spatial Design

Complete guide for using this prompt library effectively.

## For First-Time Users

### Step 1: Understand the Model

**Nano Banana Pro (Gemini 3 Pro Image)** is an advanced image generation model with:
- Enhanced logical reasoning (Thinking Mode)
- Multi-reference image consistency
- Precise text rendering capabilities
- 4K+ high-resolution outputs

### Step 2: Access the Model

[Instructions will depend on how users access Nano Banana Pro - add links/instructions here]

### Step 3: Browse the Library

Navigate by workflow need:
1. **Architecture**: [cases/architecture](../cases/architecture/)
2. **Interior**: [cases/interior](../cases/interior/)
3. **Landscape**: [cases/landscape](../cases/landscape/)

Each category has a README with full case listings.

### Step 4: Choose a Use Case

Look for cases matching:
- Your design challenge (see Problem Statement)
- Your skill level (Beginner/Intermediate/Advanced)
- Your available resources (reference images, time)

### Step 5: Prepare Your Prompt

1. **Copy the template** from your chosen case
2. **Replace placeholders** with your specific requirements
3. **Prepare reference images** if needed (follow guidance in case)
4. **Set parameters** as recommended

### Step 6: Generate and Iterate

1. Generate your first output
2. Evaluate results against your goals
3. Adjust prompt details for refinement
4. Save successful prompts for future use

## Understanding Prompt Structure

### Anatomy of a Good Prompt

```
[CONTEXT] + [SPECIFICATIONS] + [TECHNICAL REQUIREMENTS] + [REFERENCE GUIDANCE]
```

**Example breakdown:**

**Context**: "Create a photorealistic architectural visualization..."
↳ Sets overall task and quality expectation

**Specifications**: "Modern minimalist style, 100 sq m apartment..."
↳ Defines design parameters

**Technical Requirements**: "Top-down view, natural lighting, 16:9 aspect ratio..."
↳ Controls output format and quality

**Reference Guidance**: "Reference uploaded CAD plan for spatial layout..."
↳ Explains how to use reference images

## Key Parameters Explained

### aspect_ratio
Controls image dimensions:
- `16:9` - Widescreen, good for panoramic views
- `4:3` - Traditional, balanced compositions
- `1:1` - Square, ideal for social media or floor plans
- `9:16` - Vertical, for tall buildings or elevations

### thinking_mode
Enables logical reasoning:
- `On` - Use for complex spatial relationships, structural logic, technical accuracy
- `Off` - Use for artistic/stylistic generation where strict logic isn't critical
- `Optional` - Test both to see which gives better results

**When to use Thinking Mode:**
- Complex multi-room layouts
- Structural diagrams
- Technically accurate visualizations
- Code compliance illustrations

### guidance_scale
Controls prompt adherence (typically 1-20):
- `7-9` - More creative freedom, less literal interpretation
- `10-12` - Balanced (recommended for most cases)
- `13-15` - Strict adherence to prompt details
- `16+` - Very literal, may reduce natural quality

### seed
For reproducibility:
- Leave empty for random variations
- Save seed number to recreate similar outputs
- Use same seed with prompt variations to test changes

## Working with Reference Images

### Types of Reference Images

1. **Structural References** (CAD, floor plans, elevations)
   - Model extracts spatial layout and proportions
   - Best: High contrast, clear line work

2. **Style References** (inspiration images, mood boards)
   - Model adopts aesthetic direction
   - Best: Clear, professional photography

3. **Material References** (texture samples, finish boards)
   - Model applies specific materials
   - Best: Close-up, well-lit, neutral background

4. **Context References** (site photos, existing conditions)
   - Model understands surroundings
   - Best: Clear, good lighting, minimal clutter

### Preparing Reference Images

**Do:**
- Use high resolution (min 1500px)
- Ensure good lighting and clarity
- Crop to relevant content
- For CAD: clean line work, minimal text
- For photos: avoid heavy filters

**Don't:**
- Use low-resolution or blurry images
- Include excessive text or annotations
- Use heavily edited or stylized images
- Upload copyrighted work without permission

## Tips for Different Design Phases

### Early Concept Phase
- Use lower guidance_scale (7-9) for exploration
- Generate multiple quick variations
- Focus on overall composition and style
- Don't worry about perfect details

### Design Development
- Increase guidance_scale (10-12) for accuracy
- Enable Thinking Mode for spatial logic
- Use reference images for consistency
- Refine material and color specifications

### Presentation Phase
- Use highest quality settings
- Specify exact materials and lighting
- Generate multiple angles if needed
- Ensure text elements are legible (if applicable)

## Common Challenges and Solutions

### Problem: Furniture/objects are wrong scale
**Solution**: Add "appropriately scaled for human use" and specify dimensions

### Problem: Spatial layout doesn't make sense
**Solution**: Enable Thinking Mode, provide clearer dimensional information

### Problem: Materials don't look realistic
**Solution**: Use specific material names (e.g., "white oak" not "wood")

### Problem: Output doesn't match reference image
**Solution**: Increase guidance_scale, add explicit instruction "maintain exact layout from reference"

### Problem: Results are inconsistent
**Solution**: Save successful seeds, be more specific in prompt wording

## Next Steps

1. **Try your first generation** using a Beginner-level case
2. **Experiment with parameters** to understand their effects
3. **Build a personal library** of successful prompts
4. **Share your results** and contribute back to the community

## Resources

- [Case Template](../CASE_TEMPLATE.md) - For understanding case structure
- [Contributing Guide](../CONTRIBUTING.md) - To submit your own cases
- [GitHub Discussions](#) - Community Q&A

---

Ready to start? Choose your first case:
- [Architecture: CAD to Visualization](../cases/architecture/A-001-cad-to-colored-plan.md)
- [Interior: Furniture Layout](../cases/interior/I-001-furniture-layout.md)
- [Landscape: Master Plan](../cases/landscape/L-001-master-plan-visualization.md)
