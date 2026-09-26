## Soul Instances

A soul in souls/ describes a family of games. An **instance** is the soul of one game: the positions, tunings, translated pillars, banned mechanics, and recorded deviations that a single project commits to and defends from its first sketch to its last patch.

Instances are built phase by phase with SOUL_INSTANCE_GUIDE.txt. Each phase fills one section of the instance file and ends in a gate.

### Files

| File | What It Holds |
| --- | --- |
| TEMPLATE.txt | The empty instance, with one section per phase. Copy it to start a new instance. |
| the_pass.txt | A worked example: a hypothetical kitchen game that adopts the Vigil soul, taken through Phase 4 on paper, with a sample of what Phases 5–7 record. |

### Instance Status

An instance's status is the last gate it passed:

| Status | Gate Passed | Meaning |
| --- | --- | --- |
| Seeded | Phase 0 | Verbs, a feeling, and a next-day story exist. |
| Chosen | Phase 1 | A lead soul and an ideal player are named. |
| Committed | Phase 2 | All six axes are fixed, and the banned list is written. |
| Composed | Phase 3 | Components are tuned, conflicts are resolved, and the economy has a shape. |
| Translated | Phase 4 | Pillars are translated and the Instance Litmus exists. |
| Proven | Phase 5 | A verb prototype produced the intended dynamic with real testers. |
| Sliced | Phase 6 | One full loop, including failure, produced the intended tone. |
| Guarded | Phase 7 | In production; every feature runs the Feature Gate. |
| Locked | Phase 8 | The pre-ship drift audit passed, and the costs are accepted. |
| Live | Phase 9 | Shipped; live changes run the gate, and the game has fed the library. |

### Rules for Instances

* **An instance never changes a soul.** It records how one game bends its lead soul, in its Soul Ledger. Changes to souls/, components/, or pitfalls/ happen only through Phase 9's feedback step, and only for what a shipped game proved.
* **Reference, don't copy.** An instance holds tuning, translations, and decisions. Rules stay in the component and soul files and are referenced by path.
* **Findings come from players.** Prototype, slice, and live findings sections are filled only from real playtests. A worked example that illustrates them says so.
* **Hypothetical games are allowed; invented facts about real games are not.** An instance for a real, shipped game must follow the same evidence rules as an analysis in LLM_SOUL_GUIDE.txt.
* **Keep it short.** A Translated instance runs about 2,000–3,500 words, most of it tables. The instance is a constraint document, not a design bible. Implementation detail belongs in the project's own documents.
