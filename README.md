# Field Atlas

A five-level study app for learning all 50 U.S. states and capitals — built as a single self-contained web app that installs like a native app on your phone's home screen.

![Overview](screenshots/overview.png)

## How it works

You move through **five levels**, each one harder than the last. Every level needs a passing score to unlock the next:

| # | Level | What it tests |
|---|-------|----------------|
| 1 | **Flash Cards** | Self-graded recall — flip the card, mark "Knew It" or "Didn't Know" |
| 2 | **Multiple Choice** | Pick the right capital from 4 options (wrong answers are pulled from *nearby* states, so it's genuinely testing recognition, not just guessing) |
| 3 | **Matching** | Match states to capitals in sets of 10 — works in either order (tap the state first or the capital first) |
| 4 | **Map Fill-In** | A real U.S. map highlights the state; you type the capital |
| 5 | **Fill in the Blank** | Just the state name, no aids — pure recall |

You choose how strict "passing" is, framed as a school grade:

- **A+** (100%), **A** (90%), **B** (80%), or **C** (70%)

Whichever you pick becomes the bar for unlocking the next level — so passing at the "B" setting tells you that if you took a real test on this material right now, you'd probably score a B or better.

## Screenshots

### Level 1 — Flash Cards
![Flash Cards](screenshots/level1-flash-cards.png)

### Level 2 — Multiple Choice
![Multiple Choice](screenshots/level2-multiple-choice.png)

### Level 3 — Matching
![Matching](screenshots/level3-matching.png)

### Level 4 — Map Fill-In
![Map Fill-In](screenshots/level4-map-fill-in.png)

### Level 5 — Fill in the Blank
![Fill in the Blank](screenshots/level5-fill-in-the-blank.png)

### Study List
A plain alphabetical list of all 50 state/capital pairs, for cramming before you quiz.

![Study List](screenshots/study-list.png)

## Other features

- **Territory Stamped tracker** — a passport-style progress strip at the bottom fills in as you answer correctly, resetting fresh at the start of each level.
- **Review Weak States** — every miss is quietly logged in the background; once you've missed anything, a "Review Weak States" button appears, pulling your worst 10 into a focused round.
- **Progress is saved automatically** — your level, unlocks, pass-threshold setting, and stamps all persist between visits (stored locally on your device, nothing sent anywhere).
- **Sound + light haptic feedback** on right/wrong answers.
- Works as an installed home-screen app (Add to Home Screen from Safari) with its own icon, and functions like a normal app — no browser address bar once installed.

## Running it yourself

This is a single `index.html` file with no build step. To host your own copy:

1. Fork or download this repository.
2. Upload `index.html` to a static host — the simplest option is **GitHub Pages**:
   - Repo → **Settings → Pages** → set Source to your branch, folder `/ (root)` → Save.
   - Your app will be live at `https://<your-username>.github.io/<repo-name>/`.
3. Open that URL on your phone in Safari, tap **Share → Add to Home Screen**.

The app pulls React and Tailwind from a CDN on first load (so it needs internet the very first time), then runs entirely client-side after that — no server, no database, no account required.

## Credits

- State boundary map data adapted from the MIT-licensed [Interactive and Responsive SVG Map of US States and Capitals](https://github.com/WebsiteBeaver/interactive-and-responsive-svg-map-of-us-states-capitals) by David Marcus / Website Beaver.
- Built with React and Tailwind CSS.
