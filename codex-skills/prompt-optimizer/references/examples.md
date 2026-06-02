# Prompt Optimizer Examples

## Simple Rewrite

Original:

```text
帮我写文章
```

Optimized:

```text
请围绕 `${topic}` 写一篇面向 `${target_audience}` 的文章。要求包含标题、引言、主体分析、案例或证据、结论建议，语气为 `${tone}`，字数控制在 `${word_count}` 左右。不要编造事实；不确定内容请标注并建议核验。
```

## PPT Prompt For ppt-master

Original:

```text
帮我做一个高质量 PPT，讲 AI 对投研的影响
```

Optimized:

```text
请使用 `ppt-master` 制作一份高质量、可编辑的 PPTX，主题为“AI 对投研工作的影响”。

目标受众：`${target_audience}`。
使用场景：`${presentation_context}`。
页数：`${slide_count}` 页。
密度：`${speaker_led_or_reading_first}`。

请先整理叙事结构，再生成逐页内容。每页需要包含：标题、核心观点、页面内容、视觉设计建议、必要图表、演讲备注。整体风格应专业、清晰、有高级感，避免模板化和空泛表达。

验收标准：逻辑链完整；每页只表达一个明确重点；图表和文字可读；PPTX 可编辑；无文字溢出；结论可操作。
```

## Multi-file Project Prompt

Original:

```text
做个网页工具
```

Optimized:

```text
请构建一个 `${tool_purpose}` 网页工具。目标用户是 `${target_user}`，核心工作流是 `${workflow}`。

技术约束：`${tech_stack}`。
输出要求：列出文件结构、实现主要页面和交互、提供运行命令、补充基础测试或手动验收步骤。

验收标准：首屏就是可用工具；移动端和桌面端布局正常；关键控件可操作；错误状态可见；不添加无关营销页。
```