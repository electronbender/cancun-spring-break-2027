# Cancún Spring Break 2027

A single-page spring break site for Cancún, March 2027. Everything lives in `index.html`: no build step and no dependencies.

**Live site:** https://electronbender.github.io/cancun-spring-break-2027/

## Features

- **Prefilled prompt buttons** fill in the trip planner with ready-made requests.
- **"Ask with" AI picker:** choose Claude, ChatGPT, Perplexity, Copilot, Grok or Google AI Mode. Every prompt link on the page opens in the assistant you pick. Works like springbreak.com's picker.
- **Tour operators:** StudentCity, STS Travel, Inertia Tours, StudentEscape, EF Ultimate Break and ISTours, each marked with whether it sells Cancún.
- **Hotel cards** have a **Book with tour operator** dropdown and a **Book direct** button. The dropdown lists only the operators that sell a package for that hotel.
- **Party packages:** the real VIP party packages sold by STS Travel and Inertia Tours, with Buy buttons that open the operator's own site.
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

Which operators sell which hotels was checked on the operators' own sites on Nov 16, 2026. The "7 nights from" hotel prices are sample figures.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
