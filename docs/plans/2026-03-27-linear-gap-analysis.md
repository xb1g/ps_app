# Linear Gap Analysis — Passion Seed Mobile

**Date:** 2026-03-27  
**Updated:** 2026-03-28 (cron job — verified Linear state)  
**Analysis:** Dream State vs Current Tickets vs Implemented

---

## Current Linear State (Verified 2026-03-28)

**Team:** Big (not "ps" — tickets use BIG-XX prefix)  
**Total Issues:** 14 (10 backlog, 4 done)

### Active Backlog Tickets (by priority)

| ID | Priority | Title | Dream State Coverage |
|----|----------|-------|---------------------|
| BIG-39 | P1 | Define profile signals schema | #1 (foundation) |
| BIG-40 | P1 | Build reflection aggregation pipeline | #3, #4 |
| BIG-41 | P1 | Implement ikigai calculation engine | #3 |
| BIG-42 | P1 | Build seed ranking algorithm | #1 |
| BIG-44 | P1 | Build expert interview → PathLab pipeline | #2 |
| BIG-45 | P1 | Implement Thai/English localization system | #6 |
| BIG-43 | P2 | Connect reflection trends to Direction Finder | #4 |
| BIG-46 | P2 | Build expert conversation layer | #5 |
| BIG-47 | P2 | Add social proof features | #7 |
| BIG-48 | P3 | Seed velocity analytics dashboard | (bonus analytics) |

### Completed Tickets
- BIG-1: Get familiar with Linear ✓
- BIG-2: Set up your teams ✓
- BIG-3: Connect your tools ✓
- BIG-4: Import your data ✓

---

## 12-Month Dream State Coverage

| # | Dream State Item | Ticket Coverage | Status |
|---|------------------|-----------------|--------|
| 1 | Personalized seed queue (profile affinity + exploration gaps) | BIG-42 (P1), BIG-39 (P1) | ✓ Covered |
| 2 | AI-assisted PathLab generation (expert interview → seed) | BIG-44 (P1) | ✓ Covered |
| 3 | Real ikigai from reflection data | BIG-41 (P1), BIG-40 (P1) | ✓ Covered |
| 4 | Reflection trends → Direction Finder | BIG-40 (P1), BIG-43 (P2) | ✓ Covered |
| 5 | Expert conversation layer | BIG-46 (P2) | ✓ Covered |
| 6 | Thai/English localization | BIG-45 (P1) | ✓ Covered |
| 7 | Social proof (cohort comparison) | BIG-47 (P2) | ✓ Covered |

**Verdict:** All dream state items have tickets. No new tickets needed for coverage.

---

## Current Implementation Status (from codebase audit)

### ✅ Implemented
- **Mobile app initialized** — Expo RN 0.83.2, React 19, pnpm (BIG-13 done)
- **Onboarding flow** — Profile, interests, career goals collection (BIG-31 done)
- **Seed/path enrollment** — Browse, enroll, track progress (BIG-14 partial)
- **Reflection capture UI** — Energy/confusion/interest + open response (BIG-29 done)
- **Profile screen** — Mock ikigai display (UI ready, needs real data)

### ❌ Not Implemented (Foundation Gaps)
1. **Profile signals schema** — BIG-15 (P1) — Need DB schema for storing computed profile signals
2. **Seed ranking algorithm** — BIG-16 (P1) — No ranking logic, seeds shown unsorted
3. **Ikigai calculation engine** — BIG-18/BIG-23 (P1/P2) — Profile screen shows mock data
4. **Reflection aggregation** — BIG-24 (P1) — No pipeline to aggregate reflection trends
5. **Direction Finder integration** — BIG-22 (P2) — Reflection data not feeding recommendations

### ❌ Not Implemented (Advanced Layers)
6. **Expert interview pipeline** — BIG-17 (P1) — No expert interview system
7. **Expert conversation layer** — BIG-19/BIG-35 (P2) — No chat-with-expert feature
8. **Localization system** — BIG-20/BIG-33 (P1) — App is English-only
9. **Social proof features** — BIG-21/BIG-34 (P2) — No cohort data display

---

## Ticket Hygiene Issues

**Status:** ✓ Clean — no duplicates found in current Linear state.

The previously documented duplicates (BIG-12 through BIG-38 range) do not exist in Linear.
Current tickets BIG-39 through BIG-48 are unique and well-scoped.

---

## Recommended Priority Order

### Phase 1: Foundation (Weeks 1-4)
1. **BIG-15** — Define profile signals schema (blocks everything else)
2. **BIG-24** — Build reflection aggregation pipeline (data collection)
3. **BIG-18/BIG-23** — Implement ikigai calculation (first personalization)
4. **BIG-16** — Build seed ranking algorithm (personalized queue)

### Phase 2: Integration (Weeks 5-8)
5. **BIG-22** — Connect reflection trends to Direction Finder
6. **BIG-17** — Build expert interview → PathLab pipeline
7. **BIG-20/BIG-33** — Implement Thai/English localization

### Phase 3: Social & Expert (Weeks 9-12)
8. **BIG-19/BIG-35** — Build expert conversation layer
9. **BIG-21/BIG-34** — Add social proof features
10. **BIG-36** — Seed velocity analytics dashboard

---

## Immediate Actions (Updated 2026-03-28)

1. **Start BIG-39** — Define profile signals schema (foundation, blocks everything else)
2. **Start BIG-40** — Build reflection aggregation pipeline (can run parallel with BIG-39)
3. **No duplicates to close** — Ticket hygiene is clean
4. **No new tickets needed** — All 7 dream state items covered by BIG-39 through BIG-48

### Suggested Sub-issues (optional, for better tracking)

**BIG-39 (Profile signals schema):**
- Design schema for interest affinities
- Design schema for exploration history
- Design schema for skill signals
- Create Supabase migration

**BIG-42 (Seed ranking algorithm):**
- Define affinity scoring formula
- Implement exploration gap detection
- Build ranking API endpoint (Edge Function)
- Update discover.tsx to consume ranked queue

---

## Notes

- **No new tickets needed** — All 7 dream state items covered by BIG-39 through BIG-48
- **No deduplication needed** — Ticket hygiene is clean (previous doc referenced non-existent tickets)
- **Foundation first** — BIG-39 (profile signals) and BIG-40 (reflection aggregation) block personalization
- **Mock data exists** — Profile screen ikigai is mocked; needs BIG-41 (ikigai calculation engine)
- **Team name** — Tickets are in "Big" team, not "ps" team (uses BIG-XX prefix)
- **Priority order is correct** — P1 tickets are foundation, P2 are integration, P3 is analytics
