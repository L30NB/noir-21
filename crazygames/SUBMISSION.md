# Submitting Noir 21 to CrazyGames

## Files
- `noir-21-upload.zip`: the game (upload this as the game build)
- `cover-1920x1080.png`, `cover-800x1200.png`, `cover-800x800.png`: cover images
- `screenshot-gameplay.png`: a gameplay screenshot

Check the developer portal for the exact cover sizes it asks for; regenerate if they differ.

## What the game does with the CrazyGames SDK (v3)
- Loads `https://sdk.crazygames.com/crazygames-sdk-v3.js` and calls `SDK.init()`
- `gameplayStart()` when a hand is dealt, `gameplayStop()` before an ad and when the stats panel opens
- Midgame ad every 5 rounds, shown before the next deal
- Rewarded ad: "Watch an ad for 1,000 chips" when the player is out of chips
- `happytime()` when the player wins with a blackjack
- Progress (balance, stats) saved with `SDK.data`, plus localStorage as a fallback
- Outside CrazyGames the SDK reports `disabled` and the game runs with no ads

## Before submitting
1. Test the build with the CrazyGames QA tool in the developer portal.
2. Play with ads on: midgame ad after 5 rounds, rewarded ad when broke.

## Suggested listing text
**Title:** Noir 21

**Description:** A clean, minimal game of blackjack. Six-deck shoe, dealer stands on soft 17, blackjack pays 3 to 2. Double down, split up to four hands, take insurance or surrender. Build your bankroll, track your win rate and chase your best streak.

**Controls:**
- Mouse or touch: click chips to bet, then Deal, Hit, Stand, Double, Split or Surrender
- Keyboard: 1–4 add chips, Space deal, H hit, S stand, D double, P split, R surrender, I/N insurance, T stats

**Category:** Card / Casino. Uses play money only; no real-money gambling.
