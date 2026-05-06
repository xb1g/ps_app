# AGENTS.md

Instructions for AI coding agents working in this repository.

## Versioning Rule

- On every shipped app update, bump `expo.version` in `app.json`.
- Do not hardcode version text in UI. Read it from Expo config (`Constants.expoConfig.version`).
- Keep the Profile screen footer version label present and accurate.

## Linear Project Structure (Team: Big / BIG)

| Project | Color | Linear ID |
|---------|-------|-----------|
| Mobile App | #3B82F6 | a029f65b-49d5-410f-b6bb-3363aea49f8c |
| Backend | #8B5CF6 | 43186723-0897-4093-a0a8-9f8457e4c6e2 |
| Infrastructure | #F59E0B | 7065ac8f-559a-4f8b-93da-509a94573e71 |
| AI & ML | #EF4444 | b85e5915-e0ed-4acd-b445-b51f8cf123e7 |
| Content | #10B981 | 0c16a2bd-9b68-4c9a-8f5a-2e3452810766 |
| Growth | #EC4899 | 3dabe534-6a4c-4c7d-bcc6-aec93764c0f3 |

## Linear Backlog (open tickets, 2026-05-05)

| ID | Title | Project | Status |
|----|-------|---------|--------|
| BIG-50 | Seed Ranking Engine — profile affinity + exploration gaps | AI & ML | Backlog |
| BIG-51 | Real Ikigai Calculation — replace MOCK_IKIGAI | AI & ML | Backlog |
| BIG-52 | Expert Conversation Layer — RAG chatbot per expert | AI & ML | Backlog |
| BIG-53 | Thai/English i18n System — full localization | Content | Backlog |
| BIG-54 | Social Proof — enrollment counters + cohort features | Growth | Backlog |
| BIG-55 | Reflection Aggregation Pipeline — trends for Direction Finder | Backend | Backlog |
| BIG-56 | PathLab Pipeline Testing & Validation | Infrastructure | Backlog |
| BIG-57 | E2E Testing with Detox — core user flows | Infrastructure | Backlog |
| BIG-59 | Discover Screen UI — personalized seed ranking integration | Mobile App | Backlog |
| BIG-60 | Push Notification System — engagement & retention | Growth | Backlog |
| BIG-61 | University Roadmap Match — TCAS program alignment | Mobile App | Backlog |

## 12-Month Dream State Coverage

| Dream State Item | Linear Ticket | Coverage |
|-----------------|--------------|----------|
| 1. Personalized seed queue (ranking) | BIG-50, BIG-59 | ✅ |
| 2. AI-assisted PathLab generation | BIG-56 | ✅ |
| 3. Real ikigai from reflection data | BIG-51 | ✅ |
| 4. Reflection trends → Direction Finder | BIG-55 | ✅ |
| 5. Expert conversation layer (RAG) | BIG-52 | ✅ |
| 6. Thai/English full localization | BIG-53 | ✅ |
| 7. Social proof + cohort comparison | BIG-54 | ✅ |
| + Discover screen UI integration | BIG-59 | ✅ |
| + Push notifications | BIG-60 | ✅ |
| + University roadmap match | BIG-61 | ✅ |

## Key Mock Data to Replace

- `app/(tabs)/profile.tsx:36` — `MOCK_IKIGAI` (hardcoded 85/72/48/61) → replace with BIG-51 output
- `app/(tabs)/profile.tsx:98` — `MOCK_ACHIEVEMENTS` (fake social) → replace with BIG-54 output
- `lib/pathlab.ts:15` — `getAvailableSeeds()` orders by `created_at` → replace with BIG-50 ranking

## Supabase Edge Functions

- `career-insights` — career recommendations
- `portfolio-fit` — portfolio matching
- `score-engine` — ikigai/scoring
- `push-notifications` — scheduled push (BIG-60)
- `scripts/generate-pathlab/` — 5-agent PathLab generation CLI
