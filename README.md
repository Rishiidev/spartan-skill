# ⚔️ Spartan — Token Compression Skill for Claude

<div align="center">

**Cut Claude's token usage 65–75%. Zero loss of technical accuracy.**

[![Stars](https://img.shields.io/github/stars/Rishiidev/spartan-skill?style=for-the-badge&color=gold)](https://github.com/Rishiidev/spartan-skill/stargazers)
[![License](https://img.shields.io/github/license/Rishiidev/spartan-skill?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-blue?style=for-the-badge)](https://github.com/Rishiidev/spartan-skill/releases)
[![Claude Code](https://img.shields.io/badge/Claude_Code-✓-green?style=for-the-badge)](https://claude.ai/code)

*Works in Claude.ai · Cowork · Claude Code — no CLI, no Node.js, one command.*

</div>

---

## The Problem

Claude is verbose by default. Every response comes padded with filler, pleasantries, and hedging that burns tokens without adding value.

```
"That's a great question! I'd be happy to help you with that.
The issue you're experiencing is most likely caused by the fact
that your authentication token is expiring. You might want to
consider looking at the comparison operator being used..."
```

## The Fix

```
spartan
```

```
Auth token expiry. Check uses `<` not `<=`. Fix:
```

Same answer. **73% fewer tokens.**

---

## Install

| Platform | Command |
|----------|---------|
| **Claude Code** | `/plugin install github:Rishiidev/spartan-skill` |
| **Cowork** | `/plugin install github:Rishiidev/spartan-skill` |
| **Claude.ai** | Download [`spartan.skill`](https://github.com/Rishiidev/spartan-skill/releases/latest) → import it |

---

## Two Modes

### `spartan out` — Output Compression
Claude's responses go terse. Filler removed. Technical accuracy untouched.

### `spartan in` — Input Compression
Paste long docs, error logs, or briefs. Spartan compresses them into a dense version you reuse across the session — saving tokens on every future message.

### `spartan` — Both at once
Maximum savings. This is the default.

---

## Three Intensity Levels

| Level | What changes | Token reduction |
|-------|-------------|----------------|
| `spartan lite` | Removes filler and hedging. Keeps full sentences. | ~30% |
| `spartan full` *(default)* | Drops articles, uses fragments, short synonyms. | ~65% |
| `spartan ultra` | Abbreviates prose (DB/auth/config/req/res). Arrows for causality (X → Y). | ~75% |

---

## Before / After

**"Why is my React component re-rendering?"**

| Mode | Response |
|------|---------|
| Default Claude | "Your component is re-rendering because you're creating a new object reference on each render cycle. You might want to consider wrapping the value in a `useMemo` hook to prevent unnecessary re-renders." |
| `spartan full` | "New object ref each render. Inline object prop = new ref = re-render. `useMemo`." |
| `spartan ultra` | "Inline obj → new ref → re-render. `useMemo`." |

**"Explain database connection pooling."**

| Mode | Response |
|------|---------|
| Default Claude | "Connection pooling is a technique where a set of database connections are kept open and reused across multiple requests, rather than opening and closing a new connection for each request..." |
| `spartan full` | "Pool reuse open DB connections. No new connection per request. Skip handshake overhead." |
| `spartan ultra` | "Pool = reuse DB conn. Skip handshake → fast under load." |

---

## All Commands

| Command | Effect |
|---------|--------|
| `spartan` | Both modes ON, full intensity |
| `spartan out` | Output compression only |
| `spartan in` | Input compression only |
| `spartan lite` | Drop to lite intensity |
| `spartan ultra` | Push to ultra intensity |
| `spartan status` / `spartan ?` | Show current state |
| `spartan, [task]` | Activate AND complete task in one shot |
| `normal mode` / `stop spartan` | Turn off |

---

## What Gets Removed

| Removed | Example |
|---------|---------|
| Pleasantries | "Sure! Happy to help!" → gone |
| Filler words | just / really / basically / actually → gone |
| Hedging | "it seems" / "you might want to consider" → gone |
| Preamble | "Let me explain..." → just explain |
| Articles | a / an / the → dropped in full/ultra |
| Sign-offs | "Hope that helps!" → gone |

## What Never Gets Removed

- Code blocks (always untouched)
- Technical terms (exact, never abbreviated)
- Error messages (quoted exact)
- Numbers, dates, measurements
- Security warnings
- Destructive action confirmations

---

## Input Compression Example

**You paste (60 words):**
> "In order to optimize the performance of the database queries, it is important to note that we should consider implementing indexes on the columns that are most frequently accessed..."

**Spartan returns (20 words):**
```
[SPARTAN IN — compressed. Copy this for future messages.]
Optimize DB query perf: index frequently-accessed columns, add query caching, use connection pooling.
```

Copy that. Paste it in every future message instead of the original. **Tokens saved every turn.**

---

## Safety: Auto-Clarity Exceptions

Spartan temporarily drops compression for:
- Security warnings
- Destructive / irreversible action confirmations (DROP TABLE, file deletion, prod deploys)
- Steps where fragment order could cause misread

It resumes immediately after.

---

## Platform Notes

| Platform | Output compression | Input compression | Install method |
|----------|--------------------|------------------|---------------|
| Claude Code | ✅ | ✅ | `/plugin install` |
| Cowork | ✅ | ✅ | `/plugin install` or `.skill` file |
| Claude.ai | ✅ | ✅ | `.skill` file or Project instruction |

---

## License

MIT — use it, fork it, share it.

---

<div align="center">

If Spartan saves you tokens, a ⭐ helps others find it.

</div>
