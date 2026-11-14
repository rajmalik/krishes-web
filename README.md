# krishes-web

The public website for Krishes Inc., served at **https://www.krishes.com**.

It is plain static HTML, CSS and JS: no framework, no build step, no dependencies.

## Files

| File | What it is |
|---|---|
| `index.html`, `about.html`, `products.html`, `services.html` | The pages |
| `tokens.css` | Design tokens: every colour, font and spacing value |
| `styles.css` | Page styles, built only from the tokens |
| `script.js` | Nav shadow on scroll, copy-email button, scroll reveal |
| `krisheslogo.png`, `meridian-icon.png` | Logo / favicon and the Meridian app icon |
| `vercel.json` | Vercel config (defaults; nothing custom) |
| `.hallmark/` | Notes from the design pass that set up the tokens and fonts |

## Preview locally

```bash
npx serve .
```

Then open http://localhost:3000. Check pages at phone width (375 px) as well as desktop.

## Deploy

Vercel deploys this repo automatically:

- push / merge to **`main`** → production (`www.krishes.com`)
- any other branch or PR → a preview URL posted on the PR

## History

Until November 2026 the site lived in the `krishes-inc/` folder of the private
`rajmalik/proceedings` repo (the Meridian app). Its commits were carried over
with `git subtree split`, so `git log` and `git blame` go back to the first version.
