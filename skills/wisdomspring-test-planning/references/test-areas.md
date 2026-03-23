# Test Areas

Use this baseline when the user asks for a broad or initial WisdomSpring test plan.

## 1. 홈 or 발견

Check:

- today's question exposure and CTA behavior
- theme-card ordering, badges, and open-state labels
- recommendation sections by content type
- transition from home to theme detail, content, and full-list layers
- mobile versus web layout differences

High risk:

- wrong theme ordering or badge state
- mismatched CTA target by platform
- recommendation logic inconsistent with content type

## 2. 질문피드 and 답변

Check:

- daily-question fixation and collapsed header behavior
- write-answer entry and completion state change
- answer list paging or load-more behavior
- answer detail, likes, comments, privacy or visibility
- older-question behavior versus latest seven days

High risk:

- wrong write or view state after submitting
- sticky header state mismatch
- answer counts or pagination inconsistencies

## 3. 테마 상세 and 학습

Check:

- theme to subtheme to learning-content path
- video versus article entry point
- all-episode layer or popup behavior
- note or comment side flows if present

High risk:

- wrong content-type routing
- progress or episode state mismatch
- missing open-state gating

## 4. 프로필, 노트, 댓글, 팔로우

Check:

- profile tabs or sections
- own content versus others' content
- note and comment list rendering
- follower and following views
- account settings and notification toggles

High risk:

- identity or ownership confusion
- hidden or deleted content still visible
- count mismatches between list and detail

## 5. 멤버십 and 결제 관리

Check:

- subscribed state
- cancellation reserved state
- suspended state due to repeated payment failure
- CTA routing to payment management or restore flows

High risk:

- wrong state card or title
- recovery CTA missing
- payment-failure threshold handled incorrectly

## 6. 공통 안내 영역

Check:

- intro
- notices
- FAQ
- empty states

High risk:

- broken first-visit path
- inconsistent empty-state copy or actions

## 7. Admin-policy sync

Check:

- scheduled open date
- `NEW` and `COMING SOON` state
- duplicate-date restrictions
- edit and delete lock after open
- hidden versus deleted behavior

High risk:

- admin rules documented but front does not reflect them
- content or question schedule allows invalid dates
- deleted data still exposed
