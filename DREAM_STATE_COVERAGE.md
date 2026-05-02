# Dream State Coverage — 12-Month Roadmap

**Last Updated:** 2026-05-01
**Status:** Project corrections for PS-20, PS-39, PS-40, PS-67. New ticket PS-70 for seed content translation.

---

## Dream State Items vs Ticket Coverage

| # | Dream State | Tickets | Coverage |
|---|-------------|---------|----------|
| 1 | Personalized seed queue (affinity + gaps) | PS-55, PS-24 | ✅ Covered |
| 2 | AI-assisted PathLab generation (expert → seed in 1hr) | PS-56, PS-9 | ✅ Covered |
| 3 | Real ikigai from reflection data | PS-46, PS-54, PS-65 | ✅ Covered |
| 4 | Reflection trends → Direction Finder + university roadmap | PS-54, PS-50 | ✅ Covered |
| 5 | Expert conversation layer | PS-38 | ✅ Covered |
| 6 | Thai/English seed content localization | PS-60, PS-70 (new) | ✅ Covered |
| 7 | Social proof: "N students tried this" + cohort comparison | PS-67, PS-58, PS-14 | ✅ Covered (⚠️ see duplicates) |

---

## Current State (2026-05-01)

| Metric | Count |
|--------|-------|
| Total issues | 64 |
| Done | 5 |
| In Progress | 1 |
| Backlog | 30 |
| Duplicate | 28 (⚠️ 44% duplication!) |

### Done Tickets (5)
- PS-57: Seed queue UI with ranking display → Mobile App
- PS-51: Deduplicate and prioritize backlog tickets → Content
- PS-33: Initialize Expo React Native mobile app → Mobile App
- PS-18: Build mobile reflection capture UI → Mobile App
- PS-16: Implement app onboarding flow → Mobile App

### In Progress (1)
- PS-31: Define and implement user profile signals schema → Backend

### Open Issues by Project (non-Duplicate, Backlog only)

| Project | Count | Tickets |
|---------|-------|---------|
| AI & ML | 8 | PS-24, PS-34, PS-38, PS-46, PS-50, PS-54, PS-55, PS-56 |
| Growth | 4 | PS-14, PS-21, PS-39 (→Content), PS-58, PS-6 |
| Mobile App | 6 | PS-19, PS-20 (←Growth), PS-22, PS-32, PS-67 (←Growth), PS-70 (new) |
| Backend | 3 | PS-53, PS-65, PS-66 |
| Infrastructure | 4 | PS-40 (←Growth), PS-61, PS-62, PS-63, PS-69 |
| Content | 3 | PS-39, PS-60, PS-70 |

*Note: Growth count excludes PS-39 (now Content) and PS-67 (now Mobile App).*

---

## Projects in PS Team

| Project ID | Name |
|------------|------|
| 1ea9aa51-e3ec-4d34-bd98-50b18c859213 | Mobile App |
| a22f2444-7a05-45a3-a7dd-4503937304b6 | Backend |
| 1358137d-f9ef-4486-bada-c44c22c1fa87 | Infrastructure |
| 163baf10-fed5-4dc9-ab30-c0029dea9dc5 | AI & ML |
| ca0b0197-f32b-4e53-aec7-2f83f84b218a | Content |
| 9967dd59-657b-496a-b995-37efd03cc436 | Growth |

---

## Actions Taken This Run (2026-05-01)

### Project Corrections
1. ✅ **PS-20** → Mobile App (was Growth): Push notification infrastructure is ps_app-specific mobile client work
2. ✅ **PS-40** → Infrastructure (was Growth): Seed velocity analytics dashboard → belongs in Infrastructure (analytics infra)
3. ✅ **PS-39** → Content (was Growth): Parent willingness to pay validation is content/research work
4. ✅ **PS-67** → Mobile App (was Growth): "N students tried this path" counter on seed cards is mobile UI

### New Tickets Created
- ✅ **PS-70** (Content): "Translate all seed content to Thai and English" — PS-60 built the i18n system; this ticket covers the actual content translation work (seed titles, descriptions, tasks, reflection prompts, expert insights)

---

## Duplicate Groups (⚠️ 28 duplicates = 44% of all tickets!)

| Topic | Duplicates | Lead |
|-------|------------|------|
| Thai/English localization | PS-60 (active), PS-43, PS-27, PS-15 | PS-60 |
| Social proof / cohort | PS-67, PS-58, PS-14 (active), PS-41, PS-26 | PS-67 |
| Expert conversation | PS-38 (active), PS-36, PS-42, PS-59 | PS-38 |
| PathLab pipeline | PS-56 (active), PS-44, PS-29, PS-34 | PS-56 |
| Seed ranking algorithm | PS-55 (active), PS-30, PS-49 | PS-55 |
| Ikigai calculation | PS-46 (active), PS-28, PS-52, PS-65 | PS-46 |
| Reflection pipeline | PS-54 (active), PS-23, PS-47, PS-25, PS-45 | PS-54 |
| Profile signals | PS-31 (in progress), PS-48, PS-64 | PS-31 |
| Parent willingness | PS-39 (active), PS-7, PS-37 | PS-39 |
| Profile scoring | PS-24 (active), PS-53 | PS-24 |
| University roadmap | PS-50 (active) | PS-50 |
| Direction Finder | PS-21 (active), PS-13, PS-45, PS-25 | PS-21 |
| Profile reveal UI | PS-22 (active), PS-17, PS-11 | PS-22 |
| Offline caching | PS-19 (active), PS-12 | PS-19 |
| PathLab request | PS-34 (active), PS-10, PS-8 | PS-34 |

**Action needed:** Manual review of each duplicate group to confirm which ticket is canonical and close the rest.

---

## Key Gaps Identified

| Gap | Notes |
|-----|-------|
| Seed content translation (PS-70) | Created — PS-60 built the system, translation work itself was untracked |
| Social proof consolidation | PS-14, PS-58, PS-67 all active — overlap, need to merge into one |
| Analytics data pipeline | PS-40 (dashboard) moved to Infrastructure; underlying event tracking pipeline needs scoping |
| PS-5 About page | Low priority — PS web non-core feature, consider closing |

---

## Dream State Coverage Assessment

| # | Dream State | Status |
|---|-------------|--------|
| 1 | Personalized seed queue (affinity + exploration gaps) | ✅ Covered: PS-24 (affinity scoring), PS-55 (ranking + gaps) |
| 2 | AI-assisted PathLab (expert interview → seed in 1hr) | ✅ Covered: PS-56 (pipeline), PS-9 (PathLab build) |
| 3 | Real ikigai from reflection data | ✅ Covered: PS-46 (calculation), PS-54 (reflection→ikigai flow), PS-65 (snapshots table) |
| 4 | Reflection trends → Direction Finder + roadmap | ✅ Covered: PS-54 (reflection pipeline), PS-50 (university matching) |
| 5 | Expert conversation layer | ✅ Covered: PS-38 (chat layer) |
| 6 | Fully localized seed content (Thai/English) | ✅ Covered: PS-60 (system), PS-70 (translation work) |
| 7 | Social proof + cohort comparison | ⚠️ Covered but fragmented: PS-67 (counter), PS-58/PS-14 (cohort) — consolidation needed |

**All 7 dream state pillars have backlog coverage.** Main risks: duplication overhead, social proof ticket fragmentation.

---

*Report auto-generated by ps_app cron job — Linear PS team sync*
