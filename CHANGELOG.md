# Changelog

All notable changes documented here.
Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

## [1.0.0] — 2026-06-17

### Added
- Dual-mode compression: `spartan out` for output, `spartan in` for input
- Three intensity levels: lite (~30%), full (~65%), ultra (~75%)
- `spartan both` — both modes at once for maximum savings
- `spartan, [task]` — activate and complete a task in one shot
- `spartan status` / `spartan ?` — show state without changing it
- Auto-clarity exceptions: security warnings, destructive ops always full prose
- State tracking display: `[SPARTAN: out=ON in=OFF level=full]`
- Works in Claude.ai, Cowork, and Claude Code — no CLI or Node.js required
- Input compression labels output `[SPARTAN IN — compressed. Copy this for future messages.]`
- Drift warning guidance for 20+ turn sessions
