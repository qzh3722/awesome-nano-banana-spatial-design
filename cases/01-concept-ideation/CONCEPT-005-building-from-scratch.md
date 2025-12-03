# Building from Scratch / 平地起高楼

## 效果预览 / Preview

> Generate architectural visualizations from pure text descriptions without reference images.
>
> 无需参考图片，仅通过文字描述生成建筑可视化。

![Text Input](../../assets/placeholders/input.jpg)
*Input: Text Description (Placeholder) / 输入：文字描述（占位符）*

![Output Render](../../assets/cases/1.2-building-from-scratch/output.jpg)
*Output: Architectural Render (Placeholder) / 输出：建筑渲染（占位符）*

---

## 提示词 / Prompt

### English Version

```
Generate an architectural perspective rendering of a two-story contemporary villa with approximately 300 square meters of living space. The building should feature an L-shaped plan configuration with a south-facing courtyard. Primary materials include exposed concrete walls and large-format glazing systems. The ground floor contains open-plan living areas with direct access to outdoor terraces, while the upper floor houses private sleeping quarters. Flat roof with deep overhangs for solar control. Minimal ornamentation emphasizing horizontal lines and material honesty.
```

### 中文版

```
生成一栋约300平方米的两层现代别墅的建筑透视渲染图。建筑应采用L形平面布局，并带有一个朝南的庭院。主要材料包括清水混凝土墙和大幅面玻璃系统。一楼包含开放式起居区，可直接通往室外露台，而二楼则容纳私人睡眠区。平屋顶带有深远的挑檐以控制日照。极简装饰，强调水平线条和材料的真实性。
```

---

## Tips / 使用技巧

### English

For describing a villa from scratch (without an uploaded reference image), you should provide Gemini Image Pro with a structured description that follows this framework:

**Core Elements to Include:**
1.  **Visualization Type**: First, specify the visualization type you want generated. State whether you need an architectural rendering, an axonometric projection, an elevation drawing, a perspective view, or a floor plan representation. This establishes the technical drawing convention Gemini should follow.
2.  **Essential Parameters**: Second, define the essential architectural parameters. Describe the building massing, the number of stories, the overall footprint dimensions if relevant, and the primary spatial organization. For example, you might specify a two-story villa with a central courtyard configuration, or an L-shaped plan with distinct public and private wings.
3.  **Key Features**: Third, identify the key architectural features that define the character of the villa. This might include roof configuration, window patterns, material expression on exterior surfaces, entrance location and treatment, or relationship to surrounding site conditions.
4.  **Functional Requirements**: Fourth, specify any functional requirements or spatial relationships that matter to your design intent. Indicate how interior spaces should relate to exterior areas, where primary circulation should occur, or how the building should orient relative to sun exposure or views.

**What to Avoid:**
Do not provide exhaustive lists of every design detail, material specification, or decorative element unless these are genuinely essential to your concept. Allow Gemini Image Pro to resolve secondary details through professional conventions. Do not over-prescribe aesthetic qualities with elaborate descriptive language when functional and technical parameters will suffice.

### 中文

当从零开始描述别墅（没有上传参考图）时，您应该为 Gemini Image Pro 提供遵循以下框架的结构化描述：

**核心要素：**
1.  **可视化类型**：首先，指定您想要生成的可视化类型。说明您是需要建筑渲染图、轴测投影图、立面图、透视图还是平面图表现。这确立了 Gemini 应遵循的技术绘图惯例。
2.  **基本参数**：其次，定义基本的建筑参数。描述建筑体量、层数、总占地尺寸（如果相关）以及主要的空间组织。例如，您可以指定一个带有中央庭院布局的两层别墅，或者一个具有明显公共和私密翼楼的L形平面。
3.  **关键特征**：第三，确定定义别墅特征的关键建筑特征。这可能包括屋顶配置、窗户样式、外表面的材料表现、入口位置和处理方式，或与周围场地条件的关系。
4.  **功能要求**：第四，指定对您的设计意图至关重要的任何功能要求或空间关系。指出内部空间应如何与外部区域联系，主要流线应发生在哪里，或者建筑应如何根据日照或景观进行朝向。

**应避免的内容：**
不要提供每一个设计细节、材料规格或装饰元素的详尽清单，除非这些对您的概念真正至关重要。允许 Gemini Image Pro 通过专业惯例来解决次要细节。当功能和技术参数足以说明问题时，不要用复杂的描述性语言过度规定审美特质。

---

## 标签 / Tags

`#concept-ideation` `#text-to-image` `#architectural-design` `#villa`
`#概念构思` `#文生图` `#建筑设计` `#别墅`
