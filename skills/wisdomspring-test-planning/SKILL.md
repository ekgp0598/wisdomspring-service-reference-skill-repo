---
name: wisdomspring-test-planning
description: Plan and execute manual testing for the WisdomSpring service using bundled IA maps, bundled screen-planning markdown, and bundled policy notes. Use when Codex needs to create a test plan, derive test scenarios, run QA for WisdomSpring web or mobile or admin flows, summarize defects, or produce a Korean QA report for WisdomSpring without relying on a specific user's local folders.
---

# WisdomSpring Test Planning

## Overview

Use this skill to turn bundled WisdomSpring artifacts into a practical QA plan and execution report. Build only the minimum context needed, test with explicit assumptions, and leave a clear Korean record of scenarios, results, defects, and open questions.

If the user is new to WisdomSpring, do not jump straight into test cases. First explain the service, the major screens, the user journey, and the visual tone using the bundled newcomer and design references.

## Workflow

### 1. Fix the scope first

Classify the request into one of these modes before reading many files:

- smoke: verify major user journeys quickly
- feature: test one screen, one flow, or one requirement change
- regression: cover impacted areas around a release or policy change
- exploratory: inspect unclear behavior and surface risks
- admin-policy: compare admin rules with front behavior

If the user names screen IDs such as `HM-001`, `FD-001`, or `PR-410`, use those as the primary scope. If the user is vague, start with the baseline areas in `references/test-areas.md`.

### 2. Build context with progressive disclosure

Always read these first:

- `references/source-locations.md`
- `references/service-overview.md`
- `references/service-primer.md`
- `references/visual-design-summary.md`
- `references/ia-map.md`
- `references/screen-index.md`

Read these only when needed:

- `references/test-areas.md` for coverage planning
- `references/admin-policy-summary.md` when the request touches admin, scheduling, open states, content visibility, or edit-delete rules
- `references/report-template.md` when you need to return a structured QA artifact
- `references/expected-results.md` when you need richer expected-result patterns
- `references/example-prompts.md` when you need ready-to-copy usage examples for end users
- `references/design-image-index.md` when you need to map a screen or flow to specific design image files

Then load only the matching local artifacts for the scoped area:

- bundled IA map for menu depth, page or layer shape, and platform mapping
- bundled markdown screen definitions under `references/screen-plans/` for steps, rules, and unresolved notes
- user-provided screenshots or live-service evidence only when visual confirmation is required

Do not bulk-load the full `screen-plans` folder unless the user explicitly asks for a full-system regression.

### 2-1. Newcomer onboarding mode

When the user appears unfamiliar with WisdomSpring, answer in this order before deeper QA work:

1. what the service is
2. who it is for
3. the main user journey
4. the major screens and content types
5. the visual and interaction tone
6. the membership and admin-policy implications

Use `references/service-primer.md` and `references/visual-design-summary.md` first for this mode.

### 3. Derive test scenarios

For each scoped area, produce scenarios in this order:

1. happy path
2. boundary and validation
3. state transition
4. permission or visibility
5. platform difference
6. policy sync between admin and front

Write each case with:

- id
- objective
- preconditions
- steps
- expected result bundle
- priority

Do not collapse the expected result into a single sentence unless the flow is trivial. By default, structure the expected result bundle with these lenses:

- 정상 결과: expected success outcome
- 예외 결과: blocked or rejected outcome when preconditions are missing or invalid
- 상태 변화: UI, CTA, count, badge, route, modal, or visibility changes after the action
- 데이터 반영: whether submitted, edited, deleted, hidden, or scheduled data is reflected correctly
- 플랫폼 차이: web and mobile differences when both exist

When requirements are incomplete, mark the gap explicitly as `spec gap` instead of silently inventing behavior.

### 4. Execute and log carefully

When actually testing, record:

- actual result
- pass or fail
- evidence path or screenshot reference
- suspected cause if inferable
- whether the issue is reproducible

When a test case contains multiple expected-result branches, log which branch was exercised and which branches remain unverified.

Separate findings into:

- bug: behavior conflicts with explicit artifact or stable expectation
- spec gap: artifact is ambiguous or conflicting
- setup issue: account, data, environment, or permission problem blocks execution

### 5. Report in Korean

Default output order:

1. scope and assumptions
2. test scenarios or executed cases
3. findings ordered by severity
4. open questions
5. next recommended checks

Use concise Korean that a planner, designer, developer, or QA can all read quickly.

## Expected Result Rule

Default to richer expected results. Prefer this format when the user asks for test cases:

- `정상`: expected success path
- `예외`: invalid input, empty data, locked state, permission denial, or missing membership handling
- `상태변화`: button label, toast, badge, count, route, modal, or visibility changes
- `플랫폼`: mobile-web behavior differences

If the flow has admin dependencies, also include:

- `정책 연동`: scheduled open, duplicate-date restriction, edit-delete lock, hidden-delete distinction

If the flow has user-state dependencies, also include:

- `사용자 상태별`: logged-in or logged-out, subscribed or unsubscribed, own content or others' content

## Prompt Examples

If the user needs starter prompts, onboarding guidance, or shareable examples, use `references/example-prompts.md`. Prefer examples that include the skill name, the scope, the platform, and the expected output.

## Coverage Rules

Unless the user narrows the request, prioritize these WisdomSpring areas:

- 홈 또는 발견
- 질문피드와 답변 작성 또는 답변 상세
- 테마 상세와 학습화면
- 프로필, 노트, 댓글, 팔로우
- 멤버십 상태와 결제 관리
- 인트로, 공지사항, FAQ

Always call out web and mobile differences when both artifacts exist.

## Working Rules

- Prefer bundled WisdomSpring artifacts over generic QA theory.
- Use file names and screen IDs exactly as written in the artifacts.
- State assumptions when environment access, test accounts, or payment conditions are unknown.
- If you cannot run the service, still return a document-based test plan and risk list.
- If artifacts conflict, quote both sources briefly and mark the discrepancy as a spec gap.
- This skill is packaged to be shareable; prefer bundled references over machine-specific absolute paths.
- If the user asks what the service looks or feels like, answer from the bundled visual-design summary rather than generic design language.
