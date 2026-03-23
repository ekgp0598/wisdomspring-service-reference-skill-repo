# Admin Policy Summary

Use this file when testing WisdomSpring behavior that depends on admin configuration or lifecycle rules.

## Theme management

- Expose themes on the front by open date.
- Keep `NEW` state until the next theme opens.
- Use open date, not registration date, for admin list search and inspection.
- Allow 1 to 10 thumbnails per theme.
- Expose the thumbnail with the latest valid exposure date as of today.
- Restrict subtheme content type:
  - `TALK`, `BOOK`, `ETC-영상` accept video content only.
  - `ESSAY`, `ETC-아티클` accept article content only.
- Show `COMING SOON` before open.
- Show `NEW` for one week after open.
- Reapply state rules when the open schedule changes later.
- Block theme exposure on when the subtheme has no content.
- Block duplicate content registration across themes or subthemes.

## Today's question

- Block duplicate registration for the same date.
- Block registration for past dates.
- Block edit and delete for already-opened past questions.

## Today's content

- Manage today's quote or sentence together with today's content, not as a separate feature.
- Block duplicate registration for the same date.
- Allow registration for past dates.
- Block edit and delete for already-opened content and quote.

## Answer records

- Keep hidden answers visible in the admin management list.
- Hide deleted answers from the admin management list.

## Content notes

- Treat note deletion as hidden-state processing, not physical deletion.
- Hide deleted notes from the admin note list.

## Testing implication

When a front behavior conflicts with these rules, mark it as a likely bug. When the local screen artifact conflicts with this file, mark it as a spec gap and report both sources.
