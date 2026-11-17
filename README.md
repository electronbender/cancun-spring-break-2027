# Cancún Spring Break 2027

A single-page spring break site for Cancún, March 2027. Everything lives in `index.html`: no build step and no dependencies.

**Live site:** https://electronbender.github.io/cancun-spring-break-2027/

## Features

- **Prefilled prompt buttons** fill in the trip planner with ready-made requests.
- **"Ask with" AI picker:** choose Claude, ChatGPT, Perplexity, Copilot, Grok or Google AI Mode. Every prompt link on the page opens in the assistant you pick. Works like springbreak.com's picker.
- **Tour operators:** StudentCity, STS Travel and Inertia Tours, the student tour companies that sell Cancún packages.
- **Hotel cards** have a **Book with tour operator** dropdown and a **Book direct** button. The dropdown lists only the operators that sell a package for that hotel.
- **Excursion cards** have a **Book direct** dropdown, listing official providers such as Grupo Xcaret, and a **Book with tour operator** dropdown when an operator sells that excursion.
- **Top 8 nightclubs:** Coco Bongo, Mandala, Mandala Beach, Señor Frog's, La Vaquita, Congo Bar, H Roof and Rakata, each with a link to its official ticket and table booking page.
- **Party packages:** the real VIP party packages sold by STS Travel and Inertia Tours, with Buy buttons that open the operator's own site.
- Excursions, spring break weeks, FAQ and a countdown.

## Updating data

All data is at the top of the `<script>` in `index.html`:

| What | Variable |
|---|---|
| Hotels and which operators sell them | `hotels` (each hotel's `ops`) |
| Tour operators | `operators` |
| Operator party packages | `partyVendors` |
| Nightclubs and their booking links | `clubs` |
| Excursions, direct providers and operators | `excursions` (each one's `direct` and `ops`) |
| AI assistants | `ENGINES` |
| Prompt buttons | `prompts` |

Which operators sell which hotels was checked on the operators' own sites on Nov 16, 2026. The "7 nights from" hotel prices are sample figures.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
