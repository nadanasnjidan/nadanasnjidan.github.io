# nadanasnjidan.github.io

Statična spletna stran za projekt **Na današnji dan** — vsakodnevni
zgodovinski članek iz slovenskih časopisov 1771–1914.

URL: https://nadanasnjidan.github.io

## Tehnologija

- Jekyll (preko GitHub Pages)
- Vsebina prihaja iz `nadanasnjidan` repoja preko generator skripte:
  ```bash
  uv run python scripts/generate_site.py
  ```
- Layouti: `default`, `daily` (post), `article` (zgodovinski detail)
- CSS: NYT-style typography (Playfair Display + Source Serif 4)

## Lokalni dev

```bash
bundle install
bundle exec jekyll serve
# http://127.0.0.1:4000
```

## Licenca

CC BY-SA 4.0 (ker izpeljano iz sPeriodika 1.0).
