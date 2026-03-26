# IA Map

This file is a portable text version of the core WisdomSpring IA needed for QA planning.

## IA conventions

- `M-...`: mobile screen or layer ID
- `W-...`: web screen or layer ID
- `page`: full page
- `popup`, `modal`, `bottom sheet`, `drawer`: overlay interaction
- shared IDs such as `HM-001`, `FD-001`, `PR-410` describe the same feature family across platforms

## Home and theme flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-IN-001` |  | 1 | 인트로 | page |
| `M-HM-001` | `W-HM-001` | 1 | 홈(발견) | page |
| `M-HM-030` | `W-HM-030` | 1 | 상단 메뉴 | drawer / side drawer |
| `M-HM-B002` | `W-HM-P002` | 2 | 테마 전체보기 | bottom sheet / popup |
| `M-HM-010` | `W-HM-010` | 2 | 테마 상세 | page |
| `M-HM-020` | `W-HM-020` | 3 | 학습화면-영상 | page |
| `M-HM-021` | `W-HM-021` | 3 | 학습화면-아티클 | page |
| `M-HM-B022` | `W-HM-P022` | 4 | 전체회차 | bottom sheet / popup |
| `M-HM-B023` |  | 4 | 노트 | bottom sheet |
|  | `W-HM-P024` | 4 | 노트 댓글 | popup |
| `M-SH-010` | `W-SH-010` | 2 | 검색결과 | popup / layer |

## Question and answer flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-FD-001` | `W-FD-001` | 1 | 질문피드 | page |
| `M-FD-B030` | `W-FD-M030` | 2 | 답변쓰기 | modal |
| `M-FD-010` | `W-FD-010` | 2 | 답변 상세 | page |
| `M-FD-020` | `W-FD-020` | 3 | 오늘의 콘텐츠 | content |

## Profile and membership flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-PR-001` | `W-PR-001` | 1 | 프로필 | content |
| `M-PR-P110` | `W-PR-P110` | 3 | 프로필 설정 | popup |
| `M-PR-120` | `W-PR-120` | 4 | 생각기록-오늘의 질문 | tab |
| `M-PR-121` | `W-PR-121` | 4 | 노트 | tab |
| `M-PR-122` | `W-PR-122` | 4 | 댓글 | tab |
| `M-PR-130` | `W-PR-130` | 3 | 관심콘텐츠 | tab |
| `M-PR-140` | `W-PR-140` | 3 | 팔로워 / 팔로잉 | tab |
| `M-PR-210` | `W-PR-210` | 2 | 회원정보(설정) | page |
| `M-PR-211` | `W-PR-211` | 3 | 비밀번호 확인 | page |
| `M-PR-212` | `W-PR-212` | 3 | 회원정보 변경 | page |
| `M-PR-213` | `W-PR-213` | 3 | 이벤트 혜택 알림 | page |
| `M-PR-310` | `W-PR-310` | 2 | 결제관리 | page |
| `M-PR-410` | `W-PR-410` | 2 | 멤버십 정보 | page |
| `M-PR-420` | `W-PR-420` | 3 | 멤버십 가입 | page |
| `M-PR-421` | `W-PR-421` | 4 | 결제정보 입력 및 가입 | page |
| `M-PR-422` | `W-PR-422` | 5 | 상품 결제 | page |
| `M-PR-P423` | `W-PR-P423` | 5 | NHN KCP 결제 | popup |

## Auth and common information flow

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-IN-010` | `W-IN-010` | 1 | 로그인 | page |
| `M-IN-011` | `W-IN-011` | 2 | 아이디 찾기 | page |
| `M-IN-012` | `W-IN-012` | 3 | 비밀번호 찾기 | page |
| `M-IN-020` | `W-IN-020` | 1 | 회원가입 | page |
| `M-IN-021` | `W-IN-021` | 4 | 약관 동의 | page |
| `M-IN-022` | `W-IN-022` | 4 | 회원가입 정보입력 | page |
| `M-IN-023` | `W-IN-023` | 4 | 회원가입 완료 | page |
| `M-CS-010` | `W-CS-010` | 1 | About(멤버십 소개) | page |
| `M-CS-011` | `W-CS-011` | 2 | 1개월 무료 체험권 | page |
| `M-CS-020` | `W-CS-020` | 1 | 공지사항 | page |
| `M-CS-030` | `W-CS-030` | 1 | 이용약관 | link |
| `M-CS-040` | `W-CS-040` | 1 | 개인정보처리방침 | link |
| `M-CS-050` | `W-CS-050` | 1 | 자주묻는질문(FAQ) | page |
| `M-ST-010` |  | 1 | 앱푸시설정 | page |

## QA implications

- `HM` 영역은 발견, 테마, 학습, 상단 메뉴 탐색을 검증하는 핵심 흐름이다.
- `HM-030 상단 메뉴`는 GNB 햄버거 메뉴 진입, 테마 보기 리스트 노출, 주요 이동 링크를 검증하는 공통 메뉴 레이어다.
- `FD` 영역은 오늘의 질문, 답변 작성, 답변 상세를 검증한다.
- `PR` 영역은 프로필, 멤버십 상태, 결제, 설정을 검증한다.
- `IN`, `CS`, `ST` 영역은 첫 방문, 계정, About, 공지, FAQ, 알림 설정을 검증한다.
- `앱푸시설정`은 모바일 앱 전용이며 PC 웹과 모바일 웹 범위에서는 제외한다.
