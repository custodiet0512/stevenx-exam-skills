# stevenx-exam-skills

一个面向人文社科考试的 Skill。它不会先套用固定模板，而是从用户资料与考试约束出发，通过“证据建模 → 最小诊断 → 训练决策 → 作答批改 → 状态更新”循环，持续选择当前最值得练习的任务。

支持通用人文社科、法学和新闻传播学，可用于考点地图、冲刺计划、主动回忆、模拟训练、论述或案例题改写以及答案批改。

## 主要特点

- 资料优先：区分“资料明确”“结构推断”和“待核验”。
- 先诊断后规划：用少量高信息量任务识别知识、检索、应用、结构和时间问题。
- 动态训练：根据每次作答更新掌握状态，而不是一次生成静态复习清单。
- 证据化批改：没有正式评分细则时只给区间或等级判断，并标注置信度。
- 按需加载：根据任务读取法学、新传、通用文科或练习格式参考，减少无关上下文。

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

Codex 示例：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R stevenx-exam-skills/skill/stevenx-exam-skills "${CODEX_HOME:-$HOME/.codex}/skills/"
```

对于其他支持 `SKILL.md` 目录式技能的 Agent，同样复制 `skill/stevenx-exam-skills/`，然后按该 Agent 的方式重新加载技能。`agents/openai.yaml` 是可选的界面元数据；不识别该文件的 Agent 可以忽略它，核心行为由 `SKILL.md` 和 `references/` 提供。

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
使用 $stevenx-exam-skills，根据我提供的社会学复习大纲一次出 3 题。先不要展示答案；我回答后按 K/R/A/S/T 类型诊断并决定下一组题。
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
