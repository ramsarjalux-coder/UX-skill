---
name: ux-audit
description: Conduct structured UX audits and heuristic evaluations of digital products. Use this skill whenever the user wants to review, critique, or evaluate an existing UI/UX design, app, website, or screen. Trigger when the user says things like "audit this design", "review my app's UX", "find UX problems", "heuristic evaluation", "what's wrong with this interface", "critique this screen", or uploads screenshots for feedback. Also trigger when the user asks about accessibility, usability issues, cognitive load, or information architecture problems in an existing product.
---

# UX Audit Skill

Conduct thorough, structured UX audits using Nielsen's 10 Heuristics plus modern UX principles. Deliver actionable, prioritized findings.

## Audit Framework

### Phase 1 — Gather Context
Before auditing, clarify:
- **Product type**: Web app, mobile app, desktop, e-commerce, SaaS, etc.
- **Target users**: Who uses this? What's their tech literacy level?
- **Primary tasks**: What are users trying to accomplish?
- **Scope**: Full audit or focused area (onboarding, checkout, navigation, etc.)?

If the user uploads screenshots or shares a URL, proceed directly to the audit.

---

### Phase 2 — Heuristic Evaluation (Nielsen's 10)

Evaluate against each heuristic. For each one, note: **Pass / Partial / Fail** + specific observations.

| # | Heuristic | Key Questions |
|---|-----------|---------------|
| 1 | Visibility of system status | Does the UI always communicate what's happening? Loading states, progress, confirmations? |
| 2 | Match between system and real world | Does language match the user's mental model? Are metaphors intuitive? |
| 3 | User control and freedom | Can users undo, go back, cancel? Are exits clearly marked? |
| 4 | Consistency and standards | Is the UI internally consistent? Does it follow platform conventions? |
| 5 | Error prevention | Does the UI prevent errors before they happen? Smart defaults, constraints, confirmation dialogs? |
| 6 | Recognition over recall | Can users recognize options vs. memorize them? Are labels visible? |
| 7 | Flexibility and efficiency | Are there shortcuts for expert users? Can workflows be accelerated? |
| 8 | Aesthetic and minimalist design | Is irrelevant information removed? Is visual hierarchy clear? |
| 9 | Help users recover from errors | Are error messages plain-language and constructive? |
| 10 | Help and documentation | Is contextual help available when needed? Is it easy to find? |

---

### Phase 3 — Additional Audit Dimensions

**Accessibility (WCAG 2.1)**
- Color contrast ratios (minimum 4.5:1 for normal text)
- Touch targets ≥ 44×44px (mobile)
- Keyboard navigability
- Alt text, ARIA labels
- Focus states visible

**Information Architecture**
- Navigation clarity and depth
- Labeling consistency
- Search functionality
- Wayfinding / breadcrumbs

**Visual Hierarchy & Cognitive Load**
- F-pattern / Z-pattern reading flow
- Chunking of information
- Use of whitespace
- Typography hierarchy (H1 → H2 → body)

**Mobile / Responsive**
- Thumb-zone optimization
- Tap target sizing
- Content reflow at breakpoints
- Swipe gestures and affordances

---

### Phase 4 — Severity Ratings

Rate every finding using this scale:

| Severity | Label | Description |
|----------|-------|-------------|
| 🔴 | Critical | Blocks task completion or causes significant errors |
| 🟠 | Major | Causes user frustration, significant slowdown |
| 🟡 | Minor | Small friction, workarounds exist |
| 🟢 | Suggestion | Enhancement, not a problem |

---

### Phase 5 — Output Format

Structure the audit report as:

```
## UX Audit: [Product/Screen Name]

### Executive Summary
[2–3 sentences on overall UX health, biggest wins, biggest issues]

### Critical Findings 🔴
1. [Issue title]
   - **Where**: [Screen/component]
   - **Problem**: [What's wrong and why it matters]
   - **Recommendation**: [Specific fix]

### Major Findings 🟠
...

### Minor Findings 🟡
...

### Suggestions 🟢
...

### Positive Observations ✅
[What the design does well — always include this]

### Priority Fix List
[Top 5 things to fix first, ranked]
```

---

## Tips for Great Audits

- **Be specific**: Reference exact UI elements, not vague areas
- **Cite the heuristic**: Helps developers/PMs understand the why
- **Always include positives**: Balanced feedback builds trust
- **Suggest, don't prescribe**: Offer 1–2 options per recommendation, not mandates
- **Use "the user" language**: Frame problems from the user's perspective, not your opinion

---

## Quick Reference: Common UX Red Flags

- No empty states designed
- Form errors only shown on submit (not inline)
- Disabled buttons with no explanation why
- Modals without escape (no X, no Esc, no overlay click)
- Infinite scroll with no way to return to position
- Jargon or acronyms unexplained
- CTAs that say "Click here" or "Submit"
- Mobile layouts that require horizontal scrolling
- Low-contrast text on decorative backgrounds
- Actions with no confirmation (especially destructive ones)
