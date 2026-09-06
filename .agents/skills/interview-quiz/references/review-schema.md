# Review Data Schema

技能在工作区根目录维护 `interview-review/`，推荐结构：

```text
interview-review/
├── wrong-answers.md
├── review-schedule.md
└── sessions/
    └── YYYY-MM-DD.md
```

## wrong-answers.md

每道错题一个条目，至少包含：

- `ID`：稳定编号，例如 `CXX-001`、`ALG-001`
- `题目`、`主题`、`来源`
- `我的回答`、`判定`、`关键缺口`、`示例/反例`
- `首次记录`、`上次复习`、`连续答对次数`
- `下次复习`、`状态`（待复习/已掌握）

## review-schedule.md

用 Markdown 表格维护到期视图：`ID`、`主题`、`下次复习`、`间隔天数`、`状态`。每次复习后更新，不重复复制完整题目。

## sessions/YYYY-MM-DD.md

记录当日题目、回答摘要、判定、来源和本轮统计。不要保存与复习无关的个人敏感信息。

## Date policy

使用工作区本地日期（当前环境为 Asia/Shanghai）。日期只写 `YYYY-MM-DD`。到期判断为“下次复习日期小于或等于今天”。
