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

## 💡 Tips / 技巧

### 1. Style Variations / 风格变体
You can replace **'blueprint style'** in the prompt with any of the following to achieve different visual effects:
您可以将提示词中的 **'blueprint style'** 替换为以下任意一种，以获得不同的视觉效果：

*   **'wireframe style'** (线框风格)
    *   *Only shows edge lines, no surface fill, demonstrating structural logic.*
    *   *仅显示边缘线条,无表面填充,展示结构逻辑*
*   **'technical line drawing style'** (技术线图风格)
    *   *Precise black and white line drawing, different line weights indicating hierarchy, similar to construction drawings.*
    *   *精确的黑白线条绘制,不同线宽表示层级,类似施工图*
*   **'flat color blocking with ambient occlusion'** (平面色块+环境光遮蔽)
    *   *Each mass filled with a single color, retaining shadow depth.*
    *   *每个体块用单一颜色填充,保留阴影深度感*
*   **'watercolor rendering style'** (水彩渲染风格)
    *   *Soft watercolor texture, edges slightly bleeding, artistic expression.*
    *   *柔和的水彩质感,边缘略带晕染效果,艺术化表达*
*   **'hand-drawn sketch style with hatching'** (手绘素描风格+阴影线)
    *   *Simulates manual drawing, using parallel lines to represent shadows and materials.*
    *   *模拟手工绘制,用平行线表示阴影和材质*
*   **'physical model photography style'** (实体模型摄影风格)
    *   *Simulates physical architectural models made of white cardstock or wood.*
    *   *模拟白色卡纸或木材制作的实体建筑模型*
*   **'ghost render with transparency'** (半透明幽灵渲染)
    *   *Translucent exterior walls, allowing visibility into internal spatial layout.*
    *   *外墙半透明,可透视内部空间布局*
*   **'material study render'** (材质研究渲染)
    *   *Accurately displays the real texture of different materials (concrete/wood/glass).*
    *   *精确显示不同材料(混凝土/木材/玻璃)的真实质感*
*   **'diagram style with color-coded functional zones'** (图解风格+功能分区色标)
    *   *Different functional spaces distinguished by different colors, with legend.*
    *   *不同功能空间用不同颜色区分,带图例说明*
*   **'clay render style'** (粘土渲染风格)
    *   *Soft, matte finish resembling clay models.*
    *   *柔和的哑光表面，类似于粘土模型*

### 2. Viewpoint Variations / 视角变体
You can also specify different rotation angles:
您还可以指定不同的旋转角度：

*   **90 Degrees (Side View) / 90度 (侧面):**
    *   `"rotated 90 degrees clockwise/counterclockwise"`
*   **45 Degrees (Corner View) / 45度 (斜角):**
    *   `"rotated 45 degrees to show the adjacent corner perspective"`
*   **Bird's Eye View / 鸟瞰俯视:**
    *   `"from a higher bird's eye view angle looking down at 60 degrees"`

## 🏷️ Tags
`#technical-to-visual` `#plan-to-isometric` `#blueprint-style` `#3d-visualization`
`#技术转视觉` `#平面转轴测` `#蓝图风格` `#三维可视化`
