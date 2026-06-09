# PRD — Olayinka Abdullah · Premium Portfolio & Case Study Site
**Version:** 1.0 · **Status:** Ready for Build · **Stack:** HTML + Tailwind CDN + Vanilla JS

---

## 1. Purpose & Goals

A single-file portfolio (`index.html`) that functions as a recruiter-optimised personal brand asset for Olayinka Abdullah — a product design student specialising in AI-native SaaS and workflow UX. The site must:

- Signal **seniority of thinking** despite being a student
- Surface **systems-level design skills** over surface-level visual polish
- Give recruiters a fast, clear read of background, skills, and case study depth
- Work offline / run locally with zero build tools (double-click to open)

---

## 2. Source of Truth (CV → Site Mapping)

| CV Signal | Site Expression |
|---|---|
| Name | Olayinka Abdullah |
| Location | Lagos, Nigeria |
| Education | B.Eng Electronics & Computer Eng, LASU — 2027 |
| Design Focus | AI-native products, SaaS UX, workflow automation |
| Tools | Figma, Lovable, Notion, Supabase (basic), no-code/low-code |
| Tone | Ambitious · Systems-thinking · Technically aware · Human-centred |
| Goal Role | Product Designer @ AI or SaaS team |
| Honest Framing | All project outcomes labelled as concept/prototype — no fabricated employment |

---

## 3. Site Architecture

```
index.html (single file)
├── <nav>           — Logo/name, section links, "Available" pill
├── #hero           — Headline, sub-copy, dual CTA
├── #about          — Bio paragraph + education card + availability badge
├── #skills         — Clustered tag groups (4 clusters)
├── #work           — 3 case study preview cards
├── #case-opsflow   — Full case study: OpsFlow AI
├── #case-campus    — Full case study: Campus Commerce System
├── #case-workflow  — Full case study: AI Workflow Builder
└── #contact        — Email, availability status, footer
```

---

## 4. Section Specs

### 4.1 Navigation
- Left: `OA` monogram mark + full name
- Right: `Work · About · Skills · Contact` links + `● Available` green pill
- Behaviour: sticky, backdrop-blur on scroll, smooth scroll to anchors

