# JD Bank · Index

每份分析过的 JD 的反查表。**每次新增 / 更新 JD 文件，必须同步更新这里。**

文件命名规则：`<company-slug>-<role-slug>-<YYYYMM>.md`
例：`tencent-ai-hr-communication-202607.md`

---

## 按状态汇总

| Status | 含义 |
|---|---|
| `decoded` | 仅做了 JD 解码 |
| `matched` | 跑了 Match Score |
| `tailored` | 简历已 tailor |
| `applied` | 已投递 |
| `interview` | 在面试流程中 |
| `offer` | 拿到 offer |
| `closed` | 决定不投 / reject / 关闭 |

---

## All JDs（按状态分组）

### 📊 Matched（已算匹配度）

| 文件 | 公司 | 岗位 | Match | ⭐ | 候选人 |
|---|---|---|---|---|---|
| [tencent-ai-hr-communication.md](tencent-ai-hr-communication.md) | 腾讯 | AI-HR培训生（沟通方向） | 68–78% | 4/5 | 曹健僖 |

### 🔍 Decoded（已解码，未决定）

> 暂无

### ✍️ Tailored（简历已改）

> 暂无

### 📤 Applied（已投）

> 暂无

### 🎤 Interview（面试中）

> 暂无

### 🎉 Offer

> 暂无

### 📁 Closed

> 暂无

---

## 按公司聚合

### 腾讯
- [tencent-ai-hr-communication.md](tencent-ai-hr-communication.md) — AI-HR培训生（沟通方向）/ HR STAR

---

## 按岗位类型聚合

### AI-HR / 人力资源培训生
- [tencent-ai-hr-communication.md](tencent-ai-hr-communication.md) — 腾讯 · 沟通方向

---

## 维护规则

1. **新增 JD 文件**：必须同时在「按状态」「按公司」「按岗位类型」三处登记。
2. **状态变更**：从一个 section 移到另一个，不要重复列。
3. **关闭一份**：移到 Closed，并在文件里补上「复盘」section。
4. **半年清理一次**：closed 超过 6 个月可以归档到 `jd-bank/archive/`。
