# WisdomSpring Service Reference Skill

WisdomSpring 서비스의 기획, 디자인, 정책, QA를 AI 에이전트에게 가르치는 레퍼런스 스킬입니다.

화면기획서, IA 맵, 디자인 이미지, 어드민 정책 문서를 번들로 포함하고 있어 별도 자료 없이 서비스 설명, 테스트 시나리오 설계, 정책 비교, 한국어 QA 보고서 작성이 가능합니다.

## What is WisdomSpring?

WisdomSpring(위즈덤스프링)은 인문학 기반 구독형 학습 서비스입니다.

- 매일 제공되는 **오늘의 질문**과 답변 기록
- 철학·문학·역사 중심의 **테마 콘텐츠** (영상 + 아티클)
- 개인 **노트, 댓글, 팔로우** 등 소셜 기록 공간
- **멤버십** 기반 접근 제어

## Use When

- "위즈덤스프링이 뭔지 설명해줘"
- "HM-001 화면 테스트 케이스 만들어줘"
- "질문피드 → 답변 작성 → 답변 상세 흐름 QA 시나리오"
- "어드민 정책과 프론트 동작이 충돌하는 부분 점검"
- "멤버십 상태별 회귀 테스트 항목 정리"
- "스모크 테스트 시나리오 작성"
- "화면 구조와 디자인 톤 설명"

## Features

| 기능 | 설명 |
|------|------|
| 서비스 온보딩 | WisdomSpring을 모르는 사람에게 서비스 목적, 사용자 여정, 핵심 화면, 콘텐츠 구조를 설명 |
| 테스트 시나리오 설계 | 화면 ID 기반으로 happy path, 예외, 상태 전이, 권한, 플랫폼 차이 시나리오 생성 |
| 어드민 정책 비교 | admin 정책과 front 동작 간 충돌 가능성 점검 |
| QA 보고서 작성 | 범위, 시나리오, 발견사항, 오픈 이슈, 다음 확인사항을 한국어 문서로 출력 |
| 디자인 워크스루 | 번들된 디자인 이미지와 화면 구조 문서를 기반으로 레이아웃·톤 설명 |
| 탐색형 QA | 문서만으로 결함 가능성이 높은 영역을 탐색적으로 도출 |

## Example Prompts

```text
# 서비스 처음 이해하기
$wisdomspring-service-reference 위즈덤스프링이 어떤 서비스인지 설명해줘.

# 특정 화면 테스트 설계
$wisdomspring-service-reference HM-001 메인(발견) 화면 웹/모바일 공통 테스트 케이스 작성해줘.

# 질문피드 흐름 점검
$wisdomspring-service-reference FD-001, FD-B030, FD-010 흐름 기준 QA 시나리오 작성해줘.

# 어드민 정책 싱크 검토
$wisdomspring-service-reference admin 정책 기준으로 front 동작과 충돌할 수 있는 포인트 정리해줘.

# 멤버십 회귀 테스트
$wisdomspring-service-reference PR-410 멤버십 정보 화면 상태별 회귀 테스트 항목 정리해줘.

# 스모크 테스트
$wisdomspring-service-reference 전체 서비스 스모크 테스트 시나리오 작성해줘.

# QA 결과 보고서
$wisdomspring-service-reference HM-001과 FD-001 테스트 결과를 한국어 QA 보고서 형식으로 정리해줘.
```

> Claude Code에서는 `$wisdomspring-service-reference` 대신 `/wisdomspring-service-reference`를 사용합니다.

## Bundled References

이 스킬은 다음 레퍼런스를 번들로 포함합니다. 별도 파일 준비 없이 바로 사용 가능합니다.

| 카테고리 | 내용 |
|----------|------|
| 서비스 개요 | 서비스 소개, 입문 가이드, IA 맵, 화면 인덱스 |
| 화면기획서 | HM(홈), FD(질문피드), PR(프로필), IN(인트로) 등 18개 화면 상세 기획 |
| 디자인 이미지 | 주요 화면 디자인 시안 30+장 (모바일/웹) |
| 어드민 정책 | 정책 요약, 상세 기획서 (목록 컬럼, 필드 제약, 수정/삭제 규칙) |
| QA 가이드 | 테스트 영역, 기대결과 패턴, 보고서 템플릿, 예제 프롬프트 |
| 디자인 가이드 | 비주얼 디자인 요약, 영역별 화면 구조 |

## Skill Structure

```
skills/wisdomspring-service-reference/
├── SKILL.md                          # 스킬 정의 (Agent Skills 표준)
├── agents/
│   ├── openai.yaml                   # Codex 에이전트 설정
│   └── claude.yaml                   # Claude Code 에이전트 설정
└── references/
    ├── service-overview.md           # 서비스 개요
    ├── service-primer.md             # 입문 가이드
    ├── ia-map.md                     # IA 맵
    ├── screen-index.md               # 화면 인덱스
    ├── screen-plans/                 # 화면별 상세 기획서 (18개)
    ├── design-images/                # 디자인 시안 이미지 (30+장)
    ├── design-image-index.md         # 디자인 이미지 인덱스
    ├── visual-design-summary.md      # 비주얼 디자인 요약
    ├── visual-structure-by-area.md   # 영역별 화면 구조
    ├── admin-policy-summary.md       # 어드민 정책 요약
    ├── admin-planning-spec.md        # 어드민 상세 기획
    ├── test-areas.md                 # 테스트 영역
    ├── expected-results.md           # 기대결과 패턴
    ├── report-template.md            # QA 보고서 템플릿
    ├── example-prompts.md            # 예제 프롬프트
    └── source-locations.md           # 소스 위치 참조
```

## Installation

### Quick Install (skills CLI)

```bash
# Codex
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a codex -g

# Claude Code
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a claude -g

# 둘 다 한번에
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a codex -a claude -g
```

### Codex (수동)

```powershell
# Windows
python "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo ekgp0598/wisdomspring-service-reference-skill-repo --path skills/wisdomspring-service-reference
```

```bash
# macOS
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo ekgp0598/wisdomspring-service-reference-skill-repo --path skills/wisdomspring-service-reference
```

### Claude Code (수동)

```powershell
# Windows
git clone https://github.com/ekgp0598/wisdomspring-service-reference-skill-repo.git
xcopy /E /I wisdomspring-service-reference-skill-repo\skills\wisdomspring-service-reference "%USERPROFILE%\.claude\skills\wisdomspring-service-reference"
```

```bash
# macOS / Linux
git clone https://github.com/ekgp0598/wisdomspring-service-reference-skill-repo.git
cp -r wisdomspring-service-reference-skill-repo/skills/wisdomspring-service-reference ~/.claude/skills/wisdomspring-service-reference
```

## Compatibility

| Agent | 설치 옵션 | 상태 |
|-------|----------|------|
| Codex | `-a codex` | Tested |
| Claude Code | `-a claude` | Tested |
| Cursor | `-a cursor` | Compatible |
| Other agents | [See supported list](https://github.com/vercel-labs/skills#supported-agents) | Compatible |

`SKILL.md`는 [Agent Skills](https://agentskills.io) 오픈 스탠다드를 따르므로 해당 표준을 지원하는 모든 에이전트에서 사용 가능합니다.

## Notes

- 완전 자급형(self-contained) 스킬입니다. 로컬 폴더 의존 없이 번들된 레퍼런스만으로 동작합니다.
- 출력은 기본 한국어입니다. 영어 출력이 필요하면 프롬프트에서 요청하세요.
- 레퍼런스 파일명이나 내부 경로는 사용자 응답에 노출되지 않습니다.

## License

MIT
