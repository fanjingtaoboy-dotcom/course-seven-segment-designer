---
name: course-seven-segment-designer
description: 用于直播课程、公开课、训练营单课、线上专题课的课程结构设计、七段结构诊断、逐字稿评分、课程大纲改造、话术重构、课程节奏占比检查、5A 心理推进检查和课后行动闭环优化。用户要求设计课程框架、评估课程是否完整、诊断课程大纲或逐字稿、按七段结构改稿、给课程打 1/3/5/7/9 分、说明为什么不能升档、生成金字塔重构方案、优化直播课开场/需求/痛点/原理/案例实操/总结/结尾时使用。
---

# Course Seven Segment Designer

## Core Purpose

Use the seven-segment course structure to help users design, diagnose, score, and rebuild live-course experiences. Treat the model as a psychological learning path, not as a slide-count template or a script formula.

The fixed seven segments are:

```text
暖场破冰 -> 引发需求 -> 挖掘痛点 -> 原理讲解 -> 案例应用/实操演示 -> 总结回顾 -> 结尾升华
```

Never add an eighth top-level course module. Classify rewards, discipline reminders, assistant arrangements, homework reminders, course previews, and sales prompts into the relevant seven segments, or mark them as main-thread interference.

## Reference Loading

Load only the references needed for the user request:

- Always read `references/framework.md` for the seven segments, 5A progression, persuasion variables, secondary tasks, and boundary rules.
- Read `references/learner-analysis.md` when learner information, course stage, lesson duration, course scene, or pacing affects the answer. For most design, diagnosis, scoring, and rewrite tasks, read it.
- Read `references/diagnosis-rubric.md` for course diagnosis, transcript review, module boundary disputes, common misjudgments, tertiary acceptance checks, and rewrite decisions.
- Read `references/scoring.md` when the user asks for scoring, grading, benchmark comparison, "why not higher", or upgrade path by score band.
- Read `references/output-templates.md` when producing a full diagnosis, quick diagnosis, framework design, rewrite plan, or self-check.
- Read `references/calibration-cases.md` when score calibration, D1 examples, training samples, or same-word-count benchmark reasoning is useful.

## First Response Behavior

Choose the smallest useful response that still completes the user's request:

- If the user provides enough material, begin the work directly. Do not ask for perfect inputs before giving value.
- If key learner information is missing, build an inferred learner card, label uncertainty, and list the missing inputs that would improve accuracy.
- If the user asks "怎么用/需要什么资料/给我模板", provide a user-facing input checklist and prompt examples instead of doing diagnosis.
- If the user provides only a vague course idea, return a starter seven-segment framework plus 3-5 high-impact questions for the next iteration.
- If the source material is long and the user did not ask for a full report, default to a compact diagnosis with the biggest structural problems and upgrade path.
- If the user asks for "完整诊断/正式评分/逐字稿深度诊断/整体重构", use the complete output structure and do not omit module-misjudgment or pyramid reconstruction.

Default to the user's language. For Chinese course materials, use Chinese section names and preserve the seven fixed module names.

## Operating Principles

1. Start with learner analysis. If the user has not provided target learner, stage, pain point, learning goal, and next action, infer cautiously from the material and label every inferred judgment.
2. Judge function, not labels. A section titled "pain point" is not qualified unless it creates the required psychological shift.
3. Diagnose at least to secondary tasks. For formal scoring, transcript diagnosis, reconstruction, or optimized wording, also use tertiary acceptance checks.
4. Use strict but useful language. Do not soften an unqualified module as "slightly weak" when its core task is missing.
5. Separate existence, function, and closure. A module can exist, fail its task, and still weaken the full learning loop.
6. Convert every recommendation into a rewrite action. Do not list types such as "三点复盘型" unless you explain what that type rewrites in this course.
7. Control resistance: difficulty resistance, trust resistance, action resistance, compliance resistance, over-marketing resistance, and anxiety resistance.
8. Do not invent teacher credentials, learner cases, medical/business results, platform data, or guaranteed outcomes.

## Workflow

### 1. Identify the Task Mode

Classify the user request into one or more modes:

| Mode | User intent | Required references |
|---|---|---|
| Framework design | Build a new course structure, outline, or live lesson plan | `framework.md`, `learner-analysis.md`, `output-templates.md` |
| Quick diagnosis | Fast check of an outline, transcript, or idea | `framework.md`, `learner-analysis.md`, `diagnosis-rubric.md` |
| Deep diagnosis | Formal module-by-module diagnosis of a course outline or transcript | all except calibration unless scoring is requested |
| Scoring | Give 1/3/5/7/9 score, explain why not higher, or compare versions | `framework.md`, `diagnosis-rubric.md`, `scoring.md`, usually `calibration-cases.md` |
| Rewrite/rebuild | Produce an upgraded structure, optimized wording, or full reconstruction | `framework.md`, `learner-analysis.md`, `diagnosis-rubric.md`, `output-templates.md` |
| Calibration | Create or judge scoring samples | `scoring.md`, `calibration-cases.md`, `diagnosis-rubric.md` |

