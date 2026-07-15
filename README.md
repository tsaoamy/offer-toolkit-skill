<div align="center">

[中文](./README.zh.md) · **English**

# 🧰 Offer Toolkit

---

**Three job-hunt tools in one agent skill pack — JD · Resume · BQ.**

[![License](https://img.shields.io/badge/LICENSE-MIT-4c8bf5?style=flat-square&labelColor=333)](./LICENSE)
[![Version](https://img.shields.io/badge/VERSION-1.2.0-2ea44f?style=flat-square&labelColor=333)]()
[![Skills](https://img.shields.io/badge/SKILLS-3-2ea44f?style=flat-square&labelColor=333)]()
[![Stars](https://img.shields.io/github/stars/tsaoamy/offer-toolkit-skill?style=flat-square&label=STARS&color=e37f2c&labelColor=333)](https://github.com/tsaoamy/offer-toolkit-skill/stargazers)

[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-d97757?style=flat-square&labelColor=1a1a1a&logo=anthropic&logoColor=white)](https://claude.ai/code)
[![Cursor](https://img.shields.io/badge/Cursor-Skill-000000?style=flat-square&labelColor=1a1a1a)]()
[![Codex](https://img.shields.io/badge/Codex-Skill-2ea44f?style=flat-square&labelColor=1a1a1a)]()

</div>

Turn “saw a job I want → get an offer” into a reusable pipeline. Install the whole pack, or just one sub-skill.

```
See a job you want → job-description-skill   decode the JD, get an Offer Strategy report
       ↓ decide to apply
                     resume-skill            tailor & polish, print-ready templates
       ↓ get the interview
                     bq-skill                mine stories, build a story bank, prep BQs
```

## What's inside

| Sub-skill | What it does |
|---|---|
| **[job-description-skill](job-description-skill/)** | Paste a JD + your resume. Get an HTML report: whether to apply, match score, gaps, interview predictions, salary range, and a 6-week plan. |
| **[resume-skill](resume-skill/)** | Polish an existing resume, import from LinkedIn, or build from a chat. Outputs a print-ready HTML and a browser-editable version. |
| **[bq-skill](bq-skill/)** | Mine real experiences into a reusable STAR/CAR story bank. Can also reverse-engineer Top 20 behavioral questions from a JD. |

## Three shared rules

1. **Never fabricate.** Every experience, number, and title comes from what you actually said.
2. **One question at a time.** Resume building, story mining, BQ prep — conversations, not questionnaires.
3. **Structure first, render second.** Confirm the data model before generating HTML / answers.

## Install

Drop the whole `offer-toolkit-skill/` folder into your skills directory, e.g.:

- Claude: `~/.claude/skills/`
- Cursor: project or user skills folder

Only want one? Copy just that sub-folder — each is self-contained.

## Trigger phrases

| You say | Runs |
|---|---|
| Paste a JD / *“should I apply?”* / *“help me with this job”* | job-description-skill |
| *“Beautify my resume”* / *“build one from scratch”* / upload PDF / paste LinkedIn | resume-skill |
| *“Prep me for behavioral interviews”* / *“tell me about a time…”* / *“mine a story”* | bq-skill |
| *“Help me find a job”* / hand over JD + resume at once | Top-level [SKILL.md](SKILL.md) routes you |

## Layout

```
offer-toolkit-skill/
├── SKILL.md                        # Router: intent → sub-skill
├── README.md / README.zh.md
├── NOTICE.md                       # Attribution
├── LICENSE                         # MIT
├── job-description-skill/          # ① JD decoder + Offer Strategy report
├── resume-skill/                   # ② Resume builder + templates
└── bq-skill/                       # ③ Behavioral interview / story bank
```

Generated personal reports/resumes/stories go under local `output/` (gitignored).

## License

MIT — fork it, remix it, ship your own version.

Maintained by [Rick (@tsaoamy)](https://github.com/tsaoamy)

See [NOTICE.md](./NOTICE.md).
