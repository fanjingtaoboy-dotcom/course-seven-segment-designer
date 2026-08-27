# Course Seven Segment Designer

课程七段结构设计诊断器。A Codex skill for designing, diagnosing, scoring, and rebuilding live-course structures.

It uses a seven-segment psychological progression:

```text
暖场破冰 -> 引发需求 -> 挖掘痛点 -> 原理讲解 -> 案例应用/实操演示 -> 总结回顾 -> 结尾升华
```

This skill is designed for live public classes, training-camp single lessons, delivery classes, and online topic lessons. It helps an AI assistant produce structured course outlines, diagnose course drafts or transcripts, clean and map long transcripts, score a lesson on 1/3/5/7/9 anchors, explain why a course cannot move to a higher band, and produce pyramid-style reconstruction plans.

## What It Can Do

- Design a new live-course framework from learner information.
- Diagnose a course outline, PPT structure, transcript, or lesson script.
- Clean and structure long or noisy transcripts before diagnosis.
- Diagnose training-camp delivery lessons where the priorities are delivery effect, next-session attendance, and homework.
- Convert production labels such as welfare, cases, course preview, homework, and assistant follow-up into seven-segment functions.
- Produce teacher-facing feedback for course consultants and teaching researchers.
- Score a lesson using 1/3/5/7/9 anchors and explain why it cannot score higher.
- Rebuild a weak course into a seven-segment pyramid.
- Improve openings, need activation, pain excavation, principle explanation, practice/application, summary, and ending.
- Check course pacing, 5A psychological progression, and after-class action closure.

## Install In Codex

Paste this into Codex:

```text
请使用 $skill-installer 安装：
https://github.com/fanjingtaoboy-dotcom/course-seven-segment-designer/tree/main/skills/course-seven-segment-designer
```

After installation, the skill is usually available on the next Codex turn. If it does not appear, restart Codex and try again.

You can also install with the helper script:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo fanjingtaoboy-dotcom/course-seven-segment-designer \
  --path skills/course-seven-segment-designer
```

## Basic Usage

The safest way to invoke the skill is to mention it explicitly:

```text
请使用 $course-seven-segment-designer 诊断这节直播课结构。
```

You can also ask naturally with phrases such as "课程七段结构", "直播课结构诊断", "逐字稿评分", "课程大纲改造", or "金字塔重构方案".

## Input Template

Copy this template when you want a higher-quality result:

```text
请使用 $course-seven-segment-designer 帮我做【快速诊断 / 完整诊断 / 评分 / 重构方案 / 优化话术 / 新课框架】。

课程主题：
目标学员：
课程阶段：D1破冰 / 知识交付 / 营销转化
课程类型：训练营单课 / 交付课 / 公开课 / 专题课
直播时长：
学员已有基础：
表层痛点：
深层需求：
本节课要记住：
本节课要理解：
本节课要掌握/应用：
课后下一步行动：
优先级排序：交付效果 / 次日到课 / 交作业 / 咨询转化 / 其他
已有材料：大纲 / PPT / 逐字稿 / 录音转写 / 其他

请分析的材料：
【粘贴课程大纲、逐字稿或重点片段】
```

## Example Prompts

### Quick Diagnosis

```text
请使用 $course-seven-segment-designer 快速检查这个课程大纲，指出最影响学习效果的三个问题。
```

### Full Diagnosis

```text
请使用 $course-seven-segment-designer 诊断这节直播课逐字稿，给出七段结构识别、评分、不能升档原因和金字塔重构方案。
```

### Course Design

```text
请使用 $course-seven-segment-designer 帮我设计一节 60 分钟直播公开课，目标学员是新手门店老板，课程目标是让他们学会设计第一次体验课。
```

### Scoring

```text
请使用 $course-seven-segment-designer 给这节课打 1/3/5/7/9 分，并说明为什么不能给更高分。
```

### Rewrite

```text
请使用 $course-seven-segment-designer 把这节课重构成七段金字塔方案，并给出每段的二级任务、关键三级验收点和话术落点。
```

### Long Transcript Cleanup

```text
请使用 $course-seven-segment-designer 先整理这份 90 分钟逐字稿，输出生产标签归类、七段结构映射、实操循环和最影响交付效果的问题。
```

### Training-Camp Delivery

```text
请使用 $course-seven-segment-designer 诊断这节训练营单课。优先级是交付效果、次日到课、交作业。请输出给讲师看的保留、压缩、重说和排练清单。
```

## Output Modes

| Mode | Use when | Typical output |
|---|---|---|
| 快速诊断 | You want the biggest issues first | conclusion, evidence boundary, top 3 issues, priority fixes |
| 完整诊断 | You want a serious review | learner card, seven-segment mapping, secondary-task checks, key tertiary checks, reconstruction |
| 正式评分 | You need a score | score, closest anchor, cannot-upgrade reason, next upgrade task |
| 重构方案 | You need a better structure | top goal, learner takeaway, seven segments, secondary tasks, wording landing points |
| 优化话术 | You need wording | optimized lines plus mapping to tasks and psychological shifts |
| 长逐字稿整理 | You need a long script understood first | cleaned structure map, production label mapping, practice loops, risks |
| 讲师反馈 | You need a teacher-ready memo | keep/change/rewrite/rehearse checklist |

## Tips

- Provide learner information whenever possible. The skill can infer, but it will label inferred judgments.
- For formal scoring, include the full outline or transcript rather than only a title.
- For long transcripts, ask for "快速诊断" first, then request a full report for the most important segments.
- For noisy transcripts, ask for "先整理逐字稿" before scoring or rewriting.
- Do not create extra top-level modules such as "课程管理" or "奖励纪律"; the skill will classify those into the seven fixed segments.
- For practice classes, describe the intended action, demonstration, feedback standard, and homework.
- For private or proprietary course materials, ask the skill to use 脱敏分析. Public examples should use abstracted patterns instead of raw transcripts.

## Updating The Skill

If this repository changes later, reinstall with:

```text
请使用 $skill-installer 重新安装：
https://github.com/fanjingtaoboy-dotcom/course-seven-segment-designer/tree/main/skills/course-seven-segment-designer
```

## Repository Structure

```text
skills/course-seven-segment-designer/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── framework.md
    ├── learner-analysis.md
    ├── course-types.md
    ├── transcript-processing.md
    ├── production-label-map.md
    ├── diagnosis-rubric.md
    ├── scoring.md
    ├── mature-delivery-benchmarks.md
    ├── teacher-feedback.md
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
- Long transcript work must separate source cleanup, production labels, seven-segment function, and teacher-facing actions.

## Attribution And License

This project is licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). You may share and adapt it, but must give appropriate attribution.

Suggested attribution:

```text
Course Seven Segment Designer by 梵净淘宝网
```
