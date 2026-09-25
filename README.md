# Hostline: low-fi prototype

A clickable wireframe of **Hostline**, a B2B SaaS voice AI that answers restaurant calls for multi-location groups. It is built from the *Hostline — Project Summary* (Sep 25, 2026). All data is sample data for the fictional Harbor & Hearth Group (18 locations, 2 brands, 3 regions).

It is one static file (`index.html`, plain HTML/CSS/JS with no build step), so it can be deployed to Vercel as is.

```sh
open index.html          # or: npx serve .
```

## Prototype controls (top bar)

- **View as**: HQ Ops Admin, Guest Experience Lead, Regional Manager (Coastal) or GM (Pier 21). Scope, navigation and edit rights follow the permission matrix.
- **Desktop / GM phone**: the GM phone view is mobile web with four tabs: Tonight, Follow-ups, Quick changes, Calls.
- **Simulate failed saves**: shows the error states (explicit error and Retry, never silently queued, plus a version conflict on policy publish).
- **Design notes**: yellow sticky notes that link the UI back to jobs, gaps and decisions in the brief.
- **Reset data**: restores the sample data.

## What's covered

| Area | Screens |
| --- | --- |
| Desktop | Overview (per role), Calls with call drawer, Follow-ups (call, text, reassign, resolve, 2-attempt unreachable, add answer to Knowledge), Knowledge (Policies with inheritance and lock states, Menu availability, Hours with split-hours warning, Change log), Locations (sortable comparison and location detail with "where calls fail"), Reports, Settings (Voice & greeting, Routing & escalation with transfer-loop check, Team & permissions, Integrations) |
| GM phone | Tonight, Mark sold out (linked items, HQ-managed block, already off in POS, failed save), Pause orders, Close early, follow-up detail, simulated push alert, Undo |

## Core flows to try

1. **HQ changes a brand policy**: Knowledge → Policies → Large party threshold → Edit brand value. The impact panel shows the overrides, you choose to keep, reset or decide per location, then resolve the routing-rule conflict and publish. Undo is available.
2. **A call creates a follow-up and the GM resolves it on mobile**: GM phone → Simulate incoming alert → tap the banner → Call guest, then choose No answer or Resolve with an outcome.
3. **GM marks an item sold out mid-shift**: GM phone → Mark sold out → search "salmon". It then shows on desktop as a temporary override (Knowledge → Menu, scoped to Pier 21).
