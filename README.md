# High School Preview Coach

一个个人使用的 Codex Skill，用来帮助高一新生在开学前预习数学和英语。

它的目标不是替代老师或教材，而是把 AI 固定成一个学习教练：先检查复述，再检查理解，再批改答案，再分析错因，再安排复习任务，避免学生直接让 AI 给答案。

## 适用场景

- 看完 B 站数学或英语预习课后，检查 3-5 句话复述并生成小测。
- 批改学生自己的作答，并按错因分类。
- 把错题改编成 3 天后重做的同类题。
- 每周根据错题记录生成知识地图、复盘和下周重点。
- 为家长输出简短、可检查的学习进度总结。

## 支持科目

- 数学：复述检查、概念理解、小测、错因分类、变式题、3 天后重做、周复盘。
- 英语：复述检查、词汇、课文理解、语法点、句子翻译、错因复盘、听说读写周任务。

## 学习闭环

推荐按这个顺序使用：

```text
看视频 / 读材料
-> 学生用 3-5 句话复述
-> AI 检查遗漏和误解
-> AI 根据薄弱点出检查题
-> 学生独立作答
-> AI 批改、分类错因、给具体正反馈
-> AI 生成同类变式题
-> 3 天后错题重做
-> 每周生成知识地图和家长复盘
```

这个流程的重点是把“看懂了”拆成可验证的几个动作：能复述、能做基础题、能解释错因、能在 3 天后重做正确。

## 反馈方式

批改时不要只输出“对/错”，而是固定输出：

- 对错结果。
- 错因分类：概念不清、计算错误、条件遗漏、题型不熟等。
- 具体正反馈：指出学生这次做对或进步的一个真实细节。
- 正确思路：只解释缺失的一步，不直接堆完整答案。
- 同类变式题：每道错题给 1 道。
- 一句话复述任务：让学生重新表达本节最关键知识点。

## 安装

把本仓库放到 Codex skills 目录下：

```powershell
git clone https://github.com/kingfly2016/High-School-Preview-Coach.git "$env:USERPROFILE\.codex\skills\high-school-preview-coach"
```

如果目录已经存在，可以进入目录后更新：

```powershell
cd "$env:USERPROFILE\.codex\skills\high-school-preview-coach"
git pull
```

## 使用示例

复述检查：

```text
Use $high-school-preview-coach 做高一数学预习复述检查。
今天课程：简易逻辑
我的复述：
...
```

数学预习检查：

```text
Use $high-school-preview-coach 帮学生做今天的高一数学集合预习检查。
下面是他的听课笔记：
...
```

数学批改：

```text
Use $high-school-preview-coach 批改这份高一数学小测，并按错因给同类变式题。
题目和答案如下：
...
```

英语专项：

```text
Use $high-school-preview-coach 帮学生预习这组高一英语单词，先生成检查题，不要直接给答案。
单词表如下：
...
```

周复盘：

```text
Use $high-school-preview-coach 根据这周的数学和英语错题记录，生成知识地图和家长可读的周复盘。
记录如下：
...
```

## 文件结构

```text
high-school-preview-coach/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── study-record-template.csv
│   └── weekly-review-template.md
└── references/
    ├── english-preview.md
    └── math-preview.md
```

## 学习原则

- 学生先作答，AI 后批改。
- 视频课后先做 3-5 句话复述，再进入小测。
- 优先补基础，不追求超纲难题。
- 每次错题都记录错因和复做结果。
- 3 天后能独立做对，才算真正掌握。
- 每周用知识地图看到已掌握、摇摆中、待补的内容。
- 家长重点看完成情况、正确率、错题复做情况和具体进步。

## License

MIT License. See [LICENSE](LICENSE).
