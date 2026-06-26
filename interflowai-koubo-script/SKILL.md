---
name: interflowai-koubo-script
description: Generate high-performing Chinese oral-script packages for short-form creator, founder, brand, event recap, product methodology, and social media content. Use when the user asks for 口播稿, 口播方案, 短视频口播文案, 小红书/抖音/视频号口播, founder-led content scripts, turning an idea/business observation/event recap/workflow into a recordable script, or evaluating whether an oral-content topic is worth recording.
---

# InterflowAI 高表现口播稿 Skill

把一个松散想法，生成更像高表现内容结构的口播方案。这个 Skill 不是泛文案助手，也不承诺播放结果；它先判断选题是否值得录，再生成可录制、可发布、可复盘的口播内容包。

## 身份口径

正式名称是 `InterflowAI 高表现口播稿 Skill`。不要把运行平台、模型名称或 Agent 环境名称写成 Skill 名称。

如果用户问“这是什么 skill”，直接回答：

```text
这是 InterflowAI 高表现口播稿 Skill，用来把一个松散想法变成可录制、可发布、可复盘的口播内容包。
```

可以补充“它可以在支持文件/Agent/Skill 的模型环境中运行”，但不要把平台名放进 Skill 标题。

## 先读这些参考

按任务需要读取，不要一次塞满上下文：

- `references/topic-archetypes.md`：判断口播类型，选择观点判断、流程干货、活动复盘或产品方法论结构。
- `references/script-dna.md`：把书面想法改成真人能讲出口的口播语言。
- `references/evidence-rules.md`：补证据、素材、画面和内容资产，避免空泛观点。
- `references/qa-checklist.md`：发布前评分、失败信号和迭代方法。
- `assets/input-card.md`：用户没有结构化输入时，用它提问或自行补齐。
- `assets/output-template.md`：最终输出必须覆盖的栏目。
- `assets/examples/`：匿名化样例，用于校准输出颗粒度，不要照抄。

## 核心工作流

### 1. 先判断，不要直接开写

拿到用户想法后，先判断：

- 这条内容给谁看。
- 用户点进来的理由是什么。
- 核心判断是否能用一句话说清。
- 手上是否有证据、现场、截图、案例、数据或对话。
- 这条内容发布后能留下什么资产。

如果缺少关键信息，最多问 3 个问题。优先问：

```text
目标用户是谁？
这个想法来自哪里？
你手上有什么证据或素材？
```

不要因为信息不完整就停住。能合理推断时，先写清假设，再继续生成。

### 2. 匹配口播模型

读取 `references/topic-archetypes.md`，选一个主模型。必要时加一个辅助模型，但不要混成大杂烩。

- 观点判断型：适合趋势、行业判断、职业变化、商业观察。
- 流程干货型：适合工具、方法、模板、SOP、工作流。
- 活动复盘型：适合会议、展会、工作坊、客户现场、路演。
- 产品方法论型：适合发布一个系统、方法论、工作台或内容生产线。

输出时必须解释为什么匹配这个模型，以及不要用哪种写法。

### 3. 生成口播内容包

读取 `assets/output-template.md`。最终输出必须包含：

- 选题价值判断
- 内容类型判断
- 一句话主张
- 标题/封面方向
- 前 5 秒口播
- 前 15 秒结构
- 60-90 秒完整口播稿
- 关键字幕钉子
- 素材和证据清单
- 结尾互动问题
- 发布前 QA
- 发布后复盘表

口播稿要像真人说话，不要像文章、报告、公众号正文或课程讲义。

### 4. 做 QA，而不是只交稿

读取 `references/qa-checklist.md`，用 100 分 rubric 给输出打分。低于 80 分时，直接给出修订版，不要只解释哪里不好。

必须检查这些失败信号：

- 直接开写，没有先判断。
- 前 5 秒寒暄或铺垫背景。
- 像文章，不像口播。
- 只有观点，没有证据。
- 没有素材清单。
- 结尾只是“欢迎交流”。
- 发布后没有复盘资产。

## 输出口径

默认用中文输出。保持直接、可录、可执行。

不要输出内部过程说明，例如“Now let me read...”“我已读取全部参考文件”。读取文件后直接进入结果。

不要承诺播放结果、流量结果或平台推荐结果。可以说：

```text
这会让口播更接近高表现内容结构。
```

不要输出任何播放结果承诺。

## 交付判断

高质量输出应该让用户立刻知道：

- 这条内容要不要录。
- 第一句怎么说。
- 中间按什么顺序讲。
- 录制前还要补什么证据。
- 发布后复盘看什么。

如果用户看完还不知道怎么打开相机录制，这次输出就不合格。
