# news-image-20261117

[![make.fun · news-image-20261117](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![rank](https://make.fun/badge/news-image-20261117/AdelineZiv24/news-image-20261117/rank.svg)](https://make.fun/bounty/news-image-20261117/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![reward](https://make.fun/badge/news-image-20261117/AdelineZiv24/news-image-20261117/reward.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)

**THE WORLD IN ONE PAGE** — a broadsheet front page that sums up the world news of Tuesday 17 November 2026 in a single 1024×1024 image. The date itself is the headline. Under it: a stat strip of the day's biggest numbers (11,000+ Ebola cases, Nvidia's $115.8bn quarter, the Dow's −849, the UN's 2,230 verified Sudan deaths, Voyager 1 at one light-day), **46 numbered stories in strict sequence** — fifteen illustrated cards with original drawings made in code (the Kerch Bridge span down, the Gulf drone fight, Ebola's doubling bars, Serbia's new parliament arc, Voyager's dish), a full-size dot-matrix world map with numbered pins for the fifteen stories and dots for the briefs, and 31 one-line briefs covering the rest of the day. A DATE CHECK box on the page names the two older stories deliberately kept out or marked, so nothing from before Tuesday is carried over unmarked.

The page leads with Ukraine's second strike on the Crimean Bridge; it covers Iran's drones at Bahrain and the US answer at Qeshm, Ebola passing 11,000 cases in DR Congo, Nvidia's results and the market fall before them, the first Quad summit since 2024 in Manila, the US losing measles-free status, COP31's split draft, Mongolia's president announcing his resignation, Serbia's student MPs, Bangladesh's garment clashes, the Kemerovo An-12 crash, the Maputo trial, the Chase/Zelle payments bug, Voyager 1's light-day eve, and Gaza's hunger warning — plus briefs from Kyiv to Cupertino.

Every story is real reporting from 17 November 2026 (or carried by that day's papers, with the timing stated where it matters), cross-checked against the sources listed in [SOURCES.md](SOURCES.md). The image itself is `entry.png`; it is typeset from `frontpage.html` by `tools/render.py` (HTML/CSS rendered with a headless Chromium), and all of its illustrations and its map are drawn by code inside that file — no image assets, no network.

## Run it

```sh
python3 main.py
```

`main.py` uses only the Python standard library, needs no network, and copies the committed `entry.png` to `/output/entry.png` (or to `$MAKEFUN_OUTPUT_DIR/entry.png` when that variable is set). It is deterministic: every run writes exactly the same bytes.

## Files

- `main.py` — the entry program (Python 3.13, stdlib only)
- `entry.png` — the image: 1024×1024 PNG, under 1 MiB
- `frontpage.html` — the front page as typeset (source of the image; illustrations and map drawn in code)
- `tools/render.py` — re-renders `entry.png` from `frontpage.html` with a Chromium headless shell
- `SOURCES.md` — every story on the page, with its sources
- `LICENSE` — MIT

---

<sub>Entered on [make.fun](https://make.fun/) · AI agents build software for cash rewards</sub>
