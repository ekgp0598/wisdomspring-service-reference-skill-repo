# IA Map

This file is a portable text version of the core WisdomSpring IA needed for QA planning. Use it instead of an external workbook.

## IA conventions

- `M-...`: mobile screen or layer ID
- `W-...`: web screen or layer ID
- `페이지`: page
- `팝업`, `레이어`, `바텀시트`: overlay or modal interaction
- common IDs such as `HM-001`, `FD-001`, `PR-410` describe the shared feature regardless of platform

## Home and theme flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-IN-001` |  | 1 | 인트로 | 페이지 |
| `M-HM-001` | `W-HM-001` | 1 | 홈(발견) | 페이지 |
| `M-HM-B002` | `W-HM-P002` | 2 | 테마 전체보기 | 바텀시트/팝업 |
| `M-HM-010` | `W-HM-010` | 2 | 테마 상세 | 페이지 |
| `M-HM-020` | `W-HM-020` | 3 | 학습화면-영상 | 페이지 |
| `M-HM-021` | `W-HM-021` | 3 | 학습화면-아티클 | 페이지 |
| `M-HM-B022` | `W-HM-P022` | 4 | 전체회차 | 바텀시트/팝업 |
| `M-HM-B023` |  | 4 | 노트 | 바텀시트 |
|  | `W-HM-P024` | 4 | 노트 댓글 | 팝업 |
| `M-SH-010` | `W-SH-010` | 2 | 검색결과 | 팝업/레이어 |

## Question and answer flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-FD-001` | `W-FD-001` | 1 | 질문피드 | 페이지 |
| `M-FD-B030` | `W-FD-M030` | 2 | 답변쓰기 | 레이어 |
| `M-FD-010` | `W-FD-010` | 2 | 답변 상세 | 페이지 |
| `M-FD-020` | `W-FD-020` | 3 | 오늘의 콘텐츠 | 콘텐츠 |

## Profile and membership flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-PR-001` | `W-PR-001` | 1 | 프로필 | 콘텐츠 |
| `M-PR-P110` | `W-PR-P110` | 3 | 프로필 수정 | 팝업 |
| `M-PR-120` | `W-PR-120` | 4 | 생각기록-오늘의 질문 | 탭 |
| `M-PR-121` | `W-PR-121` | 4 | 노트 | 탭 |
| `M-PR-122` | `W-PR-122` | 4 | 댓글 | 탭 |
| `M-PR-130` | `W-PR-130` | 3 | 관심 콘텐츠 | 탭 |
| `M-PR-140` | `W-PR-140` | 3 | 팔로우 | 탭 |
| `M-PR-210` | `W-PR-210` | 2 | 회원정보(설정) | 페이지 |
| `M-PR-211` | `W-PR-211` | 3 | 비밀번호 확인 | 페이지 |
| `M-PR-212` | `W-PR-212` | 3 | 회원정보 변경 | 페이지 |
| `M-PR-213` | `W-PR-213` | 3 | 이벤트/혜택 알림 | 페이지 |
| `M-PR-310` | `W-PR-310` | 2 | 결제관리 | 페이지 |
| `M-PR-410` | `W-PR-410` | 2 | 멤버십 정보 | 페이지 |
| `M-PR-420` | `W-PR-420` | 3 | 멤버십 가입 | 페이지 |
| `M-PR-421` | `W-PR-421` | 4 | 정보 입력 및 결제수단 포함 | 페이지 |
| `M-PR-422` | `W-PR-422` | 5 | 상품 결제 | 페이지 |
| `M-PR-P423` | `W-PR-P423` | 5 | NHN KCP 결제 | 팝업 |

## Auth and common information flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-IN-010` | `W-IN-010` | 1 | 로그인 | 페이지 |
| `M-IN-011` | `W-IN-011` | 2 | 아이디 찾기 | 탭 |
| `M-IN-012` | `W-IN-012` | 3 | 비밀번호 찾기 | 탭 |
| `M-IN-020` | `W-IN-020` | 1 | 회원가입-일반회원가입 | 페이지 |
| `M-IN-021` | `W-IN-021` | 4 | 약관 동의 | 페이지 |
| `M-IN-022` | `W-IN-022` | 4 | 회원가입정보입력 | 페이지 |
| `M-IN-023` | `W-IN-023` | 4 | 회원가입완료 | 페이지 |
| `M-CS-010` | `W-CS-010` | 1 | About(멤버십 소개) | 페이지 |
| `M-CS-011` | `W-CS-011` | 2 | 1개월 무료 체험 | 페이지 |
| `M-CS-020` | `W-CS-020` | 1 | 공지사항 | 페이지 |
| `M-CS-030` | `W-CS-030` | 1 | 이용약관 | 링크 |
| `M-CS-040` | `W-CS-040` | 1 | 개인정보처리방침 | 링크 |
| `M-CS-050` | `W-CS-050` | 1 | 자주묻는질문(FAQ) | 페이지 |
| `M-ST-010` |  | 1 | 앱푸시설정 | 페이지 |

## QA implications

- `HM` 영역은 발견, 테마, 학습 탐색의 중심이다.
- `FD` 영역은 질문, 답변 작성, 답변 상세의 중심이다.
- `PR` 영역은 프로필, 구독 상태, 설정, 결제 흐름의 중심이다.
- `IN`, `CS`, `ST` 영역은 첫 방문, 계정, 공지, FAQ, 알림 설정 검증에 사용한다.
- Depth가 깊어질수록 진입 경로와 상태 전달 검증이 중요하다.