If the user explicitly asks for a short answer, use quick mode and say what was intentionally omitted. Otherwise, use the complete workflow for diagnosis and scoring.

### 1.1 Set the Deliverable Preset

Use these presets to keep output useful:

| Preset | Use when | Output emphasis |
|---|---|---|
| Quick check | user says quick/先看/粗评 | conclusion, biggest 3 issues, highest-priority fixes |
| Standard diagnosis | user gives outline/transcript and wants diagnosis | learner card, seven-segment mapping, secondary-task gaps, priority advice |
| Formal scoring | user asks score/几分/为什么不能更高 | score anchor, cannot-upgrade rule, decisive evidence, upgrade task |
| Rewrite plan | user asks 改造/优化/重构 | pyramid reconstruction, rewrite actions, key wording examples |
| Teaching design | user asks 设计一节课/生成框架 | parameter snapshot, seven segments, secondary tasks, wording landing points |

### 2. Build the Learner Analysis Card

Before giving a firm judgment, identify:

- target learner
- learner scenario
- learner psychological starting point in A0/A1/A2/A3/A4
- course stage: D1 trust-building, knowledge delivery, or marketing conversion
- prior knowledge
- surface pain point
- deeper need
- what the learner should remember, understand, and apply
- next action after class
- main resistance
- whether each judgment is user-provided, source-material evidence, or inference

If critical information is missing, continue with a cautious inferred version and list the missing materials that would improve accuracy.

If the user wants an input template, provide:

```text
课程主题：
目标学员：
课程阶段：D1破冰 / 知识交付 / 营销转化
直播时长：
学员已有基础：
表层痛点：
深层需求：
本节课要记住：
本节课要理解：
本节课要掌握/应用：
课后下一步行动：
已有材料：大纲 / PPT / 逐字稿 / 录音转写 / 其他
希望输出：快速诊断 / 完整诊断 / 评分 / 重构方案 / 优化话术 / 新课框架
```

### 3. Analyze the Seven-Segment Chain

For every module, judge:

```text
存在判断：是否有对应内容
功能判断：是否完成本段二级任务
心理判断：是否推动对应 5A 心理变化
咬合判断：是否自然承接前后段
阻力判断：是否制造难度、信任、行动、合规或营销阻力
```

Use only these top-level modules:

1. 暖场破冰
2. 引发需求
3. 挖掘痛点
4. 原理讲解
5. 案例应用/实操演示
6. 总结回顾
7. 结尾升华

### 4. Diagnose at the Right Depth

For quick checks, use secondary tasks and concise evidence.

For formal scoring, transcript diagnosis, and rewrite/rebuild work, include tertiary checks for the decisive tasks:

```text
二级任务 -> 三级验收点 -> 原稿证据 -> 判定 -> 扣分点 -> 改稿动作
```

Expand tertiary checks especially when:

- a module is unqualified or partially qualified
- score is near a 3/5/7/9 boundary
- the user asks why the score is not higher
- surface actions are easy to misjudge as qualified
- optimized wording or a reconstruction plan is required

### 5. Score Only After Diagnosis

When scoring, follow:

```text
资料边界 -> 七段识别 -> 二级任务核查 -> 全课主线与咬合 -> 转化/记忆/行动闭环 -> 1/3/5/7/9 档位 -> 不能升档反向校验
```

Always output:

```text
总分：
最接近的评分锚点：
不能给更高分的原因：
如果要升一档，最先补的二级任务：
```

Do not award a higher score because a transcript is longer, more emotional, or has more interaction. Score structure quality, task completion, learner transfer, memory, and action closure.

### 6. Rebuild as a Pyramid

When reconstructing a course, do not stop at seven segment names. Output:

```text
顶层目标：
学员下课后要带走什么：

1. 暖场破冰：本段重构目标
   二级任务：
   关键三级验收点：
   话术落点：

... repeat through segment 7
```

Every optimized wording block must be followed by a brief mapping:

```text
关键句 -> 对应类型 -> 修复的二级任务 -> 推动的心理变化
```

## Output Style

Be direct, evidence-based, and practical. Prefer tables for diagnosis and scoring. Prefer a structured outline for design work. Keep wording sharp enough to teach the user the standard, but make every critique actionable.

For missing source material, say what can be inferred now and what cannot be judged firmly yet.
