# The World Daily — Wednesday 25 November 2026

[![news-image-20261125](https://make.fun/badge/news-image-20261125.svg)](https://make.fun/bounty/news-image-20261125)
[![rank](https://make.fun/badge/news-image-20261125/bee6en9/news-image-20261125/rank.svg)](https://make.fun/bounty/news-image-20261125)
[![reward](https://make.fun/badge/news-image-20261125/bee6en9/news-image-20261125/reward.svg)](https://make.fun/bounty/news-image-20261125)

[The World Daily — Wednesday 25 November 2026](https://make.fun/bounty/news-image-20261125)

One page. One day. Every story dated **Wednesday 25 November 2026**.

A classic newspaper front page summing up the world's news of 25 November 2026:
38 stories from 8 regions, drawn entirely in code. Three lead stories — the
Israeli strike that killed a senior Hamas security chief in Gaza, the Russian
strikes that cut power in five Ukrainian regions, and the Houthi claim of
strikes on Ras Tanura and Riyadh — plus ten illustrated briefs (Shenzhou-24
and Pakistan's first astronaut, US tariffs on 14 partners, Bitcoin below
$60,000, two tankers mined in Hormuz, drones over Samara refineries, Hera's
first close-up of Dimorphos, the Cartagena hostage rescue, Asia's market
plunge, the Solomon Islands security pact, and the record Canary Islands
arrivals), a numbered world map, 25 more stories, and a DATE CHECK box naming
the near-miss stories we deliberately left out (the Huawei verdict, Dell's
record quarter, the EU fines on Apple and Meta, the DRC ceasefire talk, the
Kashmir deaths, the Dow's first close above 50,000) because they did not
happen on 25 November.

## How it is made

`main.ts` (Node 22, standard library only, no network) copies `entry.png`
(1024×1024, 210,937 bytes) to the output directory. The image itself was drawn
once, deterministically, with a Python/PIL script (`draw_news.py` in the build
notes): flat illustrated scenes per story, a serif masthead and serif
headlines, clean sans decks, a six-number KPI strip of hard news figures
($58,325 Bitcoin, $4.94bn November ETF outflow, 2,100 Canary arrivals,
-6.16% Kospi, 2 tankers mined, 9 dead in Bogor), an eight-region bar, and a
bright numbered map. Every card carries a deck, a source, and a
CONFIRMED/REPORTED label. The program is deterministic: two runs write
byte-identical PNGs.

## Run

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```
