# Passion Seed Mobile App - 12-Month Roadmap

**Last updated:** March 28, 2026 (auto-updated by cron)  
**GitHub:** https://github.com/Ongpaoaa/ps_app  
**Linear:** PS team (https://linear.app/bigf/PS)

---

## Current State Summary

**Total open tickets:** 33 (PS-1 through PS-33)  
**All tickets in:** Backlog  
**Phase 1 ready to start:** Yes (PS-11 → PS-12 → PS-23)

### What Exists Today
- ✅ Edge functions: career-insights, portfolio-fit, score-engine, push-notifications, university-insights
- ✅ Core screens: seed, path, reflection, portfolio, university, career, fit
- ✅ Database schema: seeds, paths, path_days, path_enrollments, path_reflections, learning_maps, map_nodes, jobs, tcas_programs

### What's Missing (Dream State Gaps)
- ❌ user_profile_signals table for affinity tracking
- ❌ Seed ranking algorithm (affinity + exploration gaps)
- ❌ Ikigai calculation from reflection data
- ❌ Reflection trends aggregation
- ❌ Content localization system (TH/EN)
- ❌ Social proof counters and cohort comparisons
- ❌ AI PathLab seed generator
- ❌ Expert conversation layer (RAG chatbot)

---

## 12-Month Dream State

1. **Personalized seed queue** ranked by profile affinity + exploration gaps
2. **AI-assisted PathLab generation** (expert interview → seed in 1 hour)
3. **Real ikigai** derived from reflection data across all completed seeds
4. **Reflection trends** feed Direction Finder and university roadmap match
5. **Expert conversation layer** (student can "talk" to the expert via RAG chatbot)
6. **Fully localized seed content** (Thai/English)
7. **Social proof**: "N students tried this path" + cohort comparison analytics

---

## Phase 1: Foundation (Q2 2026)

**Goal:** Enable personalization by collecting profile signals and building core ranking

### Priority Tickets

| Ticket | Title | Priority | Status |
|--------|-------|----------|--------|
| PS-23 | Phase 1 Foundation: Profile signals data collection layer | High | Backlog |
| PS-24 | Phase 1: Seed ranking edge function (affinity + exploration gaps) | High | Backlog |
| PS-25 | Phase 1: Ikigai edge function MVP | High | Backlog |
| PS-28 | Phase 1: Reflection trends → Direction Finder integration | Medium | Backlog |

### Supporting Tickets

| Ticket | Title | Priority |
|--------|-------|----------|
| PS-11 | Database migrations for Phase 1 (ikigai, localization, social proof) | High |
| PS-12 | Create user_profile_signals table for tracking affinity data | High |
| PS-13 | Build career-insights edge function for ikigai calculation | High |
| PS-1 | Implement real Ikigai calculation from reflection data | High |
| PS-2 | Add profile affinity scoring to seed ranking | High |
| PS-3 | Create seed content localization system (TH/EN) | High |
| PS-5 | Build exploration gap detection system | Medium |
| PS-15 | Implement seed ranking algorithm (affinity + exploration gaps) | High |
| PS-17 | Add exploration gap tracking to profile signals | Medium |
| PS-32 | Add ikigai visualization to Profile screen | Medium |

### Dependencies

```
PS-11 (migrations) → PS-12 (profile_signals table) → PS-23 (data collection)
                                                  → PS-24 (ranking function)
PS-11 → PS-13 (ikigai function) → PS-25 (ikigai MVP) → PS-14 (profile.tsx)
PS-25 → PS-21 (Direction Finder) → PS-28 (integration)
PS-24 → PS-16 (discover.tsx update)
```

---

## Phase 2: AI & Expert Layer (Q3 2026)

**Goal:** Automate content creation and enable expert conversations

### Priority Tickets

| Ticket | Title | Priority | Status |
|--------|-------|----------|--------|
| PS-26 | Phase 2: AI PathLab seed generator pipeline | Medium | Backlog |
| PS-27 | Phase 2: Expert conversation layer (RAG chatbot) | Low | Backlog |

### Supporting Tickets

| Ticket | Title | Priority |
|--------|-------|----------|
| PS-9 | AI-assisted PathLab seed generator | Low |
| PS-10 | Expert conversation layer (chat with expert avatar) | Low |
| PS-3 | Create seed content localization system (TH/EN) | High |
| PS-31 | Build content localization workflow for expert contributors | High |

### Dependencies

```
PS-3 (localization) → PS-26 (PathLab pipeline)
PS-26 → PS-27 (expert chatbot RAG)
```

---

## Phase 3: Social & Analytics (Q4 2026)

**Goal:** Add social proof and cohort insights

### Supporting Tickets

| Ticket | Title | Priority |
|--------|-------|----------|
| PS-6 | Build reflection trends dashboard | Medium |
| PS-7 | Add social proof counters to seed cards | Medium |
| PS-8 | Build university roadmap matching engine | Medium |
| PS-21 | Build Direction Finder recommendation algorithm | Medium |
| PS-22 | Build cohort comparison analytics for social proof | Low |
| PS-29 | Build reflection trends aggregation pipeline (daily/weekly/monthly) | Medium |
| PS-30 | Define cohort segmentation logic for social proof | Medium |

---

## Infrastructure (Ongoing)

| Ticket | Title | Priority |
|--------|-------|----------|
| PS-18 | Build A/B testing infrastructure for feature experiments | Medium |
| PS-19 | Implement analytics event tracking system | Medium |
| PS-20 | Build push notification scheduler for daily seed queue refresh | Low |
| PS-33 | Seed queue A/B test framework integration | Low |

---

## Ticket Summary

**Total open tickets:** 33 (PS-1 through PS-33)

**By Priority:**
- High (P1): 11 tickets (PS-1, PS-2, PS-3, PS-11, PS-12, PS-13, PS-14, PS-15, PS-23, PS-24, PS-25, PS-31)
- Medium (P2): 13 tickets (PS-4, PS-5, PS-6, PS-7, PS-8, PS-16, PS-17, PS-18, PS-19, PS-21, PS-26, PS-28, PS-29, PS-30, PS-32)
- Low (P3): 9 tickets (PS-9, PS-10, PS-20, PS-22, PS-27, PS-33)

**By Phase:**
- Phase 1 Foundation: 16 tickets (PS-1 through PS-5, PS-11 through PS-17, PS-23 through PS-25, PS-28, PS-29, PS-31, PS-32)
- Phase 2 AI/Expert: 4 tickets (PS-9, PS-10, PS-26, PS-27)
- Phase 3 Social: 6 tickets (PS-6, PS-7, PS-8, PS-21, PS-22, PS-30)
- Infrastructure: 7 tickets (PS-18, PS-19, PS-20, PS-33 + edge functions)

---

## Next Actions

### Sprint 1 (Week 1-2): Database Foundation
1. **PS-11** - Database migrations for Phase 1 (unblocks everything)
2. **PS-12** - Create user_profile_signals table
3. **PS-31** - Build content localization workflow (parallel, unblocks PathLab)

### Sprint 2 (Week 3-4): Data Collection
4. **PS-23** - Profile signals data collection layer
5. **PS-13** - Career-insights edge function for ikigai
6. **PS-3** - Seed content localization system (TH/EN)

### Sprint 3 (Week 5-6): Core Algorithms
7. **PS-24** - Seed ranking edge function
8. **PS-25** - Ikigai edge function MVP
9. **PS-15** - Seed ranking algorithm implementation

### Parallel Tracks
- **PS-29** - Reflection trends aggregation (can start after PS-23)
- **PS-30** - Cohort segmentation spec (can start anytime)
- **PS-32** - Ikigai visualization (depends on PS-25)

---

## Notes

- All tickets currently in Backlog state
- Priority should be re-evaluated before starting each phase
- Consider batching Phase 1 tickets into sprints of 3-4 tickets each
