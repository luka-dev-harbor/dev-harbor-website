# Dev Harbor Website Content Improvement Plan

## Company Positioning Summary

### What Dev Harbor Is
A small, senior-level software development company based in Belgrade, Serbia. Not a body shop or agency with layers of account managers. A tight network of experienced developers where clients get direct access to the people doing the work.

### Target Clients

**Primary:**
- Startups needing MVPs to validate ideas or raise funding
- Growing companies that need a specific application or feature built
- Western European companies (especially BeNeLux) looking for reliable development partners

**Secondary:**
- Teams that need to augment with senior front-end expertise
- Companies with legacy systems that need modernization

**Not for:**
- Companies looking for the cheapest option
- Projects requiring massive teams (50+ developers)
- Clients who want to micromanage hourly work

### Key Differentiators
1. Senior developers, not juniors — experienced people on every project
2. Direct communication — talk to the person writing the code, not a project manager
3. Proven in complex domains — 5+ years building front-end for Twikey (European payments platform)
4. Fixed-scope, outcome-focused — clear deliverables over open-ended hourly billing
5. Small and selective — take on projects we can deliver well

### Core Strengths
- Front-end for complex applications (Angular, TypeScript, enterprise UI, dashboards)
- MVPs and prototypes (idea to working product)
- Working with Western European clients (culture fit, time zone, reliability)

### Proof Points
- 5-year ongoing engagement with Twikey (Belgian fintech)
- Recently delivered MVP with small team
- Track record of long-term client relationships

### Desired Tone
- Confident but not arrogant
- Professional but human
- Reliable, not flashy
- "We're a small, experienced team. We're selective. If we take your project, we'll deliver it properly."

---

## Content Decisions Made

### Hero Section (COMPLETED)

**Before:**
```
Built in harbor.
Ready for open waters.

At Dev Harbor, we build custom software that's more than just code.
It's the foundation for your journey.
```

**After:**
```
Software,
built as it should be.

From a team where every detail matters — since 2020.
```

**Rationale:**
- Two-line title for visual balance
- "As it should be" implies quality standards without being explicit
- Subtitle reinforces premium, detail-oriented positioning
- "Since 2020" adds credibility without being boastful

### Track Record Section (COMPLETED)

**Badge:** TRACK RECORD
**Headline:** Where we've proven ourselves
**Design:** WhiteCard components with icons (same as old Core Values design)

**Final cards:**
1. **Startups** (magic icon) — "We've helped founders go from idea to launch. We know what matters when runway is short and stakes are high."
2. **Complex front-ends** (code icon) — "The kind of front-end work that most teams avoid. That's our specialty."
3. **Long-term partnerships** (iris-scan icon) — "Our longest client relationship is 5+ years and counting. We stick around."
4. **Team integration** (dashboard-dots icon) — "We've embedded with teams across Europe. Direct communication, no layers — just delivery."

**Rationale:**
- Framed around "proof/experience" rather than client types or services
- Each card shows something Dev Harbor has actually done
- Personal to the company, not generic descriptions

### How We Work Section (COMPLETED)

**Badge:** HOW WE WORK
**Headline:** What to expect
**Design:** Outlined cards in 2x2 grid

**Final cards:**
1. **Direct access** — "You talk to the people writing the code. No layers, no middlemen."
2. **Clear scope** — "We define exactly what we're building before we start. Defined deliverables, realistic timelines."
3. **Consistent updates** — "Weekly progress, clear timelines. You always know where things stand."
4. **Honest feedback** — "We speak up when something doesn't make sense. We're partners, not people-pleasers."

**Rationale:**
- Shows what it's actually like to work with Dev Harbor
- Frames commitments to the client
- Replaces generic "Core Values" with actionable expectations

### Core Values Section (REMOVED)

**Reason:** Generic values that any dev shop could claim. The Track Record and How We Work sections communicate quality through proof and commitments instead of empty claims.

---

## Sections Still To Review

### Services Sections
**Current:**
1. Custom Software Development (BUILT FROM SCRATCH)
2. Full Scope of Work (END-TO-END)
3. Modernizing Legacy Tech (FUTURE)

**Needs:** Review copy to align with new positioning

### Expertise Section
**Current:**
- Web Apps
- Native Mobile
- Consulting

**Concerns:**
- Native Mobile listed as equal expertise when it's not primary strength
- May need to highlight Angular/TypeScript/complex front-end more

### Pricing Section
**Current:** Fixed Price, Time & Materials, Dedicated Developer
**Status:** Already decent, may just need minor copy tweaks

### Quote Section
**Current:** "We are a small team of hand-picked experts."
**Needs:** Review if this still fits the new tone

### Contact Section
**Status:** Functional, probably fine as-is

### Meta Tags / SEO
**Current:**
```
<title>Dev Harbor - Custom Web Development</title>
<meta name="description" content="Dev Harbor builds custom web applications, mobile apps, and enterprise software. Belgrade-based development team specializing in modern, scalable solutions." />
```
**Needs:** Update to match new positioning

---

## Design Guidelines Established

### Tone of Voice
- Confident, not arrogant
- Professional but human
- Quality-focused, not feature-listing
- "You're in good hands" energy

### Visual Patterns
- Two-line headlines for visual impact
- Outlined cards for differentiation
- Minimal, clean approach
- Premium feel over flashy

### What to Avoid
- Generic "we do everything" messaging
- Listing services in headlines
- Mentioning team size or "senior developers" explicitly (sounds small)
- Price positioning ("not the cheapest")
- Geographic focus in main messaging

### What to Include
- Confidence in quality
- Proof through experience (since 2020, Twikey)
- Clear who it's for
- Premium, detail-oriented positioning

---

## Research: Competitor Hero Examples

| Company | Headline | Approach |
|---------|----------|----------|
| Thoughtbot | "When the stakes are high, experience matters" | Trust/experience |
| Reaktor | "We're a global technology consultancy that designs and builds category-defining digital solutions" | What we are + aspirational |
| Futurice | "Digital transformation with measurable outcomes" | Outcome-focused |
| Metalab | "We make interfaces" | Dead simple + proof |
| Mainmatter | "Team Up With Us To Go Further!" | Partnership model |
| Linear | "Plan and build your product" | Direct action |

**Takeaway:** The most effective are either very simple about WHAT, or focus on OUTCOME/VALUE. Avoid listing services or features.

---

## Next Steps

1. [ ] Review "Who we work with" section live — adjust headline and card content
2. [ ] Decide on Core Values — rework or remove
3. [ ] Update Services sections copy
4. [ ] Review Expertise section — rebalance to highlight actual strengths
5. [ ] Update meta tags and SEO
6. [ ] Review Quote section
7. [ ] Final pass for consistency

---

## File Locations

- Main page: `/src/routes/+page.svelte`
- Components: `/src/lib/components/`
- This plan: `/WEBSITE-CONTENT-PLAN.md`
