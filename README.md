# AI-Skill — 个人 AI 技能合集

> 仓库地址：[https://github.com/Daniel1107/AI-skill](https://github.com/Daniel1107/AI-skill)

两个子目录分别服务于 **Codex** 和 **Claude Code**，各取所需。

## 目录结构

```
AI-skill/
├── codex-skills/        ← 21 个精选 Codex skill（直接 git clone 挂载使用）
├── claude code-skill/   ← 24 个精选合集（给 Claude Code 端使用）
└── README.md
```

## `codex-skills/` — Codex 精选（21 个）

已删重去冗，留存优质。

| 技能 | 用途 |
|------|------|
| agent-browser | 浏览器自动化 |
| baoyu-image-gen | AI 图像生成（10+ API 提供商） |
| canvas-design | 视觉设计 / 海报制作 |
| financial-statements | 财务报表生成 |
| find-skills | 发现与安装更多技能 |
| frontend-slides | 动画 HTML 演示文稿 |
| frontend-ui-ux | 前端 UI/UX 设计 |
| github | GitHub CLI 操作 |
| guizang-ppt-skill | 横向翻页网页 PPT（两套视觉风格） |
| Humanizer-zh | 中文 AI 痕迹去除 |
| markitdown | 文件转 Markdown（15+ 格式） |
| minimax-docx | Word 文档创建编辑（OpenXML SDK） |
| minimax-pdf | PDF 生成（15 种文档类型） |
| minimax-xlsx | Excel 电子表格创建编辑 |
| network-interface-health | 网络接口健康诊断 |
| pdf | PDF 处理工具 |
| pptx-generator | PPTX 生成（PptxGenJS） |
| project-planner | 项目规划与任务分解 |
| prompt-optimizer | 提示词优化专家 |
| self-improvement | 自我改进 / 学习记录 |
| validate-idea | 商业创意验证 |

**使用方式：**

```bash
# 只拉 codex-skills 子树作为稀疏检出
git clone --depth 1 --filter=blob:none --sparse https://github.com/Daniel1107/AI-skill.git $CODEX_HOME/skills
cd $CODEX_HOME/skills
git sparse-checkout set codex-skills

# 或直接全库拉取，手动挂载子目录
git clone https://github.com/Daniel1107/AI-skill.git
```

## `claude code-skill/` — Claude Code 精选（24 个）

已按 Claude Code 生态评估，删除 7 个冗余/过薄项。

| 技能 | 用途 |
|------|------|
| agent-browser | 浏览器自动化 |
| baoyu-image-gen | AI 图像生成（多 API） |
| canvas-design | 视觉设计 / 海报制作 |
| coding-agent | 后台编码代理（OpenClaw worker） |
| financial-statements | 财务报表生成 |
| find-skills | 发现与安装更多技能 |
| frontend-slides | 动画 HTML 演示文稿 |
| frontend-ui-ux | 前端 UI/UX 设计 |
| github | GitHub CLI 操作 |
| guizang-ppt-skill | 横向翻页网页 PPT |
| harness | Agent 团队与 Skill 架构元技能 |
| Humanizer-zh | 中文 AI 痕迹去除 |
| markitdown | 文件转 Markdown |
| minimax-docx | Word 文档创建编辑 |
| minimax-pdf | PDF 生成 |
| minimax-xlsx | Excel 电子表格 |
| network-interface-health | 网络接口健康诊断 |
| pptx-generator | PPTX 生成（PptxGenJS） |
| project-planner | 项目规划与任务分解 |
| prompt-optimizer | 提示词优化专家 |
| self-improvement | 自我改进 / 学习记录 |
| skill-vetter | 技能安全审查 |
| using-superpowers | 技能发现入口 |
| validate-idea | 商业创意验证 |

---

*由 [Daniel1107](https://github.com/Daniel1107) 维护*
