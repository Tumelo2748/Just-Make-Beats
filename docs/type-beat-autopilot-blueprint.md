# Type-Beat Auto-Pilot — Product Blueprint

## 1) Product North Star
**Promise:** Producers upload beats; the platform handles SEO, packaging, and publishing decisions automatically.

**Primary user:** Independent type-beat producers (single channel) and collectives (multi-channel).

**Core KPI:** Increase qualified search impressions and upload consistency without requiring manual SEO work.

---

## 2) Problem Statement
Type-beat producers lose momentum because YouTube growth requires repetitive, technical tasks:
- keyword research,
- title and tag formatting,
- thumbnail/visual consistency,
- post timing and scheduling,
- performance interpretation.

Most current tools are **diagnostic** (analytics-heavy) instead of **operator-like** (action-taking).

---

## 3) Differentiated Product Thesis
Generic YouTube tools optimize broad channels. This platform is niche-locked by design:
1. Each account is calibrated around an **Anchor Artist** (e.g., Gunna, Yeat).
2. Every upload is scored against the channel's sonic and metadata DNA.
3. Recommendations are constrained to that niche unless confidence suggests a deliberate expansion.

Result: The product behaves like a specialized channel manager, not a generic SEO dashboard.

---

## 4) Core Features and Functional Specs

### A. Niche-Lock Calibration
**User flow**
1. Connect YouTube channel.
2. Select primary anchor artist + optional secondary artists.
3. Baseline sync runs over last N uploads (e.g., 30–90 videos).

**Outputs**
- Baseline Performance Profile:
  - median CTR,
  - average watch duration,
  - views @ 24h / 7d,
  - top performing title patterns,
  - top search query clusters.
- Channel DNA vector:
  - sonic fingerprint centroid,
  - dominant BPM range,
  - mood/genre profile,
  - metadata language profile.

**Guardrail logic**
- Suggestions outside anchor niche require high confidence and explicit opt-in.

---

### B. Sonic Fingerprinting + No-Input SEO
**Input:** Uploaded beat audio file.

**Pipeline**
1. Audio feature extraction (tempo, key, spectral characteristics).
2. Instrument and texture tagging (e.g., muted guitar, airy pad, slide 808).
3. Similarity matching vs. niche trend corpus (anchor-specific).
4. Generate metadata pack:
   - title candidate set,
   - description blocks,
   - tags/hashtags,
   - upload category and playlist suggestion.

**Consistency Guard**
- Drift score (0–100) compares new beat vs channel DNA.
- If drift exceeds threshold (e.g., 85%), user sees:
  - "Upload anyway",
  - "Route to alt channel",
  - "Retune metadata for experimental drop".

---

### C. Vibe-Consistent Visual Generator
**Concept:** Genre/artist aesthetic packs + dynamic generation.

**Pack examples**
- Gunna / YSL: dark luxury, chrome gradients, Atlanta nights.
- Yeat: hyper-digital, neon distortion.
- Brent Faiyaz: grainy cinematic, warm dusk tones.

**Generation modes**
- Static cover + waveform layer.
- Beat-reactive visualizer (energy-reactive motion).

**Output guarantees**
- Brand-safe by pack constraints.
- Unique per upload but channel-cohesive over time.

---

### D. Smart-Title Syntax Engine
**Primary formula**
`[FREE] {Anchor_Artist} Type Beat {Year} - "{Beat_Name}" {Secondary_Artist_Logic} | {Sub_Genre_Tag}`

**Engine behavior**
- Produces 5–10 ranked options.
- Applies syntax constraints:
  - exact anchor token in front half,
  - year normalization,
  - quote style consistency,
  - fallback if beat-name confidence is low.
- Optional auto A/B testing (for tiers with experimentation).

---

### E. Anti-Quit Niche Authority Dashboard
**Reframe metrics away from vanity views.**

**Primary metric:** Niche Authority Score (NAS)
- Proxy for search ownership within anchor niche.
- Derived from search impressions, CTR rank vs niche peers, and upload consistency.

**Actionable coaching examples**
- "You own ~2.1% of estimated Gunna-type search share."
- "3 melodic uploads this week could raise projected share to 3.0%."

**Behavioral goal:** sustain creator motivation with controllable actions.

---

## 5) Suggested Technical Architecture (MVP-friendly)

### Services
1. **Auth + User Service**
2. **YouTube Connector Service** (OAuth + upload/publish + analytics pull)
3. **Audio Intelligence Service** (fingerprinting + similarity + tag generation)
4. **Metadata Engine** (title/description/tag generation + policy filters)
5. **Visual Generation Service** (template packs + render queue)
6. **Scheduler/Automation Service**
7. **Analytics + Scoring Service** (NAS + cohort tracking)

### Data Stores
- Postgres: users, channels, uploads, experiments, plans.
- Object storage (S3/GCS): audio, generated video assets.
- Vector store (pgvector or dedicated): sonic embeddings + trend embeddings.
- Time-series/warehouse: metrics history for scoring and forecasting.

### AI/ML Components
- Audio embedding model for beat similarity.
- Classification model for mood/subgenre/instrument tags.
- LLM template engine for title/description generation with strict schema validation.
- Forecasting model for NAS and upload impact recommendations.

---

## 6) MVP Scope (First 8–10 Weeks)

### Must-have
- Channel onboarding + anchor artist setup.
- Upload ingestion.
- Auto-generated title, tags, and description.
- Simple visual generation (template + waveform).
- Scheduled YouTube publishing.
- Basic NAS + weekly action recommendations.

### Defer to Phase 2
- Full beat-reactive visuals.
- Auto A/B test with adaptive winner selection.
- Multi-channel agency workspace.
- Deep competitive benchmark panels.

---

## 7) Monetization
- **Hobbyist:** limited monthly uploads, baseline metadata generation, static visuals.
- **Pro:** unlimited uploads, reactive visuals, title experiments, advanced NAS insights.
- **Agency/Collective:** multi-channel management, permissions, batch scheduling, shared asset library.

Add-ons:
- Premium aesthetic packs,
- bulk back-catalog optimization,
- managed growth playbooks.

---

## 8) Risk & Mitigation
- **Risk:** YouTube API quota/limits.
  - *Mitigation:* queued sync windows + selective polling.
- **Risk:** Metadata over-optimization looks spammy.
  - *Mitigation:* quality and policy filters, semantic variety constraints.
- **Risk:** Copyright/policy visual content issues.
  - *Mitigation:* pack-level policy-safe assets + moderation checks.
- **Risk:** Producer trust in automated actions.
  - *Mitigation:* transparent confidence scores + one-click manual override.

---

## 9) Success Metrics
- Activation: % users completing calibration + first publish.
- Time-to-publish: median minutes from upload to scheduled post.
- Retention: weekly active uploaders.
- Content consistency: reduction in niche drift over time.
- Performance: delta in search impressions/CTR vs baseline.

---

## 10) Build Sequence Recommendation
1. Build metadata autopilot first (fastest user value).
2. Add visual generation templates second.
3. Add consistency guard and NAS dashboard third.
4. Add experimentation and agency workflows last.

This ordering maximizes speed to market while preserving your core edge: **prescriptive automation for a specific producer niche**.
