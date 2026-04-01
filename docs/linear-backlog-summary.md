# Linear Backlog Summary

**Generated:** 2026-03-31  
**Total Open Tickets:** 57 (excluding duplicates)  
**Project Tags Updated:** 15 tickets

---

## Project Distribution

| Project | Ticket Count | Description |
|---------|-------------|-------------|
| AI & ML | ~20 | Algorithms, ikigai, expert features, PathLab, Direction Finder |
| Mobile App | ~12 | UI screens, React Native components, offline caching |
| Backend | ~10 | Database schemas, tables, RLS, edge functions, profile signals |
| Growth | ~8 | Social proof, cohort analytics, push notifications |
| Infrastructure | ~3 | Testing (Detox), monitoring (Sentry), CI/CD (EAS) |
| Content | ~4 | Thai/English localization, i18n |

---

## Project Tagging Updates Applied

15 tickets were updated with correct project assignments:

| Ticket | From | To | Reason |
|--------|------|-----|--------|
| 3841c10e | Growth | AI & ML | Seed ranking algorithm |
| 5aa26fbe | AI & ML | Backend | Profile signals implementation |
| b22305d4 | AI & ML | Backend | ikigai_snapshots table |
| 96f746c4 | Growth | AI & ML | University roadmap matching |
| a08cd284 | AI & ML | Backend | Profile signals schema |
| fe1f63cc | None | AI & ML | Validate parent willingness |
| 4f020da1 | None | AI & ML | Validate parent willingness |
| ec0e8c0c | Mobile App | Backend | Profile signals schema |
| b9d45666 | Mobile App | AI & ML | Seed ranking algorithm |
| 57b9011a | AI & ML | Mobile App | Profile reveal UI |
| a82289f2 | Mobile App | Growth | Push notification infrastructure |
| d7002474 | Content | Mobile App | Profile reveal screen |
| 9f27f107 | Growth | Mobile App | Profile reveal UI |
| d5e25888 | PS mobile | AI & ML | Path Lab |
| d21c4d7f | PS mobile | AI & ML | Validate parent willingness |

---

## 12-Month Dream State Coverage

All 7 dream state features have ticket coverage:

### ✓ 1. Personalized Seed Queue
- Seed ranking algorithm (profile affinity + exploration gaps)
- Profile scoring engine for seed affinity
- Seed queue UI implementation

### ✓ 2. AI-Assisted PathLab Generation
- Expert interview → seed generation pipeline
- PathLab content creation workflow
- Multiple Path implementations (Business Innovation, etc.)

### ✓ 3. Real Ikigai from Reflection Data
- Ikigai calculation engine
- Ikigai snapshots table for historical tracking
- Reflection → ikigai data pipeline

### ✓ 4. Reflection Trends → Direction Finder
- Reflection trends aggregation
- Direction Finder integration
- University roadmap matching engine

### ✓ 5. Expert Conversation Layer
- Expert conversation feature (talk to experts)
- Multiple implementation tickets

### ✓ 6. Fully Localized Content
- Thai/English localization system
- i18n infrastructure

### ✓ 7. Social Proof Features
- "N students tried this path" counter
- Cohort comparison features
- Social proof analytics

---

## Identified Duplicates

The following tickets are marked as `[Duplicate]` and should be consolidated:

- Expert conversation layer (multiple duplicates)
- Thai/English localization (multiple duplicates)
- Reflection aggregation pipeline (duplicates)
- Validate parent willingness to pay (multiple duplicates)
- Request path for Pathlab (multiple duplicates)

**Recommendation:** Close duplicate tickets and link to primary tickets before sprint planning.

---

## Gaps

No unrepresented gaps identified. All dream state features have ticket coverage.

---

## Next Steps

1. **Close duplicate tickets** - Consolidate ~15 duplicate tickets
2. **Prioritize by dream state** - Organize sprint planning around the 7 dream state features
3. **Project cleanup** - Consider deprecating "PS mobile" and "PS web" projects in favor of "Mobile App", "Backend", "Content"
4. **Sprint planning** - Focus on foundation items first:
   - Profile signals schema + implementation (Backend)
   - Seed ranking algorithm (AI & ML)
   - Localization system (Content)
