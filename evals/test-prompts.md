# Test Prompts

Use these prompts to regression-test the skill before publishing or after major edits.

## Usage Help

```text
我刚安装了 $course-seven-segment-designer，这个 skill 怎么用？我需要提供哪些材料？
```

Expected behavior: provide install/use reminder, input template, common task prompts, and output modes; do not diagnose without course material.

## Explicit Invocation

```text
请使用 $course-seven-segment-designer 诊断下面这节直播课大纲，输出七段结构识别、一级模块误判问题、总分、不能升档原因和金字塔重构方案。
```

## Implicit Trigger

```text
我有一节 90 分钟直播公开课逐字稿，想知道课程结构是否完整、哪里导致学员听完不行动，请帮我做深度诊断。
```

## Framework Design

```text
帮我设计一节 60 分钟直播课。目标学员是刚入门的私域运营，主题是如何设计第一次成交型咨询，学完要能写出自己的咨询流程。
```

Expected behavior: build learner card, state assumptions, output parameter snapshot, then seven fixed segments with secondary tasks and wording landing points.

## Quick Diagnosis

```text
先快速看看这个大纲最大的问题，不要写长报告。
```

Expected behavior: use quick mode, keep seven-segment logic, say what was omitted.

## Missing Learner Data

```text
这是我的课程大纲，帮我判断能不能讲。标题：三步提升表达力。内容：开场、表达重要性、三个表达技巧、案例、总结、作业。
```

Expected behavior: mark learner profile, stage, pain, and action as inferred or missing; avoid confident claims.

## Scoring Boundary

```text
请给这节课打分，并说明为什么不能给 7 分。
```

Expected behavior: read scoring reference, identify closest anchor, apply cannot-upgrade rules.

## Misclassification Trap

```text
老师让大家在公屏打出自己想解决的问题，然后直接说这就是引发需求，继续讲理论。这个判断对吗？
```

Expected behavior: identify "收集需求" vs "引发需求", explain missing ability gap and learning reason.

## Non-Main-Thread Content

```text
这节课中间有抽奖、口令、助教提醒、作业打卡和明日课程预告，它们是不是应该成为单独的课程管理模块？
```

Expected behavior: reject eighth module; classify into the seven segments or mark as main-line interference.

## Rewrite Request

```text
请把这节课的总结回顾和结尾升华改得更有行动力，并解释每句优化话术修复了哪个二级任务。
```

Expected behavior: use diagnosis-rubric and output-templates; include key sentence mapping.

## Calibration Case

```text
我想做 1/3/5/7/9 分档样例，请帮我列每档差异，要求不要把高分样例简单写得更长。
```

Expected behavior: use same-word-count calibration principle and anchors.

## Long Transcript Cleanup

```text
请使用 $course-seven-segment-designer 先理解这份 90 分钟训练营逐字稿，不要评分。请输出生产标签归类、七段结构映射、两个实操循环、非主线内容和下一步诊断建议。
```

Expected behavior: read transcript-processing and production-label-map; do not quote large transcript blocks; produce a cleaned structure map before diagnosis.

## Mature Delivery Script

```text
这是两份成熟交付课逐字稿，讲师不同，数据不做参考。请评估它们能怎样反哺课程七段 skill 的迭代，必须脱敏。
```

Expected behavior: separate maturity from score, avoid ranking teacher personality, extract reusable anonymized patterns and residual upgrade rules.

## Training-Camp Priority

```text
请诊断这节训练营单课，优先级是交付效果、次日到课、交作业，输出给讲师看的修改建议。
```

Expected behavior: read course-types and teacher-feedback; treat attendance/homework as support goals under the seven segments, not separate modules.

## Production Label Trap

```text
逐字稿里有“案例佐证、整体课程安排、注意事项、学员案例效果、布置作业、明日预告、到课福利”，这些要不要作为七段之外的新模块？
```

Expected behavior: reject eighth module, map labels by function, and flag interference when they crowd the main line.
