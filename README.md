# WisdomSpring Service Reference Skill

WisdomSpring 서비스 레퍼런스 스킬 — Codex와 Claude Code 모두 지원.

서비스 개요, 화면기획서, 디자인 이미지, 어드민 정책, QA 가이드를 번들로 제공하여 서비스 설명, 정책 비교, 테스트 시나리오 설계, 한국어 QA 보고서 작성을 지원합니다.

## Included path

- `skills/wisdomspring-service-reference`

## Install with Codex

```powershell
# Windows
python "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo ekgp0598/wisdomspring-service-reference-skill-repo --path skills/wisdomspring-service-reference
```

```bash
# macOS
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo ekgp0598/wisdomspring-service-reference-skill-repo --path skills/wisdomspring-service-reference
```

Then restart Codex and use:

```text
$wisdomspring-service-reference Create QA test cases for HM-001
```

## Install with Claude Code

### 방법 1: skills CLI (추천)

```bash
# Claude Code용으로 설치
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a claude -g
```

### 방법 2: 수동 설치

레포를 클론한 뒤 스킬 폴더를 Claude Code 스킬 디렉토리에 복사합니다.

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

Then use in Claude Code:

```text
/wisdomspring-service-reference HM-001 화면 테스트 시나리오 만들어줘
```

## Install with skills.sh

```bash
# Inspect available skills in this repo
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --list
```

```bash
# Install for Codex
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a codex -g

# Install for Claude Code
npx skills add ekgp0598/wisdomspring-service-reference-skill-repo --skill wisdomspring-service-reference -a claude -g
```

## Notes

- The skill is self-contained and does not require a specific local `Documents` folder.
- The bundled references include IA, screen plans, policy summaries, design images, and example prompts.
- `SKILL.md` follows the [Agent Skills](https://agentskills.io) open standard — compatible with both Codex and Claude Code.
- `agents/openai.yaml` is for Codex, `agents/claude.yaml` is for Claude Code. Each platform reads its own agent config and ignores the other.
