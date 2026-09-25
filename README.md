# Hostline: low-fi prototype (admin-only MVP)

A clickable wireframe of **Hostline**, a B2B SaaS voice AI that answers restaurant calls for multi-location groups. This version is **admin-only**: one person (Alex Moreno, admin at the fictional Harbor & Hearth Group) sets up the workspace, launches restaurants and manages the phone channel. GMs still own follow-ups, but only as data: they get SMS and don't sign in.

The structure follows the **Hostline MVP — IA map (admin only)** in FigJam. All data is sample data: 18 locations, 2 brands (Harbor Kitchen, Hearth Pizza) and 3 regions.

It is one static file (`index.html`, plain HTML/CSS/JS with no build step), in a single white theme, so it can be deployed to Vercel as is.

## Prototype controls (top bar)

- **Start from**: *Established workspace* (13 live, 2 in pilot, 3 setting up), *New workspace (email)* (admin onboarding and empty states) or *Log in*.
- **Simulate failed saves**: every popup and save goes from loading to an error state with Try again.
- **Design notes**: sticky notes that link screens to the IA map.
- **Reset**: restores the sample data.

## IA map coverage

| IA node | In the prototype |
| --- | --- |
| Admin onboarding | Email "workspace ready" → Create account → Setup checklist: 1) Review structure (+ Edit location popup) 2) Voice & greeting 3) Brand policies with lock state 4) Routing & escalations 5) Invite team (popup) → Finish → Locations. Log in and reset password |
| Global elements | Scope switcher (All / Region / Location), Notifications drawer, Profile / Log out menu |
| Overview | Key metrics, Needs attention, Rollout status (Setting up · Pilot · Live) |
| Calls | List with filters → Call detail drawer with the linked order, reservation or lead |
| Follow-ups | Open · Overdue · Closed → detail panel → Resolve with outcome, Reassign and Close without action popups |
| Knowledge | Policies (brand value → location override, Review impact and apply popup) · Menu (Sold out and item note popups) · Reservations (max party, booking window, table duration, Close date/slot popup) · Hours (Edit hours popup) · Special events (Add event popup) · Change log |
| Locations | List with metrics and status → location page (Overview · Calls · Follow-ups · Knowledge). Launch restaurant: Hours → Menu → Reservations → Test call → Start pilot popup → Go live popup |
| Reports | Period and location filters; Calls and outcomes, AI resolution rate, Revenue from calls, Follow-up performance, Escalations, Location comparison, Unanswered questions; Export CSV popup |
| Settings | Voice & greeting (Listen to sample popup) · Routing & escalations (Edit rule and Test transfer popups, transfer-loop check) · Integrations (read-only, connection error popup) · Team (Invite, Change role, Remove) · Phone numbers (read-only) · Profile & notifications |

Every popup has a form state, then loading, then success or error.
