# Service Primer

Use this file when the user does not know WisdomSpring yet and needs a plain-language explanation before QA planning.

## What WisdomSpring is

WisdomSpring is a subscription learning service that combines:

- a daily reflection prompt
- themed humanities content
- short-form videos and articles
- a personal record space for answers, notes, and comments
- membership-based access

The service is positioned less like a course platform with rigid curricula and more like a guided thinking and discovery product. The core promise is to help users discover new perspectives through philosophy, literature, history, and reflective writing.

## Who it is for

- users interested in humanities and reflective learning
- professionals seeking perspective, not just factual study
- people who want short, repeatable learning sessions
- users willing to record their own thoughts, not just consume content

## Main user journey

1. enter through the intro or home
2. encounter `오늘의 질문`
3. browse themes and subthemes
4. consume video or article content
5. leave an answer, note, or comment
6. revisit personal records in profile
7. manage membership for full access

## Main product areas

### Home or Discover

The home screen acts as the service storefront and orientation layer. It mixes:

- today's question
- theme cards
- currently watched content
- today's quote or sentence
- curation rails
- theme exploration

This area tells a new user what the service values: reflective prompts, curated humanities content, and repeat visits.

### Question Feed

The question feed is the community-reflection surface. Users can:

- read the current question
- write an answer
- inspect others' answers
- interact with comments and likes
- discover related content

This makes the service feel social, but in a low-noise editorial tone rather than a fast social-media tone.

### Theme Detail and Learning

Theme detail pages organize content into structured learning journeys. A theme leads into subthemes and then into individual learning assets such as videos and articles. This is the main content-consumption surface.

### Profile

The profile area is not just account management. It is also a personal archive of:

- today's question records
- notes
- comments
- saved content
- follow relationships

This makes the product feel partly like a reflective journal.

### Membership

Membership determines access and billing state. The service explicitly models:

- subscribed
- cancellation reserved
- suspended due to payment failure
- unsubscribed

These states affect both UI and what QA must verify.

## Content model

The artifacts show three main content-type behaviors:

- `TALK`: video-centric
- `BOOK`: video-centric or guided book-related learning
- `ESSAY`: article-centric

Theme and subtheme structure determine what can be registered and what should be exposed.

## Why QA matters here

WisdomSpring has many stateful rules that can confuse users if they drift from the plan:

- open scheduling
- `NEW` and `COMING SOON`
- question date restrictions
- edit-delete locks after open
- membership state transitions
- hidden versus deleted distinctions

So QA must check policy reflection, not only screen rendering.
