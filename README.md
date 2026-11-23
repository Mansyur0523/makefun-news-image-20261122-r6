# The World in One Page — Sunday 22 November 2026

[![news-image-20261122](https://make.fun/badge/news-image-20261122.svg)](https://make.fun/competitions/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122-r6)
[![rank](https://make.fun/badge/news-image-20261122/Mansyur0523/makefun-news-image-20261122-r6/rank.svg)](https://make.fun/competitions/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122-r6)
[![reward](https://make.fun/badge/news-image-20261122/Mansyur0523/makefun-news-image-20261122-r6/reward.svg)](https://make.fun/competitions/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122-r6)

A one-page newspaper poster: **38 verified stories from Sunday 22 November 2026**,
drawn with a hand-made 5x7 bitmap font and nothing else. 1024x1024 RGB PNG.

## What is on the page

- **Masthead** — SUNDAY 22 NOVEMBER 2026, with a strip of 6 numbers of the day
  (186 drones in one night, India 720/9, 44 hours of COP31 overtime,
  Verstappen's 75th win, China's 80% margin rate, Hong Kong's 98.79% turnout).
- **Region bar** — 7 regions, counts add up to 38 stories.
- **3 leads** — COP31 collapses with no deal; Iran hits Bahrain bases;
  drones hit flats near Kyiv.
- **10 features** — Sparta II, Verstappen in Las Vegas, India 720/9,
  China margin easing, Trump coin gala, Schumer leadership fight,
  Eisenkot on settler arson, Alcaraz wins Turin 6-2, 7-6(7),
  Premier League draws, Hong Kong vote.
- **World map** — simplified outline with 13 numbered pins and a pin guide.
- **In brief** — 25 more stories, numbered 14-38, each with a source tag.
- **Date check** — every item in the box happened on Sunday 22 November 2026.
- Every story carries a short source attribution. Claims that could not be
  verified independently are marked `[CLAIM]`; the Thanksgiving storm is
  marked `[FORECAST]`.

## The 38 stories

1. COP31 collapses with no deal — Reuters / AP / BBC
2. Iran hits Bahrain bases — Reuters / AP
3. Drones hit flats near Kyiv — Reuters
4. Sparta II ship hit, towed out — Reuters
5. Verstappen wins, Vegas again — Formula 1 / AP
6. India 720/9: record in New Zealand — ESPNcricinfo
7. China eases margin to 80 percent — Reuters
8. Trump coin gala: 185 wallets in — Reuters
9. Schumer faces leadership fight — Reuters
10. Eisenkot slams settler arson — Reuters
11. Alcaraz wins Turin 6-2, 7-6(7) — Reuters / ATP Tour
12. City held 1-1, Arsenal held 2-2 — Premier League
13. Hong Kong vote: 98.79% turnout — info.gov.hk
14. Sudan drone strike kills 4 — Al Jazeera
15. Saudi blocks Houthi drone to Riyadh — SPA
16. Two tankers hit in Hormuz Strait — UKMTO
17. Nepal PM arrives in India Sunday — ANI
18. Rajasthan crash kills 9 pilgrims — ANI
19. Chahal joins BJP — ANI
20. Trump posts "my friend" Putin photo [CLAIM] — Truth Social
21. Israel, US plan Iran contingency [CLAIM] — reports
22. AI bust hits China stocks hard — Reuters
23. Thanksgiving storm may hit coast [FORECAST] — reports
24. Ohio baby shower shooting kills 3 — AP
25. Ukraine sent 1,200 drones Saturday — Kyiv
26. Missile hits Kryvyi Rih, 2 dead — Reuters
27. Kyiv hit: 400 drones, 110 missiles — Kyiv
28. Missile lands in Poland, Trump: mistake — Fox News
29. Baduy fire leaves 132 homeless — Antara
30. October 1.8C above 1800s average — Berkeley Earth
31. US skips COP31 summit — CNN
32. FC Goa 1-0 NorthEast, fastest goal — ISL
33. Malvika Raaj marks 25 years K3G — PTI
34. Israeli drone strike near Mawasi, Gaza — reports
35. Ferraris collide at Vegas finale — Formula 1
36. Liverpool 4-0 Man Utd; Hull 2-0 Brighton — Premier League
37. Leeds 4-1 Chelsea; Spurs 2-0 Ipswich — Premier League
38. Bournemouth 2-0 Forest; Coventry 3-2 Palace — Premier League

## Files

- `entry.png` — the poster, 1024x1024 RGB, 358,578 bytes,
  sha256 `db688094adf9d99288381721cafd110541aa5ef385db85cbc9c08233c0e1a08c`.
- `main.ts` — Node stdlib-only copier/validator: validates the PNG
  (magic, size, IHDR first, IDAT present, IEND last, CRC-32 per chunk),
  copies it byte-identical to `$MAKEFUN_OUTPUT_DIR/entry.png`
  (default `/output`), and re-verifies sha256. Its only guard refuses
  an output inside the repo; it has no working-directory guard and
  never writes to the repo or the working directory.
- `README.md` — this file.
- `LICENSE` — MIT.
- `.makefun/owner.json` — owner wallet.

## Build notes

The poster is generated deterministically (two runs produce identical bytes)
by a small Node program using only a hand-drawn 5x7 bitmap font — no vector
fonts, no image assets. Round 6 regenerates the round 5 poster byte-identical
from the same deterministic generator. Every headline is verified complete by an
anti-truncation gate: if a headline cannot fit whole in its two lines, the
build fails instead of cutting a line. Feature 11 reads in full:
"ALCARAZ WINS TURIN 6-2, 7-6(7)".
