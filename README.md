# AppADay 103 - Bracket Maker

**Type in the names, then tap the winner of each match.**

**Live:** https://augustineiacopelli.github.io/appaday-103-bracket-maker/

**Portfolio:** https://augustineiacopelli.github.io/appaday/

App 103 of the AppADay project, a daily discipline and public portfolio project by Augustine Iacopelli. One complete, functional, mobile-friendly web app designed, built, and published every single day.

## What it does

Enter a list of names, choose how the draw is filled, and tap winners to advance them through a single-elimination bracket. Good for a family game night, a homebrew tasting showdown, or anything else where somebody has to be declared the winner.

The draw can be seeded in the order you typed the names, shuffled at random, or set by a round robin play-in. Fields that are not a power of two are padded to the next one with byes, and byes always land on the top seeds. Everything is saved as you go and the whole tournament fits in a link you can hand to someone else.

## The draw

Seeded mode treats the first name as the top seed and pairs 1 against the last, 2 against the second to last, and so on, so the strongest and second strongest can only meet in the final. Shuffled mode randomizes positions before applying the same structure.

Byes are computed rather than approximated. A field of five becomes a bracket of eight, the top three seeds sit out the first round, and four plays five. Those matches resolve themselves the moment the bracket is built.

## Regions

The field can be split into regions of four, eight, or sixteen, each seeded independently from 1. Sixty-four entrants in regions of sixteen gives four regions seeded 1 through 16 rather than one line seeded 1 through 64.

Entrants are spread across regions on an S-curve rather than in blocks: overall seeds 1 through 4 become the top seeds of the four regions, then 5 through 8 come back the other direction as the 2 seeds, and so on. The regions are placed so the strongest meets the fourth strongest in the semifinal and the second meets the third, which is how the NCAA does it.

Region names are yours to set, comma separated, defaulting to Region A onward. They run down a sticky rail on the left so they stay visible while you scroll a wide bracket sideways, and dashed dividers mark the boundaries until the regions merge.

## Round robin play-in

Optional pools of three, four, five, or six can be played first to set the seed line. Nobody is eliminated; the pools exist only to decide the order.

Pools are filled on the same S-curve so they are balanced rather than stacked. Every member plays every other once. Tap a name to give it the win or D for a draw, and tap again to clear. Three points for a win, one for a draw, with a live standings table above each pool's game list.

Ties break on head-to-head points among only the tied entrants, then on wins, then on the order you originally typed. When a three-way cycle defeats all of that, small arrows let you set the order by hand; touching a result in that pool discards the manual order so it cannot go stale.

Once every game is in, the standings convert to a seed line by finishing position: every pool winner first, ordered by points then wins, then every runner-up, and so on. That line feeds the bracket exactly as if it had been typed in that order, and works alongside regions.

## Other things it does

- Optional third place match, contested by the two semifinal losers and reset automatically if a semifinal result changes
- Changing a decided match clears everything downstream of it and says so
- Next match jumps to and focuses the first undecided match
- Champion plate with the path to the title, listing everyone beaten along the way
- Round robin standings fold into a collapsible panel under the finished bracket
- Copy link carries the whole tournament, results included, in the URL
- Print produces a clean black-on-white draw sheet or pool scoring sheet, landscape

## Built with

Single file. Vanilla HTML, CSS, and JavaScript. No frameworks, no build step, no dependencies beyond Google Fonts. Bebas Neue, Barlow Condensed, and Space Mono over a mid-century enamel scoreboard palette. State persists in localStorage and travels in the URL hash; nothing is sent anywhere.

## Rules of the project

One app ships every day. No skip days, no carryover. Each app is single-purpose, usable on a 375px phone, intentionally designed, and live at its own URL the day it is built.

---

*Ship something every day. It compounds.*
