# Service Overview

WisdomSpring is a learning service centered on discovery, reflection, themed content, and membership-based access. The bundled artifacts in this skill cover both mobile and web flows, plus admin policies that affect what appears on the front.

## Main functional areas

- 홈 or 발견: daily question, theme cards, recommendations, current learning content, and navigation entry points
- 질문피드: daily question exposure, answer writing, answer detail, list behavior, and content recommendations
- 테마 탐색: theme detail, subtheme progression, video or article learning entry, and content navigation
- 프로필: thought records, notes, comments, follow relationships, and account settings
- 멤버십: current subscription state, cancellation reservation, payment-management entry, and recovery from payment failure
- 공통: intro, notices, FAQ, content visibility, and open-state badges

## Platform structure

- Mobile artifacts typically use `M-...`
- Web artifacts typically use `W-...`
- Common screen IDs appear in markdown documents without the platform prefix

## Typical high-value journeys

- first visit to intro and home
- browse today's question and write an answer
- move from home to theme detail and into learning content
- inspect profile, note, and comment areas
- review membership state and payment-related CTAs
- confirm admin-driven states such as `NEW`, `COMING SOON`, content visibility, and edit restrictions

## Testing stance

Prefer service-specific verification over generic UI checks. The core risk is usually not component polish, but mismatch between planned policy, exposed state, and platform-specific behavior.
