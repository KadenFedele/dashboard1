# Kaden's Personal Dashboard

A single-page personal dashboard that displays a weather widget and lets the
reader switch between a light and a dark theme. Weather data is loaded at
runtime from a local JSON file with `fetch()`, and the chosen theme is saved so
it is still in place the next time the page is opened.

## Features

- **Weather widget** — temperature, location, condition and icon, loaded from
  `data/weather.json` with `fetch()`. If the request fails, the widget shows a
  readable error message instead of breaking the page.
- **Dark / light theme toggle** — one button in the header swaps the entire
  colour scheme by reassigning CSS custom properties on `body.theme-dark`.
- **Persistent preference** — the selected theme is written to `localStorage`
  and restored on load, so a returning reader keeps their choice across
  reloads and new tabs.
- **Accessible colour pairs** — every text/background pair in both themes
  meets the WCAG AA contrast minimum of 4.5:1.
- **Responsive layout** — the page is centred, capped to a readable width, and
  works down to phone widths.

## Technologies Used

- **HTML5** — semantic structure (`header`, `main`, `section`)
- **CSS3** — custom properties (design tokens), a reset, and theming by
  overriding role-named tokens on a single class
- **JavaScript (ES6)** — `fetch()` with promise chaining, DOM manipulation via
  `classList` and template literals, and the `localStorage` API
- **Git / GitHub Pages** — version control and static hosting

## Live Site

https://kadenfedele.github.io/dashboard1/
