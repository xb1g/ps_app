# Passion Seed Mobile - 12-Month Roadmap Tickets

**Generated:** 2026-03-28
**Team:** PS (Passion Seed Main)
**Context:** Gap analysis between current app state and 12-month dream state

---

## Current State Summary

✅ **What exists:**
- 3-tab app structure (Discover, My Paths, Profile)
- Seed browsing and enrollment system
- Daily reflection collection
- Journey/Path visualization
- Mock ikigai display (not calculated from real data)
- Onboarding flow
- Push notification infrastructure

❌ **Dream state gaps:**
1. No personalized seed ranking
2. No AI-assisted PathLab generation
3. Ikigai is mock data, not from reflections
4. No reflection trends/insights
5. No expert conversation layer
6. Limited Thai localization
7. No social proof counters

---

## Priority 1 (Foundation) - Q1 2026

### PS-1: Implement real Ikigai calculation from reflection data
**Priority:** 🔴 High
**Estimate:** 5 days

**Problem:** Profile screen shows MOCK ikigai data. Should be calculated from actual user reflection data.

**Acceptance Criteria:**
- [ ] Query path_reflections table for user's completed reflections
- [ ] Calculate 4 ikigai scores:
  - **Passion:** Average interest_level across all reflections
  - **Mission:** Correlation between energy_level and world-impact seeds
  - **Profession:** Completion rate × skill node progress
  - **Vocation:** Average confusion_level (inverted) + node assessment scores
- [ ] Store calculated scores in user_profiles or ikigai_snapshots table
- [ ] Update profile.tsx to fetch real data instead of MOCK_IKIGAI
- [ ] Show trend arrows (↑↓→) comparing to previous week

**Technical Notes:**
- Use Supabase edge function `career-insights` for heavy calculation
- Cache results, recalculate on new reflection submission
- Fallback to mock data if < 3 reflections exist

---

### PS-2: Add profile affinity scoring to seed ranking
**Priority:** 🔴 High
**Estimate:** 4 days

**Problem:** Discover screen shows seeds in chronological order. Should rank by user's profile affinity.

**Acceptance Criteria:**
- [ ] Create `calculate_seed_affinity(user_id, seed_id)` function
- [ ] Affinity factors:
  - Interest category match (from onboarding)
  - Career goal similarity
  - Past seed completion patterns
  - TCAS program alignment
- [ ] Update getAvailableSeeds() to return sorted by affinity score
- [ ] Add "Why recommended" explainer chip on seed cards
- [ ] A/B test: 50% users get affinity sort, 50% chronological

**Technical Notes:**
- Start with simple rule-based scoring
- Can upgrade to ML model later
- Cache affinity scores, invalidate on new reflection

---

### PS-3: Create seed content localization system (TH/EN)
**Priority:** 🔴 High
**Estimate:** 6 days

**Problem:** Seed content is English-only. Thai students need Thai language support.

**Acceptance Criteria:**
- [ ] Add `title_th`, `description_th`, `slogan_th` columns to seeds table
- [ ] Add `language` preference to user_profiles
- [ ] Update getAvailableSeeds() to return localized content
- [ ] Add language toggle in Settings
- [ ] Create admin interface for Thai content entry
- [ ] Migrate existing seeds with AI translation + human review

**Technical Notes:**
- Use Supabase RLS to serve correct language
- Fallback to English if Thai not available

---

### PS-4: Seed queue personalization algorithm
**Priority:** 🔴 High
**Estimate:** 5 days

**Problem:** No unified ranking system combining affinity, gaps, and social signals.

**Acceptance Criteria:**
- [ ] Create `rank_seeds(user_id)` edge function
- [ ] Ranking formula:
  ```
  score = 
    0.4 × affinity_score +
    0.3 × exploration_gap_bonus +
    0.2 × social_proof_factor +
    0.1 × recency_boost
  ```
- [ ] A/B test different weightings
- [ ] Log ranking decisions for analysis
- [ ] Refresh queue daily via push notification

**Technical Notes:**
- Start with rule-based, upgrade to ML ranking model
- Track CTR on recommended seeds

---

## Priority 2 (Personalization) - Q2 2026

### PS-5: Build exploration gap detection system
**Priority:** 🟡 Medium
**Estimate:** 4 days

**Problem:** Users don't know what careers/paths they're missing.

**Acceptance Criteria:**
- [ ] Analyze user's completed seeds → extract skill/topic tags
- [ ] Compare against career path requirements
- [ ] Identify gaps: "You haven't explored any healthcare paths"
- [ ] Surface in Discover as "Recommended for exploration" section
- [ ] Track exploration diversity score in profile

