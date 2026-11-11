# Ronald's Out-of-Office Countdown

A static countdown page (plain HTML, CSS and JavaScript, no build step).

## Edit the details

Open `index.html` and change the `CONFIG` block near the bottom:

- `departure` / `returnAt`: keep the fixed `+01:00` offset so everyone sees the same moment
- `destination`: name, description, time zone and the airport codes on the flight path
- `contacts`: public page, so work contact info only
- `messages` (away), `welcomeMessages` (after return) and `sunMessages` (click the sun)

## How it behaves

- Before departure: countdown to departure, plane waiting at Amsterdam
- At departure: a 6 second "Wheels up!" moment with confetti
- During the vacation: countdown to the return, plane on the flight path showing how much of the vacation has passed
- After return: "Welcome back" with the plane back at Amsterdam

Dates are always shown in British English, 24-hour time and CET, plus the visitor's own time when it differs.

## Testing other moments

The page has no test switches. To preview a state, fake the clock from outside, for example with Playwright:

```js
await page.clock.install({ time: new Date("2026-12-17T23:30:00+01:00") });
await page.goto("file:///path/to/vacation-countdown/index.html");
```

## Share preview

`og-image.png` (1200x630) is used by Teams and Slack. The Open Graph tags point to
`https://rowocloudfactory.github.io/vacation/vacation-countdown/`. Update them if the page is hosted elsewhere.
Icons: `icon.svg`, `favicon-32.png` and `apple-touch-icon.png`.
