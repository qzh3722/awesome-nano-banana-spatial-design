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

### 使用说明（Translation Notes）
上传顺序说明：

第一张图：风格参考图（可以是室内照片、艺术作品、插画、摄影作品等任何具有明确视觉风格的图片）
第二张图：需要改变风格的目标空间照片

适用场景范围：
此提示词模板适用于各类风格来源：
室内设计风格参考：

特定设计流派的室内照片（如日式侘寂、北欧极简、工业风等）
其他项目的设计效果图
高端酒店或商业空间照片

艺术风格参考：

绘画作品（印象派、表现主义、抽象等）
插画风格
摄影作品的调性和氛围
平面设计或视觉艺术作品

技术原理说明：
此提示词会迁移以下风格特征：

色彩系统：色调、饱和度、对比关系
材质处理方式：表面质感的表现手法
光影氛围：照明的情绪和品质
装饰语汇：设计元素的表达方式
整体美学感受：视觉语言的统一性

同时保持不变的元素：

空间的三维结构和布局
家具的位置和配置
建筑特征和空间比例
透视关系和视角

与材质替换的区别：

材质替换：精确替换特定元素的表面材料（如地板、墙面）
风格迁移：改变整个场景的视觉美学和表现方式，是全局性的风格重新诠释

注意事项：
这是一个整体风格转换工具，如果你只需要改变特定元素的材质，请使用之前的材质替换提示词模板。风格迁移会影响场景的整体视觉表达，而不仅仅是个别材质的替换。

---

## 标签 / Tags

`#style-transfer` `#aesthetic-adaptation` `#interior-design` `#visualization`
`#风格迁移` `#美学适配` `#室内设计` `#效果图`

---

**Last Updated**: 2025-12-05
**Version**: 1.0