**Data Model:**
```sql
-- Add to user_profiles
exploration_diversity_score FLOAT
exploration_gaps TEXT[] -- ['healthcare', 'arts', 'trades']
```

---

### PS-6: Build reflection trends dashboard
**Priority:** 🟡 Medium
**Estimate:** 6 days

**Problem:** Reflection data is collected but not visualized.

**Acceptance Criteria:**
- [ ] Create /reflections screen with:
  - Energy level trend (line chart, last 14 days)
  - Interest vs Confusion scatter plot
  - Streak calendar (GitHub-style contribution graph)
  - "Best day" insights (when energy + interest peak)
- [ ] Add "Direction Finder" section:
  - Top 3 career categories by engagement
  - Recommended next seed based on trends
- [ ] Export to PDF for university applications

**Technical Notes:**
- Use react-native-svg-charts or skia

---

### PS-7: Add social proof counters to seed cards
**Priority:** 🟡 Medium
**Estimate:** 3 days

**Problem:** No social validation on paths.

**Acceptance Criteria:**
- [ ] Add `enrollment_count` to seeds (computed column or cache)
- [ ] Add `completion_count` (enrollments with status='explored')
- [ ] Display on seed cards: "🔥 234 students tried this"
- [ ] Add cohort comparison: "85% of completers continued to university"
- [ ] Show trending badge for seeds with >50% enrollment growth MoM

---

### PS-8: University roadmap matching engine
**Priority:** 🟡 Medium
**Estimate:** 7 days

**Problem:** Reflections don't connect to university choices.

**Acceptance Criteria:**
- [ ] Map seeds to TCAS programs (many-to-many)
- [ ] Calculate fit score: user's reflections → program requirements
- [ ] Show "University Match" section in profile
- [ ] Push notification: "New program matches your profile"

---

## Priority 3 (Expert/Social Layer) - Q3-Q4 2026

### PS-9: AI-assisted PathLab seed generator
**Priority:** 🟢 Low
**Estimate:** 10 days

**Problem:** Creating new seeds is manual. Should auto-generate from expert interviews.

**Acceptance Criteria:**
- [ ] Build expert interview form (10-15 questions)
- [ ] Call LLM to generate seed content + 20-30 day path
- [ ] Human review queue before publishing
- [ ] Target: expert interview → published seed in <1 hour

---

### PS-10: Expert conversation layer (chat with expert avatar)
**Priority:** 🟢 Low
**Estimate:** 8 days

**Problem:** Static seed content. Students should ask questions to experts.

**Acceptance Criteria:**
- [ ] Add `expert_persona` field to seeds (LLM system prompt)
- [ ] Build chat UI in seed detail screen
- [ ] Conversation saved to `expert_chats` table
- [ ] NPC avatar speaks with expert's voice

---

## Implementation Order

**Phase 1 (Foundation - 3 weeks):**
1. PS-1: Real Ikigai calculation
2. PS-3: Thai localization
3. PS-2: Affinity scoring

**Phase 2 (Personalization - 3 weeks):**
4. PS-4: Queue ranking algorithm
5. PS-5: Exploration gaps
6. PS-6: Reflection trends

**Phase 3 (Social - 2 weeks):**
7. PS-7: Social proof
8. PS-8: University matching

**Phase 4 (Expert Layer - future):**
9. PS-9: AI seed generator
10. PS-10: Expert chat

---

## Database Changes Required

```sql
-- Ikigai snapshots
CREATE TABLE ikigai_snapshots (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES auth.users(id),
  passion_score FLOAT,
  mission_score FLOAT,
  profession_score FLOAT,
  vocation_score FLOAT,
  calculated_at TIMESTAMPTZ DEFAULT NOW()
);

-- Exploration tracking
ALTER TABLE user_profiles ADD COLUMN exploration_diversity_score FLOAT;
ALTER TABLE user_profiles ADD COLUMN exploration_gaps TEXT[];

-- Social proof cache
ALTER TABLE seeds ADD COLUMN enrollment_count INTEGER DEFAULT 0;
ALTER TABLE seeds ADD COLUMN completion_count INTEGER DEFAULT 0;

-- Localization
ALTER TABLE seeds ADD COLUMN title_th TEXT;
ALTER TABLE seeds ADD COLUMN description_th TEXT;
ALTER TABLE seeds ADD COLUMN slogan_th TEXT;

-- Expert personas
ALTER TABLE seeds ADD COLUMN expert_persona TEXT;
CREATE TABLE expert_chats (
  id UUID PRIMARY KEY,
  seed_id UUID REFERENCES seeds(id),
  user_id UUID REFERENCES auth.users(id),
  messages JSONB,
  created_at TIMESTAMPTZ
);
```
