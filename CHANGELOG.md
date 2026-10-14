# Changelog

All notable changes to CueDeck are listed here, newest first. Dates are year‑month‑day.

## 0.3.0 — 2026‑10‑14

**Smarter port handling, and a new Settings popup.**

We ran into a challenge with network ports. CueDeck talks to grandMA3 over a UDP port, and on some setups that port turned out to be busy — taken by another tool on the machine, or by a previous CueDeck instance that hadn't let go of it yet. A single fixed port simply wasn't robust enough, so we rethought how the two sides find each other.

- **Automatic port fallback (no setup).** CueDeck no longer depends on one fixed port. The grandMA3 side now picks the first free port in a small range and tells the Stream Deck which one it landed on, so the connection just works — even when the default port is occupied.
- **New: a CueDeck Settings popup.** For advanced users who would rather decide for themselves, the Connection key's settings now let you:
  - see which port CueDeck is currently running on,
  - choose **Automatic**, or set a **port manually** when automatic isn't good enough for your setup, and
  - **restart** the grandMA3‑side plugin straight from the Stream Deck.

If you just want it to work, do nothing — Automatic handles it. If you have other things on your network and prefer a fixed port, you now have the choice.
