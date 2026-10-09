# Lab 4: VibeCoding (Coin Collector)

**Forked repository:** https://github.com/Gagan-1718/LAB-4-SE (game code in [`coin-collector/`](https://github.com/Gagan-1718/LAB-4-SE/tree/main/coin-collector))

## Submission

| Item | Link |
|---|---|
| Gameplay **before** changes, showing the bug (10 s) | [before.mp4](before.mp4) |
| Gameplay **after** changes, showing the fix and new features (10 s) | [after.mp4](after.mp4) |
| Chat / LLM page link | https://claude.ai/code/session_01VukeSwwdWVR7jDoVKwC5Jv |
| Complete chat history (export) | [chat-history.md](chat-history.md) |

## What was done

The LLM used was Claude Code. Each change was committed separately on the fork with a `Task N:` prefix.

- **Task 1: coin-collection bug.** Standing on a coin raised the score every frame because collected coins were never removed. Collected coins are now removed, so each coin scores exactly once.
- **Task 2: coin types.** Bronze (1 point), silver (3) and gold (5) coins, each with its own color, plus an on-screen legend.
- **Task 3: obstacles.** Red obstacles bounce around inside the play area. Touching one costs 1 of 3 lives, only when contact starts, followed by a 1-second blinking grace period.
- **Task 4: timed round.** A 30-second countdown is shown on screen and turns red in the last 5 seconds. The round ends when time or lives run out and shows the final score. R, Enter or Space starts a new round with score, lives and timer reset.

21 unit tests cover the bug fix and all three features. Run them from `coin-collector/` with `python -m unittest discover -p "test_*.py"`.
