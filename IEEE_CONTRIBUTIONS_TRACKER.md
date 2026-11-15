# 🏆 IEEE Contributor Pull Requests Tracker

This document tracks all pull requests submitted by **Sri Ram Kunamsetty** to the upstream repository [praveenscience/One-File-Tools](https://github.com/praveenscience/One-File-Tools) as an **IEEE Contributor**, including submission timestamps, maintainer review feedback from Project Mentor **Praveen Kumar Purushothaman** (@praveenscience), and resolution status.

---

## 👤 Contributor Information
- **Contributor Name:** Sri Ram Kunamsetty
- **GitHub Username:** [@SriRamkunamsetty](https://github.com/SriRamkunamsetty)
- **Email:** `mohansriramkunamsetty@gmail.com`
- **Fork Repository:** [https://github.com/SriRamkunamsetty/One-File-Tools](https://github.com/SriRamkunamsetty/One-File-Tools)
- **Upstream Repository:** [https://github.com/praveenscience/One-File-Tools](https://github.com/praveenscience/One-File-Tools)
- **Project Mentor:** [Praveen Kumar Purushothaman (@praveenscience)](https://github.com/praveenscience)

---

## 📊 Summary Dashboard
- **Total Pull Requests Submitted:** 11 (10 Feature PRs + 1 Upstream CI Bugfix PR)
- **Merged PRs:** 1 ([PR #854](https://github.com/praveenscience/One-File-Tools/pull/854) - Upstream CI fix merged by @praveenscience)
- **Open Feature PRs:** 10
- **Maintainer Status:** Mentor reviewed all PRs and requested minor polish (Dark mode FOUC prevention IIFE, XSS sanitization, and rebase against main) to merge them all!
  > *"@SriRamkunamsetty for all the PRs can you please rebase once with the main branch so that all the workflows will be successful and we can merge them all?"* — Praveen Kumar Purushothaman

---

## 📅 Pull Requests Log & Submission Timestamps

| # | PR | Contributed Item | Pillar | Difficulty / Points | Branch | Submitted Date & Time (IST) | Submitted Date & Time (UTC) | Review Status |
|:---:|:---:|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **1** | [**#844**](https://github.com/praveenscience/One-File-Tools/pull/844) | **CORS Header Debugger & Tester** | Tools | Easy (20 pts) | `add/cors-debugger` | 15 Nov 2026, 09:08:22 AM IST | 2026-11-15 03:38:22 UTC | 🟡 Changes Requested (FOUC + XSS) |
| **2** | [**#845**](https://github.com/praveenscience/One-File-Tools/pull/845) | **JSON-LD Schema Generator** | Tools | Medium (30 pts) | `add/json-ld-generator` | 15 Nov 2026, 10:50:48 AM IST | 2026-11-15 05:20:48 UTC | 🟡 Changes Requested (FOUC + XSS) |
| **3** | [**#846**](https://github.com/praveenscience/One-File-Tools/pull/846) | **Tailwind CSS to Vanilla CSS Converter** | Tools | Medium (30 pts) | `add/tailwind-to-css` | 15 Nov 2026, 10:54:20 AM IST | 2026-11-15 05:24:20 UTC | 🟡 Duplicate flag (Swap with Crontab Explainer) |
| **4** | [**#847**](https://github.com/praveenscience/One-File-Tools/pull/847) | **JavaScript Event Loop Output Predictor** | Quests | Medium (30 pts) | `add/quest-event-loop` | 15 Nov 2026, 11:01:43 AM IST | 2026-11-15 05:31:43 UTC | 🟡 Changes Requested (FOUC IIFE) |
| **5** | [**#848**](https://github.com/praveenscience/One-File-Tools/pull/848) | **JavaScript Type Coercion Gauntlet** | Quests | Easy (20 pts) | `add/quest-type-coercion` | 15 Nov 2026, 11:09:55 AM IST | 2026-11-15 05:39:55 UTC | 🟡 Changes Requested (FOUC IIFE) |
| **6** | [**#849**](https://github.com/praveenscience/One-File-Tools/pull/849) | **Binary & Hex Bitwise Speed Trainer** | Quests | Easy (20 pts) | `add/quest-binary-hex` | 15 Nov 2026, 11:15:19 AM IST | 2026-11-15 05:45:19 UTC | 🟡 Changes Requested (FOUC IIFE) |
| **7** | [**#850**](https://github.com/praveenscience/One-File-Tools/pull/850) | **Destructuring Mastery Puzzle Quest** | Quests | Easy (20 pts) | `add/quest-destructuring` | 15 Nov 2026, 11:17:32 AM IST | 2026-11-15 05:47:32 UTC | 🟡 Changes Requested (FOUC IIFE) |
| **8** | [**#851**](https://github.com/praveenscience/One-File-Tools/pull/851) | **SaaS Modern Pricing Matrix & Calculator** | Design System | Easy (20 pts) | `add/ds-saas-pricing` | 15 Nov 2026, 11:35:40 AM IST | 2026-11-15 06:05:40 UTC | 🟡 Changes Requested (FOUC IIFE) |
| **9** | [**#852**](https://github.com/praveenscience/One-File-Tools/pull/852) | **Interactive Toast & Notification System** | Design System | Easy (20 pts) | `add/ds-notifications` | 15 Nov 2026, 11:43:06 AM IST | 2026-11-15 06:13:06 UTC | 🟡 Changes Requested (FOUC + XSS) |
| **10** | [**#853**](https://github.com/praveenscience/One-File-Tools/pull/853) | **Project Management Kanban Board** | Design System | Medium (30 pts) | `add/ds-kanban-board` | 15 Nov 2026, 11:51:34 AM IST | 2026-11-15 06:21:34 UTC | 🟡 Changes Requested (FOUC + XSS + JSON schema) |
| **11** | [**#854**](https://github.com/praveenscience/One-File-Tools/pull/854) | **Fix password-analyzer-uncodebar category** | Bug Fix | 10 pts | `fix/password-analyzer-category` | 15 Nov 2026, 02:14:47 PM IST | 2026-11-15 08:44:47 UTC | 🟢 **MERGED** by @praveenscience |

---

## 🔍 Detailed Maintainer Review Feedback & Resolution Plan

### 1. PR #844: CORS Header Debugger & Tester
- **Mentor Review:**
  - **Issue 1:** XSS in flow visualization (`clientOrigin`, `method`, `contentType`, `requestHeaders` interpolated directly into `innerHTML`).
  - **Issue 2:** Dark mode FOUC (Flash of Unstyled Content) — needs an IIFE in `<head>` to read `cors_tool_theme` from `localStorage` before render.
- **Resolution Plan:**
  - Add `escapeHtml()` function and wrap all user inputs.
  - Insert `<script>(function(){var t=localStorage.getItem('cors_tool_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 2. PR #845: JSON-LD Schema Generator
- **Mentor Review:**
  - **Issue 1:** XSS in `renderForm()` — unescaped form attributes break out on quotes.
  - **Issue 2:** Dark mode FOUC — needs an IIFE in `<head>` for `jsonld_theme`.
- **Resolution Plan:**
  - Add `escapeHtml()` and sanitize all input values and map iterations.
  - Insert `<script>(function(){var t=localStorage.getItem('jsonld_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 3. PR #846: Tailwind CSS to Vanilla CSS Converter
- **Mentor Review:**
  - **Issue 1:** Duplicate tool — repository already contains `tailwind-vanilla-css-converter.html`.
  - **Issue 2:** Dark mode FOUC.
- **Resolution Plan:**
  - Convert/replace this branch with **Crontab Explainer** (`tools/crontab-explainer.html`), an official unbuilt tool idea from the Ideas Board that does not duplicate any existing tool.
  - Include dark mode FOUC prevention and sanitization.
  - Rebase onto updated `upstream/main`.

### 4. PR #847: JavaScript Event Loop Output Predictor
- **Mentor Review:**
  - *"Otherwise the code looks good — no XSS, no stuck-on-last-level, state resets correctly."*
  - **Issue:** Dark mode FOUC (`eventloop_theme`).
- **Resolution Plan:**
  - Add `<script>(function(){var t=localStorage.getItem('eventloop_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 5. PR #848: JavaScript Type Coercion Gauntlet
- **Mentor Review:**
  - *"Otherwise clean — no XSS, JSON entry is correct."*
  - **Issue:** Dark mode FOUC (`coercion_theme`).
- **Resolution Plan:**
  - Add `<script>(function(){var t=localStorage.getItem('coercion_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 6. PR #849: Binary & Hex Bitwise Speed Trainer
- **Mentor Review:**
  - *"Otherwise clean — no XSS, JSON entry is correct."*
  - **Issue:** Dark mode FOUC (`binhex_theme`).
- **Resolution Plan:**
  - Add `<script>(function(){var t=localStorage.getItem('binhex_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 7. PR #850: Destructuring Mastery Puzzle Quest
- **Mentor Review:**
  - *"Otherwise clean — no XSS, JSON entry is correct."*
  - **Issue:** Dark mode FOUC (`destruct_theme`).
- **Resolution Plan:**
  - Add `<script>(function(){var t=localStorage.getItem('destruct_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 8. PR #851: SaaS Modern Pricing Matrix & Calculator
- **Mentor Review:**
  - *"Otherwise clean — no XSS (no user input), JSON entry is correct."*
  - **Issue:** Dark mode FOUC (`pricing_theme`).
- **Resolution Plan:**
  - Add `<script>(function(){var t=localStorage.getItem('pricing_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 9. PR #852: Interactive Toast & Notification System
- **Mentor Review:**
  - **Issue 1:** XSS in `spawnToast()` when rendering user-entered title and description.
  - **Issue 2:** Dark mode FOUC (`notif_theme`).
- **Resolution Plan:**
  - Add `escapeHtml()` to sanitize title and description.
  - Add `<script>(function(){var t=localStorage.getItem('notif_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Rebase onto updated `upstream/main`.

### 10. PR #853: Project Management Kanban Board
- **Mentor Review:**
  - **Issue 1:** XSS in `renderBoard()` for `task.title`, `task.desc`, `task.assignee`.
  - **Issue 2:** Dark mode FOUC (`kanban_theme`).
  - **Issue 3:** JSON metadata: change `"JavaScript"` to `"Vanilla JS"`, remove `"Tailwind CSS"` from `techStack` (keep in `frameworks`).
- **Resolution Plan:**
  - Add `escapeHtml()` and sanitize task properties.
  - Add `<script>(function(){var t=localStorage.getItem('kanban_theme');if(t)document.documentElement.setAttribute('data-theme',t);})();</script>` in `<head>`.
  - Correct `data/design-system.json` metadata.
  - Rebase onto updated `upstream/main`.

### 11. PR #854: Correct password-analyzer-uncodebar Category
- **Status:** **MERGED** 🎉
- **Maintainer Review:** *"Correct fix — changes invalid category 'Security' to valid 'utilities' for password-analyzer-uncodebar. LGTM."*
- **Outcome:** The upstream `main` branch now passes `node scripts/validate.js` with `All clean. No issues found.`!
