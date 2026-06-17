# Spartan Skill

Dual-mode token compression for Claude. Cuts token usage **65–75%** with zero loss of technical accuracy. Works in Claude.ai, Cowork, and Claude Code — no CLI or Node.js required.

## Install

```
/plugin install github:Rishiidev/spartan-skill
```

## Two Modes

| Mode | Command | What it does |
|------|---------|--------------|
| Output compression | `spartan out` | Claude responds terse — no filler, no pleasantries |
| Input compression | `spartan in` | Compresses pasted docs/context into a dense reusable version |
| Both | `spartan` / `spartan both` | Maximum token savings |

## Three Intensity Levels

| Level | Reduction |
|-------|-----------|
| `spartan lite` | ~30% |
| `spartan full` (default) | ~65% |
| `spartan ultra` | ~75% |

## Quick Commands

```
spartan          → both modes ON, full intensity
spartan out      → output compression only
spartan in       → input compression only
spartan lite     → drop to lite intensity
spartan ultra    → push to ultra intensity
spartan status   → show current state
normal mode      → turn off spartan
```

## What Gets Removed

- Articles (a / an / the)
- Filler words (just / really / basically / actually)
- Pleasantries (sure / certainly / happy to / great question)
- Hedging (it seems / you might want to consider)
- Preamble ("Let me explain..." → just explain)

## What Never Gets Removed

- Code blocks (always untouched)
- Technical terms (exact, never abbreviated)
- Error messages (quoted exact)
- Numbers, dates, measurements
- Security warnings
- Irreversible action confirmations

## License

MIT
