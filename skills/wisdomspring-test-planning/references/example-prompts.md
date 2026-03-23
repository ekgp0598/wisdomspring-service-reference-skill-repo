# Example Prompts

Use these prompts as copy-paste starters when sharing the skill with other people. The safest form is to mention the skill name explicitly.

## 1. 빠른 스모크 테스트

```text
$wisdomspring-test-planning 위즈덤스프링 전체 서비스 기준으로 오늘 바로 돌릴 수 있는 스모크 테스트 시나리오를 작성해줘. 홈, 질문피드, 테마 상세, 학습화면, 프로필, 멤버십을 포함하고 우선순위와 기대결과를 표로 정리해줘.
```

## 2. 특정 화면 테스트 설계

```text
$wisdomspring-test-planning HM-001 메인(발견) 화면만 기준으로 웹/모바일 공통 테스트 케이스를 작성해줘. 오늘의 질문, 테마 카드, 큐레이션, 전체보기 진입을 포함하고 spec gap 후보도 따로 정리해줘.
```

## 3. 질문피드와 답변 흐름 점검

```text
$wisdomspring-test-planning FD-001, FD-B030, FD-010 흐름 기준으로 질문피드 진입부터 답변 작성, 답변 상세 확인까지 QA 시나리오를 작성해줘. 정상 흐름, 예외 흐름, 상태 전이를 나눠서 정리해줘.
```

## 4. 멤버십 정책 회귀 테스트

```text
$wisdomspring-test-planning PR-410 멤버십 정보 화면 기준으로 구독중, 해지 예약, 사용정지 상태를 비교하는 회귀 테스트 항목을 정리해줘. 각 상태의 CTA와 결제 관리 연결도 확인 항목에 넣어줘.
```

## 5. Admin 정책 싱크 검토

```text
$wisdomspring-test-planning 위즈덤스프링 admin 정책 기준으로 front 동작과 충돌할 수 있는 테스트 포인트를 정리해줘. NEW, COMING SOON, 날짜 중복 제한, 수정/삭제 제한 중심으로 리스크 목록을 만들어줘.
```

## 6. 실행 결과 리포트 요청

```text
$wisdomspring-test-planning HM-001과 FD-001을 테스트했다고 가정하고, QA 결과 보고서 형식으로 정리해줘. 테스트 범위, 실행 결과, 발견사항, 오픈 이슈, 다음 확인 권장사항 순서로 한국어 문서 형태로 작성해줘.
```

## 7. 탐색형 QA 요청

```text
$wisdomspring-test-planning 위즈덤스프링에서 지금 문서만 보고도 결함 가능성이 높은 영역을 탐색형 QA 관점으로 뽑아줘. 근거가 되는 화면 ID와 정책 충돌 가능성도 같이 적어줘.
```

## 8. 사용자 제공 증빙 기반 분석

```text
$wisdomspring-test-planning 내가 올리는 스크린샷과 함께 HM-010 테마 상세 화면을 검토해줘. 문서 기준 기대동작과 실제 화면 차이를 비교해서 bug, spec gap, 확인 필요 항목으로 나눠줘.
```

## Writing guidance

- Prefer Korean output unless the user asks otherwise.
- Include screen IDs whenever possible.
- If the user wants execution-ready QA, ask for platform and environment only when the assumption would be risky.
- If live execution is impossible, return a document-based test plan instead of stopping.
