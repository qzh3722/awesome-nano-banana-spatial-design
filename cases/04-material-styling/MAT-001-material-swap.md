# Realistic Material Replacement / 真实材质替换 `[Original]`

## 效果预览 / Preview

> Replace specific materials in a scene with a provided sample while maintaining lighting and geometry.
>
> 使用提供的样本替换场景中的特定材质，同时保持光照和几何结构。

![Input Material](../../assets/cases/4.1-material-swap/input-material.jpg)
*Input 1: Material Sample / 材质样本*

![Input Scene](../../assets/cases/4.1-material-swap/input-scene.jpg)
*Input 2: Target Scene / 目标场景*

![Output Image](../../assets/cases/4.1-material-swap/output.jpg)
*Output: Material Replaced / 材质替换后*

---

## 提示词 / Prompt

**English:**
```markdown
Using the first uploaded image as the source material sample and the second uploaded image as the target scene, replace the [specify element: flooring/wall tiles/wall paint/cabinet surfaces/countertops/etc.] in the target scene with the material pattern and texture shown in the source sample. Apply the source material while maintaining the target scene's existing perspective distortion, lighting conditions, shadows, reflections, and surface geometry. Preserve all other elements in the target scene completely unchanged, including furniture placement, spatial configuration, architectural features, and any elements not specifically designated for material replacement. Ensure the replaced material responds naturally to the scene's lighting environment and integrates seamlessly with surrounding surfaces.
```

**中文:**
```markdown
使用第一张上传的图片作为源材质样本，第二张上传的图片作为目标场景，将目标场景中的 [指定元素：地板/墙砖/墙漆/柜体表面/台面等] 替换为源样本中显示的材质图案和纹理。应用源材质时，保持目标场景现有的透视变形、光照条件、阴影、反射和表面几何形状。保持目标场景中的所有其他元素完全不变，包括家具摆放、空间配置、建筑特征以及任何未指定进行材质替换的元素。确保替换后的材质自然地响应场景的光照环境，并与周围表面无缝融合。
```

---

## 💡 Tips / 使用技巧

### 使用说明（Translation Notes）
上传顺序说明：

第一张图：材质样本照片（地板花色、瓷砖纹理、油漆色样、柜体表面处理等）
第二张图：需要替换材质的实景效果照片

填写参数说明：
在提示词中的 [specify element] 位置填入具体要替换的元素：

flooring - 地板
wall tiles - 墙面瓷砖
wall paint/wall surface - 墙面油漆/墙面
cabinet surfaces/cabinet doors - 柜体表面/柜门
countertops - 台面
ceiling finish - 吊顶/天花表面
furniture upholstery - 家具软包面料

示例应用：
如果要替换地板材质：
"...replace the flooring in the target scene..."
如果要替换柜门表面：
"...replace the cabinet doors in the target scene..."
如果要同时替换多个相同类型的元素（如所有墙面）：
"...replace all wall surfaces in the target scene..."

---

## 标签 / Tags

`#material-replacement` `#texture-swap` `#interior-design` `#renovation`
`#材质替换` `#纹理更换` `#室内设计` `#装修`

---

**Last Updated**: 2025-12-05
**Version**: 2.0

