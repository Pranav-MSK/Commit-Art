# 🎨 Contributing to Issue-Ink

> **The Core Principle:** Input → Mutation → Public Record. If your contribution preserves this loop and keeps the system simple, it’s welcome. If it tries to transform Issue-Ink into a traditional web app, it will be rejected.

`Issue-Ink` is a collaborative 8×8 pixel grid driven entirely by GitHub Issues and GitHub Actions. Here, every commit is a brushstroke. 

---

## 🖌 How to Paint (For Users)

Anyone can participate in this experiment. To paint a pixel, you don't need to write code—you just need to open an issue.

### The Input Format
1. Open the **Issues** tab and click **New Issue**.
2. Use this exact format for the title: `Paint [Coordinate] #HexCode`

### Valid Parameters

| Parameter | Allowed Values | Examples |
| :--- | :--- | :--- |
| **Rows** | `A` through `H` | `Paint [A1] #FF0000` |
| **Columns** | `1` through `8` | `Paint [B5] #00FFAA` |
| **Color** | 6-digit HEX code | `Paint [H8] #FFFFFF` |

### ⏳ The Game Rules
* 🕒 **Rate Limit:** One paint per user every 24 hours.
* 🔒 **Territory Lock:** A newly painted tile is locked for 1 hour.
* 🤖 **No Automation:** Do not script or spam the painting process. This system is slow by design.
* ❌ **Validation:** Invalid formats automatically receive the `Invalid` label. Successful paints receive the `Completed` label.

---

## 🧠 Project Philosophy

Issue-Ink is a behavioral experiment. The canvas is **open, mutable, conflict-driven, and emergent.** To maintain the purity of the experiment, we intentionally avoid:
* Complex external UIs or web frontends.
* Hidden backend logic or centralized moderation algorithms.
* Off-platform state storage (databases/servers).

**GitHub is the engine. Transparency is the absolute rule.**

---

## 🛠 Engineering & Code Contributions

We welcome engine enhancements, provided they respect our architectural boundaries.

### Architecture Overview
```
[Issue Opened] ➔ [GitHub Action Parses Title] ➔ [Validates Rules] ➔ [Mutates map.svg & state.json] ➔ [Commits to Main]

```

* **State Storage:** `data/state.json` holds the current canvas values.
* **Canvas Render:** `map.svg` represents the live visual state.
* **Ledger:** The Git commit history serves as our immutable public record.

### 🚀 High-Priority Enhancement Ideas

We are actively looking for contributions in the following areas:

#### 1. Stability & Edge Cases
* More robust input validation and syntax parsing.
* Enhanced edge-case handling for simultaneous issue submissions (race conditions).
* Improved cache-busting logic for the README SVG display.

#### 2. Experimental Mechanics (Must be minimal)
* **Soft Pixel Decay:** Gradually fading colors after prolonged inactivity.
* **Contested Tiles:** Logic to track and display the most fought-over coordinates.
* **Controlled Expansion:** Expanding the grid (e.g., to 10×10) only after specific global milestones are met.

#### 3. Observability
* Auto-generating a lightweight leaderboard or "Total Paints" counter inside the README.
* *Note: All metrics must live inside the repository. No external dashboards.*

---

## ❌ What Will Be Rejected

The constraints of this project are the point. We will automatically decline Pull Requests that attempt to introduce:
* 🛑 Backend servers (Node, Python APIs, etc.)
* 🛑 External databases (MongoDB, PostgreSQL, Firebase, etc.)
* 🛑 Third-party authentication systems.
* 🛑 Alternatives to GitHub Actions.

---

## 📦 How to Submit a Change

1. **Fork** the repository and create your feature branch.
2. Keep your commits **small, atomic, and well-documented**.
3. Open a Pull Request clearly explaining:
   * What changed.
   * Why it improves the system.
   * How it strictly adheres to the project philosophy.

---

## 🛡 Moderation & Behavior

While this is an open, conflict-driven experiment, harassment, hate symbols, explicit content, or coordinated malicious abuse will be reverted, and offending users will be blocked. The maintainer retains final decision authority.

---
Built carefully. Played creatively. 🎨
