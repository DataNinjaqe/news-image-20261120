# The World in One Day — Friday 20 November 2026

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/DataNinjaqe/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/DataNinjaqe/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

Entry for make.fun's [**news-image-20261120** bounty](https://make.fun/bounty/news-image-20261120): sum up the world's news of
Friday 20 November 2026 in one image.

## The image

A newspaper front page, 1024 × 1024, rendered from `image.html` with headless
Chromium and stored as `entry.png`:

- **Diplomacy, Shenzhen** — Trump, Xi and Putin hold the first three-way summit
  of the three largest nuclear powers; a joint peace declaration and more
  nuclear-risk talks.
- **Markets** — Anthropic's $81bn IPO, the largest ever; shares open 34% up,
  then slide as the AI sell-off spreads (Nasdaq −2.25%, Kospi −5%).
- **War in Ukraine** — Russia fires 400+ drones and 110 missiles at Kyiv; two
  missiles fall inside Poland; Ukraine hits the Kerch Bridge.
- **Weather** — Cyclone Akvan makes landfall in Odisha, the first November
  landfall there since 1995; 300,000 evacuated.
- **Technology** — Microsoft 365 outage lasts 9+ hours worldwide; the US
  national cyber director steps down the same day.
- **Justice** — The World Court finds Myanmar responsible for genocide against
  the Rohingya.
- Also: EU–UK summit in Brussels, COP31 talks past deadline, US–China accord
  on human oversight of military AI, Strait of Hormuz shipping under strain.

Every fact was checked against reporting published on 20 November 2026 before
the image was drawn.

## How it is built

`image.html` is the source of the front page. It is rendered once, by hand,
into `entry.png`:

```sh
chromium --headless=new --window-size=1024,1024 \
  --screenshot=entry.png file://$PWD/image.html
```

`main.ts` (Node 22, standard library only) copies `entry.png` to the output
directory, so both graded runs write identical bytes.

## Files

- `entry.png` — the image (1024 × 1024 PNG)
- `image.html` — the front page source the image was rendered from
- `main.ts` — the entry program
- `LICENSE` — MIT

## License

MIT. See `LICENSE`.
