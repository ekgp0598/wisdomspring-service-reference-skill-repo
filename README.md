# WisdomSpring Test Planning Skill

Portable Codex skill for planning and executing QA on the WisdomSpring service.

## Included path

- `skills/wisdomspring-test-planning`

## Install with Codex

After this repo is pushed to GitHub, install it with:

```powershell
python "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo OWNER/REPO --path skills/wisdomspring-test-planning
```

Then restart Codex and use:

```text
$wisdomspring-test-planning Create QA test cases for HM-001
```

## Notes

- The skill is self-contained and does not require a specific local `Documents` folder.
- The bundled references include IA, screen plans, policy summaries, and example prompts.
