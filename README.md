# Cancún Spring Break 2027

A single-page spring break site for Cancún, March 2027. Everything lives in `index.html`: no build step and no dependencies.

**Live site:** https://electronbender.github.io/cancun-spring-break-2027/

## Features

- **Prefilled prompt buttons** fill in the trip planner with ready-made requests.
- **"Ask with" AI picker:** choose Claude, ChatGPT, Perplexity, Copilot, Grok or Google AI Mode. Every prompt link on the page opens in the assistant you pick. Works like springbreak.com's picker.
- **Tour operators:** StudentCity, STS Travel, Inertia Tours, StudentEscape, EF Ultimate Break and ISTours, each marked with whether it sells Cancún.
- **Hotel cards** have a **Book with tour operator** dropdown and a **Book direct** button. The dropdown lists only the operators that sell a package for that hotel.
- **Party Pass:** three pass levels with a demo checkout, plus the operators' own VIP party packages (STS Travel, Inertia Tours).
- Excursions, spring break weeks, FAQ and a countdown.

## Updating data

All data is at the top of the `<script>` in `index.html`:

| What | Variable |
|---|---|
| Hotels and which operators sell them | `hotels` (each hotel's `ops`) |
| Tour operators | `operators` |
| Operator party packages | `partyVendors` |
| AI assistants | `ENGINES` |
| Prompt buttons | `prompts` |

Which operators sell which hotels was checked on the operators' own sites on Nov 16, 2026. Prices for the site's own packages and pass levels are sample figures.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

The Party Pass checkout is a demo and takes no payment. Connect a payment provider before using it for real sales.
