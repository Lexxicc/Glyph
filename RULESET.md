# GLYPH — Ruleset

> Keep this file in sync with the How to Play page in `Glyph.html` whenever rules or mechanics change.

---

## Goal

Solve **3 hidden 5-letter words** as fast as possible. You have **10 minutes** and **6 guesses per word**.

---

## Controls

| Input | Action |
|---|---|
| Keyboard (A–Z) | Type a letter |
| Enter | Submit guess |
| Backspace | Delete last letter |
| On-screen keyboard | Full mobile support |

---

## How to Play

- Type a 5-letter word and press **Enter** to submit
- Only valid dictionary words are accepted — invalid guesses trigger a lock for 1.2 seconds
- After each guess, tiles change colour to reveal how close you were

---

## Tile Colours

| Colour | Meaning |
|---|---|
| Green | Letter is correct and in the right position |
| Yellow | Letter is in the word but in the wrong position |
| Grey | Letter is not in the word at all |

**Duplicate letters:** if a letter appears only once in the target word but you guess it twice, only one tile lights up green or yellow — telling you exactly how many times it appears.

---

## Match Structure

- 3 words per match
- 6 guesses allowed per word
- If all 6 guesses are used without solving, the answer is revealed and the match moves on
- Match ends when all 3 words are attempted or the timer hits 0:00

---

## Scoring

```
Base Points      = Solved Words × 1000
Accuracy Factor  = Solved Words / Total Guesses Used
Time Bonus       = floor(Seconds Remaining × 2)  [only if ≥1 word solved]

Final Score      = floor((Base Points × Accuracy Factor) + Time Bonus)
```

---

## Challenge Mode

- After a match, share a challenge link — your opponent plays the exact same 3 words (same seed)
- Results show **WIN / LOSE / DRAW** side by side

---

## Win / Loss Conditions

| Condition | Result |
|---|---|
| Solve word within 6 guesses | Word cleared |
| Use all 6 guesses without solving | Word revealed, match continues |
| All 3 words attempted | Match over |
| Timer reaches 0:00 | Match over immediately |

---

Last updated: 2026-05-02 — v0.0.10
