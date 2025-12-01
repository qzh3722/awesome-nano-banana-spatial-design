# 如何为新CAD图生成JSON提示词

**English** | [简体中文](#中文版使用说明)

---

## English Version

### Overview

When you have a **new CAD floor plan** and need to generate a JSON prompt for it, use our **JSON Generator Prompt Template** instead of manually analyzing the drawing.

### Workflow

```
1. Prepare CAD Drawing
   ↓
2. Use JSON Generator Prompt Template
   ↓  
3. Vision AI Analyzes & Generates JSON
   ↓
4. Review & Refine JSON
   ↓
5. Use JSON with Image Generation
```

### Step-by-Step Instructions

#### Step 1: Prepare Your CAD Drawing

- Upload your CAD floor plan
- Ensure it's clear and readable
- Black & white line drawing preferred

#### Step 2: Load the JSON Generator Prompt

**File**: `prompts/json-generator-prompt.md` (English)  
**File**: `prompts/json-generator-prompt-cn.md` (Chinese)

Copy the **entire content** of this file.

#### Step 3: Send to Vision AI

1. Open a Vision-capable AI (e.g., Gemini, GPT-4 Vision, Claude with vision)
2. Upload your CAD floor plan image
3. Paste the **JSON Generator Prompt** as your message
4. Send

#### Step 4: Review the Generated JSON

The AI will output:

1. **Analysis Summary** (room counts, identified features)
2. **Complete JSON Prompt** (ready to use)

**Review Checklist**:
- [ ] All rooms from CAD are included
- [ ] Room labels are unique (no duplicates)
- [ ] Multi-room types are numbered correctly
- [ ] Task field mentions "UPLOADED"
- [ ] No estimated dimensions in JSON
- [ ] Critical counts are marked
- [ ] Separation rules are defined

#### Step 5: Refine if Needed

Common refinements:
- Add missing small rooms (storage, closets)
- Correct room type classifications
- Add specific critical constraints
- Adjust material descriptions

#### Step 6: Use the JSON

- Save as `prompts/[case-id]-json-[lang].json`
- Use with image generation AI
- Embed in README if this becomes a new case

---

## 中文版使用说明

### 概述

当你有**新的CAD平面图**需要生成JSON提示词时，使用我们的**JSON生成器提示词模板**，而非手工分析图纸。

### 工作流程

```
1. 准备CAD图纸
   ↓
2. 使用JSON生成器提示词模板
   ↓  
3. Vision AI分析并生成JSON
   ↓
4. 审核与优化JSON
   ↓
5. 使用JSON进行图片生成
```

### 详细步骤

#### 第1步：准备CAD图纸

- 上传你的CAD平面图
- 确保清晰可读
- 推荐黑白线稿

#### 第2步：加载JSON生成器提示词

**文件**: `prompts/json-generator-prompt.md` (英文)  
**文件**: `prompts/json-generator-prompt-cn.md` (中文)

复制此文件的**完整内容**。

#### 第3步：发送给Vision AI

1. 打开支持视觉的AI（如Gemini、GPT-4 Vision、带视觉的Claude）
2. 上传你的CAD平面图图片
3. 粘贴**JSON生成器提示词**作为消息
4. 发送

#### 第4步：审核生成的JSON

AI会输出：

1. **分析摘要**（房间计数、识别的特征）
2. **完整JSON提示词**（可直接使用）

**审核清单**:
- [ ] CAD中所有房间都已包含
- [ ] 房间标签唯一（无重复）
- [ ] 多房间类型正确编号
- [ ] Task字段提到"上传的"
- [ ] JSON中无估计尺寸
- [ ] 关键计数已标记
- [ ] 分离规则已定义

#### 第5步：必要时优化

常见优化：
- 添加遗漏的小房间（储藏间、衣帽间）
- 修正房间类型分类
- 添加特定关键约束
- 调整材质描述

#### 第6步：使用JSON

- 保存为 `prompts/[案例ID]-json-[语言].json`
- 用于图片生成AI
- 如成为新案例，嵌入README

---

## Advanced Tips

### For Complex Floor Plans

If the floor plan is very large or complex:

1. **Increase Grid Density**: Ask AI to use 4×4 or 5×5 grid
2. **Separate Analysis**: Analyze by zones (public vs private areas)
3. **Multi-Pass Review**: Run generator twice, compare results

### For Commercial Spaces

Commercial spaces (offices, restaurants, retail) may need:
- Different room naming (MEETING ROOM A/B/C)
- More storage/utility spaces
- Specialized fixtures (commercial kitchen equipment)

Modify the generator prompt to emphasize commercial-specific categories.

### Quality Control

Always verify:
```
Generated JSON room_count >= Manual count from CAD
```

If numbers don't match → Re-analyze with emphasis on small rooms.

---

## Troubleshooting

### Issue: AI missed some rooms

**Solution**:
- Explicitly list the missing rooms in a follow-up message
- Ask: "Please add the following rooms I see in the CAD: [list]"

### Issue: Duplicate room labels

**Solution**:
- Review the numbering rules in the prompt
- Manually rename duplicates following our standard

### Issue: Too many decorative details

**Solution**:
- Remove dimension specifications
- Remove color codes
- Focus JSON on constraints, not descriptions

---

## Integration with Case Development

When developing a new case:

1. **Generate JSON** using this workflow
2. **Test with image generation** (2-3 iterations)
3. **Refine JSON** based on results
4. **Validate** against Anti-Regression Principles
5. **Add to repository** with proper naming
6. **Update README** with the new case

---

## Files Reference

| File | Purpose |
|------|---------|
| `json-generator-prompt.md` | English JSON generator |
| `json-generator-prompt-cn.md` | Chinese JSON generator |
| `2.1-cad-to-topview-json-en.json` | Example output (English) |
| `2.1-cad-to-topview-json-cn.json` | Example output (Chinese) |

---

**Questions?** Check DEVELOPMENT_CONTEXT.md or create an issue.
