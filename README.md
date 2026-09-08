# Interview Gym

一个面向技术面试的个人知识训练场。这里集中维护 C++、数据结构与算法资料，并通过 CodeX skill 把“阅读知识”转成“主动回忆、答题和复习”。

## 内容

- `c++interview/`：C++、数据结构、STL、设计模式和经典算法资料。
- `llm-algo-leetcode/`：算法与机器学习/LLM 相关的学习资料。
- `InterviewGuide/`：C++、ROS、DDS、MPC、系统与工程实践资料。
- `.agents/skills/interview-quiz/`：面试抽查 skill 的项目内版本。
- `interview-review/`：自动生成的错题集、复习计划和答题记录；该目录已加入 Git 忽略。

两个知识源目录作为资料来源使用，默认不由 skill 修改。

## 面试抽查

在 Codex 中调用：

```text
$interview-quiz cpp
$interview-quiz algorithm
$interview-quiz guide
$interview-quiz all
```

不指定范围时使用 `all`，默认生成 10 道题，一次回答一道。普通抽查优先生成未覆盖的新题，不会因为存在到期错题而自动变成复习；答错或部分正确时，skill 会给出来源、具体代码/反例和记忆提示。

复习到期错题：

```text
$interview-quiz review all
```

默认复习间隔为 1、3、7、14、30 天；连续答对会逐步延长间隔，再次答错则回到较短间隔。

## 维护约定

- 原始资料优先：事实应能追溯到对应知识源文件。
- 派生复习资料单独保存，不回写原始资料。
- 新增题库后纳入 `all` 范围，保持调用方式稳定。
