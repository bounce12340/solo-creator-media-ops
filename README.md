# solo-creator-media-ops

**English** · [繁體中文](#繁體中文)

An open-source agent skill for running a one-person short-video channel with
a small team of AI agents: topic scouting, production, fact review,
multi-platform publishing, comment replies and nightly reconciliation. It came
out of a real daily posting operation (Instagram, Threads, X, Facebook,
YouTube Shorts, TikTok, LinkedIn) and focuses on the boring rules that keep
an automated channel from embarrassing its owner: approval gates, no guessed
facts, and "press post once".

## What's inside

```
SKILL.md                     core workflow, roles, golden rules
references/
  video.md                   format, fair use, voiceover, footage, motion, covers
  subtitles.md               bilingual subtitles, 2-line limit, ≤0.3 s drift
  post-copy.md               captions per platform, AI label, credits
  publishing-checks.md       queue, slot test, the three checks, failure handling
  review-checklist.md        fact editor checklist, optional viral scoring
  community.md               comment replies and escalation
  topics-intel.md            topic dedupe, benchmark split, "no update" rule
  operations.md              routines, nightly reconciliation, archive, handoffs
templates/
  approval-message.md        Action / Target / Reason (動作／對象／理由)
  review.md                  review report
  publish-queue.md           approved queue + published log
  posting-slots.md           slot test, then fixed slot
  config.example.md          your configurable defaults
```

## Install

**Claude Code / Claude skills**

```bash
git clone <THIS_REPO_URL> ~/.claude/skills/solo-creator-media-ops
```

**Cursor** (project or user skills folder)

```bash
git clone <THIS_REPO_URL> .cursor/skills/solo-creator-media-ops
```

**Any other agent:** point it at `SKILL.md` and let it open the reference
files as needed. Then copy `templates/config.example.md` to `config.md` and
fill in your own values. Keep real voice IDs and keys in environment
variables, not in the repo.

## Roles

| Role | Job |
|---|---|
| Orchestrator | Talks to the creator, assigns work, owns the queue, posts approved items |
| Producer | Script, voiceover, subtitles, footage, cover, platform copy |
| Fact editor | Reviews script and final cut before anything is published |
| Scout | Finds topics, dedupes them, watches benchmark accounts |
| Community manager | Replies to ordinary comments, escalates sensitive ones |
| Data reviewer | 24h / 72h metrics, slot tests, viral-score calibration |

## Defaults vs. safety rules

Rules marked **(default)** are one creator's taste (English voiceover with a
Chinese subtitle line, TikTok uploaded by hand, one post per day). Change them
in your config. The rest are safety rules: creator approval before anything
public, no guessed numbers, three checks per post, no automatic reposts, no
DMs, no voice cloning without consent. Keep those.

Not legal advice. Fair-use and advertising rules differ by country.

## License

MIT

---

## 繁體中文

一套開源的 agent skill，讓一個人用幾個 AI agent 經營短影音帳號：找選題、製作、
事實審稿、多平台發文、回留言、每晚對帳。內容來自一個實際每天發文的帳號
（IG、Threads、X、FB、YouTube Shorts、TikTok、LinkedIn），重點放在讓自動化帳號
不出包的規則：發之前一定要本人核准、數字查不到就不寫、發文鍵只按一次。

### 內容

- `SKILL.md`：核心流程、角色分工、基本守則。
- `references/`：每個規則領域一份，包括影片內容、字幕、貼文文案、發文三查、
  審稿清單、社群互動、選題與情報、日常營運。
- `templates/`：核准訊息（動作／對象／理由）、審稿 review.md、發布佇列、
  發文時段、個人設定範本。

### 安裝

- Claude Code：clone 到 `~/.claude/skills/solo-creator-media-ops`。
- Cursor：clone 到專案的 `.cursor/skills/solo-creator-media-ops`。
- 其他 agent：讓它讀 `SKILL.md`，需要時再開 references。

接著把 `templates/config.example.md` 複製成 `config.md`，填上你自己的設定。
聲音 ID、API key 放在環境變數，不要寫進 repo。

### 角色分工

| 角色 | 負責 |
|---|---|
| 總管（Orchestrator） | 跟本人溝通、派工、管發布佇列、發已核准的內容 |
| 內容製作（Producer） | 腳本、配音、字幕、素材、封面、各平台文案 |
| 事實編輯（Fact editor） | 發布前審腳本和成片 |
| 情報偵察員（Scout） | 找選題、查重、看對標帳號 |
| 社群經營（Community manager） | 回一般留言，敏感留言先問本人 |
| 數據復盤師（Data reviewer） | 記 24 小時／72 小時數據、時段測試、校正爆文分數 |

### 預設和安全規則

標 **(default)** 的是可調整的個人偏好，例如英文配音加中文副字幕、TikTok 自己上傳、
一天發一支，改 config 就好。其他是安全規則：公開的東西都要本人核准、數字不用猜的、
每則貼文做三查、不自動重發、不碰私訊、沒有本人同意不複製聲音。這些建議保留。

本文件不是法律意見。合理使用和廣告法規各國不同。

### 授權

MIT
