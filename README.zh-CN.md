<div align="center">

![Awesome Nano Banana 空间设计 Banner](./assets/images/banner.jpg)

# Awesome Nano Banana 空间设计提示词库

> 专为空间设计专业人士精心策划的 Nano Banana Pro 提示词合集

<!-- Language Switcher -->
<table>
<tr>
<td align="center"><b>🌐 Language / 语言</b></td>
</tr>
<tr>
<td align="center">
<a href="./README.md">English</a> |
<b>简体中文</b>
</td>
</tr>
</table>

</div>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

## 项目简介

**Awesome Nano Banana 空间设计** 是一个精心策划的提示词库，旨在展示 Nano Banana Pro（Gemini 3 Pro Image）在解决真实空间设计挑战中的强大能力。这不仅仅是一个美图合集——而是一个专业工具包，专门用于解决建筑、室内设计和景观设计工作流中的具体痛点。

### 为什么选择这个库?

- **聚焦实际问题**: 每个提示词都解决一个具体的设计挑战(如"CAD转效果图"、"材质方案对比"、"光影分析")
- **逻辑优先方法**: 充分利用思考模式(Thinking Mode)处理复杂的空间推理，确保准确性
- **参考一致性**: 掌握使用参考图像保持设计一致性的技巧
- **生产就绪**: 提供完整参数，确保结果可复现、符合专业标准
- **双语支持**: 完整的中英文文档

## 目标用户

- 建筑师
- 室内设计师
- 景观设计师
- 3D渲染艺术家
- 设计专业学生

## 内容结构

本库包含 **100+个精选用例**，按照**设计师工作流阶段**组织，而非传统类别划分。这种基于工作流的方式更贴合设计师的实际工作过程，让您更容易找到当前任务所需的提示词。

### 🎨 01 - 概念构思
从零到创意方案。生成初始设计概念、探索风格方向、从文字描述可视化创意。

[浏览概念构思案例 →](./cases/01-concept-ideation/)

### 📐 02 - 空间规划
布局优化与动线设计。生成家具布局、优化空间利用、设计人流动线、定义功能分区。

**示例**: 客厅、办公室等空间的家具布局生成

[浏览空间规划案例 →](./cases/02-space-planning/)

### 🔧 03 - 技术转可视化
CAD/图纸转照片级可视化。将技术图纸(平面图、立面图、剖面图)转换为演示级渲染图。

**示例**: CAD平面图 → 彩色俯视图，景观总平面 → 鸟瞰可视化

[浏览技术转可视化案例 →](./cases/03-technical-to-visual/)

### 🎨 04 - 材质软装
材质细化与软装搭配。更换材质、测试色彩方案、设计软装配饰、转换风格。

[浏览材质软装案例 →](./cases/04-material-styling/)

### 🖼️ 05 - 场景渲染
最终演示效果图。生成高质量透视图、人视角场景、氛围渲染，适合客户演示。

[浏览场景渲染案例 →](./cases/05-scene-rendering/)

### ⚙️ 06 - 专项应用
特殊场景与高级功能。多语言文字渲染、图像编辑、视觉一致性、技术分析图等。

[浏览专项应用案例 →](./cases/06-specialized-tasks/)

---

### 传统分类索引

为了向后兼容，案例也可以通过原有的领域分类访问:
- [建筑](./cases/architecture/) - 建筑设计与可视化
- [室内](./cases/interior/) - 室内空间设计
- [景观](./cases/landscape/) - 景观建筑设计

## 快速开始

### 1. 按工作流阶段浏览
导航到与您当前任务匹配的工作流阶段:
- **从零开始?** → [01 - 概念构思](./cases/01-concept-ideation/)
- **有尺寸，需要布局?** → [02 - 空间规划](./cases/02-space-planning/)
- **有CAD/图纸，需要效果图?** → [03 - 技术转可视化](./cases/03-technical-to-visual/)
- **需要细化材质/风格?** → [04 - 材质软装](./cases/04-material-styling/)
- **准备最终渲染?** → [05 - 场景渲染](./cases/05-scene-rendering/)
- **特殊需求?** → [06 - 专项应用](./cases/06-specialized-tasks/)

