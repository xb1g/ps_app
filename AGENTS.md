# AGENTS.md

Instructions for AI coding agents working in this repository.

## Versioning Rule

- On every shipped app update, bump `expo.version` in `app.json`.
- Do not hardcode version text in UI. Read it from Expo config (`Constants.expoConfig.version`).
- Keep the Profile screen footer version label present and accurate.

## Linear Project Structure (Team: BIG / Passion Seed)

| Project | Color | Linear ID |
|---------|-------|-----------|
| Mobile App | #3B82F6 | a029f65b-49d5-410f-b6bb-3363aea49f8c |
| Backend | #8B5CF6 | 43186723-0897-4093-a0a8-9f8457e4c6e2 |
| Infrastructure | #F59E0B | 7065ac8f-559a-4f8b-93da-509a94573e71 |
| AI & ML | #EF4444 | b85e5915-e0ed-4acd-b445-b51f8cf123e7 |
| Content | #10B981 | 0c16a2bd-9b68-4c9a-8f5a-2e3452810766 |
| Growth | #EC4899 | 3dabe534-6a4c-4c7d-bcc6-aec93764c0f3 |

**Note:** Linear workspace uses "BIG" team key with "BIG-XX" ticket identifiers.

## Project Tagging Rules

1. Query all existing projects in the BIG team first
2. For each ticket, determine the primary project based on content:
   - UI/screens/components → Mobile App
   - Database/RLS/edge functions → Backend
   - Testing/monitoring/CI → Infrastructure
   - Algorithms/AI/NLP/ranking/ikigai → AI & ML
   - Localization/content/CMS → Content
   - Analytics/push/social/retention → Growth
3. Some tickets may span multiple projects — use the PRIMARY focus
4. When creating new tickets, assign the correct projectId
5. When updating existing tickets, add the project if missing

## Keyword to Project Mapping

| Keyword | Project |
|---------|--------|
| "expert" | AI & ML |
| "localization" / "Thai" / "i18n" | Content |
| "ranking" / "affinity" / "personalized" | AI & ML |
| "ikigai" | AI & ML |
| "profile signals" | Backend |
| "reflection" | Backend or AI & ML (data model=Backend, analysis=AI&ML) |
| "Direction Finder" | AI & ML |
| "social" / "cohort" | Growth |
| "testing" / "E2E" / "Detox" | Infrastructure |
| "monitoring" / "Sentry" | Infrastructure |
| "database" / "migration" / "RLS" | Backend |
| "push" / "notification" | Growth |
| "analytics" / "dashboard" | Growth |

## Linear Backlog (open tickets, 2026-05-08)

| ID | Title | Project | Status |
|----|-------|---------|--------|
| BIG-50 | [AI & ML] Seed Ranking Engine - profile affinity + exploration gaps | AI & ML | Backlog |
| BIG-51 | [AI & ML] Real Ikigai Calculation - replace MOCK_IKIGAI with reflection data | AI & ML | Backlog |
| BIG-52 | [AI & ML] Expert Conversation Layer - RAG chatbot per expert | AI & ML | Backlog |
| BIG-53 | [Content] Thai/English i18n System - full localization | Content | Backlog |
| BIG-54 | [Growth] Social Proof - enrollment counters + cohort features | Growth | Backlog |
| BIG-55 | [Backend] Reflection Aggregation Pipeline - trends for Direction Finder | Backend | Backlog |
| BIG-56 | [Infrastructure] PathLab Pipeline Testing & Validation | Infrastructure | Backlog |
| BIG-57 | [Infrastructure] E2E Testing with Detox - core user flows | Infrastructure | Backlog |
| BIG-59 | [Mobile App] Discover Screen UI - personalized seed ranking integration | Mobile App | Backlog |
| BIG-60 | [Growth] Push Notification System - engagement & retention | Growth | Backlog |
| BIG-61 | [Mobile App] University Roadmap Match - TCAS program alignment | Mobile App | Backlog |
| BIG-63 | [AI & ML] PathLab Generation Pipeline - expert interview to seed in 1 hour | AI & ML | Backlog |

**Archived:** BIG-58 (duplicate placeholder - archived 2026-05-08)

## 12-Month Dream State Coverage

| Dream State Item | Linear Ticket | Coverage |
|-----------------|--------------|----------|
| 1. Personalized seed queue (ranking) | BIG-50 (algo), BIG-59 (UI) | ✅ |
| 2. AI-assisted PathLab generation | BIG-63 (build), BIG-56 (test) | ✅ |
| 3. Real ikigai from reflection data | BIG-51 (engine) | ✅ |
| 4. Reflection trends → Direction Finder | BIG-55 (Backend pipeline) | ✅ |
| 5. Expert conversation layer (RAG) | BIG-52 | ✅ |
| 6. Thai/English full localization | BIG-53 | ✅ |
| 7. Social proof + cohort comparison | BIG-54 | ✅ |
| + Discover screen UI | BIG-59 | ✅ |
| + Push notifications | BIG-60 | ✅ |
| + University roadmap match | BIG-61 | ✅ |

**All 7 dream state items are covered.** Gap closed: BIG-63 (PathLab generation pipeline) was missing and is now created.

## Key Mock Data to Replace

- `app/(tabs)/profile.tsx:36` - `MOCK_IKIGAI` (hardcoded 85/72/48/61) -> replace with BIG-51 output
- `app/(tabs)/profile.tsx:98` - `MOCK_ACHIEVEMENTS` (fake social) -> replace with BIG-54 output
- `lib/pathlab.ts:15` - `getAvailableSeeds()` orders by `created_at` -> replace with BIG-50 ranking

## Supabase Edge Functions

- `career-insights` - career recommendations
- `portfolio-fit` - portfolio matching
- `score-engine` - ikigai/scoring
- `push-notifications` - scheduled push (BIG-60)
- `scripts/generate-pathlab/` - 5-agent PathLab generation CLI (BIG-63)

## CI/CD Pipeline

- EAS Build: `eas build --platform android --profile preview`
- EAS Submit: `eas submit --platform android --latest`
- CI/CD configured via GitHub Actions (`.github/workflows/`)
