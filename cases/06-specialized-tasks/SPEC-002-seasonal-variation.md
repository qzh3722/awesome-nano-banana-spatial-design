# Seasonal Landscape Variation / 景观四季变化

## 效果预览 / Preview

> Demonstrate how landscape designs transform across seasons by changing vegetation states and atmospheric conditions.
>
> 通过改变植被状态和大气条件展示景观设计如何随季节变化。

![Seasonal Variation Example](../../assets/images/SPEC-002-output-placeholder.jpg)
*Same garden in Summer vs Winter / 同一花园的夏季与冬季对比*

---

## 提示词 / Prompt

### 中文版

```
将此景观场景转换为指定季节的效果。

季节设定:
- 目标季节: {季节} (例如: "深冬"、"早春"、"盛夏"、"晚秋")

植被变化:
- 落叶树木: {树木状态}
  春季: "嫩绿新叶"
  夏季: "浓密深绿叶冠"
  秋季: "金黄和橙红色叶子"
  冬季: "光秃枝干，无叶片"
- 常绿植物: {常绿状态} (例如: "保持绿色但略暗淡")
- 草坪: {草坪状态}
  春夏: "翠绿茂盛"
  秋: "黄绿混杂"
  冬: "枯黄或被雪覆盖"
- 花卉: {花卉状态} (例如: "冬季无花"、"春季樱花盛开")

地面覆盖:
- 冬季: "地面覆盖厚白雪"
- 秋季: "地面散落落叶"
- 春季: "地面湿润，新草萌发"
- 夏季: "地面干燥，草地浓密"

大气条件:
- 天空: {天空状态} (例如: "冬季阴沉灰色低云"、"夏季明亮蓝天")
- 光照: {光照}
  夏季: "明亮强烈阳光，短阴影"
  冬季: "低角度冷色调阳光，长阴影"
- 温度感: {温度氛围} (例如: "冬季寒冷雾气"、"夏季温暖通透")

建筑互动:
- 窗户: {窗户变化} (例如: "冬季窗户结霜"、"夏季窗户打开")
- 照明: {照明变化} (例如: "冬季黄昏提前开启室内暖光")

技术要求:
- **保持建筑、硬景和构图完全不变**
- **仅改变季节相关的自然元素**
- 真实的季节特征(雪的质感、落叶的堆积方式)
- 符合该季节的光线角度和色温

结果应能清晰展示同一景观设计在不同季节的表现力。
```

### English Version

```
Transform this landscape scene to show the specified season.

Seasonal Settings:
- Target Season: {SEASON} (e.g., "deep winter", "early spring", "mid-summer", "late autumn")

Vegetation Changes:
- Deciduous Trees: {TREE_STATE}
  Spring: "tender green new leaves"
  Summer: "dense deep green canopy"
  Autumn: "golden and orange-red foliage"
  Winter: "bare branches without leaves"
- Evergreens: {EVERGREEN_STATE} (e.g., "remain green but slightly darker")
- Lawn: {LAWN_STATE}
  Spring/Summer: "vibrant green and lush"
  Autumn: "yellow-green mixed"
  Winter: "brown/dormant or snow-covered"
- Flowers: {FLOWER_STATE} (e.g., "no flowers in winter", "cherry blossoms in spring")

Ground Cover:
- Winter: "ground covered in thick white snow"
- Autumn: "fallen leaves scattered on ground"
- Spring: "moist ground, new grass emerging"
- Summer: "dry ground, dense grass"

Atmospheric Conditions:
- Sky: {SKY_STATE} (e.g., "winter grey overcast with low clouds", "summer bright blue sky")
- Lighting: {LIGHTING}
  Summer: "bright intense sunlight, short shadows"
  Winter: "low-angle cool-toned sunlight, long shadows"
- Temperature Feel: {TEMPERATURE_ATMOSPHERE} (e.g., "winter cold with mist", "summer warm and clear")

Building Interaction:
- Windows: {WINDOW_CHANGES} (e.g., "frost on windows in winter", "open windows in summer")
- Lighting: {LIGHTING_CHANGES} (e.g., "early dusk in winter activates warm interior lights")

Technical Requirements:
- **Keep architecture, hardscape, and composition completely unchanged**
- **Only alter nature-related seasonal elements**
- Realistic seasonal characteristics (snow texture, fallen leaf accumulation patterns)
- Accurate light angle and color temperature for the season

The result should clearly demonstrate how the same landscape design performs across different seasons.
```

---

## Tips / 使用技巧

### 中文

- **结构锁定**: 使用Structure Reference(强度0.8)确保建筑和硬景不变
- **季节特征库**: 建立"夏季=短阴影+蓝天"、"冬季=长阴影+低云+雪"的特征清单
- **植物知识**: 了解常见树种(如枫树、樱花、松树)在不同季节的真实表现
- **系列对比**: 一次性生成春夏秋冬4张图，制作对比图册展示全年景观效果
- **细节强化**: 冬季添加"窗户结霜"、"烟囱冒烟"等细节增强季节氛围

### English

- **Structure Locking**: Use Structure Reference (strength 0.8) to ensure architecture and hardscape remain unchanged
- **Seasonal Feature Library**: Build a checklist like "Summer=short shadows+blue sky", "Winter=long shadows+low clouds+snow"
- **Plant Knowledge**: Understand how common tree species (maple, cherry, pine) actually appear in different seasons
- **Series Comparison**: Generate all 4 seasons (spring/summer/autumn/winter) at once to create a year-round landscape showcase
- **Detail Enhancement**: Add details like "frost on windows", "smoke from chimney" in winter to enhance seasonal atmosphere

---

## 标签 / Tags

`#专项应用` `#季节变化` `#景观设计` `#四季对比` `#植物配置` `#气候模拟`

`#specialized-tasks` `#seasonal-variation` `#landscape-design` `#seasonal-comparison` `#planting-design` `#climate-simulation`

---

**Last Updated**: 2025-11-29
**Contributor**: Project Maintainer
**Version**: 2.0
