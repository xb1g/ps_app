# AGENTS.md

Instructions for AI coding agents working in this repository.

## Versioning Rule

- On every shipped app update, bump `expo.version` in `app.json`.
- Do not hardcode version text in UI. Read it from Expo config (`Constants.expoConfig.version`).
- Keep the Profile screen footer version label present and accurate.

## Linear Project Structure (Team: Passionseed Main / PS)

| Project | Color | Linear ID |
|---------|-------|-----------|
| Mobile App | #3B82F6 | 1ea9aa51-e3ec-4d34-bd98-50b18c859213 |
| Backend | #8B5CF6 | a22f2444-7a05-45a3-a7dd-4503937304b6 |
| Infrastructure | #F59E0B | 1358137d-f9ef-4486-bada-c44c22c1fa87 |
| AI & ML | #EF4444 | 163baf10-fed5-4dc9-ab30-c0029dea9dc5 |
| Content | #10B981 | ca0b0197-f32b-4e53-aec7-2f83f84b218a |
| Growth | #EC4899 | 9967dd59-657b-496a-b995-37efd03cc436 |

**Duplicate State UUID:** `7edad5a0-dad8-4c65-9d59-3fa37cec787c`

## Project Tagging Rules

1. Query all existing projects in the PS team first
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

## Linear Backlog (open tickets, 2026-05-07)

| ID | Title | Project | Status |
|----|-------|---------|--------|
| PS-70 | [Content] Translate all seed content to Thai and English | Content | Backlog |
| PS-69 | [Monitoring] Sentry acceptance criteria and release tracking | Infrastructure | Backlog |
| PS-68 | [Edge Function] Implement push notification trigger system | Growth | Backlog |
| PS-67 | [Social] Add 'N students tried this path' counter to seed cards | Growth | Backlog |
| PS-66 | [Edge Function] Deploy career-insights edge function | Backend | Backlog |
| PS-65 | [Database] Create ikigai_snapshots table | Backend | Backlog |
| PS-63 | [CI/CD] Configure EAS Build and automated deployments | Infrastructure | Backlog |
| PS-62 | [Monitoring] Integrate Sentry for error tracking | Infrastructure | Backlog |
| PS-61 | [Testing] Set up E2E testing with Detox | Infrastructure | Backlog |
| PS-60 | [i18n] Thai/English localization system | Content | Backlog |
| PS-58 | [Social] Add cohort comparison and social proof | Growth | Backlog |
| PS-56 | [PathLab] Build expert interview → seed generation pipeline | AI & ML | Backlog |
| PS-55 | [AI] Implement seed ranking algorithm with exploration gap detect | AI & ML | Backlog |
| PS-54 | [Data Pipeline] Build reflection → ikigai → Direction Finder flow | AI & ML | Backlog |
| PS-53 | [Foundation] Complete profile signals implementation and validation | Backend | Backlog |
| PS-50 | [Data] Build university roadmap matching engine | AI & ML | Backlog |
| PS-46 | Implement ikigai calculation engine | AI & ML | Backlog |
| PS-40 | Seed velocity analytics dashboard | Growth | Backlog |
| PS-39 | Validate parent willingness to pay for career exploration | Content | Backlog |
| PS-38 | [Feature] Build expert conversation layer (talk to experts) | AI & ML | Backlog |
| PS-34 | Request path for Pathlab | AI & ML | Backlog |
| PS-32 | [ps_app] Build seed queue and daily task completion UI | Mobile App | Backlog |
| PS-31 | [Data] Define and implement user profile signals schema | Backend | In Progress |
| PS-24 | [Data] Build profile scoring engine for ikigai and seed affinity | AI & ML | Backlog |
| PS-22 | [Feature] Build profile reveal UI — show students what seeds taught them | Mobile App | Backlog |
| PS-21 | [Analytics] Track seed velocity and Direction Finder readiness | Growth | Backlog |
| PS-20 | [ps_app] Set up push notification infrastructure | Mobile App | Backlog |
| PS-19 | [ps_app] Build offline-first seed content caching | Mobile App | Backlog |
| PS-14 | [Social] Build social proof features (cohort comparison) | Growth | Backlog |
| PS-9 | Build Path Lab for Business Innovation Path | AI & ML | Backlog |
| PS-6 | Train team to be AI-native | Growth | Backlog |
| PS-5 | About page | PS web | Backlog |

## 12-Month Dream State Coverage

| Dream State Item | Linear Ticket | Coverage |
|-----------------|--------------|----------|
| 1. Personalized seed queue (ranking) | PS-55 (algo), PS-32 (UI) | ✅ |
| 2. AI-assisted PathLab generation | PS-56 | ✅ |
| 3. Real ikigai from reflection data | PS-46 (engine), PS-65 (snapshot DB) | ✅ |
| 4. Reflection trends → Direction Finder | PS-54 | ✅ |
| 5. Expert conversation layer (RAG) | PS-38 | ✅ |
| 6. Thai/English full localization | PS-60 (system), PS-70 (content) | ✅ |
| 7. Social proof + cohort comparison | PS-67 (counter), PS-14 (cohort) | ✅ |
| + Discover screen UI | PS-32 (seed queue) | ✅ |
| + Push notifications | PS-68 (trigger), PS-20 (infra), PS-60 (system) | ✅ |
| + University roadmap match | PS-50 (engine), PS-61 (UI — not in backlog yet) | ⚠️ UI gap |

**Gap:** PS-61 "University Roadmap Match — TCAS program alignment" exists but is marked Backlog with no dedicated UI ticket. Ensure PS-61 or a new Mobile App ticket covers the TCAS roadmap UI.

## Key Mock Data to Replace

- `app/(tabs)/profile.tsx:36` — `MOCK_IKIGAI` (hardcoded 85/72/48/61) → replace with PS-46 output
- `app/(tabs)/profile.tsx:98` — `MOCK_ACHIEVEMENTS` (fake social) → replace with PS-67/PS-14 output
- `lib/pathlab.ts:15` — `getAvailableSeeds()` orders by `created_at` → replace with PS-55 ranking

## Supabase Edge Functions

- `career-insights` — career recommendations
- `portfolio-fit` — portfolio matching
- `score-engine` — ikigai/scoring
- `push-notifications` — scheduled push (PS-68)
- `scripts/generate-pathlab/` — 5-agent PathLab generation CLI

## CI/CD Pipeline

- EAS Build: `eas build --platform android --profile preview`
- EAS Submit: `eas submit --platform android --latest`
- CI/CD configured via GitHub Actions (`.github/workflows/`)
