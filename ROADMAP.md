# Passion Seed Mobile App - Product Roadmap

**Last updated:** March 28, 2026  
**GitHub:** https://github.com/Ongpaoaa/ps_app  
**Linear:** PS team (tickets PS-XX)

---

## 12-Month Dream State

1. **Personalized seed queue** ranked by profile affinity + exploration gaps
2. **AI-assisted PathLab generation** (expert interview → seed in 1 hour)
3. **Real ikigai** derived from reflection data across all completed seeds
4. **Reflection trends** feed Direction Finder and university roadmap match
5. **Expert conversation layer** (student can "talk" to the expert)
6. **Fully localized seed content** (Thai/English)
7. **Social proof**: "N students tried this path" + cohort comparison

---

## Phase 1: MVP Foundation (Sprint 1-3)

**Goal:** Ship core loop with basic personalization

### Data Layer
- [x] PS-42: user_profile_signals table schema
- [x] PS-38: Reflection data model and aggregation schema
- [x] PS-83: Seed completion tracking and user progress aggregation
- [ ] PS-67: RLS policies for user data isolation *(new)*

### Core Features
- [ ] PS-68: User onboarding flow for profile signals collection *(new)*
- [ ] PS-69: Seed completion tracking UI and progress indicators *(new)*
- [ ] PS-70: Ikigai visualization component for Profile screen *(new)*
- [ ] PS-71: Connect profile.tsx to real ikigai edge function *(new)*

### Personalization
- [ ] PS-72: Seed ranking algorithm (affinity + exploration gaps) *(new)*
- [ ] PS-73: Seed ranking display in Discover screen *(new)*
- [ ] PS-74: portfolio-fit edge function for seed → user matching *(new)*

### Infrastructure
- [ ] PS-58: MVP Scope Definition and Prioritization
- [ ] PS-79: E2E testing infrastructure with Detox *(new)*
- [ ] PS-80: Sentry error monitoring integration *(new)*
- [ ] PS-78: Thai/English localization system *(new)*

---

## Phase 2: Intelligence & Insights (Sprint 4-6)

**Goal:** Add AI-powered features and analytics

### Analytics
- [ ] PS-55: Track seed velocity and Direction Finder readiness
- [ ] PS-61: Dashboard for seed velocity and completion funnel
- [ ] PS-75: Reflection trends aggregation pipeline *(new)*
- [ ] PS-76: Direction Finder screen with university roadmap integration *(new)*

### Advanced Features
- [ ] PS-52: Direction Finder screen with university roadmap integration
- [ ] PS-25: Ikigai edge function MVP
- [ ] PS-24: Seed ranking edge function (affinity + exploration gaps)

### Content Pipeline
- [ ] PS-77: Expert interview → seed content pipeline *(new)*
- [ ] PS-59: Seed creator CMS for expert contributors

---

## Phase 3: Social & Expert Layers (Sprint 7-12)

**Goal:** Build community and expert engagement

- [ ] PS-81: Expert conversation layer (RAG chatbot) *(new)*
- [ ] PS-10: Expert conversation layer (chat with expert avatar)
- [ ] PS-9: AI-assisted PathLab seed generator
- [ ] PS-26: AI PathLab seed generator pipeline
- [ ] PS-82: Cohort comparison analytics for social proof *(new)*
- [ ] PS-30: Cohort segmentation logic for social proof
- [ ] PS-40: Cohort segmentation logic and definitions

---

## Infrastructure & Quality

### Testing
- [ ] PS-60: E2E testing with Detox *(new)*
- [ ] PS-36: A/B testing framework for feature experiments
- [ ] PS-18: A/B testing infrastructure

### Monitoring
- [ ] PS-62: Sentry error monitoring *(new)*
- [ ] PS-35: Analytics event tracking schema
- [ ] PS-19: Analytics event tracking system

### DevOps
- [ ] PS-50: Feature flag system for gradual rollouts
- [ ] PS-34: Edge function deployment and testing pipeline
- [ ] PS-56: Offline-first seed content caching

---

## Current Sprint: Sprint 1 (Foundation Kickoff)

**Ticket:** PS-41

### Priority Focus
1. **Profile signals collection** - PS-68 (onboarding), PS-67 (RLS)
2. **Ikigai calculation** - PS-70 (visualization), PS-71 (integration), PS-74 (edge fn)
3. **Seed ranking** - PS-72 (algorithm), PS-73 (UI), PS-74 (portfolio-fit)
4. **Localization** - PS-78 (i18n system)

