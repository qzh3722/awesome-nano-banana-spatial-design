# Case 2.4: Site Plan to Photorealistic Aerial `[Original]`

> **From 2D Plan to 3D Reality.**
>
> Using the uploaded site plan as the source document, generate a photorealistic rendering that shows the site as it would appear in reality to an ordinary observer.

![Site Plan Input](../../assets/cases/2.4-site-plan-to-aerial/input.jpg)
*Input: Site Plan CAD / 输入：总平面CAD*

![Aerial View Output](../../assets/cases/2.4-site-plan-to-aerial/output.jpg)
*Output: Photorealistic Aerial View (Morning) / 输出：照片级鸟瞰图（清晨）*

---

## 🔄 Iteration: Nighttime Lighting / 迭代：夜间照明

> **Transforming Time of Day.**
>
> Using the morning rendering as a base, shift the atmosphere to a dramatic evening scene with artificial lighting.

![Aerial View Output (Morning)](../../assets/cases/2.4-site-plan-to-aerial/output.jpg)
*Input: Previous Output (Morning) / 输入：上一步输出（清晨）*

![Nighttime Output](../../assets/cases/2.4-site-plan-to-aerial/output-night.jpg)
*Output: Nighttime Illumination / 输出：夜间照明效果*

---

## 📝 Prompts / 提示词

### Phase 1: Site Plan to Aerial (Morning)
**English:**
```markdown
Using the uploaded site plan as the source document, generate a photorealistic rendering that shows the site as it would appear in reality to an ordinary observer. Convert the plan view into a three-dimensional realistic visualization with the residential building, water features, and public park areas rendered with real-world materials, textures, and natural lighting. Model the topographic contour lines shown in the plan as actual terrain elevation changes, creating visible hills, slopes, and landform variations across the landscape. Position the viewpoint as a centered aerial perspective directly above the site center, as if captured by drone photography from overhead. Apply morning light conditions with the sun at low angle appropriate to early morning hours, creating corresponding shadows, warm light quality, and atmospheric effects characteristic of dawn illumination. Present the scene as a realistic photograph-quality image that clearly communicates how the completed development would appear when built.
```

**中文:**
```markdown
使用上传的总平面图作为源文件，生成一张照片级渲染图，展示该场地在现实中对普通观察者的外观。将平面视图转换为三维逼真可视化，使用真实世界的材质、纹理和自然光照渲染住宅建筑、水景和公共公园区域。将平面图中显示的等高线建模为实际的地形高程变化，在景观中创造可见的山丘、斜坡和地貌变化。将视点定位为直接位于场地中心上方的居中鸟瞰视角，仿佛是无人机从头顶拍摄的。应用适合清晨时分的低角度阳光光照条件，创造相应的阴影、温暖的光质和具有黎明照明特征的大气效果。将场景呈现为一张逼真的照片级图像，清晰地传达建成后的开发项目外观。
```

### Phase 2: Morning to Night (Lighting Iteration)
**English:**
```markdown
Using the previously generated morning rendering as the base image, convert the lighting conditions from early morning to nighttime. Remove the natural daylight illumination and replace with nighttime lighting scenario. Add artificial lighting appropriate to the site elements including interior building lights visible through windows, exterior architectural lighting for the residential structure, landscape lighting for pathways and public park areas, and accent lighting for water features. Maintain all spatial configurations, materials, textures, topography, and viewing angle exactly as shown in the current image, modifying only the time of day and corresponding lighting conditions to represent evening illumination.
```

**中文:**
```markdown
使用之前生成的清晨渲染图作为底图，将光照条件从清晨转换为夜间。移除自然日光照明，替换为夜间照明场景。添加适合场地元素的人工照明，包括透过窗户可见的室内建筑灯光、住宅结构的室外建筑照明、道路和公共公园区域的景观照明，以及水景的重点照明。保持所有空间配置、材质、纹理、地形和视角与当前图像完全一致，仅修改一天中的时间和相应的光照条件，以表现晚间照明效果。
```

## 💡 Tips / 技巧

*   **Continuous Iteration:** Nano Banana Pro supports continuous iteration. You can use the output of a previous generation as the input for the next step without re-uploading, allowing for progressive refinement (e.g., changing time of day).
*   **持续迭代：** Nano Banana Pro 支持持续迭代。您可以将上一次生成的输出直接用作下一步的输入，无需重新上传，从而实现逐步优化（例如：更改一天中的时间）。

## 🏷️ Tags
`#space-planning` `#site-plan` `#aerial-view` `#photorealistic` `#landscape-design` `#lighting-design` `#night-render`
