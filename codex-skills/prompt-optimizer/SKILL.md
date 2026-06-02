---
name: prompt-optimizer
description: "Use when the user explicitly asks to optimize, rewrite, enhance, structure, or design a prompt; when a vague idea must be converted into an executable AI prompt; or when a complex deliverable request needs a prompt before handing off to another Skill. Do not use for ordinary task execution, direct PPT/DOCX/PDF creation, simple Q&A, or when the user already provided complete requirements."
---

# Prompt Optimizer

## Purpose

Turn vague, incomplete, or scattered user intent into a clear prompt that another AI agent or Skill can execute. This Skill optimizes the prompt only. It does not complete the user's underlying task unless the user explicitly asks for execution after the optimized prompt is accepted.

## Trigger Rules

Use this Skill when the user asks for any of these:

- optimize a prompt, rewrite a prompt, improve a prompt, prompt engineering
- turn an idea into a prompt
- make this request clearer for AI
- create a prompt for PPT, PDF, DOCX, image, video, spreadsheet, webpage, code, research, or multi-file delivery
- structure a vague task before calling a production Skill such as `ppt-master`

Do not use this Skill for:

- direct execution of a clear task
- ordinary Q&A or explanation
- simple sentence polishing
- direct PPT/PDF/DOCX/image/video generation
- tasks where a domain Skill should run immediately, such as A-share strategy work or `ppt-master` production

## Core Rules

1. Preserve the user's real intent. Do not add unrelated goals.
2. Keep all placeholders unchanged, including `${name}`, `{{name}}`, `<name>`, and `[name]`.
3. Match the user's language unless they ask otherwise.
4. Add only useful context, constraints, output format, success criteria, and safety boundaries.
5. Keep simple prompts simple. Do not expand a small request into a bloated framework.
6. For high-stakes content, require uncertainty labeling and verification.
7. For deliverables, include structure, production requirements, and acceptance checks.

## Operating Modes

### Light Mode

Use when the prompt is simple or only mildly vague.

Output only:

```markdown
## 优化后的提示词
[rewritten prompt]

## 关键改动
- [1-3 concise bullets]
```

### Standard Mode

Use for most non-trivial prompt optimization requests.

Output:

```markdown
## 优化后的提示词
[complete rewritten prompt]

## 变量与占位符
- `[name]`: [meaning or keep as-is]

## 验收标准
- [clear pass/fail criteria]

## 不应做什么
- [scope and safety limits]
```

### Delivery Mode

Use when the optimized prompt is meant to drive a production Skill or generate a real deliverable such as PPTX, PDF, DOCX, spreadsheet, image, video, webpage, code, or a multi-file project.

Before writing the final prompt, identify the likely downstream Skill. Examples:

- High-quality editable PPTX: `ppt-master`
- Fast PPTX generation or editing: `pptx-generator`
- HTML/web deck: `frontend-slides` or `guizang-ppt-skill`
- DOCX: `minimax-docx`
- PDF: `minimax-pdf`
- XLSX/spreadsheet: `minimax-xlsx`
- Image generation: `baoyu-image-gen` or `imagegen`

Output:

```markdown
## 建议调用的 Skill
[skill name and reason]

## 优化后的执行提示词
[complete prompt for the downstream Skill]

## 交付物规格
- Type:
- Audience:
- Content structure:
- Style or tone:
- Required assets:
- Output format:

## 验收清单
- [quality checks]

## 风险与边界
- [what must be verified or avoided]
```

## Workflow

1. Identify the user's target task, intended output, audience, constraints, and missing information.
2. Decide Light, Standard, or Delivery Mode.
3. Preserve all meaningful details and placeholders.
4. Add missing execution details only when they help the downstream model or Skill produce a better result.
5. If the task is under-specified but still actionable, include reasonable assumptions as editable placeholders.
6. If the missing information would materially change the result, ask one concise clarifying question instead of inventing details.
7. Return the optimized prompt and a short explanation of key changes.

## When To Read References

Read `references/delivery-patterns.md` only when optimizing prompts for concrete deliverables such as PPT, PDF, DOCX, image, video, spreadsheet, webpage, code, or multi-file projects.

Read `references/examples.md` only when the user asks for examples, templates, or before/after prompt rewrites.

## Quality Bar

A good optimized prompt should be:

- executable without extra interpretation
- specific enough to avoid generic output
- scoped enough to avoid task drift
- structured enough to verify
- concise enough to be used directly

If the optimized prompt becomes longer than the original by more than 3x, check whether the added structure is truly necessary. If not, shorten it.