# stevenx-exam-skills

一个面向人文社科考试的高效复习与提分 Skill。它根据考试要求和用户资料，优先选择最值得掌握的内容，并通过闭卷训练和即时批改把知识转化为考场答案。

支持通用人文社科、法学和新闻传播学，可用于考点地图、冲刺计划、主动回忆、模拟训练、论述或案例题改写以及答案批改。

## 主要特点

- 得分优先：先拿基础分，再练高分项，时间不足时明确暂缓内容。
- 输出优先：用闭卷回忆、答题提纲和限时作答代替重复通读。
- 即练即改：每轮只解决当前最影响得分的 1–3 个问题。
- 资料优先：不编造重点、评分规则、法条或理论元数据。
- 按需加载：只读取当前学科和题型需要的参考模块。

## 下载与安装

### Git Clone

```bash
git clone https://github.com/custodiet0512/stevenx-exam-skills.git
```

### ZIP 下载

[下载最新 main 分支 ZIP](https://github.com/custodiet0512/stevenx-exam-skills/archive/refs/heads/main.zip)

### 安装到 Agent

可安装技能位于：

```text
skill/stevenx-exam-skills/
```

将这个完整目录复制到你的 Agent 所使用的 skills 目录，不要只复制 `SKILL.md`。不同 Agent 的技能目录和刷新方式可能不同，请以对应产品文档为准。

对于支持 `SKILL.md` 目录式技能的 Agent，复制 `skill/stevenx-exam-skills/` 后，按该 Agent 的方式重新加载技能。`agents/openai.yaml` 是可选的界面元数据；不识别该文件的 Agent 可以忽略它，核心行为由 `SKILL.md` 和 `references/` 提供。

安装完成后，以对应 Agent 支持的技能调用方式使用 `stevenx-exam-skills`；支持 `$skill-name` 语法的平台可调用 `$stevenx-exam-skills`。

## 使用示例

### 48 小时抢救

```text
使用 $stevenx-exam-skills。距离《传播学概论》考试还有 48 小时，附件是讲义和两套真题。先做最小诊断，再给我保过导向的安排；所有高频判断都注明依据。
```

### 从资料建立考点地图

```text
使用 $stevenx-exam-skills，把这份法理学笔记整理成 Evidence Map。区分资料明确、结构推断和待核验内容，不要根据常识补写老师的考试重点。
```

### 逐题互动训练

```text
使用 $stevenx-exam-skills，根据我提供的社会学复习大纲一次出 3 题。先不要展示答案；我回答后只指出最影响得分的问题，并立即给下一组变式训练。
```

### 提交答案后批改

```text
使用 $stevenx-exam-skills 批改下面这道新闻评论题。评分细则未提供，请给等级或区间判断和置信度，不要编造逐点分值；指出依据、缺漏、事实风险，并给最小必要的改写示范。
```

## 目录

```text
skill/stevenx-exam-skills/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── drill-formats.md
    ├── journalism.md
    ├── law.md
    └── liberal-arts.md
```

## 使用边界

- 本技能提供复习与训练辅助，不保证考试成绩，也不提供无依据的精确押题。
- 通用题型结构不等于某次考试的正式评分标准；教师要求、考试说明和正式评分细则优先。
- 法律内容用于考试学习，不构成现实法律意见；现行法与现实案件应核验权威来源并在需要时咨询专业人士。
- 使用真实笔记、试卷或作答前，请自行移除姓名、学号、联系方式和未公开教学资料等敏感信息。

## 贡献

欢迎通过 Issue 描述实际使用场景、失败示例或资料类型。提交修改时，请保持资料边界明确，避免加入未经核验的评分断言、法条编号、理论元数据或“必考”结论。

## License

[MIT](LICENSE)
