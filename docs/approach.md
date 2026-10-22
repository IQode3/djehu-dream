# Locked decisions

22 October 2026. This file is our decisions. The organizer's guide is not copied here. HackOS is the source for rules and sponsor setup.

## Problem

Fragment and witness only. The run starts from a dream note that is already written.

The user is a person who has already written a dream. The decision is which links a passage supports, and which are refused. The output is one graph and one card. The association line stays blank. There is no sentence about the dreamer's life.

The practice is von Franz's report in *The Way of the Dream*: another person is a better slant than reading the dream alone. No sentence from that book is stored here.

## Level

Level 2, ambitious. Solo. Four agents: planner, witness, evaluator, reporter. One revision. The evaluator sends a weak link back once, then it stays a refusal.

If the graph or a sponsor connection slips, the cut is a passage or the screen.

## Track

**The Agent That Can Explain Why.** One question. The two passages disagree, so the explanation has something to refuse. That disagreement is the shape of the data. It is not a second track. This is not a Wildcard entry. There is no earlier product to extend.

## Data

Three local files. The judged run does not download and does not call an API. `SAMPLE_MODE=true` reads them. The trace says `fallback` when a web page was not used.

1. A short dream note we write. Not a personal dream. Not a report copied from DreamBank or from a book.
2. One short passage from Sigmund Freud, *The Interpretation of Dreams*, A. A. Brill, 1913, Gutenberg 66048. The remembered dream disguises a wish.
3. One short passage from a public-domain English translation of Aristotle, *On Dreams*. Most dreams are leftovers of waking sensation.

Jung, "The Psychology of Dreams" (1916), chapter XII, stays a link. The chapter is not stored, and neither is a paragraph from it. Detail is in `docs/research/data-slice.md`.

## Agents

The planner writes nodes and edges from the note only. The witness proposes a link only with the sentence that bears on that edge. If the two passages disagree, both proposals stay. The evaluator returns a weak proposal once, then refuses it. The reporter draws solid links, dashed refusals, and an empty association line.

Shared state is the card. There is no fifth agent.

## Sponsors and stack

| Requirement | This build |
|---|---|
| Zetaris | Holds the two passages apart |
| Meterless | Holds the proposals, the refusals, and the blank line |
| Cursor | The editor |
| NVIDIA | May extract the symbols and phrase the card only from links the evaluator kept |
| Stack | Python, FastAPI, REST. React, TypeScript, Tailwind. React Flow for the graph |
| Secrets | Environment variables only. `.env.example` has placeholders |
| Runtime | One dream, two passages, one retry. Target 5–10 minutes |

## Score

| Question | Score |
|---|---:|
| Can we explain the problem clearly in 30 seconds? | 2 |
| Do we know who the user is? | 2 |
| Do we have accessible data? | 1 |
| Can we build a working version in 144 hours? | 2 |
| Can it run quickly and predictably? | 2 |
| Do Zetaris and Meterless have a real role in the build? | 1 |
| Do agents interact more than once? | 2 |
| Is there critique, validation, or retry? | 2 |
| Can we show useful output in a 1–4 minute demo? | 2 |
| Can we document limitations clearly? | 2 |
| **Total** | **18** |

The two 1s are the first tasks: write the three files, and connect Zetaris and Meterless from their HackOS folders.

## Five checks

1. Yes. The user and the card are named above.
2. Yes. The dream note is ours. Freud's 1913 English and a public-domain Aristotle can be stored.
3. Yes, at this cut, with the sponsor roles above.
4. Yes. The evaluator sends a weak link back once.
5. Yes. The demo is one kept link, one refused link, and the blank line.

## Submission

Demo, 1–4 minutes. Slides. Repo with README, sample input, sample output, and a trace. A short account of Zetaris, Meterless, Cursor, and where NVIDIA contributes. Submit on HackOS before 27 October, 23:45 UTC.

Declare these planning notes if the form asks. No product code was written before 22 October, 00:00 UTC.