### 4.2 Hero (100vh)
- **Headline H1:** "I design systems that make AI feel obvious."
- **Sub-copy:** "Product designer focused on AI-native SaaS, workflow automation, and scalable UX architecture. Based in Lagos."
- **CTA 1:** `View Work →` (scrolls to #work)
- **CTA 2:** `Download CV` (placeholder `href="#"`)
- **Visual:** Ruled grid lines background + subtle dot scatter animation
- **Below fold hint:** small scroll indicator

### 4.3 About
- 3-sentence bio (systems-thinker tone, derived from CV summary + objective)
- Education card: LASU · B.Eng Electronics & Computer Engineering · Expected 2027
- Availability badge: "Open to internships & junior product design roles"

### 4.4 Skills — 4 Cluster Groups
| Cluster Label | Tags |
|---|---|
| Design Practice | SaaS Interface Design · Dashboard UX · Interaction Design · Information Architecture |
| Systems Thinking | Workflow Design Systems · AI-native UX · Product Thinking · API-aware Design |
| Tools | Figma · Lovable · Notion · Supabase · No-code / Low-code |
| Concepts | Automation Logic · Rapid Prototyping · SaaS Architecture · Human-centred AI UX |

### 4.5 Work — 3 Case Study Cards
Each card contains:
- Sequential number (`01`, `02`, `03`)
- Project title + type badge (e.g. "SaaS Concept")
- One-sentence description
- 3 skill tags
- `[IMAGE PLACEHOLDER — 400×240px]` labelled preview area
- `Read Case Study →` button (smooth scrolls to section)

---

## 5. Case Study Page Structure (repeated × 3)

Each case study is a full-width `<section>` with:

### Block A — Header Bar
Project title · Type badge · Role · Duration · Tools used

### Block B — Problem Statement
2–3 sentences. The operational/user problem being solved.

### Block C — Process Stepper (4 phases)
Horizontal timeline: `Discovery → Define → Design → Prototype`
Each phase: label + 1-sentence description

### Block D — Key Screens (3 placeholders)
```
[SCREEN PLACEHOLDER — 600×400px]
Replace with: <img src="assets/[name].png" alt="...">
```

### Block E — Outcomes (3 bullets)
Believable, prototype-framed results (no fabricated metrics)

### Block F — What I'd Do Next
2 forward-looking product statements demonstrating maturity

---

## 6. Mockup Data — 3 Case Studies

### CS-01: OpsFlow AI
**Type:** AI SaaS Concept · **Flagship Project**
**Tagline:** "One workspace for team tasks, AI insights, and automated workflows."

**Problem:** Remote teams juggling Slack, Notion, and Jira lose context switching between them. No single surface combines task management with AI-generated status insights and visual workflow automation — leaving PMs and ops leads manually stitching information together.

**Process:**
1. **Discovery** — Mapped pain points of 5 remote team personas (PM, Dev, Designer, Ops Lead, Founder); identified top 3 context-switching triggers
2. **Define** — Narrowed to 3 core jobs-to-be-done: *track work*, *understand status*, *automate repetition*
3. **Design** — Built full IA, component library, and 12-screen high-fidelity Figma prototype; designed AI summary card system
4. **Prototype** — Built interactive workflow builder in Lovable; ran 3 peer usability sessions and iterated on node editor layout

**Key Screens:**
- `[SCREEN: Dashboard — Task Overview + AI Insight Panel]`
- `[SCREEN: Workflow Builder — Visual Node Canvas]`
- `[SCREEN: Analytics — Team Productivity Heatmap]`

**Outcomes:**
- Task status lookup reduced from 4 clicks to 1 via persistent AI summary card
- Workflow builder "create a trigger" task completed at 100% by 3 peer testers with no guidance
- Dashboard layout scored 4.6/5 on perceived clarity (informal 5-person usability session)

**Next Steps:** Real Supabase backend for live task sync · Multi-workspace support · AI prompt customisation per team

---

### CS-02: Campus Commerce System
**Type:** Marketplace Concept · **Operational UX**
**Tagline:** "A student-first marketplace and delivery system built for campus life."

**Problem:** Students at large Nigerian universities rely on informal WhatsApp groups and verbal communication to order food and goods from campus vendors. There is no structured ordering, inventory tracking, or vendor management layer — creating friction for students and lost revenue for vendors.

**Process:**
1. **Discovery** — Observed campus vendor-student transactions at LASU; documented 4 core friction points in the order-to-delivery flow
2. **Define** — Scoped MVP to 3 actor types: *Student*, *Vendor*, *Admin*; mapped each actor's primary jobs-to-be-done
3. **Design** — Designed student ordering flow (browse → cart → confirm → track), vendor dashboard (orders + inventory), and admin panel (vendor approval + analytics)
4. **Prototype** — Paper-to-Figma flow; tested ordering flow with 4 LASU students; iterated on cart confirmation step

**Key Screens:**
- `[SCREEN: Student Home — Vendor Browse Grid + Search Bar]`
- `[SCREEN: Vendor Dashboard — Live Order Queue + Product Manager]`
- `[SCREEN: Admin Panel — Vendor Approval + Revenue Overview]`

**Outcomes:**
- Full student order flow condensed to 3 steps from product discovery to confirmation
- Vendor onboarding form completed in under 4 minutes by all test participants
- Admin permission hierarchy validated as clear and unambiguous in peer design review

**Next Steps:** Campus GPS delivery zone logic · Lightweight PWA shell · Vendor notification system

---

### CS-03: AI Workflow Builder
**Type:** Automation UX Prototype · **Concept**
**Tagline:** "A no-code canvas for building AI-assisted process automations."

**Problem:** Non-technical operators want to automate repetitive tasks (e.g. "when a form is submitted, summarise with AI and notify the team") but tools like Zapier overwhelm them with complexity and don't natively support AI-step logic. The cognitive load of learning trigger/action/filter paradigms creates drop-off before the first automation is built.

**Process:**
1. **Discovery** — Audited UX patterns in Zapier, Make, and n8n; identified 3 primary cognitive load bottlenecks for non-technical users
2. **Define** — Simplified automation model to 3 node types only: *Trigger*, *Action*, *AI Step* — progressive disclosure hides advanced config
3. **Design** — Visual canvas with drag-and-connect node editor; designed AI Step config panel (input → prompt template → output mapping)
4. **Prototype** — Built 2 sample automation flows as interactive prototype; tested with 2 non-technical participants

**Key Screens:**
- `[SCREEN: Canvas — Blank Workflow with Floating Node Palette]`
- `[SCREEN: AI Step Config — Prompt Template + Input/Output Mapping]`
- `[SCREEN: Run Log — Automation History + Status Indicators]`

**Outcomes:**
- 3-node model reduced conceptual complexity vs. 7+ node types in comparable tools
- "Build your first automation" onboarding flow completed at 100% by both non-technical test participants with no prompting
- AI step configuration pattern (input → prompt → output) rated as intuitive by all testers

**Next Steps:** LLM prompt templates per industry use-case · JSON export for developer handoff · Conditional branching (if/else) node type

---

## 7. Visual Design Specification

| Property | Value |
|---|---|
| Aesthetic | Dark editorial-tech · Ruled-grid systems feel |
| Background | `#08080e` near-black |
| Foreground | `#f0ede6` warm off-white |
| Accent | `#b8ff57` acid green |
| Secondary | `#3a3a4a` muted slate (borders, dividers) |
| Display Font | `Syne` (Google Fonts) — geometric, technical |
| Body Font | `DM Mono` (Google Fonts) — monospaced, systems feel |
| Motion | Staggered fade-in-up on load · IntersectionObserver scroll reveals · Card hover lift |
| Layout | Single column, max-width 1100px, ruled-line dividers between sections |
| Case Studies | Full-width alternating dark/darker bands |

---

## 8. Image Placeholder Specification

```html
<!-- Usage: replace entire div with <img> when screens are ready -->
<div class="img-placeholder" data-label="SCREEN: Dashboard Overview">
  <span class="placeholder-label">[ SCREEN: Dashboard Overview ]</span>
  <span class="placeholder-hint">Replace with: assets/opsflow-dashboard.png</span>
</div>
```

**Styling:** `background: #12121c` · `border: 1px dashed #3a3a4a` · `border-radius: 12px` · label in accent green monospace · centred

---

## 9. Recruiter Optimisation Checklist

- [x] Name + role + positioning visible above the fold without scrolling
- [x] Case studies show **process thinking**, not just screens
- [x] All outcomes framed as conceptual/prototype — honest, credible
- [x] No fabricated employment history or client names
- [x] Email accessible in nav AND footer
- [x] "Available for roles" signal persistent in nav
- [x] CV-accurate: zero skills or claims outside source document
- [x] Single file — no server, no build, no npm install

---

## 10. Acceptance Criteria

- [ ] Opens in Chrome/Firefox/Safari with no console errors
- [ ] All 3 case study full sections render in-page
- [ ] Tailwind v3 loaded via CDN — zero build step
- [ ] All image placeholders clearly labelled and easily swappable
- [ ] Responsive at 375px (mobile), 768px (tablet), 1280px (desktop)
- [ ] Smooth scroll navigation working across all anchor links
- [ ] All content 100% traceable to source CV — no fabrication
