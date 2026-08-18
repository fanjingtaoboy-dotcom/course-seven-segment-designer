# Output Templates

## Deliverable Presets

Use these presets to keep answers sized to the user's intent.

| Preset | When to use | Must include | May omit or compress |
|---|---|---|---|
| 使用说明 | user asks how to use the skill | install/use prompts, input template, common modes | course diagnosis |
| 快速诊断 | user asks quick check | conclusion, information boundary, seven-segment completeness, 3 biggest issues, priority fixes | tertiary tables and long wording examples |
| 标准诊断 | user provides outline/transcript and wants diagnosis | learner card, overall judgment, seven-segment mapping, secondary-task checks, priority fixes | exhaustive tertiary checks unless decisive |
| 正式评分 | user asks score/grade/why not higher | score, closest anchor, evidence, cannot-upgrade rule, upgrade action | long full rewrite |
| 深度诊断 | user asks full/deep/transcript diagnosis | all full diagnosis chapters, key tertiary checks, module misjudgment, pyramid reconstruction | nothing structurally required |
| 改稿重构 | user asks optimize/rewrite/rebuild | diagnosis basis, pyramid plan, rewrite actions, key wording, wording mapping | full scoring unless requested |
| 新课设计 | user asks design/generate course | parameter snapshot, seven segments, secondary tasks, wording landing points, risks | original-evidence tables |

## Full Diagnosis

Unless the user explicitly asks for a short version, a complete diagnosis should include:

```text
一、用户分析卡
二、总判定
三、七段结构识别
四、一级模块误判问题
五、逐段深度诊断
六、整体重构方案：金字塔版
七、优先调整建议
八、输出自检
```

Minimum chapter requirements:

| Chapter | Must include |
|---|---|
| 用户分析卡 | target learner, stage, psychological starting point, surface pain, deeper need, next action, source/inference |
| 总判定 | score if requested, core conclusion, biggest strength, biggest problem, most harmful learning issue, most harmful action issue |
| 七段结构识别 | original content mapped to seven segments, qualified or not, main reason |
| 一级模块误判问题 | surface action, easily misjudged as, actual issue |
| 逐段深度诊断 | secondary task check, key tertiary acceptance check, main problem deep-dive, type translation, optimized wording mapping |
| 整体重构方案：金字塔版 | top goal, learner takeaway, seven segments, secondary tasks, key tertiary checks, wording landing points |
| 优先调整建议 | prioritized by impact, with why |
| 输出自检 | check against seven-segment standard |

## Per-Segment Diagnosis Block

Use this structure for each of the seven segments in deep diagnosis:

```text
当前内容：
功能判断：
是否合格：
学员资料依据：
5A 心理推进判断：
内容占比判断：
二级任务核查表：
三级验收核查表：
主要问题深拆：
调整切入思路：
可选方向：
推荐类型：
类型如何转化为改稿动作：
优化话术：
优化话术拆解：
风险与边界：
```

If answer length must be controlled, keep the secondary and key tertiary tables; compress optimized wording examples rather than removing structural judgment.

## Quick Diagnosis

Use when the user asks for quick review, rough check, or "先看大问题":

```text
结论：
资料边界：
七段完整性：
最主要的 3 个结构问题：
最高优先级改法：
需要补充的资料：
```

Keep quick diagnosis strict. Do not hide an unqualified module behind soft language.

## Usage Guidance Response

When the user asks how to use the skill, answer with:

```text
1. 安装方式
2. 最稳调用句式
3. 可提供的材料类型
4. 输入模板
5. 常用任务 prompt
6. 输出模式说明
```

Do not diagnose a course unless the user also provides course material.

## Framework Design

Start with parameter snapshot, then seven-segment body.

```text
【框架设计参数速览】
学员人群：
学员心理起点：
课程阶段类型：
课程场景：直播课程
授课时长：
语言风格：
核心痛点素材：
深层需求：
典型场景：
信任建立策略：
教学目标分解：记住 / 理解 / 掌握或应用
核心知识点：
案例应用/实操演示模式：
课后目标行动：
资料来源：用户提供 / 原稿推断 / 待补充
```

For each segment:

```text
1. 模块名称
5A 心理推进：
讲解目标：
本段采用类型：
类型如何转化为话术：
核心观点：
二级任务：
内容要点：
话术概括：
风险与边界：
```

Rules:

1. Keep seven modules in fixed order.
2. Each module must state 5A progression and teaching goal.
3. Each module must include secondary tasks.
4. Each module must include core view, secondary task, content points, and wording summary.
5. Pain excavation must use concrete pain.
6. Principle explanation must answer the cause or method logic behind the pain.
7. Case/practice must convert understanding into use.
8. Summary must help memory.
9. Ending must echo deeper need and give a specific next action.
10. Do not invent teacher identity, cases, data, credentials, or effects.

## Pyramid Reconstruction

Use for rebuilds and upgrade plans:

```text
顶层目标：
学员下课后要带走什么：

1. 暖场破冰：本段重构目标
   1.1 二级任务
   1.2 二级任务
   1.3 二级任务
   关键三级验收点：
   话术落点：

2. 引发需求：本段重构目标
   2.1 二级任务
   2.2 二级任务
   2.3 二级任务
   关键三级验收点：
   话术落点：

... through segment 7
```

## Optimized Wording Mapping

After optimized wording, include:

| 优化话术关键句 | 对应类型 | 修复的二级任务 | 学员心理变化 |
|---|---|---|---|
| sentence | type | task | shift |

## Required Summary Fields

For complete diagnosis, include:

```text
七段完整性判断：
七段顺序是否正确：
缺失模块：
过重模块：
过轻模块：
二级任务缺失模块：
一级模块误判问题：
最影响学习效果的问题：
最影响行动转化的问题：
优先调整建议：
整体重构方案：
需要补充的学员资料：
```

## Self-Check

Before completing a full diagnosis, self-check:

| 自检项 | 是/否 |
|---|---|
| 是否只使用七段作为一级模块，没有额外列出第八模块？ |  |
| 是否输出了用户分析卡，并标注资料来源或推断？ |  |
| 是否输出了总判定、评分、最大优点、最大问题？ |  |
| 是否输出了七段结构识别表？ |  |
| 是否输出了一级模块误判问题表？ |  |
| 七段逐段诊断是否都包含二级任务核查？ |  |
| 正式评分/深度诊断/改稿重构时，是否包含关键三级验收核查？ |  |
| 主要问题是否写到“表面动作-结构误判-二级缺口-三级缺口-心理失败-后续影响”？ |  |
| 推荐类型是否转译成具体改稿动作，而不是只列类型名称？ |  |
| 优化话术是否说明对应的二级任务、三级验收点和心理变化？ |  |
| 是否输出了金字塔版整体重构方案？ |  |
| 金字塔版是否写出顶层目标、学员下课带走内容、七段二级任务、关键三级验收点和话术落点？ |  |
| 是否输出了按优先级排序的调整建议？ |  |
| 是否标记了奖励、纪律、作业、预告等非教学主线内容应归入哪一段，或是否挤占主线？ |  |
