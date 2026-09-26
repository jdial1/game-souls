## Game Souls

A design library for the distinct "souls" of influential games. Each soul is a design philosophy, not a genre, and each one is built from three layers.

### The Three Layers

| Layer | Folder | What It Holds | Question It Answers |
| --- | --- | --- | --- |
| **Foundational** | axes/ | Six questions every game must answer, each with a spectrum of named positions. | "Where does this game stand?" |
| **Component** | components/ | Reusable design principles shared by several souls, each written once, with rules, costs, failure modes, and per-soul tuning. | "What building blocks does it use?" |
| **Soul** | souls/ | Compositions: a philosophy, a set of axis positions, a list of components, and only the pillars that are unique to that soul. | "What makes it *this* soul and not another?" |

Three folders sit beside the layers:

| Folder | What It Holds |
| --- | --- |
| pitfalls/ | A library of named design failures, one file each (what happens, the symptom, the fix, related pitfalls), indexed by symptom in pitfalls/README.txt. |
| instances/ | Soul instances: the soul of one specific game, built phase by phase with SOUL_INSTANCE_GUIDE.txt. Includes a template and a worked example. |
| frameworks/ | Summaries of the older frameworks the library borrows from (MDA, Gameplay Design Patterns, Machinations, Game Feel, the Gamer Motivation Model, the Game Ontology Project, Koster's grammar, TV Tropes), what was taken from each, and what the library deliberately doesn't adopt. |

Every component file opens with relationship tags (**Requires**, **Supports**, **Conflicts With**), so conflicts between building blocks are visible before a design is built on them.

archive/ holds the original single-file versions of the first nine souls, untouched.

**For language models:** start with LLM_README.txt, then follow LLM_SOUL_GUIDE.txt to analyze a game, classify it, write a new soul, or instill a soul into a game in development, and SOUL_INSTANCE_GUIDE.txt to build a new game's soul from its first idea to ship.

### Axes (Foundational Layer)

* **axes/failure.txt:** What happens when the player loses?
* **axes/information.txt:** How much does the player know, and how do they learn it?
* **axes/authorship.txt:** Who writes the story the player remembers?
* **axes/power.txt:** What kind of power does the player have?
* **axes/tone.txt:** What emotional register does the game hold, and what kills it?
* **axes/structure.txt:** How is play packaged in time?

### Where Each Soul Sits

| Soul | Failure | Information | Authorship | Power | Tone | Structure |
| --- | --- | --- | --- | --- | --- | --- |
| Looking Glass | Costly | Observed | Designer Space, Player Solution | Toolkit | Tense Paranoia | Persistent World |
| Dwarven | Terminal | Total / Oblique | System-Authored | Custodial | Tragicomic | Sandbox Chronicle |
| Loathing | Costly | Oblique | Player-Authored Build | Optimization | Deadpan Absurd | Rebirth Account |
| Ashen | Punishing but Legible | Oblique / Total | Designer Space, Player Solution | Earned Mastery | Elegiac | Persistent World |
| Hearthian | Trivial | Oblique | Designer-Authored | Understanding | Wonder | Single Journey |
| Elysium | Narrative | Filtered | Player-Authored Self | Social / Interior | Tragicomic | Single Journey |
| Spire | Punishing but Legible | Total | Player-Authored Build | Optimization | Cool Focus | Runs |
| Toybox | Trivial | Taught | Designer-Authored | Kinetic | Joyful | Levels |
| Mansion | Costly | Hidden | Designer-Authored | Poor | Dread | Single Journey |
| Containment | Costly | Total / Observed | Player-Authored Build | Optimization | Watchful Calm | Rebirth Account |
| Ampersand | Trivial / Narrative | Sealed | Mutual | Understanding | Plain Warmth | Ritual |
| Gauge | Forgone | Total / Taught | Kin-Authored | Surplus | Unhurried Warmth | Persistent World |
| Casebook | Trivial / Costly | Fair Play | Designer-Authored / Player Solution | Understanding | Armchair Intrigue | Serial |
| Chorus | Punishing but Legible | Total (taught through sound) | Designer-Authored | Kinetic | Cool Focus / Joyful | Levels |
| Swarm | Punishing but Legible | Total | Player-Authored Build | Optimization | Cool Focus / Deadpan Absurd | Runs |
| Tapestry | Narrative / Terminal | Total / Oblique | System-Authored | Custodial | Armchair Intrigue | Sandbox Chronicle |
| Assembly | Trivial | Total | Player-Authored Build | Optimization | Cool Focus | Persistent World |
| Tribunal | Terminal (for the match) | Hidden (asymmetric) | Mutual | Social / Interior | Tense Paranoia | Runs (matches) |
| Tether | Costly | Hidden | Player-Authored Build / System-Authored | Toolkit / Earned Mastery | Dread / Tense Paranoia | Runs feeding a Rebirth Account |
| Vigil | Costly | Total / Taught | Player-Authored Build | Optimization | Answerable Vigilance | Career |

### Components Used by Each Soul

| Component | Looking Glass | Dwarven | Loathing | Ashen | Hearthian | Elysium | Spire | Toybox | Mansion | Containment | Gauge | Ampersand | Casebook | Chorus | Swarm | Tapestry | Assembly | Tribunal | Tether | Vigil |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| legible_failure | | x | | x | x | | x | | x | x | x | | x | x | x | x | x | x | | x |
| failure_as_content | | x | | x | x | x | | | | | | x | | | | x | | | |  |
| systemic_consistency | x | x | | | x | | | x | | x | x | | x | x | | x | x | | |  |
| living_world | x | x | | x | | | | | x | | | | | | | x | | | x |  |
| environmental_storytelling | x | | | x | x | | | | x | | | | x | | | | | | |  |
| trusting_the_player | x | | x | x | x | | | x | | x | x | x | x | | | | x | | | x |
| interlocking_space | x | | | x | x | | | | x | | | | | | | | | | x |  |
| scarcity_economy | | x | x | | | | x | | x | x | | x | x | | x | x | x | | x | x |
| synergy_engines | x | | x | | | | x | | | x | | | | | x | | | | | x |
| difficulty_ladder | | | x | | | | x | | | x | | | x | x | x | | | | | x |
| theme_as_mechanic | | | x | | | x | | | x | | x | x | x | x | | | | x | |  |
| diegetic_interface | x | | | x | | | | | x | | x | | | | | | | x | x |  |
| shared_discovery | | | x | x | x | | | | | x | | | | | | | | x | |  |
| social_safety | | | | | | | | | | | x | x | | | | | | | | x |
| interface_voice | | | | | | | | | | x | x | x | x | x | | | | | |  |
| audio_information | | | | | | | | | x | x | | | | x | | | | | x | x |
| workbench | | | | | | | | | | x | | | | | | | x | | | x |
| automation | | | | | | | | | | x | x | | | | x | | x | | |  |
| match_integrity | | | | | | | | | | | | | | | | | | x | x |  |
| kinetic_profile | | | | x | | | | x | x | | | | | x | | | | | |  |

### How to Use This Library

**To design a new game:** Build a soul instance with SOUL_INSTANCE_GUIDE.txt, copying instances/TEMPLATE.txt. Each phase fills one section of the instance and ends in a gate:

| Phase | Name | What It Settles |
| --- | --- | --- |
| 0 | Seed | Three verbs, the fortieth-minute feeling, and the story players tell the next day |
| 1 | Soul Choice | Adopt, Blend, or Forge a soul, and name the ideal player |
| 2 | Axis Commitment | Six positions, their tensions, and the banned mechanics |
| 3 | Component Bill | Components, tunings, resolved conflicts, and the economy's shape |
| 4 | Pillar Translation | The soul's rules rewritten for this genre, and the Instance Litmus |
| 5 | Verb Prototype | The smallest playable thing, tested for the intended dynamic |
| 6 | Soul Slice | One full loop, failure included, tested for the tone and against the pitfalls |
| 7 | Production Guard | A Feature Gate for every feature, and a Soul Ledger for every deviation |
| 8 | Drift Audit and Lock | A pre-ship instillation on your own game, and the accepted costs |
| 9 | Live and Feedback | Live changes through the gate, and what the game taught returned to the library |

instances/the_pass.txt is a worked example.

**To study an existing soul:** Read the soul file first, then follow its component references for the shared rules, costs, and failure modes.

**To blend two souls:** Compare their axis rows. Where they agree, the blend is easy. Where they disagree, pick one to lead (for example, Mansion + Looking Glass gives *Prey* and *System Shock*: Poor vs. Toolkit power, resolved deliberately).

### Adding a New Soul

Create souls/<name>.txt with these sections, in order:

1. Title, subtitle, philosophy, and surface/beneath description
2. Axis Positions (a table covering all six axes)
3. Psychological Target (the six motivation pairs rated High, Medium, or Low, with reasons and a design note; the ideal player, never a market)
4. Components (each referenced by path, with a one-line note on how this soul tunes it)
5. Signature Pillars (only rules that aren't already in a component)
6. Variants & Exceptions (where the example games bend the rules)
7. What This Soul Costs (soul-specific costs only)
8. How It Fails (soul-specific failure modes, one line each, each with its own file in pitfalls/)
9. Neighboring Souls (the closest souls and what separates them)
10. Litmus Test and closing quote

Aim for 1,300–2,400 words. A soul much longer than that is usually holding rules that belong in a component, or implementation detail that belongs in the game's own design docs.

A new component is justified only by a systemic philosophy that appears in two or more souls and fits no existing component. A feature (a double jump, a skill tree, a health potion) is never a component; add it as a tuning note. See "What We Deliberately Don't Adopt" in frameworks/README.txt.

If a new soul repeats a rule that appears in another soul, move that rule into a component (a new one, or an existing one) and reference it from both.
