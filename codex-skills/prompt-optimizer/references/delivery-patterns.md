# Delivery Prompt Patterns

Use this reference only for concrete deliverables.

## PPT / PPTX

Include:

- topic and purpose
- target audience
- number of slides or duration
- density: speaker-led or reading-first
- visual style and brand constraints
- source materials
- required sections
- output format: editable PPTX, HTML deck, or outline only
- acceptance checks: no overflow, consistent visual system, readable charts, speaker notes if needed

Recommended downstream Skill:

- `ppt-master` for high-quality editable PPTX
- `pptx-generator` for faster PPTX generation or editing
- `frontend-slides` for browser-based HTML deck
- `guizang-ppt-skill` for magazine/Swiss style single HTML deck

## DOCX / Report

Include:

- document type
- target reader
- sections
- tone
- required tables or citations
- formatting requirements
- output format
- acceptance checks

Recommended downstream Skill: `minimax-docx`.

## PDF

Include:

- document purpose
- page count or length
- visual style
- print or screen use
- required charts, tables, cover, appendix
- acceptance checks for layout and rendering

Recommended downstream Skill: `minimax-pdf`.

## Spreadsheet / XLSX

Include:

- dataset or source inputs
- workbook tabs
- formulas
- formatting standards
- charts or pivots
- validation and recalculation checks

Recommended downstream Skill: `minimax-xlsx`.

## Image

Include:

- subject
- composition
- style
- aspect ratio
- color and lighting
- usage context
- negative constraints

Recommended downstream Skill: `baoyu-image-gen` or `imagegen`.

## Video

Include:

- target platform
- duration
- audience
- structure or timeline
- scenes or shots
- narration, captions, music, transitions
- deliverable format

## Code / Multi-file Project

Include:

- goal
- tech stack
- repo constraints
- expected files
- behavior requirements
- tests
- acceptance criteria
- non-goals

For implementation work, do not use this Skill as a replacement for planning, TDD, debugging, or verification Skills.