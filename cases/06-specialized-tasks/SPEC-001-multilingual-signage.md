# Multilingual Signage Design / 多语言标识设计

## 效果预览 / Preview

> Generate accurate multilingual text on architectural signage and wayfinding systems with correct typography.
>
> 在建筑标识和导视系统上生成准确的多语言文字，具有正确的排版。

![Multilingual Signage Example](../../assets/images/SPEC-001-output-placeholder.jpg)
*Retail storefront with accurate English + Chinese signage / 零售店面，准确的英文+中文标识*

---

## 提示词 / Prompt

### 中文版

```
在建筑场景中创建带有准确文字的标识系统。

标识规格:
- 位置: {位置} (例如: "建筑入口上方"、"墙面导视牌")
- 文字内容: {文字内容}
  例如:
  英文: "URBAN CAFE"
  中文: "都市咖啡"
- 字体风格: {字体风格} (例如: "复古手写体"、"现代无衬线体")

视觉设计:
- 材质: {标识材质} (例如: "3D霓虹灯管"、"拉丝不锈钢立体字")
- 颜色: {颜色} (例如: "亮粉色霓虹"、"金色金属")
- 尺寸: {尺寸} (例如: "字高60cm")
- 照明: {照明效果} (例如: "内发光"、"轮廓光")

环境设置:
- 背景: {背景} (例如: "深色混凝土墙面"、"玻璃幕墙")
- 光照效果: {光效} (例如: "霓虹灯在玻璃上的真实反射")
- 时间: {时间} (例如: "夜晚"、"黄昏")

技术要求(关键):
- **确保文字拼写100%准确**
- **多语言文字(中英日韩)渲染清晰可读**
- **字体排版专业(字间距、行高)**
- **文字与建筑透视一致(不扭曲)**
- 真实的材质质感(金属、霓虹管、亚克力)
- 准确的照明效果和反射

最终图像应达到实际施工图的标准，文字可直接用于制作。
```

### English Version

```
Create an architectural scene with accurate text-based signage system.

Signage Specifications:
- Location: {LOCATION} (e.g., "above building entrance", "wall-mounted wayfinding")
- Text Content: {TEXT_CONTENT}
  e.g.:
  English: "URBAN CAFE"
  Chinese: "都市咖啡"
- Font Style: {FONT_STYLE} (e.g., "retro script", "modern sans-serif")

Visual Design:
- Material: {SIGNAGE_MATERIAL} (e.g., "3D neon tube lights", "brushed stainless steel dimensional letters")
- Color: {COLOR} (e.g., "bright pink neon", "gold metallic")
- Size: {SIZE} (e.g., "60cm letter height")
- Illumination: {LIGHTING_EFFECT} (e.g., "internally lit", "halo lit")

Environmental Settings:
- Background: {BACKGROUND} (e.g., "dark concrete wall", "glass curtain wall")
- Lighting Effects: {LIGHT_EFFECTS} (e.g., "realistic neon reflection on glass")
- Time: {TIME} (e.g., "night", "dusk")

Technical Requirements (Critical):
- **Ensure 100% accurate text spelling**
- **Multilingual text (EN/CN/JP/KR) rendered clearly and legibly**
- **Professional typography (letter spacing, line height)**
- **Text aligned with architectural perspective (no distortion)**
- Realistic material finishes (metal, neon tubes, acrylic)
- Accurate lighting effects and reflections

The final image should meet construction drawing standards with text ready for actual fabrication.
```

---

## Tips / 使用技巧

### 中文

- **文字准确性**: Nano Banana Pro的文字渲染错误率<10%，但仍需检查拼写
- **字体具体化**: "Helvetica Neue Bold"比"现代字体"效果更可控
- **透视对齐**: 对于立面文字，使用"文字沿墙面透视正确放置"确保不扭曲
- **多语言排版**: 中英混排时，明确"英文在上，中文在下，行间距20mm"等细节
- **二次校对**: 生成后务必人工检查文字拼写，必要时用Inpainting修正个别字母

### English

- **Text Accuracy**: Nano Banana Pro has <10% error rate for text rendering, but still verify spelling
- **Font Specificity**: "Helvetica Neue Bold" is more controllable than "modern font"
- **Perspective Alignment**: For facade text, use "text correctly positioned along wall perspective" to prevent distortion
- **Multilingual Layout**: For mixed languages, specify details like "English above, Chinese below, 20mm line spacing"
- **Secondary Verification**: Always manually check text spelling after generation, use Inpainting to correct individual letters if needed

---

## 标签 / Tags

`#专项应用` `#文字渲染` `#导视系统` `#多语言` `#标识设计` `#霓虹灯`

`#specialized-tasks` `#text-rendering` `#wayfinding-system` `#multilingual` `#signage-design` `#neon-signs`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
