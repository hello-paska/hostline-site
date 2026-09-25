# Hostline: low-fi prototype

A clickable wireframe of **Hostline**, a B2B SaaS voice AI that answers restaurant calls for multi-location groups. Its structure follows the **Hostline MVP IA map** (FigJam), and its content comes from the *Hostline — Project Summary*. All data is sample data for the fictional Harbor & Hearth Group (18 locations, 2 brands, 3 regions).

It is one static file (`index.html`, plain HTML/CSS/JS with no build step), so it can be deployed to Vercel as is. The design is a single white theme.

```sh
open index.html          # or: npx serve .
```

## Prototype controls (top bar)

- **Start from**: Signed in, Invite email → HQ, Invite email → GM, or Log in.
- **View as**: HQ Ops Admin, Guest Experience Lead, Regional Manager (Coastal) or General Manager (Pier 21). Scope, navigation and edit rights follow the permission matrix.
- **Phone frame**: the same product at 390px wide. GMs use Hostline as mobile web, so there is no separate app.
- **Simulate failed saves**: shows the error states (an explicit error with Retry, and a version conflict when applying a policy).
- **Design notes**: yellow sticky notes that link screens to the IA map and to the jobs, gaps and decisions in the brief.

## IA map coverage

| IA node | In the prototype |
| --- | --- |
| Onboarding & access | Invite email → Create account → Welcome by role → HQ rollout status, or GM launch checklist (confirm hours, confirm menu, local answers, test call) → Confirm go live popup. Log in, and reset password |
| Global elements | Scope switcher menu, Notifications drawer, Profile / Log out menu |
| Overview | Key metrics, Needs attention, GM quick actions (Mark sold out, Pause orders and Close early popups) |
| Calls | Call list with filters → Call detail drawer |
| Follow-ups | Open / Overdue / Mine / Closed tabs → Follow-up detail panel → Resolve with outcome, Reassign, and Close without action popups |
| Knowledge | Policies (detail panel with caller preview → Review impact and apply popup, Request change popup), Menu availability (Mark sold out popup), Hours (Edit hours popup), Change log |
| Locations | Location list with metrics → location page with Overview / Calls / Follow-ups / Knowledge tabs; Launch status tab |
| Reports | Period and Locations filters; Calls and outcomes, AI resolution rate, Revenue from calls, Follow-up performance, Location comparison, Unanswered questions; Export CSV popup |
| Settings | Team (Invite member, Change role and Remove member popups), Phone numbers (transfer line with loop check), Profile and notifications |
