## LLM README: Game Souls Library

This file orients a language model working with this library. Read it first, then follow LLM_SOUL_GUIDE.txt for the full procedure.

### What This Library Is

A "soul" is a design philosophy that makes a family of games feel the way they do (for example, "Death is not failure; it is the curriculum"). Souls are not genres. Two shooters can have different souls, and a card game can share a soul with a stealth game.

The library has three layers:

| Layer | Folder | Use It To |
| --- | --- | --- |
| Foundational | axes/ | Place a game on six axes: failure, information, authorship, power, tone, structure. |
| Component | components/ | Recognize the reusable building blocks a game uses (13 components). |
| Soul | souls/ | Compare against 11 existing souls, and hold only what is unique to each. |

archive/ contains older single-file versions of the souls. Do not treat them as current; the souls/ folder is the source of truth.

### What You Will Usually Be Asked to Do

1. **Analyze a game:** Break an existing game into axis positions, components, and leftover unique elements ("residue").
2. **Classify a game:** Decide whether it belongs to an existing soul, is a variant of one, is a blend of two, or needs a new soul.
3. **Write a new soul:** Turn the residue into signature pillars and write souls/<name>.txt using the template.
4. **Instill a soul:** Given a target game in development, find the gaps between it and a chosen soul, and recommend changes.

All four tasks use the same core procedure in LLM_SOUL_GUIDE.txt.

### Reading Order

1. README.txt: the human overview, including the soul-by-axis table and the component matrix.
2. LLM_SOUL_GUIDE.txt: the procedure, key questions, component fingerprints, and output formats.
3. The axis and component files relevant to the task.
4. The two or three souls/ files closest to the game being analyzed.

You do not need to read every file for every task. Start from the README tables and read files on demand.

### Ground Rules

* **Evidence, not vibes.** Every axis position and component claim must cite a concrete mechanic, system, or design decision in the game. "It feels dark" is not evidence; "saves require a consumable item" is.
* **Don't invent game facts.** If you are not confident about how a game works, say so, mark the claim as uncertain, and ask the user. A wrong fact produces a wrong soul.
* **Don't duplicate components.** If a rule already exists in a component file, reference the component instead of rewriting the rule inside a soul.
* **Residue is the point.** The value of an analysis is in what is left over after axes and components are accounted for. If there is no residue, say the game belongs to an existing soul.
* **Keep the house style.** Match the tone and structure of existing files: bold rule names, italic examples, Symptom/Fix failure modes, a litmus table, and a closing quote.
* **Update the indexes.** If you add a soul or component, update the tables in README.txt and the "Used by" lines in the affected component files.
