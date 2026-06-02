MBSRN Static Migration Draft
=============================

This package is a **draft-only**, review-focused static website representation for
My Business Sucks Right Now (MBSRN). It is intended for design, content, and
workflow review by operators, admins, and other stakeholders before any
integration or deployment work.

Included files
--------------

- `index.html`
  Draft homepage that explains:
  - The core problem (weak, outdated small-business websites)
  - MBSRN as an operator-first SEO operations and migration platform
  - Key workflows (audit → recommendations → competitor insights → migration → review → publish)
  - Roles (Admins, Operators, Users)
  - Trust language around review gates, human control, and no automatic production changes
  - Primary CTAs: "Request a Website Review" and "Start an SEO Audit"

- `workflow.html`
  Draft "How It Works" style page that details:
  - End-to-end workflow and review gates
  - SEO audit details and recommendation structure
  - Competitor insights and how they influence decisions
  - Website migration planning, safety, and draft artifacts
  - CTAs that link back to the intake form on `index.html`

- `styles.css`
  Draft visual layer with:
  - Color system inspired by the mbsrn logo (green on dark grunge background)
  - Support for light and dark theme via the `data-theme` attribute on `<html>`
  - Layout and component styles (hero, cards, grids, forms, footer)
  - Simple, scannable typography and spacing

- `README-migration-notes.txt` (this file)
  Notes and safeguards explaining the intent and limits of this draft package.

Brand and media usage
---------------------

Selected brand assets are referenced only via their provided `artifact_path` values:

- `assets/images/mbsrn-fav-ico.png` – used as the site favicon.
- `assets/images/mbsrn-logo.png` – used as the primary brand logo in headers.
- `assets/images/mbsrn-logo-small.jpg` – used as a compact logo in hero cards and footer.

No additional or invented media paths are used. Other imagery described in
operator requirements is not embedded here, because corresponding assets were
not provided as selected migration media.

Theme behavior
--------------

Both `index.html` and `workflow.html` support a **light / dark theme toggle**:

- The current theme is controlled via a `data-theme` attribute on the `<html>` tag.
- A minimal inline script toggles `data-theme` between `"dark"` and `"light"`.
- `styles.css` defines color variables for both modes.

This behavior is self-contained and client-side only; no cookies or storage are
wired up in this draft.

Trust, safety, and deployment notes
-----------------------------------

- This package is purely static. There are **no** backend integrations,
  deployment pipelines, or live publishing hooks.
- The contact form in `index.html` is intentionally non-functional in this
  package and is clearly labeled as a draft-only intake form.
- Analytics placeholders are included as **commented** sections so operators
  can decide how and when to connect tools like Google Analytics 4 or Tag Manager.
- Messaging is careful not to:
  - Guarantee search rankings or specific business outcomes.
  - Claim fully automatic website publishing without review.
  - Over-promise AI accuracy or suggest that MBSRN replaces human operators.
  - Describe underlying infrastructure, CI, or deployment internals.

Operator review checklist
-------------------------

When reviewing this draft, operators and admins may want to:

1. **Validate messaging**
   - Confirm that the positioning (operator-first, small-business focused) matches
     how you want to talk about MBSRN.
   - Check that role descriptions for Admins, Operators, and Users are accurate
     and aligned with the product.

2. **Refine CTAs and flows**
   - Confirm wording and placement for:
     - "Request a Website Review"
     - "Start an SEO Audit"
     - "Review Recommendations"
     - "See How MBSRN Works"
     - "Move forward with a practical SEO plan"
     - "Explore website migration"
   - Decide how these should map to your real intake and onboarding processes.

3. **Adjust technical references**
   - Ensure mentions of Google Search Console, GA4, and Google Business Profile
     accurately reflect what the platform can incorporate today.
   - Add or remove tools as needed in the copy.

4. **Plan additional pages**
   - The operator requirements list more pages (About, Privacy Policy, Terms,
     dedicated SEO Audit / Recommendations / Competitor Insights / Migration
     pages). This draft keeps the artifact set intentionally small.
   - Once content and structure are approved, you can extend these templates
     for those additional pages.

5. **Decide on integration approach**
   - Choose how contact submissions are handled (email, CRM, ticketing, etc.).
   - Decide where this static content will live (e.g., within an existing app shell,
     a marketing site, or another reviewed environment).

Reminder
--------

This package is a **migration draft only**. It does **not**:

- Connect to live site hosting or DNS.
- Push any changes to your current website or infrastructure.
- Include CI/CD, secret management, or backend logic.

Any publishing or deployment work should be done separately, after human
review and approval of both content and behavior.