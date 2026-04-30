# Dream State Coverage — 12-Month Roadmap

**Last Updated:** 2026-04-29
**Status:** PS-39 moved to Growth. PS-68 (push notification triggers) and PS-69 (Sentry acceptance criteria) created.

---

## Dream State Items vs Ticket Coverage

| # | Dream State | Tickets | Coverage |
|---|-------------|---------|----------|
| 1 | Personalized seed queue (affinity + gaps) | PS-55, PS-49, PS-30 | ✅ Covered |
| 2 | AI-assisted PathLab generation (expert → seed in 1hr) | PS-56, PS-44, PS-29 | ✅ Covered |
| 3 | Real ikigai from reflection data | PS-46, PS-54, PS-28, PS-65 | ✅ Covered |
| 4 | Reflection trends → Direction Finder + university roadmap | PS-54, PS-50, PS-45 | ✅ Covered |
| 5 | Expert conversation layer | PS-38, PS-59, PS-42 | ✅ Covered |
| 6 | Thai/English seed content localization | PS-60, PS-27, PS-15 | ✅ Covered |
| 7 | Social proof: "N students tried this" + cohort comparison | PS-67, PS-58, PS-14, PS-41, PS-26 | ✅ Covered |

---

## Current State (2026-04-29)

| Metric | Count |
|--------|-------|
| Total issues | 50 |
| Done | 4 |
| Open | 46 |
| Open issues missing project tag | **0** |

### Done Tickets (4)
- PS-57: Seed queue UI with ranking display → Mobile App
- PS-51: Deduplicate and prioritize backlog tickets → Content
- PS-33: Initialize Expo React Native mobile app → Mobile App
- PS-18: Build mobile reflection capture UI → Mobile App

### Open Issues by Project (non-Duplicate only)
| Project | Count |
|---------|-------|
| AI & ML | 12 |
| Growth | 7 |
| Mobile App | 3 |
| Backend | 4 |
| Content | 1 |
| Infrastructure | 3 |

### Projects in PS Team
| Project ID | Name |
|------------|------|
| 9967dd59-657b-496a-b995-37efd03cc436 | Growth |
| ca0b0197-f32b-4e53-aec7-2f83f84b218a | Content |
| 163baf10-fed5-4dc9-ab30-c0029dea9dc5 | AI & ML |
| 1358137d-f9ef-4486-bada-c44c22c1fa87 | Infrastructure |
| a22f2444-7a05-45a3-a7dd-4503937304b6 | Backend |
| 1ea9aa51-e3ec-4d34-bd98-50b18c859213 | Mobile App |

---

## Actions Taken This Run

1. ✅ **PS-39 project corrected**: Moved from AI & ML → Growth (business validation research, not AI)
2. ✅ **PS-68 created**: Push notification trigger edge function (Growth) — PS-20 covers mobile UI, this covers backend triggers
3. ✅ **PS-69 created**: Sentry monitoring acceptance criteria (Infrastructure) — detailed acceptance criteria for PS-62
4. ✅ All open tickets verified with project assignments — no missing tags
5. ✅ Confirmed all 7 dream state items have backlog coverage
6. ⚠️ 22 duplicate tickets remain marked as Duplicate state (PS-37, PS-36, PS-44, PS-45, PS-47, PS-48, PS-49, PS-52, PS-59, PS-64, PS-12, PS-13, PS-15, PS-17, PS-23, PS-25, PS-26, PS-27, PS-28, PS-29, PS-30, PS-43)

---

## Key Gaps Identified

| Gap | Notes |
|-----|-------|
| Push notification backend (PS-68) | Created — PS-20 covers mobile UI, server-side triggers were missing |
| Sentry acceptance criteria (PS-69) | Created — PS-62 exists but lacked detailed acceptance criteria |
| PS-39 project reassignment | Fixed — "parent willingness to pay" is a Growth/business research task, not AI & ML |

---

## Duplicate Groups (Consolidation Candidate)

| Topic | Duplicates | Lead |
|-------|------------|------|
| Expert conversation | PS-59, PS-42, PS-38, PS-36 | PS-38 |
| Thai/English localization | PS-60, PS-43, PS-27, PS-15 | PS-60 |
| Social proof / cohort | PS-58, PS-41, PS-26, PS-14 | PS-58 |
| Direction Finder integration | PS-45, PS-25, PS-21, PS-13 | PS-45 |
| Expert → PathLab pipeline | PS-56, PS-44, PS-29 | PS-56 |
| Seed ranking algorithm | PS-55, PS-49, PS-30 | PS-55 |
| Ikigai calculation | PS-46, PS-28, PS-52 | PS-46 |
| Reflection pipeline | PS-54, PS-47, PS-23 | PS-54 |
| Profile signals | PS-53, PS-48, PS-31 | PS-31 |
| University roadmap matching | PS-50 | PS-50 |
| Parent willingness validation | PS-39, PS-37 | PS-39 |
| PathLab request | PS-34, PS-10, PS-8 | PS-34 |
| Profile reveal UI | PS-22, PS-17 | PS-22 |
| Offline caching | PS-19, PS-12 | PS-19 |
