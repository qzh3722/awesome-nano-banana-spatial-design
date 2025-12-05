# Case 3.1: 2D Floor Plan to 3D Isometric / 二维平面图转三维轴测图

> **Technical to Visual.**
>
> Transform a 2D floor plan into a 3D isometric architectural drawing with a blueprint style.
>
> **技术转视觉。**
>
> 将二维平面图转换为具有蓝图风格的三维轴测建筑图。

![Input Image](../../assets/cases/3.1-plan-to-isometric/input.jpg)
*Input: 2D Floor Plan / 输入：二维平面图*

#### Phase 1: Isometric View / 阶段 1：轴测视图

![Output Image](../../assets/cases/3.1-plan-to-isometric/output.jpg)
*Output: 3D Isometric Drawing / 输出：三维轴测图*

**Prompt:**
```markdown
Transform this 2D floor plan into a 3D isometric architectural drawing. Extrude the walls to a consistent height. Apply a 'blueprint style' style with soft ambient occlusion shadows.
```

#### Phase 2: Reverse Perspective / 阶段 2：反向视角

![Output Image Reverse](../../assets/cases/3.1-plan-to-isometric/output-reverse.jpg)
*Output: Reverse Isometric View / 输出：反向轴测视图*

**Prompt:**
```markdown
Using the previously generated 3D isometric architectural drawing as reference, create a new view from the opposite viewing angle, rotated 180 degrees around the vertical axis. Maintain the same extrusion height, rendering style, ambient occlusion shadows, and all architectural elements exactly as shown in the original. Only change the camera viewpoint to show the building from the reverse perspective, revealing the opposite facades and spatial relationships that were hidden in the first view.
```

**中文提示词:**
```markdown
使用之前生成的三维轴测建筑图作为参考，创建一个从相反视角（绕垂直轴旋转180度）的新视图。保持相同的拉伸高度、渲染风格、环境光遮蔽阴影以及所有建筑元素与原图完全一致。仅改变相机视点，从反向视角展示建筑，揭示在第一视图中被隐藏的相反立面和空间关系。
```

---

## 📝 Prompt / 提示词

**English:**
```markdown
Transform this 2D floor plan into a 3D isometric architectural drawing. Extrude the walls to a consistent height. Apply a 'blueprint style' style with soft ambient occlusion shadows.
```

**中文:**
```markdown
将此二维平面图转换为三维等距建筑图。将墙壁拉伸至一致的高度。应用带有柔和环境光遮蔽阴影的“蓝图风格”。
```

## 🏷️ Tags
`#technical-to-visual` `#plan-to-isometric` `#blueprint-style` `#3d-visualization`
`#技术转视觉` `#平面转轴测` `#蓝图风格` `#三维可视化`
