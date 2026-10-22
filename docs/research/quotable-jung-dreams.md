# First agent loop

This is the loop the software runs. It matches the card locked in `docs/approach.md`. Later passes can change the steps. This file is only the first setup.

The loop does not explain the dreamer's life. It does not fill the association line.

## Inputs

- One dream note we wrote.
- Two short passages, kept apart. They are allowed to disagree. Passage A is Freud, Brill 1913. Passage B is Aristotle, *On Dreams*. The pair is named in `docs/research/data-slice.md`.

## Agents

Four roles. One revision, then a stop.

1. **Planner.** Read only the note. Make a node for each figure, place, and object the note names. Make an edge only where the note itself relates two nodes. Label every node with the note's word. Do not attach a meaning. If the note is unclear, mark the item unknown and leave it unknown.
2. **Witness.** For each edge, look in both sources. Propose a link only as: the edge, which source, a passage, and the sentence in that passage that bears on the edge. If a source has no such passage, propose nothing from that source. If the two passages make different claims about the same edge, keep both proposals. Do not collapse them into one.
3. **Evaluator.** Check the proposal against the note and the passage. Send it back once if any of these fail:
   - the node or the edge is not in the note
   - the passage does not support that edge
   - the proposal replaces the note's word with another word
   After one return, a proposal that still fails becomes a refusal. The refusal stays visible.
4. **Reporter.** Write the graph and the card from what survived. Solid edge: accepted, with the passage. Dashed edge: refused, with the reason. The association line is empty.

## Shared rules

- A node that the note does not name is not created.
- An edge that the note does not state is not created.
- A passage that does not support the edge is not attached.
- The card has no sentence about what the dream means for the dreamer's life.

## The two sources

The judged pair is locked in `docs/research/data-slice.md`.

| Slot | Text | What the witness may take from it |
|---|---|---|
| Passage A | Sigmund Freud, *The Interpretation of Dreams*, translated by A. A. Brill (1913), Gutenberg 66048 | The remembered dream disguises a wish. The sentence has to bear on the edge. |
| Passage B | A public-domain English translation of Aristotle, *On Dreams* | Most dreams are leftovers of waking sensation. The sentence has to bear on an edge the note stated. |

They disagree on purpose. Passage A looks backward to a hidden wish. Passage B does not treat the dream as a message or a disguise. The reporter shows both when both bear on the edge. Neither passage is allowed to write what the dream means for the dreamer's life.

Jung's 1916 chapter XII is a link only. None of his wording is stored. He died in 1961. In a life-plus-seventy country his text generally runs through 2031. This project is being written in Austria.

## When a source or a model is down

`SAMPLE_MODE=true` reads the three local files: the dream note, passage A, and passage B. Label that trace `fallback`. The graph shape does not change.
