## LLM README: Game Souls Library

This file orients a language model working with this library. Read it first, then follow LLM_SOUL_GUIDE.txt for the full procedure.

### What This Library Is

A "soul" is a design philosophy that makes a family of games feel the way they do (for example, "Death is not failure; it is the curriculum"). Souls are not genres. Two shooters can have different souls, and a card game can share a soul with a stealth game.

The library has three layers, plus two reference folders:

| Layer | Folder | Use It To |
| --- | --- | --- |
| Foundational | axes/ | Place a game on six axes: failure, information, authorship, power, tone, structure. |
| Component | components/ | Recognize the reusable building blocks a game uses (20 components), each tagged with what it requires, supports, and conflicts with. |
| Soul | souls/ | Compare against 19 existing souls, each holding only what is unique to it. |
| Reference | pitfalls/ | Scan a design for named failures (one file per pitfall, indexed by symptom). |
| Reference | frameworks/ | Understand the older frameworks the library borrows from, and what it deliberately doesn't adopt. |
| Reference | instances/ | See or build the soul of one specific game: a template and a worked example, filled phase by phase. |

archive/ contains older single-file versions of the first nine souls. Do not treat them as current; the souls/ folder is the source of truth.

### What You Will Usually Be Asked to Do

1. **Analyze a game:** Break an existing game into its verbs, axis positions, components, and leftover unique elements ("residue").
2. **Classify a game:** Decide whether it belongs to an existing soul, is a variant of one, is a blend of two, or needs a new soul.
3. **Write a new soul:** Turn the residue into signature pillars and write souls/<name>.txt using the template.
4. **Instill a soul:** Given a target game in development, find the gaps between it and a chosen soul, scan it for pitfalls, and recommend changes, each traced from mechanic to feeling.
5. **Build a soul instance:** Given a new game idea, take it phase by phase from verbs to a chosen soul, committed axes, a component bill, translated pillars, and a litmus the project runs on every feature, then guard it through production and ship.

Tasks 1–4 use the core procedure in LLM_SOUL_GUIDE.txt. Task 5 uses SOUL_INSTANCE_GUIDE.txt, which borrows steps from the core procedure and adds phases, gates, and a ledger of deviations.

### Reading Order

1. README.txt: the human overview, including the soul-by-axis table and the component matrix.
2. LLM_SOUL_GUIDE.txt: the procedure, key questions, component fingerprints, and output formats.
3. The axis and component files relevant to the task.
4. The two or three souls/ files closest to the game being analyzed.
5. For instillation: pitfalls/README.txt.
6. For building an instance: SOUL_INSTANCE_GUIDE.txt, instances/TEMPLATE.txt, and instances/the_pass.txt as the example.

You do not need to read every file for every task. Start from the README tables and read files on demand.

### Ground Rules

* **Verbs before philosophy.** Start every analysis with what the player literally does (the three most frequent actions), not with setting, plot, or genre.
* **Evidence, not vibes.** Every axis position and component claim must cite a concrete mechanic, system, or design decision in the game. "It feels dark" is not evidence; "saves require a consumable item" is.
* **Trace every recommendation.** Write each recommendation as *Mechanic → Dynamic → Tone*. If you can't name what players will do differently, the recommendation isn't ready.
* **Don't invent game facts.** If you are not confident about how a game works, say so, mark the claim as uncertain, and ask the user. A wrong fact produces a wrong soul.
* **Don't invent data you can't observe.** Describe timing and feel in bands (instant, deliberate, committed, cancellable). Never state frame counts, gravity values, or millisecond thresholds.
* **Don't duplicate components.** If a rule already exists in a component file, reference the component instead of rewriting the rule inside a soul.
* **Don't create components for features.** A component is a systemic philosophy shared by two or more souls. A mechanic that fits an existing component is a tuning note.
* **Never define a soul by theme or plot.** "Cyberpunk" and "zombie survival" are not souls. Apply the Integration Check: if the theme can be removed without breaking the mechanic, it isn't the soul.
* **Describe the ideal player, never a market.** The Psychological Target names motivations the design serves, never ages, generations, or spending habits.
* **Residue is the point.** The value of an analysis is in what is left over after axes and components are accounted for. If there is no residue, say the game belongs to an existing soul.
* **Keep the house voice.** Match the tone and structure of existing files: opinionated, specific, quotable. Bold rule names, italic examples, a litmus table, and a closing quote. Framework terms (MDA, Machinations) are for analysis, never for pillar names.
* **Update the indexes.** If you add a soul, component, or pitfall, update the tables in README.txt, the "Used by" and "Tuning by Soul" sections of affected components, the axis tables, and pitfalls/README.txt.
