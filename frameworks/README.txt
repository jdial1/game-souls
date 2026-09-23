## Frameworks

Game Souls stands on older attempts to describe how games work. This folder summarizes each one, records exactly what the library borrowed and where it lives, and, just as important, what it deliberately left behind.

### What Was Borrowed

| Framework | What It Is | What Game Souls Took | Where It Lives |
| --- | --- | --- | --- |
| MDA (Hunicke, LeBlanc, Zubek) | Mechanics give rise to Dynamics, which produce Aesthetics | The causality trace: every recommended mechanic must be traced to the feeling it produces | frameworks/mda.txt, LLM_SOUL_GUIDE.txt (Step 8), axes/tone.txt |
| Gameplay Design Patterns (Björk & Holopainen) | A wiki of hundreds of patterns linked by typed relations | Relationship tags on every component: Requires, Supports, Conflicts With | frameworks/gameplay_design_patterns.txt, the top of every file in components/ |
| Machinations (Dormans) | A visual language of sources, pools, drains, and feedback loops | Economic topology: naming an economy's shape before tuning it | frameworks/machinations.txt, components/scarcity_economy.txt |
| Game Feel (Swink) | Real-time control, response envelopes, and six feel metrics | The kinetic profile: commitment or forgiveness, described in plain bands | frameworks/game_feel.txt, components/kinetic_profile.txt |
| Gamer Motivation Model (Quantic Foundry) | Twelve player motivations in six pairs | The Psychological Target section in every soul | frameworks/gamer_motivation.txt, souls/ |
| Game Ontology Project (Zagal, Mateas et al.) | A hierarchy of game elements | A five-part checklist for the Intake fact sheet | frameworks/game_ontology.txt, LLM_SOUL_GUIDE.txt (Step 1) |
| A Grammar of Gameplay (Koster) | Games as "atoms" built around a verb | The verb inventory: the literal actions come before the philosophy | frameworks/koster_grammar.txt, LLM_SOUL_GUIDE.txt (Step 1) |
| TV Tropes (video game tropes) | A crowd-sourced index of named patterns | Named, reusable failures, and mechanical trope names as aliases | frameworks/tv_tropes.txt, pitfalls/ |

### What We Deliberately Don't Adopt

Each of these frameworks is excellent at its own job. Adopted wholesale, each would also break something that makes Game Souls useful. These are standing rules for anyone (person or model) extending the library.

1. **No encyclopedic granularity (the Gameplay Design Patterns trap).** A component must describe a systemic philosophy, not a feature. "Double jump," "health potions," and "skill trees" are not components. If a new mechanic fits an existing component, add it as a tuning note there. A library of eighty components drowns the soul in trivia.

2. **No math without the feeling (the Machinations trap).** Economy is one lens, living inside scarcity_economy.txt, and it always ends in an emotion: Mansion's drain produces dread; Loathing's bottleneck produces optimization puzzles. Souls whose core is emotional or social (Ampersand, Elysium) are not forced into a topology.

3. **No demographics (the Quantic Foundry trap).** The Psychological Target names the ideal player the design serves, never a market segment. No ages, generations, or spending profiles. Audience trade-offs belong in "What This Soul Costs," stated as the designer's intent.

4. **No souls defined by theme or plot (the TV Tropes trap).** "Cyberpunk" and "zombie survival" are not souls. Two zombie games can have entirely different souls (Mansion and Swarm). Pitfalls borrow only mechanical trope names. Apply the Integration Check in components/theme_as_mechanic.txt: if the theme can be removed without breaking the mechanic, the theme isn't the soul.

5. **No sterile vocabulary (the MDA trap).** The academic terms are scaffolding for the analysis, never replacements for the library's voice. "The Verb Is Sacred" stays "The Verb Is Sacred." The opinionated, quotable voice is part of what makes the library work, for designers and as a prompt for models.

6. **No micro-physics (the Game Feel trap).** Execution is described in concepts and bands (instant, committed, cancellable), never frame counts or gravity constants. A model can't playtest a jump arc, and a design document that demands those numbers is guessing. The designer tunes values in the engine.

### Sources

* Hunicke, LeBlanc, and Zubek, "MDA: A Formal Approach to Game Design and Game Research" (2004).
* Björk and Holopainen, *Patterns in Game Design* (2004), and the Gameplay Design Patterns wiki.
* Dormans, *Engineering Emergence* (PhD thesis, 2012); Adams and Dormans, *Game Mechanics: Advanced Game Design* (2012).
* Swink, *Game Feel: A Game Designer's Guide to Virtual Sensation* (2008).
* Quantic Foundry, Gamer Motivation Model reference.
* Zagal, Mateas, Fernández-Vara, Hochhalter, and Lichti, "Towards an Ontological Language for Game Analysis" (2005), and the Game Ontology Project.
* Koster, "A Grammar of Gameplay" (GDC 2005).
* TV Tropes, video game tropes index.
