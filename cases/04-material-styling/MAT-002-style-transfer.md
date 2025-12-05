# Style Transfer / 风格迁移

## 效果预览 / Preview

> Transfer the visual style characteristics from a reference image to a target scene while preserving spatial structure.
>
> 将参考图像的视觉风格特征迁移到目标场景，同时保留空间结构。

![Style Reference](../../assets/cases/4.2-style-transfer/input-style.jpg)
*Input 1: Style Reference / 风格参考*

![Target Scene](../../assets/cases/4.2-style-transfer/input-scene.jpg)
*Input 2: Target Scene / 目标场景*

![Output Image](../../assets/cases/4.2-style-transfer/output.jpg)
*Output: Style Transferred / 风格迁移后*

---

## 提示词 / Prompt

**English:**
```markdown
Using the first uploaded image as the style reference and the second uploaded image as the target spatial scene, transfer the visual style characteristics from the reference to the target scene. Apply the reference's aesthetic qualities including color palette, tonal relationships, material treatment approach, lighting mood, textural rendering style, and decorative vocabulary to the target scene while preserving the target scene's spatial configuration, architectural structure, furniture layout, and functional organization. Maintain the target scene's perspective, proportions, and spatial relationships exactly as shown. The result should express the target space reinterpreted through the visual language and aesthetic sensibility of the style reference.
```

**中文:**
```markdown
使用第一张上传的图片作为风格参考，第二张上传的图片作为目标空间场景，将参考图的视觉风格特征迁移到目标场景中。将参考图的美学品质（包括调色板、色调关系、材质处理方法、灯光氛围、纹理渲染风格和装饰语汇）应用到目标场景，同时保留目标场景的空间配置、建筑结构、家具布局和功能组织。严格保持目标场景的透视、比例和空间关系。结果应通过风格参考的视觉语言和美学感知重新诠释目标空间。
```

---

## 💡 Tips / 使用技巧

### 使用说明 (Translation Notes)

**上传顺序说明 (Upload Order):**

1.  **第一张图 (First Image):** 风格参考图（包含期望的色彩、材质、光影氛围）
    *   *Style Reference (contains desired colors, materials, lighting mood)*
2.  **第二张图 (Second Image):** 目标空间场景图（需要改变风格的实景或模型图）
    *   *Target Spatial Scene (real scene or model to be restyled)*

**关键点 (Key Points):**

*   **结构保持 (Structure Preservation):** 提示词强调了保留"spatial configuration, architectural structure, furniture layout"（空间配置、建筑结构、家具布局）。
*   **风格迁移 (Style Transfer):** 重点在于迁移"aesthetic qualities"（美学品质），如色调、材质处理、灯光等。

---

## 标签 / Tags

`#style-transfer` `#aesthetic-adaptation` `#interior-design` `#visualization`
`#风格迁移` `#美学适配` `#室内设计` `#效果图`

---

**Last Updated**: 2025-12-05
**Version**: 1.0
