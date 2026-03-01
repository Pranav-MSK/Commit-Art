# Contributing to Commit-Art

Commit-Art powers **The Global Rorschach Canvas** — a collaborative 8×8 pixel grid driven entirely by GitHub Issues and GitHub Actions.

Every commit is a brushstroke.

This document explains:

- How to participate
- How the engine works
- What enhancements are welcome
- What changes will likely be rejected

---

# 🎨 Painting the Canvas

Anyone can paint.

## How to Paint

1. Open the **Issues** tab.
2. Click **New Issue**.
3. Use this exact format in the **title**:

```
Paint [A5] #FF5733
```

## Valid Inputs

- Rows: **A–H**
- Columns: **1–8**
- Color: **6-digit HEX code**

Examples:

- `Paint [A1] #FF0000`
- `Paint [H8] #00FFAA`

---

# ⏳ Game Rules

- 🕒 One paint per user every **24 hours**
- 🔒 A painted tile is locked for **1 hour**
- Format must match exactly
- Invalid format → Issue labeled `Invalid`
- Successful paint → Issue labeled `Completed`
- Every action is permanently stored in `data/state.json`
- SVG (`map.svg`) represents the live canvas state

Do not automate or spam painting.

This is a slow system by design.

---

# 🧠 Philosophy

Commit-Art is a behavioral experiment.

The canvas is:

- Open
- Mutable
- Conflict-driven
- Emergent

We intentionally avoid:

- Complex UI
- Hidden backend logic
- Centralized moderation algorithms
- Off-platform state storage

GitHub is the engine.

Transparency is the rule.

---

# 🛠 Code Contributions

Contributions to the engine are welcome — but must respect the core philosophy.

## Architecture Overview

- Issue Title → Parsed by GitHub Action
- Workflow validates format and rules
- SVG (`map.svg`) is mutated
- Persistent state stored in `data/state.json`
- Commit history is the public ledger

Everything must remain:

- Deterministic
- Serverless
- GitHub-native

---

# 🚀 Enhancement Ideas

Enhancements should improve one of these areas:

---

## 1️⃣ Stability Improvements

- More robust input validation
- Edge case handling
- Improved cooldown calculations
- Improved lock safety
- Better cache-busting for SVG
- State integrity verification

---

## 2️⃣ Game Mechanics (Carefully Considered)

Potential future mechanics:

- Tile ownership (consecutive paints)
- Most contested tile tracking
- Daily paint counters
- Soft pixel decay after inactivity
- Controlled canvas expansion (e.g., 10×10 after X paints)

Mechanics must:
- Be minimal
- Preserve simplicity
- Avoid turning the system into a complex app

---

## 3️⃣ Observability & Transparency

- Auto-generated stats section in README
- Lightweight leaderboard
- Total paints counter
- Timestamp display improvements

No external dashboards.

All metrics must live inside the repository.

---

## 4️⃣ Anti-Abuse Improvements

- Basic spam resistance
- Pattern abuse detection
- Safer automation guardrails

Must remain lightweight and transparent.

---

# ❌ Changes Likely to Be Rejected

- Adding a backend server
- Adding a database
- Replacing GitHub Actions
- Adding a web frontend
- Introducing complex authentication systems
- Overengineering the canvas

The constraint *is the point*.

---

# 📦 How to Submit Code Changes

1. Fork the repository.
2. Create a feature branch.
3. Keep commits small and atomic.
4. Clearly explain:
   - What changed
   - Why it improves the system
   - How it preserves philosophy
5. Submit a Pull Request.

PRs that dramatically increase complexity will likely be declined.

---

# 🛡 Moderation

This is an open experiment, but:

- Harassment
- Hate symbols
- Explicit content
- Coordinated abuse

may be reverted or blocked.

The maintainer retains final decision authority.

---

# 🧩 The Core Principle

Input → Mutation → Public Record

If your contribution preserves this loop and keeps the system simple, it will likely be considered.

If it tries to transform Commit-Art into a traditional web app, it will not.

---

Build carefully.
