# Frequently Asked Questions (FAQ)

Common questions about Awesome Nano Banana Spatial Design.

## General Questions

### What is this project?
A curated library of professional-grade prompts for Nano Banana Pro (Gemini 3 Pro Image), specifically designed to solve real spatial design challenges in architecture, interior design, and landscape architecture.

### Who is this for?
- Professional architects, interior designers, and landscape architects
- 3D rendering artists and visualization specialists
- Design students learning AI-assisted workflows
- Anyone working with spatial design who wants to leverage AI effectively

### Is this free to use?
Yes! This is an open-source project under the MIT License. You can use, modify, and share all content freely.

### How is this different from generic prompt libraries?
- **Problem-focused**: Each prompt solves a specific design workflow challenge
- **Professional-grade**: Tested for reproducible, presentation-quality results
- **Domain-specific**: Deep focus on spatial design, not general image generation
- **Bilingual**: Full English and Chinese support
- **Educational**: Includes parameters, tips, and workflow context

## Using the Library

### Do I need to know how to write prompts?
No! Each case provides complete, ready-to-use prompts. Just copy, customize the placeholders with your project details, and generate.

### How do I choose which case to use?
1. Browse by category (Architecture, Interior, Landscape)
2. Look for cases matching your design challenge in the Problem Statement
3. Check difficulty level (start with Beginner if new to AI generation)
4. Review example outputs to see if the style matches your needs

### Can I modify the prompts?
Absolutely! The prompts are templates. Customize them for your specific:
- Project requirements
- Style preferences
- Material selections
- Technical specifications

### What if a prompt doesn't work as expected?
1. Check you've replaced all `{PLACEHOLDERS}` with actual values
2. Ensure parameters match recommendations
3. Try adjusting guidance_scale up or down
4. Enable Thinking Mode for complex spatial challenges
5. Check reference image quality if using one
6. Open a GitHub issue if problems persist

## Technical Questions

### What is Thinking Mode?
A model feature that enables enhanced logical reasoning. Use it for:
- Complex spatial layouts
- Structural accuracy
- Technical diagrams
- Multi-room relationships

When enabled, the model "thinks through" spatial logic before generating.

### What resolution are the outputs?
Nano Banana Pro can generate up to 4K+ resolution. Minimum recommended for professional use: 1920px on the longest side.

### Can I use this for commercial projects?
Yes! The prompts are MIT licensed. However:
- Review Nano Banana Pro's terms of service for commercial use
- You own the outputs you generate
- Give credit to this library if you'd like (appreciated but not required)

### Do I need reference images?
It depends on the case:
- **Required**: Cases converting CAD drawings or specific layouts
- **Recommended**: Cases needing style/material consistency
- **Optional**: General concept generation

Check each case's "Reference Image Guidance" section.

### Why do my outputs look different from the examples?
Variability is normal in AI generation:
- Different random seeds produce variations
- Model versions may differ slightly
- Reference images affect results
- Prompt wording interpretation

For consistency: save seeds, use exact parameters, and generate multiple options.

## About Nano Banana Pro

### What is Nano Banana Pro?
An advanced image generation model (Gemini 3 Pro Image) with:
- Enhanced logical reasoning capabilities
- Multi-reference image consistency
- Precise text rendering in images
- High-resolution outputs (4K+)

### How do I access Nano Banana Pro?
[Add access instructions based on actual availability]

### Is Nano Banana Pro free?
[Add pricing information based on actual service]

## Contributing

### Can I submit my own prompts?
Yes! We welcome community contributions. See [CONTRIBUTING.md](../CONTRIBUTING.md) for:
- Submission guidelines
- Quality standards
- How to use the case template

### What makes a good case submission?
- Solves a real design problem
- Tested and produces consistent results
- Complete documentation (both languages)
- Professional-quality example images
- Practical tips from real usage

### How long does review take?
Typically 5-7 days. We'll provide feedback if revisions are needed.

### Can I contribute translations?
Absolutely! We welcome:
- Improvements to existing Chinese translations
- Additional languages (Spanish, Japanese, German, etc.)
- Cultural/regional design variations

## Workflow Questions

### Can I use this with my CAD software?
Yes! Many cases specifically handle CAD outputs:
- Export your CAD drawings as PNG/JPG
- Upload as reference images
- Generate photorealistic visualizations

### How long does generation take?
[Add timing information based on actual model performance]

Typically:
- Simple cases: [X] seconds
- Complex cases with Thinking Mode: [X] seconds

### Can I batch generate multiple options?
Yes! To generate variations:
1. Keep the same prompt and parameters
2. Change the seed or leave it random
3. Generate multiple times
4. Select the best result

### How do I integrate this into my workflow?
Common workflows:
1. **Early concept**: Sketch → Prompt → Quick visualizations
2. **Design development**: CAD plan → Prompt → Presentation images
3. **Material selection**: Material board → Prompt → Realistic application
4. **Client presentation**: Technical drawings → Prompts → Client-friendly visuals

## Troubleshooting

### My CAD conversion doesn't maintain accurate dimensions
- Enable Thinking Mode
- Add "maintain exact spatial proportions from reference"
- Increase guidance_scale to 12-15
- Ensure reference image is clear and high-contrast

### Text in my images is illegible
- Specify exact text needed: "signage reading 'ENTRANCE' in sans-serif font"
- Use Thinking Mode for text accuracy
- Request larger text size in prompt
- Generate multiple times (text rendering can vary)

### Materials don't look realistic
- Use specific material names ("white Carrara marble" not "white stone")
- Add surface finish descriptions ("matte", "polished", "brushed")
- Include lighting context ("natural daylight", "warm evening light")

### Plants don't look accurate
- Specify botanical names when possible
- Indicate season clearly
- Mention growth stage ("mature specimen", "young planting")
- Use regional context if relevant

## Community

### Where can I ask questions?
- [GitHub Discussions](https://github.com/yourusername/awesome-nano-banana-spatial-design/discussions) - Best for general questions
- [GitHub Issues](https://github.com/yourusername/awesome-nano-banana-spatial-design/issues) - For bugs or problems with specific cases

### Can I share my results?
Please do! We'd love to see:
- Success stories
- Real project applications
- Creative variations
- Portfolio pieces

Tag us or use discussions to share!

### How can I stay updated?
- **Watch** the GitHub repository for updates
- Check [ROADMAP.md](./ROADMAP.md) for development plans
- Join discussions for announcements

## Future Development

### Will more cases be added?
Yes! Roadmap includes:
- Community-submitted cases
- Advanced technique explorations
- Software-specific integrations
- Video tutorials

### Can I suggest new case ideas?
Absolutely! Open an issue with:
- Description of the design challenge
- Why it's useful for the community
- Any reference examples

### Will this support other AI models?
Currently focused on Nano Banana Pro. Future plans may include:
- Model comparison guides
- Cross-model prompt adaptations
- Multi-model workflows

---

## Still have questions?

- Check the [Getting Started Guide](./GETTING_STARTED.md)
- Browse [existing discussions](https://github.com/yourusername/awesome-nano-banana-spatial-design/discussions)
- Open a [new discussion](https://github.com/yourusername/awesome-nano-banana-spatial-design/discussions/new)

---

Last updated: 2025-11-28
