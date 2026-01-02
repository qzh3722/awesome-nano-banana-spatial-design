# Case 3.2: Wardrobe Interior Visualization / 衣柜内部结构可视化 `[Original]`

> **Technical to Visual.**
>
> Reveal the internal organization system of a closed wardrobe, with intelligent structure analysis and iterative refinement.
>
> **技术转视觉。**
>
> 智能分析并展示关闭状态衣柜的内部收纳系统，支持迭代优化调整。

![Input Image](../../assets/cases/3.2-wardrobe-interior/input.jpg)
*Input: Closed Wardrobe / 输入：关闭状态的衣柜*

---

## Phase 1: Interior Structure Reveal / 阶段 1：内部结构展示

![Output Image 1](../../assets/cases/3.2-wardrobe-interior/output1.jpg)
*Output: Interior Organization Reveal / 输出：内部收纳结构展示*

**Prompt:**
```markdown
Transform this wardrobe into an open interior view with the following STRICT rules:

1. STRUCTURAL FIDELITY: Preserve the EXACT number and position of compartments, doors, and drawers as shown in the reference image. Do NOT change, merge, or add any divisions.

2. REVEAL INTERIOR: 
   - Remove all cabinet doors to expose internal storage
   - Pull out all drawers partially to show their contents
   - Keep original proportions and alignments intact

3. INTELLIGENT FILL: Populate the revealed interior with realistic organized items (clothes, linens, accessories) that match the wardrobe's style.

4. CONSISTENCY: Maintain the same camera angle, lighting, room environment, and material finish as the original image.
```

**中文提示词:**
```markdown
将此衣柜转换为内部结构展示图，遵循以下严格规则：

1. 结构保真：完全保留参考图片中的隔间、门板、抽屉的精确数量和位置。禁止更改、合并或增加任何分隔。

2. 展示内部：
   - 移除所有柜门以暴露内部储物空间
   - 将所有抽屉部分拉出以展示其内容物
   - 保持原始比例和对齐方式

3. 智能填充：用与衣柜风格相匹配的真实收纳物品（衣物、床品、配饰）填充展示的内部空间。

4. 一致性：保持与原图相同的相机角度、光照、房间环境和材质饰面。
```

---

## Phase 2: Iterative Refinement / 阶段 2：迭代优化

![Output Image 2](../../assets/cases/3.2-wardrobe-interior/output2.jpg)
*Output: Modified Layout - Upper Right Changed to Hanging Rail / 输出：修改后布局 - 右上柜改为挂衣区*

**Prompt (Based on Output 1):**
```markdown
将右上柜改成衣架式，保持右下柜是抽屉不变。
```

**English Translation:**
```markdown
Change the upper right cabinet to a hanging rail style, keep the lower right cabinet as drawers unchanged.
```

---

## 💡 Tips / 技巧

### 1. Key Principles for Structure Fidelity / 结构保真关键原则

| Instruction | Purpose |
|------------|---------|
| `"Preserve the EXACT number"` | 防止 AI 自行修改分隔数量 |
| `"Do NOT change, merge, or add"` | 明确禁止任何结构变更 |
| `"Pull out all drawers partially"` | 确保抽屉展示内部内容 |
| `"Keep original proportions"` | 保持比例一致，便于对比 |

### 2. Iterative Refinement Strategy / 迭代优化策略

This case demonstrates the **two-phase workflow**:
1. **Phase 1**: Generate the initial interior reveal with strict structural fidelity
2. **Phase 2**: Apply targeted modifications using simple, precise instructions

本案例展示了**两阶段工作流**：
1. **阶段一**：在严格保持结构保真的前提下生成初始内部展示图
2. **阶段二**：使用简洁精确的指令进行针对性修改

### 3. Common Modification Requests / 常见修改请求

- 更换某区域的收纳类型（搁板 → 挂衣杆）
- 调整抽屉高度或数量
- 添加特定配件（如拉篮、裤架）
- 更换内部材质或颜色

## 🏷️ Tags
`#technical-to-visual` `#wardrobe-interior` `#furniture-visualization` `#iterative-refinement`
`#技术转视觉` `#衣柜内部` `#家具可视化` `#迭代优化`
