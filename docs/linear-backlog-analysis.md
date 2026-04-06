# Linear Backlog Analysis

**Generated:** 2026-04-05  
**Open Issues:** 96  
**Team:** Passion Seed (PS)

---

## Project Distribution

| Project | Issues | % |
|---------|--------|---|
| AI & ML | 33 | 34% |
| Growth | 17 | 18% |
| Backend | 13 | 14% |
| Infrastructure | 13 | 14% |
| Content | 10 | 10% |
| Mobile App | 10 | 10% |

**All issues are properly tagged with projects.** ✓

---

## Dream State Coverage

All 12-month dream state features have coverage:

| Dream State Feature | Coverage | Key Issues |
|---------------------|----------|------------|
| Personalized seed queue (affinity + exploration gaps) | 15 issues | PS-72, PS-24, PS-15 |
| AI-assisted PathLab generation | 3 issues | PS-26, PS-9 |
| Real ikigai from reflection data | 16 issues | PS-43, PS-49, PS-63 |
| Direction Finder + university roadmap | 8 issues | PS-76, PS-52 |
| Expert conversation layer (RAG chatbot) | 4 issues | PS-81, PS-27, PS-10 |
| Thai/English localization | 7 issues | PS-78, PS-54, PS-31 |
| Social proof + cohort comparison | 6 issues | PS-82, PS-7, PS-30 |

---

## ⚠️ Critical Issue: Duplication

The backlog contains **significant duplication** — approximately 30-40% of issues are duplicates or near-duplicates of the same feature tracked across different phases, sprints, or team perspectives.

### Exact Duplicates (1)

| Issue | Duplicate | Title |
|-------|-----------|-------|
| PS-71 (AI & ML) | PS-14 (Backend) | Connect profile.tsx to real ikigai edge function |

### Near Duplicates (15+ pairs)

These represent the same feature tracked from different angles:

| Primary | Duplicate | Feature |
|---------|-----------|---------|
| PS-89 | PS-68, PS-37 | User onboarding flow |
| PS-82 | PS-22 | Cohort comparison analytics |
| PS-81 | PS-27, PS-10 | Expert conversation layer |
| PS-79 | PS-60 | E2E testing with Detox |
| PS-78 | PS-54 | Thai/English localization |
| PS-77 | PS-51 | Expert interview → seed pipeline |
| PS-76 | PS-52 | Direction Finder screen |
| PS-75 | PS-29 | Reflection trends aggregation |
| PS-74 | PS-47 | Portfolio-fit edge function |
| PS-73 | PS-45 | Seed ranking display |
| PS-72 | PS-15 | Seed ranking algorithm |
| PS-70 | PS-44 | Ikigai visualization |
| PS-69 | PS-48 | Seed completion tracking UI |
| PS-68 | PS-37 | User onboarding flow |

### Root Cause

Many tickets were created during different planning sessions:
- Phase 1/Phase 2 planning created parallel tracks
- [Mobile], [Backend], [Content], [Infra] prefixes split single features
- Sprint planning created new tickets instead of updating existing

---

## Recommendations

### Immediate Actions

1. **Close exact duplicate PS-14** — PS-71 is the canonical ticket (AI & ML project, more recent)

2. **Consolidate near-duplicates** — For each pair above:
   - Keep the more recent/higher-numbered ticket as primary
   - Link the older ticket as related
   - Close the older ticket with comment pointing to primary

3. **Adopt single-ticket-per-feature policy** — New features get one ticket with subtasks for team-specific work

### Suggested Consolidations

| Keep (Primary) | Close (Duplicate) | Action |
|----------------|-------------------|--------|
| PS-89 (Onboarding) | PS-68, PS-37 | Close backend/mobile duplicates, add as subtasks |
| PS-82 (Cohort analytics) | PS-22 | Close PS-22, link to PS-82 |
| PS-81 (Expert chat) | PS-27, PS-10 | Close phase 2 and original, consolidate into PS-81 |
| PS-79 (E2E testing) | PS-60 | Close PS-60 |
| PS-78 (Localization) | PS-54 | Close PS-54 |
| PS-77 (Expert pipeline) | PS-51 | Close PS-51, coordinate Content team via subtask |
| PS-76 (Direction Finder) | PS-52 | Close PS-52, add mobile subtask |
| PS-75 (Reflection trends) | PS-29 | Close PS-29 |
| PS-74 (Portfolio-fit) | PS-47 | Close PS-47 |
| PS-73 (Ranking display) | PS-45 | Close PS-45, add mobile subtask |
| PS-72 (Ranking algo) | PS-15 | Close PS-15 |
| PS-70 (Ikigai viz) | PS-44 | Close PS-44 |
| PS-69 (Completion UI) | PS-48 | Close PS-48 |

**Estimated reduction:** ~20-25 tickets (25% backlog reduction)

---

## Next Steps

1. [ ] Review this analysis with team
2. [ ] Close PS-14 (exact duplicate)
3. [ ] Batch close near-duplicates with proper linking
4. [ ] Update team workflow to prevent future duplication
5. [ ] Schedule backlog grooming session

---

## Methodology

- Queried Linear API for all open issues in PS team
- Analyzed title/description keyword matching against dream state features
- Detected duplicates via exact title match and title containment
- Manual review of near-duplicate pairs for confirmation
