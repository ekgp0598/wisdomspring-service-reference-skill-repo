# Source Locations

Use these bundled references as the primary knowledge base for WisdomSpring testing. This skill is designed to work without a specific user's local folders.

## Core bundled references

- `references/ia-map.md`: portable IA summary
- `references/screen-index.md`: lookup table from screen ID to bundled markdown file
- `references/screen-plans/*.md`: detailed screen rules and flow notes
- `references/admin-policy-summary.md`: admin-driven business rules
- `references/service-overview.md`: service context
- `references/report-template.md`: reusable QA output format

## How to find scoped artifacts

When the user gives a screen ID, consult `references/screen-index.md` first.

Examples:

- `HM-001` -> main or discover home
- `FD-001` -> question feed
- `PR-410` -> membership status

If the user gives only a product area, map it this way:

- home or discover -> `HM-*`
- question or answer -> `FD-*`
- profile or membership -> `PR-*`
- intro or signup or login -> `IN-*`
- notice or FAQ -> `CS-*`

## Artifact roles

- `ia-map.md`: hierarchy, page or layer type, mobile-web mapping
- `screen-index.md`: quick routing to the correct bundled screen file
- `screen-plans/*.md`: behavior rules, transitions, notes, TBD items
- `admin-policy-summary.md`: validation source for scheduled open, visibility, edit-delete constraints, and duplicate restrictions

## Loading order

1. Read `ia-map.md` and `screen-index.md` to identify the target flow.
2. Read the matching bundled markdown screen definition.
3. Read `admin-policy-summary.md` only when the flow depends on open date, visibility, edit-delete, membership state, or content constraints.
4. Ask for screenshots or runtime evidence only if visual verification matters and the bundled text is insufficient.

Do not load unrelated screen files just because they sit in the same area.
