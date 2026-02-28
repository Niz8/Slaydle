# SLAYDLE

### Daily Goblin Battle

A Wordle-inspired daily RPG where you battle a new goblin every day. Figure out the right weapon and element combination to deplete the goblin’s HP before it defeats you.

**Play at:** https://niz8.github.io/Slaydle/

> ⚠ vibecoded — use at your own risk

-----

## How to Play

Each day a new goblin spawns with a secret weakness — one weapon type and one element type. You have **5 HP** and the goblin has **3 HP**.

**Weapons:** 🏹 Bow · ⚔️ Sword · 🪓 Club  
**Elements:** 🔥 Fire · ❄️ Ice · ⚡ Electric · 💪 Physical

Each turn, pick one weapon and one element and strike:

- **Very Effective** (both correct) = 2 damage
- **Effective** (one correct) = 1 damage
- **Ineffective** (neither correct) = 0 damage

After your attack, the goblin strikes back. Goblin damage escalates each turn (0 on turn 1, 1 on turn 2, 2 on turn 3…). Defeat the goblin before your HP hits zero.

**Crystal Ball 🔮** — Once per game, consult the crystal ball to reveal two ineffective options. Costs 1 HP.

The goblin’s name may hint at its weakness — or may just be flavor. Some days are harder than others.

Results are saved so you only play once per day. Share your scorecard with friends!

-----

## Patch Notes

### v0.6.0

- Crystal ball use now appears as a 🔮 on its own line in the shared scorecard, inserted at the position it was used
- Added version number to bottom of page
- Crystal ball state (used/turn) now saved to localStorage and restored correctly on revisit

### v0.5.0

- Expanded goblin first name pool from 30 to 76 names
- Improved seed hashing algorithm so adjacent dates scatter to different names rather than potentially repeating
- Fixed copy scorecard button not working on return visits after completing the game (listener was inside an early-return block)

### v0.4.0

- Fixed result screen (VICTORY / DEFEATED) rendering as dark text on dark background on mobile
- Replaced all inline `style="color:var(--...)"` references in JavaScript-generated HTML with hardcoded hex values, which mobile browsers handle more reliably

### v0.3.0

- Fixed all remaining CSS variable references rendering as dark-on-dark on iOS Safari
- Removed `:root` CSS variables block entirely — all colors now hardcoded hex throughout
- Unselected attack buttons now have visible bright green borders and text on dark background
- PHYSICAL selected state changed from grey to white for legibility
- Battle log text colors brightened across the board
- Moved vibecoded disclaimer from header to bottom of page

### v0.2.0

- Fixed font loading by moving Google Fonts from `@import` to `<link>` tags in `<head>`
- Added `background` color to `html` element to prevent white flash before CSS loads
- Rewrote button selected state with `!important` overrides to prevent Safari/mobile default style conflicts
- Updated scorecard share URL to `https://niz8.github.io/Slaydle/`
- Added vibecoded disclaimer

### v0.1.0

- Initial release
- Daily seeded goblin with name, HP, and dual-axis weakness (weapon + element)
- Goblin name adjective sometimes hints at weakness, sometimes flavor only
- 3 weapons × 4 elements combat system
- Very Effective / Effective / Ineffective feedback
- Escalating goblin counter-attack damage per turn
- Crystal ball hint system (costs 1 HP, usable once)
- Scrollable battle log
- Win/loss result screen with emoji scorecard
- Copy to clipboard sharecard
- localStorage daily lock — play once per day, result persists on revisit
- Green-on-black DOS terminal aesthetic with scanlines and CRT flicker
- Mobile-first design

-----

*Built with vibecode and zero guarantees.*