# Passion Seed Mobile App - 12-Month Roadmap

**Last updated:** March 28, 2026  
**GitHub:** https://github.com/Ongpaoaa/ps_app  
**Linear:** PS team (https://linear.app/passionseed)

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

---

## Infrastructure (Ongoing)

| Ticket | Title | Priority |
|--------|-------|----------|
| PS-18 | Build A/B testing infrastructure for feature experiments | Medium |
| PS-19 | Implement analytics event tracking system | Medium |
| PS-20 | Build push notification scheduler for daily seed queue refresh | Low |

---

## Ticket Summary

**Total open tickets:** 28 (PS-1 through PS-28)

**By Priority:**
- High (P1): 10 tickets
- Medium (P2): 9 tickets
- Low (P3): 9 tickets

**By Phase:**
- Phase 1 Foundation: 13 tickets
- Phase 2 AI/Expert: 4 tickets
- Phase 3 Social: 5 tickets
- Infrastructure: 6 tickets

---

## Next Actions

1. **Start with PS-11** (database migrations) - unblocks everything
2. **Then PS-12** (profile_signals table) - foundation for personalization
3. **Then PS-23** (data collection) - start gathering signals
4. **Parallel:** PS-13 (ikigai function) and PS-3 (localization)

---

## Notes

- All tickets currently in Backlog state
- Priority should be re-evaluated before starting each phase
- Consider batching Phase 1 tickets into sprints of 3-4 tickets each
