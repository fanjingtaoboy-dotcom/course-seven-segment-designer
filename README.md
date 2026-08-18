# Course Seven Segment Designer

Codex skill for designing, diagnosing, scoring, and rebuilding live-course structures using a seven-segment psychological progression:

```text
暖场破冰 -> 引发需求 -> 挖掘痛点 -> 原理讲解 -> 案例应用/实操演示 -> 总结回顾 -> 结尾升华
```

This skill is designed for live public classes, training-camp lessons, and online topic lessons. It helps an AI assistant produce structured course outlines, diagnose course drafts or transcripts, score a lesson on 1/3/5/7/9 anchors, explain why a course cannot move to a higher band, and produce pyramid-style reconstruction plans.

## Install

After this repository is published to GitHub, install with Codex's skill installer:

```text
Use $skill-installer to install:
https://github.com/fanjingtaoboy-dotcom/course-seven-segment-designer/tree/main/skills/course-seven-segment-designer
```

Or with the installer helper:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo fanjingtaoboy-dotcom/course-seven-segment-designer \
  --path skills/course-seven-segment-designer
```

The skill becomes available on the next Codex turn after installation.

## Example Prompts

```text
请使用 $course-seven-segment-designer 诊断这节直播课逐字稿，给出七段结构识别、评分、不能升档原因和金字塔重构方案。
```

```text
请使用 $course-seven-segment-designer 帮我设计一节 60 分钟直播公开课，目标学员是新手门店老板，课程目标是让他们学会设计第一次体验课。
```

```text
请使用 $course-seven-segment-designer 快速检查这个课程大纲，指出最影响学习效果的三个问题。
```

## Repository Structure

```text
skills/course-seven-segment-designer/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── framework.md
    ├── learner-analysis.md
    ├── diagnosis-rubric.md
    ├── scoring.md
    ├── calibration-cases.md
    └── output-templates.md
```

## Quality Targets

This skill is intentionally built as a progressive-disclosure skill:

- `SKILL.md` stays lean and routes the task.
- References carry detailed standards only when needed.
- Diagnosis requires learner-source boundaries.
- Formal scoring requires secondary-task checks and key tertiary acceptance checks.
- Course reconstruction must produce a pyramid, not just seven module names.

## Attribution And License

This project is licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). You may share and adapt it, but must give appropriate attribution.

Before publishing, replace the author placeholder in [LICENSE](LICENSE) with the exact public attribution name you want others to use.
