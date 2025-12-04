# Case 1.6: CAD Layout Planning / CAD 布局规划

> **Structural Layout Planning.**
>
> Analyze the spatial potential of an empty floor plan and generate a rational room division and furniture arrangement.
>
> **结构布局规划。**
>
> 分析空置平面图的空间潜力，生成合理的房间划分和家具布置。

![Input Image](../../assets/cases/1.6-cad-layout-planning/input.jpg)
*Input: Original As-built Plan / 输入：原始建成平面图*

![Output Image](../../assets/cases/1.6-cad-layout-planning/output.jpg)
*Output: Proposed Layout Plan / 输出：建议布局平面图*

---

## 📝 Prompt / 提示词

**English:**
```markdown
Using the uploaded CAD floor plan showing the original as-built condition, preserve all existing building structure including exterior walls, load-bearing walls, all door openings (especially the entrance door), and all window positions exactly as shown without any modifications. The entrance door serves as the primary orientation point for functional layout planning: spaces immediately accessible from the entrance should be public/living areas. Based on this entrance location and the existing structural configuration, analyze the spatial potential and add non-load-bearing partition walls where appropriate to create rational room divisions according to residential design standards. After establishing the spatial divisions, arrange furniture and fixtures in every defined space according to its identified function and typical layout conventions for residential interiors. All interior areas within the floor plan boundary must be assigned clear functional purposes and furnished appropriately—no spaces should be left undefined or empty. Present the result as a complete floor plan showing both the new partition wall layout and furniture arrangement in professional CAD drawing style with appropriate line weights and graphic conventions, ensuring all original structural elements and openings remain unchanged.
```

**中文:**
```markdown
使用上传的显示原始建成状态的 CAD 平面图，保留所有现有的建筑结构，包括外墙、承重墙、所有门洞（特别是入口门）和所有窗户位置，完全按照显示的内容，不做任何修改。入口门作为功能布局规划的主要定位点：紧邻入口的空间应为公共/生活区域。根据此入口位置和现有结构配置，分析空间潜力，并在适当位置添加非承重隔墙，根据住宅设计标准创建合理的房间划分。确立空间划分后，根据确定的功能和住宅室内的典型布局惯例，在每个定义的空间内布置家具和固定装置。平面图边界内的所有内部区域必须分配明确的功能用途并进行适当布置——不应有未定义或空置的空间。将结果呈现为完整的平面图，以专业的 CAD 绘图风格显示新的隔墙布局和家具布置，具有适当的线宽和图形惯例，确保所有原始结构元素和开口保持不变。
```

## 🏷️ Tags
`#concept-ideation` `#cad-planning` `#layout-design` `#space-division`
`#概念构思` `#CAD规划` `#布局设计` `#空间划分`
