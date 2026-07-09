# Math Preview Workflow

Use this reference for Grade 10 math preview coaching.

## Daily Check Recipe

Given lesson notes, generate 8 questions:

- 2 concept judgment questions.
- 3 basic calculation or direct-application questions.
- 2 variant questions.
- 1 common-mistake question.

Do not include answers until the student responds.

## Difficulty Boundary

Stay at new Grade 10 preview level. Prefer foundations:

- Sets and set operations.
- Common logic language.
- Function concept, domain, range, and representation.
- Function monotonicity and parity.
- Exponents and logarithms at introductory level.
- Quadratic function, equation, and inequality connections.
- Basic inequality only if the school preview sequence reaches it.

Avoid competition-style tricks, long multi-step synthesis, and content far beyond the first semester unless explicitly requested.

## Mistake Causes

Classify math mistakes as exactly one primary cause:

- 概念不清: definition, theorem, or condition is misunderstood.
- 计算错误: method is right but arithmetic or algebra manipulation is wrong.
- 条件遗漏: missed domain, interval, symbol, quantifier, or hidden condition.
- 题型不熟: understands pieces but cannot recognize the problem pattern.

## Prompt Templates

Daily preview:

```text
你是高一数学预习教练。下面是我的听课笔记。

【笔记】
[粘贴笔记]

请基于笔记给我出 8 道题：
1. 2 道概念判断题；
2. 3 道基础题；
3. 2 道变式题；
4. 1 道易错题。

要求：
- 难度适合刚预习高一数学的新生；
- 不要直接给答案；
- 每题只考一个关键点；
- 题目后标注考查知识点。
```

Grading:

```text
下面是我的作答。请批改。

【题目和我的答案】
[粘贴内容]

请按这个格式反馈：
1. 每题对错；
2. 错题的错因分类：概念不清、计算错误、条件遗漏、题型不熟；
3. 正确思路，不要直接堆完整答案；
4. 给每道错题再出 1 道同类变式题；
5. 最后让我用一句话复述今天最重要的知识点。
```

Low score remediation:

```text
我刚学这个知识点，小测正确率低于 60%。
请你不要出难题，先用初中生能听懂的语言重新解释这个概念。
然后给我 3 道最基础的题，确认我是否真的理解。
```

3-day retest:

```text
下面是我 3 天前做错的题。请你不要直接给答案。
请先把原题稍微改编成一道同类题，让我重新做。
如果我还错，请判断是概念没懂，还是计算/审题问题。

【错题】
[粘贴错题]
```
