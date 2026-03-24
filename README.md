# WisdomSpring Service Reference Skill

Portable Codex skill for WisdomSpring service reference, policy lookup, design walkthroughs, and QA planning.

## Included path

- `skills/wisdomspring-service-reference`

## Install with Codex

After this repo is pushed to GitHub, install it with:

```powershell
python "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo ekgp0598/wisdomspring-service-reference-skill-repo --path skills/wisdomspring-service-reference
```

Then restart Codex and use:

```text
$wisdomspring-service-reference Create QA test cases for HM-001
```

## Notes

- The skill is self-contained and does not require a specific local `Documents` folder.
- The bundled references include IA, screen plans, policy summaries, and example prompts.