### Blockers
- Need MVP scope definition (PS-58) before sprint planning
- Need testing infrastructure (PS-79) for confident shipping
- Need error monitoring (PS-80) for production readiness

---

## Metrics to Track

| Metric | Target | Current |
|--------|--------|---------|
| Daily Active Users | 100+ | - |
| Seed Completion Rate | 60%+ | - |
| Reflection Completion | 80%+ | - |
| Time to First Seed | < 5 min | - |
| Week 1 Retention | 40%+ | - |

---

## Notes

- All tickets tracked in Linear (PS team)
- Documentation lives in this repo
- Shared Supabase with web project (~/dev/pseed)
- Key edge functions: career-insights, portfolio-fit, score-engine, push-notifications

---

## Changelog

### March 28, 2026 - PM (Cron Job)

**Duplicate Cleanup Complete:** Marked 14 duplicate tickets and moved to "Duplicate" state:

| Duplicate | Canonical | Topic |
|-----------|-----------|-------|
| PS-67 | PS-53 | RLS policies |
| PS-68 | PS-37 | Profile onboarding |
| PS-69 | PS-48 | Seed completion UI |
| PS-70 | PS-44 | Ikigai visualization |
| PS-73 | PS-45 | Seed ranking display |
| PS-74 | PS-47 | Portfolio-fit edge fn |
| PS-76 | PS-52 | Direction Finder |
| PS-77 | PS-51 | Expert interview pipeline |
| PS-78 | PS-54 | Localization |
| PS-79 | PS-60 | E2E testing |
| PS-80 | PS-62 | Sentry |
| PS-42 | PS-53 | RLS (older duplicate) |
| PS-39 | PS-54 | Localization (older) |
| PS-40 | PS-82 | Cohort segmentation |

**Total active backlog:** 50 tickets → 36 unique after deduplication

**Dream State Coverage:** All 7 dream state features are now covered by active tickets:
1. ✅ Personalized seed queue — PS-72 (algorithm), PS-45 (display), PS-47 (portfolio-fit)
2. ✅ AI-assisted PathLab — PS-51 (expert→seed), PS-65 (GPU serving)
3. ✅ Real ikigai — PS-43 (calculation), PS-44 (visualization), PS-71 (integration)
4. ✅ Reflection trends → Direction Finder — PS-75 (trends), PS-52 (Direction Finder)
5. ✅ Expert conversation — PS-81 (RAG chatbot)
6. ✅ Localization — PS-54 (i18n system)
7. ✅ Social proof — PS-82 (cohort comparison)

### March 28, 2026 - Ticket Creation Sprint

Created 20 new tickets to close gaps between current state and 12-month dream:

**Phase 1 MVP Foundation (8 tickets):**
- PS-67: RLS policies for user data isolation [Urgent]
- PS-68: User onboarding flow for profile signals collection [Urgent]
- PS-69: Seed completion tracking UI and progress indicators [High]
- PS-70: Ikigai visualization component for Profile screen [High]
- PS-71: Connect profile.tsx to real ikigai edge function [High]
- PS-72: Seed ranking algorithm (affinity + exploration gaps) [Urgent]
- PS-73: Seed ranking display in Discover screen [High]
- PS-74: Portfolio-fit edge function for seed → user matching [Urgent]

**Phase 2 Intelligence & Insights (4 tickets):**
- PS-75: Reflection trends aggregation pipeline [Medium]
- PS-76: Direction Finder screen with university roadmap integration [High]
- PS-77: Expert interview → seed content pipeline [Medium]
- PS-78: Thai/English localization system [High]

**Infrastructure (4 tickets):**
- PS-79: E2E testing infrastructure with Detox [High]
- PS-80: Sentry error monitoring integration [High]
- PS-83: [Phase 1] MVP Launch Readiness Checklist [Urgent]
- PS-84: Push notification integration for daily seed reminders [High]
- PS-85: GPU model serving monitoring dashboard [Medium]

**Phase 3 Social & Expert Layers (2 tickets):**
- PS-81: Expert conversation layer (RAG chatbot) [Medium]
- PS-82: Cohort comparison analytics for social proof [Medium]

**Analytics (1 ticket):**
- PS-86: Seed quality scorecard and content iteration workflow [Medium]
