# Dream State Coverage — 12-Month Roadmap

## Dream State Items vs Ticket Coverage

| # | Dream State | Tickets | Coverage |
|---|-------------|---------|----------|
| 1 | Personalized seed queue (affinity + gaps) | PS-4 (Growth), PS-15 (AI & ML), PS-72 (AI & ML), PS-24 (AI & ML), PS-98 (Mobile App) | ✅ Covered |
| 2 | AI-assisted PathLab generation (expert → seed in 1hr) | PS-9 (AI & ML), PS-26 (AI & ML), PS-59 (Content CMS) | ✅ Covered |
| 3 | Real ikigai from reflection data | PS-1 (AI & ML), PS-13 (Backend), PS-14 (Mobile App), PS-25 (Backend), PS-43 (AI & ML), PS-71 (→ closed Duplicate) | ✅ Covered |
| 4 | Reflection trends → Direction Finder | PS-6 (AI & ML), PS-28 (AI & ML), PS-29 (AI & ML), PS-75 (AI & ML), PS-21 (AI & ML) | ✅ Covered |
| 5 | Expert conversation layer | PS-10 (AI & ML), PS-27 (AI & ML), PS-81 (AI & ML) | ✅ Covered |
| 6 | Fully localized seed content (TH/EN) | PS-3 (Content), PS-31 (Content), **PS-100 (Content)** ← NEW | ⚠️ PS-3/PS-31 create system; PS-100 ensures all seeds ARE localized |
| 7 | Social proof: "N students tried this" + cohort comparison | PS-7 (Growth), PS-22 (Growth), PS-82 (Growth), **PS-99 (Mobile App)** ← NEW | ⚠️ PS-7/PS-22/PS-82 = analytics pipeline; PS-99 = Mobile App UI for seed cards |

## Ticket Cleanup Actions (2026-04-18)

| Action | Ticket | Change |
|--------|--------|--------|
| Closed duplicate | PS-71 | State → Duplicate; comment pointing to PS-14 |
| Moved project | PS-14 | Backend → **Mobile App** (profile.tsx integration belongs to Mobile) |
| Created | **PS-99** | Mobile App: Social proof UI — seed card counter display |
| Created | **PS-100** | Content: Translate all seed content to Thai and English |

## Duplicate Pairs Identified

| Ticket A | Ticket B | Resolution |
|----------|----------|------------|
| PS-71 (AI & ML) | PS-14 (Backend → Mobile App) | PS-71 closed as Duplicate of PS-14 |
| PS-44 (Mobile App) | PS-32 (Mobile App) | Both Ikigai visualization — PS-44 is detailed spec, PS-32 is implementation. Not true duplicates. |

## Remaining Gaps

- **Phase 1 Expert Conversation foundation**: PS-10 covers Phase 1 expert chat UI, but no dedicated Phase 1 RAG foundation ticket exists separately from PS-81 (Phase 2). Could be consolidated.
- **University roadmap matching**: PS-8 (Growth) and PS-97 (AI & ML) overlap — university roadmap matching algorithm spans Growth (feature) and AI & ML (algorithm).
- **Profile reveal UI**: PS-57 (Mobile App) "show students what seeds taught them" — partially covers Dream State #4 output but may need clarification.

## Project Distribution (78 open tickets)

| Project | Count | Key Coverage |
|---------|-------|-------------|
| Mobile App | ~12 | UI screens, seed cards, ikigai viz, profile integration |
| AI & ML | ~22 | Ikigai, ranking, PathLab, expert chat, NLP |
| Growth | ~18 | Analytics, social proof, push, cohort, A/B testing |
| Backend | ~9 | Profile signals, RLS, edge functions, migrations |
| Infrastructure | ~8 | CI/CD, monitoring, feature flags, testing |
| Content | ~6 | Localization, CMS, seed content |
