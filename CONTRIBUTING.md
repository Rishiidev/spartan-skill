# Contributing to Spartan

Thanks for using Spartan. Contributions welcome.

## What to contribute

- New compression rules (things Claude says that should be stripped)
- Edge cases where spartan breaks accuracy
- Platform-specific fixes (Claude.ai vs Cowork vs Claude Code behaviour)
- Better before/after examples in the README
- Translations of the skill for non-English sessions

## How

1. Fork the repo
2. Edit `skills/spartan/SKILL.md`
3. Test it — paste the SKILL.md into a Claude session and verify the behaviour
4. Open a PR with a before/after example showing the improvement

## Skill file rules

- Keep SKILL.md under 500 lines
- Every new rule needs a "never remove" counterpart if it could cause ambiguity
- Auto-clarity exceptions (destructive ops, security warnings) are non-negotiable — don't touch them

## Questions

Open an issue.
