# nadanasnjidan.github.io

Statična spletna stran za projekt **Na današnji dan** — vsakodnevni prikaz zgodovinskih slovenskih časopisov (1797–1914), povezanih z aktualnimi novicami.

URL: https://nadanasnjidan.github.io

## Kako se stran zgradi

Vsebina je **pre-generated statični HTML**, ne Jekyll. Vsaka MM-DD mapa vsebuje samostojno stran.

Generator živi v [nadanasnjidan](https://github.com/nadanasnjidan/nadanasnjidan) repo-ju:

```bash
uv run python scripts/generate_static_calendar.py --news
```

To spiše:
- `MM-DD/index.html` — po ena stran za vsak dan v letu (366)
- `index.html` — landing z dnevnim postom + koledarjem
- `style.css` — skupni CSS

## Deploy

GitHub Pages, avto-build ob `git push origin main`. `.nojekyll` flag onemogoča Jekyll build — Pages serve raw HTML.

## Kaj vsebuje

- **366 pre-generated MM-DD strani** — vse dnevne edicije iz sPeriodika 1.0 korpusa
- **Inline lightbox** — nl.ijs.si scan viewer + Cloudflare Worker PDF proxy (`dlib-proxy.nadanasnjidan.workers.dev`) za dLib.si PDF-je
- **"Danes v novicah"** widget — semantično ujemanje sodobnih novic z zgodovinskimi članki (LLM + FTS hibrid)
- **Deep links** — hash routing (`#slovenec-1914-letnik-42-st-115-JXKPMY12`)

## Licenca

CC BY-SA 4.0 — izpeljano iz **sPeriodika 1.0** (Dobranić, Evkoski, Ljubešić, INZ 2024). ShareAlike obveznost.
