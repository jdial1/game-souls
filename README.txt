## Game Souls

A design library for the distinct "souls" of influential games. Each soul is a design philosophy, not a genre, and each one is built from three layers.

### The Three Layers

| Layer | Folder | What It Holds | Question It Answers |
| --- | --- | --- | --- |
| **Foundational** | axes/ | Six questions every game must answer, each with a spectrum of named positions. | "Where does this game stand?" |
| **Component** | components/ | Reusable design principles shared by several souls, each written once, with rules, costs, failure modes, and per-soul tuning. | "What building blocks does it use?" |
| **Soul** | souls/ | Compositions: a philosophy, a set of axis positions, a list of components, and only the pillars that are unique to that soul. | "What makes it *this* soul and not another?" |

archive/ holds the original single-file versions of each soul, untouched.

**For language models:** start with LLM_README.txt, then follow LLM_SOUL_GUIDE.txt to analyze a game, classify it, write a new soul, or instill a soul into a game in development.

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
| Swarm | Punishing but Legible | Total | Player-Authored Build | Surplus / Optimization | Cool Focus / Deadpan Absurd | Runs |
| Tapestry | Narrative / Terminal | Total / Oblique | System-Authored | Custodial | Armchair Intrigue | Sandbox Chronicle |

### Components Used by Each Soul

| Component | Looking Glass | Dwarven | Loathing | Ashen | Hearthian | Elysium | Spire | Toybox | Mansion | Containment | Gauge | Ampersand | Casebook | Chorus | Swarm | Tapestry |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| legible_failure | | x | | x | x | | x | | x | x | x | | x | x | x | |
| failure_as_content | | x | | x | x | x | | | | | | x | | | | x |
| systemic_consistency | x | x | | | x | | | x | | x | x | | x | x | | x |
| living_world | x | x | | x | | | | | x | | | | | | | x |
| environmental_storytelling | x | | | x | x | | | | x | | | | x | | | |
| trusting_the_player | x | | x | x | x | | | x | | x | x | x | x | | | |
| interlocking_space | x | | | x | x | | | | x | | | | | | | |
| scarcity_economy | | x | x | | | | x | | x | x | | x | x | | x | x |
| synergy_engines | x | | x | | | | x | | | x | | | | | x | |
| difficulty_ladder | | | x | | | | x | | | x | | | x | x | x | |
| theme_as_mechanic | | | x | | | x | | | x | | x | x | x | x | | |
| diegetic_interface | x | | | x | | | | | x | | x | | | | | |
| shared_discovery | | | x | x | x | | | | | x | | | | | | |
| social_safety | | | | | | | | | | | x | x | | | | |
| interface_voice | | | | | | | | | | x | x | x | x | | | |

### How to Use This Library

**To design a new game:**
1. Pick a position on each of the six axes. Read each axis file's "Tensions" section to check for conflicting choices.
2. Pull in the components your positions demand. Each component's "Tuning by Soul" section shows how different souls set the dial.
3. Write the signature pillars: the rules no other soul has. If you can't name any, you're describing a mix of existing souls, not a new one.
4. Write a litmus test, and check the tone killers in axes/tone.txt.

**To study an existing soul:** Read the soul file first, then follow its component references for the shared rules, costs, and failure modes.

**To blend two souls:** Compare their axis rows. Where they agree, the blend is easy. Where they disagree, pick one to lead (for example, Mansion + Looking Glass gives *Prey* and *System Shock*: Poor vs. Toolkit power, resolved deliberately).

### Adding a New Soul

Create souls/<name>.txt with these sections, in order:

1. Title, subtitle, philosophy, and surface/beneath description
2. Axis Positions (a table covering all six axes)
3. Components (each referenced by path, with a one-line note on how this soul tunes it)
4. Signature Pillars (only rules that aren't already in a component)
5. Variants & Exceptions (where the example games bend the rules)
6. What This Soul Costs (soul-specific costs only)
7. How It Fails (soul-specific failure modes only)
8. Neighboring Souls (the closest souls and what separates them)
9. Litmus Test and closing quote

Aim for 1,300–2,400 words. A soul much longer than that is usually holding rules that belong in a component, or implementation detail that belongs in the game's own design docs.

If a new soul repeats a rule that appears in another soul, move that rule into a component (a new one, or an existing one) and reference it from both.
