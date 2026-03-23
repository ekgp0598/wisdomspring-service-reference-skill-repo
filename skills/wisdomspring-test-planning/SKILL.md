---
name: wisdomspring-test-planning
description: Plan and execute manual testing for the WisdomSpring service using bundled IA maps, bundled screen-planning markdown, and bundled policy notes. Use when Codex needs to create a test plan, derive test scenarios, run QA for WisdomSpring web or mobile or admin flows, summarize defects, or produce a Korean QA report for WisdomSpring without relying on a specific user's local folders.
---

# WisdomSpring Test Planning

## Overview

Use this skill to turn bundled WisdomSpring artifacts into a practical QA plan and execution report. Build only the minimum context needed, test with explicit assumptions, and leave a clear Korean record of scenarios, results, defects, and open questions.

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
- `references/ia-map.md`
- `references/screen-index.md`

Read these only when needed:

- `references/test-areas.md` for coverage planning
- `references/admin-policy-summary.md` when the request touches admin, scheduling, open states, content visibility, or edit/delete rules
- `references/report-template.md` when you need to return a structured QA artifact
- `references/example-prompts.md` when you need ready-to-copy usage examples for end users

Then load only the matching local artifacts for the scoped area:

- bundled IA map for menu depth, page or layer shape, and platform mapping
- bundled markdown screen definitions under `references/screen-plans/` for steps, rules, and unresolved notes
- user-provided screenshots or live-service evidence only when visual confirmation is required

Do not bulk-load the full `screen-plans` folder unless the user explicitly asks for a full-system regression.

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
- expected result
- priority

When requirements are incomplete, mark the gap explicitly as `spec gap` instead of silently inventing behavior.

### 4. Execute and log carefully

When actually testing, record:

- actual result
- pass or fail
- evidence path or screenshot reference
- suspected cause if inferable
- whether the issue is reproducible

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

- Prefer existing local WisdomSpring artifacts over generic QA theory.
- Use file names and screen IDs exactly as written in the artifacts.
- State assumptions when environment access, test accounts, or payment conditions are unknown.
- If you cannot run the service, still return a document-based test plan and risk list.
- If artifacts conflict, quote both sources briefly and mark the discrepancy as a spec gap.
- This skill is packaged to be shareable; prefer bundled references over machine-specific absolute paths.