### 2. 选择用例
每个案例包含(v2.0卡片式格式):
- **效果预览** - 大图展示输入→输出
- **提示词** - 双语提示词模板(中文+英文)
- **使用技巧** - 实用建议和变体方法
- **标签** - 双语标签便于搜索

### 3. 复制并定制
复制提示词结构，并根据您的具体项目需求进行调整。提示词设计灵活，带有清晰标注的占位符。

## 案例模板结构 (v2.0)

每个案例遵循简化的卡片式格式:

```markdown
# 案例标题（英文）/ 案例标题（中文）

## 效果预览 / Preview
[大图展示输入→输出示例]
*简短描述*

---

## 提示词 / Prompt

### 中文版
[完整的中文提示词，带有{占位符}]

### English Version
[完整的英文提示词，带有{PLACEHOLDERS}]

---

## Tips / 使用技巧

### 中文
- **技巧1**: 实用建议
- **技巧2**: 使用变体
- **变体**: 如何调整

### English
- **Tip 1**: Practical advice
- **Tip 2**: Usage variations
- **Variation**: How to adjust

---

## 标签 / Tags
`#标签` `#tags`

**最后更新**: 日期
**版本**: 2.0
```

## Nano Banana Pro 核心特性

本库旨在最大化利用以下模型能力:

- **思考模式(Thinking Mode)**: 增强的逻辑推理，处理复杂空间关系
- **多参考一致性**: 使用多张参考图像同时保持连贯性
- **精准文本渲染**: 在图像中生成准确的文字(标识、标签等)
- **4K细节**: 适合专业演示的高分辨率输出

## 贡献指南

我们欢迎贡献！请在提交前阅读我们的 [贡献指南](CONTRIBUTING.md)。

### 贡献方向:
- 新用例
- 改进的提示词
- 翻译优化
- 文档增强

## 路线图

### Framework v2.0 (当前 - 2025年11月)
- ✅ 仓库结构建立
- ✅ **工作流分类系统** (6个阶段)
- ✅ **简化案例结构** (卡片式+Tips)
- ✅ 3个示例案例更新至v2.0
- ✅ 双语文档 (中文+英文)

### 内容开发 (进行中)
- 🚧 100+个精选案例覆盖6个工作流阶段
- 🚧 实战测试的提示词
- 🚧 画廊式示例图片

### 未来计划
- 社区提交案例
- 视频教程
- 工作流集成指南
- 高级参数优化技术

## 项目状态与开发

📊 **Framework v2.0 已完成** | 3个示例案例(v2.0) | 工作流分类组织 ✅

**v2.0 新特性:**
- 工作流分类系统(贴合设计师实际工作流程)
- 简化案例结构: 效果预览 + 提示词 + 使用技巧 + 标签
- 6个工作流阶段: 概念 → 规划 → 技术转化 → 材质 → 渲染 → 专项
- 视觉优先设计，大图画廊式展示

查看详细开发历史、技术决策和AI上下文：
- 📖 **[开发上下文文档](./DEVELOPMENT_CONTEXT.md)** - 完整项目历史和AI助手上下文

查看项目规划和时间线：
- 🗺️ **[路线图](./docs/ROADMAP.md)** - 开发计划

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

## 致谢

- 为空间设计社区而建
- 由 Nano Banana Pro (Gemini 3 Pro Image) 驱动

## 联系我们

- 问题反馈: [GitHub Issues](https://github.com/qzh3722/awesome-nano-banana-spatial-design/issues)
- 讨论交流: [GitHub Discussions](https://github.com/qzh3722/awesome-nano-banana-spatial-design/discussions)

---

**注意**: 随着案例开发，请替换占位图像和链接为实际内容。

用心为设计师打造 ❤️
