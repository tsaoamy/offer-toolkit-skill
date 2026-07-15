<div align="center">

**中文** · [English](./README.md)

# 🧰 Offer Toolkit

---

**三个求职工具打包成一个 Agent Skill 包 — JD · Resume · BQ。**

[![License](https://img.shields.io/badge/LICENSE-MIT-4c8bf5?style=flat-square&labelColor=333)](./LICENSE)
[![Version](https://img.shields.io/badge/VERSION-1.1.0-2ea44f?style=flat-square&labelColor=333)]()
[![Skills](https://img.shields.io/badge/SKILLS-3-2ea44f?style=flat-square&labelColor=333)]()
[![Stars](https://img.shields.io/github/stars/tsaoamy/offer-toolkit-skill?style=flat-square&label=STARS&color=e37f2c&labelColor=333)](https://github.com/tsaoamy/offer-toolkit-skill/stargazers)

[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-d97757?style=flat-square&labelColor=1a1a1a&logo=anthropic&logoColor=white)](https://claude.ai/code)
[![Cursor](https://img.shields.io/badge/Cursor-Skill-000000?style=flat-square&labelColor=1a1a1a)]()
[![Codex](https://img.shields.io/badge/Codex-Skill-2ea44f?style=flat-square&labelColor=1a1a1a)]()

</div>

把「看到心动岗位 → 拿到 offer」拆成一条可复用链路。可以整包装载，也可以只装其中某个子 skill。

```
看到心动岗位 → job-description-skill   解码 JD、出 Offer Strategy 报告
       ↓ 决定投
              resume-skill            改简历、打印级模板
       ↓ 拿到面试
              bq-skill                挖故事、建故事库、准备 BQ
```

## 里面有什么

| 子 skill | 做什么 |
|---|---|
| **[job-description-skill](job-description-skill/)** | 贴 JD + 简历，生成 HTML 报告：该不该投、匹配度、缺口、面试题预测、薪资区间、6 周行动计划。 |
| **[resume-skill](resume-skill/)** | 美化已有简历 / LinkedIn 导入 / 对话从零写。输出打印版 + 浏览器可编辑版 HTML。 |
| **[bq-skill](bq-skill/)** | 挖真实经历、STAR/CAR 结构化、建可复用故事库；也可按 JD 预测 Top 20 行为面试题并逐题准备。 |

## 三条共用规则

1. **不杜撰。** 经历、职责、数字必须来自你真实提供的内容。可 sharpen 表达，不编造事实。
2. **一次只问一个问题。** 建简历、挖故事、准备 BQ 都是对话，不是问卷。
3. **先结构化再产出。** 先落到标准数据模型，确认后再渲染 HTML / 生成答案。

## 安装

把整个 `offer-toolkit-skill/` 目录放进 skill 目录，例如：

- Claude：`~/.claude/skills/`
- Cursor：项目或用户 skills 目录

只想装一个？复制对应子目录（如 `resume-skill/`）即可，各自自包含。

## 触发词

| 你说 | 走哪个 |
|---|---|
| 贴 JD /「这个岗位该不该投」/「帮我看看这份工作」 | job-description-skill |
| 「帮我美化简历」/「从零做一份」/ 上传 PDF / 贴 LinkedIn | resume-skill |
| 「准备 behavioral 面试」/「Tell me about a time…」/「帮我挖一个故事」 | bq-skill |
| 「帮我找工作」/ 一次交出 JD + 简历 | 顶层 [SKILL.md](SKILL.md) 路由 |

## 目录结构

```
offer-toolkit-skill/
├── SKILL.md                        # 路由：意图 → 子 skill
├── README.md / README.zh.md
├── NOTICE.md                       # 来源说明
├── LICENSE                         # MIT
├── job-description-skill/          # ① JD 解码 + Offer Strategy 报告
├── resume-skill/                   # ② 简历生成 + 模板
└── bq-skill/                       # ③ 行为面试 / 故事库
```

生成的个人报告、简历、故事默认写入本地 `output/`（已在 `.gitignore` 中忽略，不会提交隐私数据）。

## License

MIT — 可 fork、改造、再发布。

Maintained by [Rick (@tsaoamy)](https://github.com/tsaoamy)

基于原项目 [yanliudesign/offer-toolkit-skill](https://github.com/yanliudesign/offer-toolkit-skill) 整理，详见 [NOTICE.md](./NOTICE.md)。
