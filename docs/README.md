# Djehu

Locked 22 October 2026. The build window is open. Official rules and sponsor setup stay on HackOS. They are not copied here.

## What this is

Guardian of Dream Knowledge. The practice comes from Marie-Louise von Franz, *The Way of the Dream*: another person, even a clumsy one, is a better slant than reading a dream alone. Her book is the reason. No sentence from it is stored here.

Track: **The Agent That Can Explain Why.** Solo. Level 2.

A person has already written a dream. The agent breaks that note into the symbols and relationships the note stated, sets two short passages beside them, and keeps a link only where a passage supports it. A refused link stays visible. The association line stays blank. The agent does not say what the dream means for the dreamer's life.

> We are building an agent that helps a person who has written down a dream resist reading it only through their own assumptions, by breaking that account into symbols and the relationships between them and setting those symbols beside sourced parallels, using the dream note and two short passages that can disagree, producing a graph of what the dream stated, which links a passage supports, which links are refused, and a blank line for the dreamer's own association.

## The judged run

| Piece | What it is |
|---|---|
| Dream | A short note we write during this window. Not a personal dream, and not a report taken from a book or a bank |
| Passage A | Freud, *The Interpretation of Dreams*, A. A. Brill, 1913, Gutenberg 66048. One short passage: the remembered dream disguises a wish. Freud died in 1939 and Brill in 1948 |
| Passage B | A public-domain English translation of Aristotle, *On Dreams*. Most dreams are leftovers of waking sensation. Jung's 1916 chapter is a link only. His text runs through 2031 in Austria, so none of it is stored |
| Agents | Planner, witness, evaluator, reporter. One retry, then a refusal |
| Output | One graph and one card. React Flow shows it |

`SAMPLE_MODE=true` reads the three local files. If Zetaris or the model is down, the trace is labeled `fallback` and the graph shape stays the same.

Zetaris holds the two passages apart. Meterless holds the proposals, the refusals, and the blank line. Cursor is the editor. An NVIDIA model may extract the symbols and phrase the card only from links the evaluator kept. Sponsor setup comes from each sponsor's folder on HackOS. No sponsor API is invented here.

Stack: Python, FastAPI, REST. React, TypeScript, Tailwind.

## Files

| File | What it is |
|---|---|
| `docs/approach.md` | The locked decisions |
| `docs/research/quotable-jung-dreams.md` | The agent loop |
| `docs/research/data-slice.md` | The three files, and what stays out |
| `docs/research/dream-corpus.md` | Why the modern Jung books are not stored |

The three sample files are added during this window:

```text
data/sample/dream.md
data/sample/passage_a.md
data/sample/passage_b.md
data/README.md
```

Planning notes written before 22 October, 00:00 UTC are declared if the form asks. No product code was written before the window.

## Still to do first

Put the three files in `data/sample/`. Run the HackOS connection test for Zetaris and Meterless. Until the passages can bear on an edge in the note, the data score stays at 1. Self-score of the cut is 18.
