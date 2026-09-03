# 课程七段与销讲八段衔接

## Core Rule

课程七段解决“学员是否听懂、学会、记住、愿意练习”；销讲八段解决“学员是否相信、觉得值、敢买、现在行动”。两者可以在同一节直播课里连续出现，但不能合并成一个结构。

## Dispatch Rule

When a user provides a whole lesson, first classify the requested work:

| User asks about | Primary skill | Reason |
|---|---|---|
| 课程结构、听懂、学会、记住、实操、作业、次日到课 | `course-seven-segment-designer` | the question is about teaching delivery and learner transfer |
| 报名、成交、价格、优惠、赠品、权益、顾虑、案例佐证、定金、咨询承接 | `sales-conversion-eight-segment` | the question is about buying confidence and conversion action |
| 一整节课里既有教学又有销讲 | both skills, in sequence | first judge S0 teaching gain, then judge sales chain |
| 用户只说“转化效果不好”但材料是整课逐字稿 | start with boundary map | decide whether the bottleneck is weak teaching gain, weak sales structure, or weak handoff |

Use the user's explicit request as priority. If the user only asks for course structure, mention that sales sections are outside the course-seven score and can be diagnosed separately.

## Boundary Signals

Teaching-main-chain signals:

- topic orientation, learner scene, pain cause, principle, method, demonstration, practice, summary, homework, next-session learning reason
- cases used to help learners understand or apply the method
- assistant reminders that support practice, homework, or feedback

Sales-main-chain signals:

- course/product introduction, price, discount, quota, bonus, refund, deposit, enrollment link, consultation, deadline
- cases used to prove product value, service effect, or buyer confidence
- assistant reminders that support ordering, registration, payment, or consultation handoff

Ambiguous content should be judged by function:

```text
Does this help the learner use today's method, or does it help the buyer decide the next paid action?
```

## S0 Handoff

Before sales starts, the teaching chain should create S0 teaching gain:

```text
学员觉得：刚才有用、老师可信、自己确实卡在下一步、继续学有理由。
```

If S0 is missing, sales diagnosis should say the conversion problem may begin before the sales section:

```text
销讲不是突然变差，而是教学主链没有先形成可承接的获得感。
```

当材料包含教学和销售转化：

1. 先划分教学主链与销讲主链。
2. 用课程七段判断教学交付质量。
3. 用 `$sales-conversion-eight-segment` 或销讲八段判断销售转化质量。
4. 不把报名、优惠、价格、案例佐证、助教发链接当成课程第八段。
5. 检查教学总结/结尾升华是否自然过渡到销讲的问题唤醒。

## Handoff Questions

| 衔接点 | 检查问题 |
|---|---|
| 教学获得 -> 问题唤醒 | 学员是否先觉得刚才内容有用，再被唤醒共性问题 |
| 结尾升华 -> 方案承接 | 是否先讲正确方向，而不是突然卖课 |
| 课后行动 -> 转化行动 | 作业、次日到课、报名购买是否彼此打架 |
| 教学信任 -> 销售信任 | 销讲是否延续老师可信度，而不是破坏教学信任 |

## Combined Output

```text
一、边界识别
- 教学主链范围：
- 销讲主链范围：
- 模糊/重叠内容：

二、教学主链结论
- 七段中最影响交付效果的点：
- 教学是否形成 S0 获得感：

三、销讲链路结论
- 是否需要调用/建议调用 $sales-conversion-eight-segment：
- 销讲链中最可能影响转化的点：

四、关键衔接断点
- 教学获得如何过渡到问题唤醒：
- 作业、次日到课、报名动作是否打架：

五、优先改稿动作
1.
2.
3.
```

## Red Flags

- 教学还没有形成获得感，就直接进入价格或优惠。
- 把“课程案例应用”误当成“销讲案例佐证”，导致教学评分虚高或销讲证据虚弱。
- 把“销讲案例佐证”误当成“教学实操”，导致课程七段第五段看似很强但学员不能练。
- 作业、次日到课、报名购买同时出现，但没有主次顺序。
- 结尾升华被硬广替代，既破坏教学信任，也削弱销售承接。
