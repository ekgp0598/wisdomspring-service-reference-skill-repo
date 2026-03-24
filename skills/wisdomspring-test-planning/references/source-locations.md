# Source Locations

Use these bundled references as the primary knowledge base for WisdomSpring testing. This skill is designed to work without a specific user's local folders.

## Core bundled references

- `references/ia-map.md`: portable IA summary
- `references/screen-index.md`: lookup table from screen ID to bundled markdown file
- `references/screen-plans/*.md`: detailed screen rules and flow notes
- `references/admin-policy-summary.md`: admin-driven business rules
- `references/admin-planning-spec.md`: detailed admin list, field, flow, and constraint spec
- `references/design-image-index.md`: bundled design-image locator
- `references/design-images/*`: bundled screen images with screen IDs
- `references/service-overview.md`: service context
- `references/report-template.md`: reusable QA output format
- `references/expected-results.md`: richer expected-result patterns

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
- `admin-policy-summary.md`: quick validation source for scheduled open, visibility, edit-delete constraints, and duplicate restrictions
- `admin-planning-spec.md`: detailed validation source for admin list columns, detail fields, registration rules, filters, and management flows
- `design-image-index.md`: locator for bundled mobile and web image files
- `design-images/*`: visual source assets for screen explanation and visual QA support

## Loading order

1. Read `ia-map.md` and `screen-index.md` to identify the target flow.
2. Read the matching bundled markdown screen definition.
3. Read `admin-policy-summary.md` first when the flow depends on open date, visibility, edit-delete, membership state, or content constraints.
4. Read `admin-planning-spec.md` when the user asks about admin list or detail spec, registration or modal flow, field-level constraints, answer record management, or content note management.
5. Read `design-image-index.md` and the matching files under `design-images/` when the user asks what a screen looks like or when visual verification matters.
6. Ask for screenshots or runtime evidence only if the bundled text and bundled images are insufficient.

Do not load unrelated screen files just because they sit in the same area.
