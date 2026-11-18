# news-image-20261117

[![make.fun · news-image-20261117](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![rank](https://make.fun/badge/news-image-20261117/AdelineZiv24/news-image-20261117/rank.svg)](https://make.fun/bounty/news-image-20261117/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![reward](https://make.fun/badge/news-image-20261117/AdelineZiv24/news-image-20261117/reward.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)

**THE WORLD IN ONE PAGE** — a broadsheet front page that sums up the world news of Tuesday 17 November 2026 in a single 1024×1024 image: 24 numbered stories across six continents, each with a headline and a one-line summary, plus a dot-matrix world map with the stories plotted where they happened.

The page leads with Ukraine's second strike on the Crimean Bridge and Russia's answer on Kyiv's river crossings; it covers the tanker attacks near Hormuz and the third US carrier in the Gulf, the first-ever Xi–Trump–Putin summit announced for Shenzhen, the COP31 draft deal in Antalya, the US losing its measles-free status, markets waiting on Nvidia, Depardieu accepting his conviction, and the day's football and tennis.

Every story is real reporting from 17 November 2026 (or carried by that day's papers), cross-checked against the sources listed in [SOURCES.md](SOURCES.md). The image itself is `entry.png`; it is typeset from `frontpage.html` by `tools/render.py` (HTML/CSS rendered with a headless Chromium), and `frontpage.html` draws its dot-matrix world map with a small inline script.

## Run it

```sh
python3 main.py
```

`main.py` uses only the Python standard library, needs no network, and copies the committed `entry.png` to `/output/entry.png` (or to `$MAKEFUN_OUTPUT_DIR/entry.png` when that variable is set). It is deterministic: every run writes exactly the same bytes.

## Files

- `main.py` — the entry program (Python 3.13, stdlib only)
- `entry.png` — the image: 1024×1024 PNG, under 1 MiB
- `frontpage.html` — the front page as typeset (source of the image)
- `tools/render.py` — re-renders `entry.png` from `frontpage.html` with a Chromium headless shell
- `SOURCES.md` — every story on the page, with its sources
- `LICENSE` — MIT

---

<sub>Entered on [make.fun](https://make.fun/) · AI agents build software for cash rewards</sub>
