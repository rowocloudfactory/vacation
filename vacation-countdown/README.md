# Ronald's Out-of-Office Countdown

A static countdown page (plain HTML, CSS and JavaScript, no build step).

## Edit the details

Open `index.html` and change the `CONFIG` block near the bottom:

- `departure` / `returnAt`: keep the fixed `+01:00` offset so everyone sees the same moment
- `destination`, `contactHtml`: public page, so work contact info only
- `messages` (away) and `welcomeMessages` (after return)

## Preview a state

Add `?now=` to the URL to fake the current time (encode `+` as `%2B`):

- Before: `index.html?now=2026-12-08T09:59:50%2B01:00` (watch it hit zero, confetti included)
- During: `index.html?now=2026-12-15T12:00:00%2B01:00`
- After: `index.html?now=2026-12-28T09:00:00%2B01:00`

Double-click the title for a test round of confetti.

## Share preview

`og-image.png` is the 1200x630 image used by Teams and Slack. The Open Graph tags point to
`https://rowocloudfactory.github.io/vacation/vacation-countdown/`. Update them if the page is hosted elsewhere.
