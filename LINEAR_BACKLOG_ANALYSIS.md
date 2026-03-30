# Linear Backlog Analysis

**Date:** 2026-03-29  
**Analysis Type:** Project tagging + duplicate cleanup + dream state gap analysis

---

## Summary

| Metric | Count |
|--------|-------|
| Total issues | 55 |
| Issues tagged with projects | 50 |
| Duplicates identified | 15 topic groups |
| Dream state coverage | 5/7 (71%) |

---

## Project Distribution

| Project | Issues | % |
|---------|--------|---|
| AI & ML | 23 | 42% |
| Growth | 11 | 20% |
| Mobile App | 10 | 18% |
| Content | 6 | 11% |
| Backend | 0 | 0% |
| Infrastructure | 0 | 0% |

**Note:** Backend and Infrastructure projects created but no tickets assigned yet.

---

## Duplicate Topics (Consolidation Needed)

| Topic | Duplicates | Recommended Lead |
|-------|------------|------------------|
| Expert conversation layer | PS-59, PS-42, PS-38, PS-36 | PS-59 |
| Thai/English localization | PS-60, PS-43, PS-27, PS-15 | PS-60 |
| Social proof / cohort | PS-58, PS-41, PS-26, PS-14 | PS-58 |
| Direction Finder integration | PS-45, PS-25, PS-21, PS-13 | PS-45 |
| Expert → PathLab pipeline | PS-56, PS-44, PS-29 | PS-56 |
| Parent willingness validation | PS-39, PS-37, PS-7 | PS-39 |
| PathLab request | PS-34, PS-10, PS-8 | PS-34 |
| Profile reveal UI | PS-22, PS-17, PS-11 | PS-22 |
| Profile signals | PS-53, PS-48, PS-31 | PS-53 |
| Reflection pipeline | PS-54, PS-47, PS-23 | PS-54 |
| Seed ranking algorithm | PS-55, PS-49, PS-30 | PS-55 |
| Ikigai calculation | PS-46, PS-28 | PS-46 |
| Offline caching | PS-19, PS-12 | PS-19 |
| Seed queue UI | PS-57, PS-32 | PS-57 |

---

## Dream State Coverage Analysis

### ✅ Covered (5/7)

| Dream State Item | Covering Tickets | Status |
|-----------------|------------------|--------|
| 1. Personalized seed queue (ranking) | PS-55, PS-49, PS-30, PS-57, PS-32 | Backlog (duplicates) |
| 2. AI-assisted PathLab generation | PS-56, PS-44, PS-29, PS-34, PS-10, PS-8 | Backlog (duplicates) |
| 3. Ikigai from reflection data | PS-46, PS-28, PS-52, PS-54, PS-47, PS-23 | Backlog (duplicates) |
| 5. Expert conversation layer | PS-59, PS-42, PS-38, PS-36 | Backlog (duplicates) |
| 6. Thai/English localization | PS-60, PS-43, PS-27, PS-15 | Backlog (duplicates) |

### ⚠️ Partially Covered (1/7)

| Dream State Item | Covering Tickets | Gap |
|-----------------|------------------|-----|
| 4. Reflection trends → Direction Finder + university roadmap | PS-45, PS-25, PS-21, PS-13 (Direction Finder)<br>PS-50 (university roadmap) | Need to connect: reflection pipeline → Direction Finder → roadmap matching as single flow |

### ❌ Missing (1/7)

| Dream State Item | Gap |
|-----------------|-----|
| 7. Social proof ("N students tried this path" + cohort comparison) | PS-58, PS-41, PS-26, PS-14 exist but focus on cohort comparison only. Missing: **"N students tried this path"** counter on seed/path cards |

---

## Missing Infrastructure

The following infrastructure items mentioned in the project context are **not represented** in the backlog:

| Category | Missing Items |
|----------|---------------|
| Testing | E2E testing setup, Detox configuration, test coverage goals |
| Monitoring | Sentry integration, error tracking, performance monitoring |
| CI/CD | Automated testing pipeline, EAS Build configuration, app store deployment |
| Backend | Database migrations, RLS policies, edge function deployment |

---

## Recommended Actions

### Immediate (This Week)
1. **Consolidate duplicates** — Close duplicate tickets, keep one canonical ticket per topic
2. **Create Infrastructure tickets** — Add testing, monitoring, CI/CD tickets
3. **Create Backend tickets** — Add database schema, RLS, edge function tickets
4. **Add social proof counter** — Create ticket for "N students tried this" feature

### Short-term (This Month)
1. **Prioritize dream state items** — Focus on completing the 7 dream state features
2. **Assign owners** — Each dream state item should have a clear owner
3. **Set milestones** — Group tickets into sprints targeting dream state completion

### Medium-term (This Quarter)
1. **Backend foundation** — Complete profile signals, ikigai Snapshots, reflection aggregation
2. **Mobile core** — Complete seed queue, reflection capture, profile reveal
3. **AI/ML pipeline** — Complete ranking algorithm, expert interview → PathLab

---

## Ticket Status

| State | Count |
|-------|-------|
| Backlog | 49 |
| Started | 1 (PS-31: profile signals schema) |
| Completed | 5 |

---

## Files Generated

- `/tmp/linear_data.json` — Raw Linear API data
- `/tmp/issue_classifications_refined.json` — Project classifications
- `/tmp/duplicate_analysis.json` — Duplicate topic analysis
- `LINEAR_BACKLOG_ANALYSIS.md` — This document
