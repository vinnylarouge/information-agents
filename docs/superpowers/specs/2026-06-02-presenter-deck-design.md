# The Constellation Deck — Design Spec

**Date:** 2026-06-02 · **Project:** Claude Code seminar (Institute for Ethics in AI)
**Source of truth for content:** `../../../spine-beats.md`
**Extends:** `2026-06-01-explainers-design.md` (the four interactive explainers)
**Status:** approved & built (`site/index.html`).

## Purpose

Turn the explainer site into a **method-of-loci presenter deck**. The speaker wants to
*not memorise*: every beat gets a distinct visual **locus**, and a global map answers
"where am I?" at a glance. Once oriented globally, the local material returns on its own.
Pedagogy goal: **global position → local recall.**

## Principle

Each beat = one **station**: a single big emblem (the locus) + the one sentence the speaker
lands. Nothing else on screen (decided: purest memory-palace — trust the loci). The four
interactive explainers (lineage, context, skills, duality) double as the *rich* stations.

## The loci (emblem set)

Distinct, memorable, in the page grammar (ink line-art; blue = structural, orange =
cost/accent). One **recurring motif** carries the talk's loop: an **open ring → half-closed
→ sealed**, mapping the open/close structure the speaker most needs to feel.

| # | id | emblem | landing line |
|---|----|--------|--------------|
| 0 | `timeline` | two-clock timeline *(interactive)* | Two clocks over one history. |
| 1 | `stakes` | **knowledge-worker bar** *(interactive, see below)* — open-ring locus kept on the landing line | What is a knowledge worker *for* now? |
| 2 | `misnomer` | ~~coding~~ → information (strike) | No more about coding than the DPRK is democratic. |
| 3 | `costume` | chat bubble masking a faint agent lattice | New tech crystallises into one metaphor — and the metaphor hides the rest. |
| 4 | `liberation` | a portcullis lifting | The gate behind code just dropped — so you choose. |
| 5 | `proof` | pipeline → ∎ (QED) | Not one step is software engineering. |
| 6 | `ctx` | token-budget bar *(interactive)* | Context is a resource, not a memory. |
| 7 | `mcp` | USB-C plug · N×M → N+M | USB-C for agents — virtual hands and eyes. |
| 8 | `disclosure`/`duality` | shelf + factory⇄one-man *(interactive)* | Progressive disclosure · the same work in space or time. |
| 9 | `sidetools` | browser window + node graph | Spin up your own modes — and your own audit layer. |
| 10 | `bootstrap` | ouroboros shrinking → 0 | Skills that write skills; the surface area → zero. |
| 11 | `hinge` | **◗ ring half-closed** | What's left is judgment about what you want. |
| II | `discussion` | **● sealed ring + seeds**, orange "?" | Now — what do you *want*? |

## Navigation — "you are here"

- **Persistent minimap** (right rail): every beat a dot, grouped `show` / `deliberate`,
  current pulsing (blue in Act I, orange in Act II), loop beats dashed-orange, hover = label,
  click = jump.
- **Press `M`** → full **constellation map** overlay: two act-rows of numbered nodes (labels
  beneath), current lit, loop beats as dashed-orange rings, and **the loop drawn as a dashed
  arc** from beat 1 to the close. Click any node to jump (closes the map). `Esc`/`M` closes.
- **Arrows / space / PageUp-Down** walk stations; the live interactives keep their prodding.

## Implementation notes

- One self-contained `site/index.html`, no build step. New emblem stations are inline SVG
  (`viewBox 0 0 200 200`) using shared classes (`.em-ink/.em-blue/.em-orange/.em-faint`).
- Emblem stations inserted at three points; the existing interactives were **never
  reordered** (DOM order already matched the beat order).
- A single `STATIONS` registry drives the minimap, the map, and keyboard/scroll nav.
- "You are here" uses **scroll-nearest-to-viewport-centre** detection (robust for sections
  taller than the viewport, e.g. the timeline), throttled with `requestAnimationFrame`.

## Beat 1 · Stakes — the knowledge-worker explainer (added 2026-06-02)

Per-beat interactives are being added where a beat *earns* one (selection principle). Stakes
earns one as an **evidence** explainer (grounds a falsifiable claim — so it's gated on real,
sourced data, not schematic vibes). Scope chosen: **two-stroke (rise + the fall).**

- A **recomposing 100%-bar** (the context-explainer grammar) — agriculture / industry /
  services, with a **knowledge-intensive slice in orange** inside services (orange = value).
  A **year scrubber 1851→2024** (drag or ▶ play); a **jobs ⇄ GVA** toggle; live readouts
  (`year · services X% · ≈ N million people · knowledge ~K%`). Headcount is always jobs-based.
- **Stroke 2 — "the twist":** a panel (lit at modern years) — knowledge work is ~20% of jobs
  but ~29% of value (~2× output per head), and the graduate premium is *falling* (~50%→36%,
  2007→2024). The scarce thing is being de-priced.
- **Data + honesty seams** committed to the spine's pre-flight checklist (item 8). Sources
  stitched (CAMPOP / BoE Millennium / ONS); agriculture-only basis avoids the 1920 artefact;
  "knowledge-intensive" flagged as a contested proxy on-screen.
- The **open-ring locus** is preserved (small ○ on the landing line) so Beat 1 stays the
  loop's opening even though the emblem gave way to the interactive.

## Beat 2 · Misnomer + Costume MERGED → "misnomer & metaphor" (added 2026-06-02)

Per the speaker's mental map, the misnomer (name borrowed from the old thing) and the costume
(metaphor crystallises) are one move; the two emblem stations were **merged into one station**
(`#metaphor`), dropping the deck from 15 → 14 stations (registry, minimap, and map rebuild
automatically). Its explainer is a **time-sorted gallery** of children's drawings of "the
internet," oldest→newest, the conceptual space visibly collapsing **rich/peopled network →
app icon / inside-the-phone** (a "richness" meter, interpretive, falls as you step right).

- **Evidence explainer → gated on real, cited sources.** It is a **cross-study trajectory, not
  a longitudinal cohort** (stated as such). Spine: Thatcher & Greyling 1998 (rich) → Botturi
  2021 (both poles, *same paper*) → Botturi & Addimando 2025 (icon). Plus the iPhone misnomer
  pillar (telephony <5% of use) and the naming-rhyme (horseless carriage … desktop … cloud).
- **Provenance is built into every plate** and the figures are **populated by the speaker**, not
  scraped: framed `<img>` slots with an `onerror` placeholder, fed from `site/img/` (manifest +
  licence in `site/img/README.md`). Botturi papers are **CC BY 4.0** (reproducible w/ credit);
  others under institutional access / outreach-credit. Figures + iPhone stat committed to the
  spine accuracy checklist (item 9). A plate may instead be a **link-card**: the 2019 slot is a
  followable link out to **Nesta's live interactive gallery**
  (https://findingctrl.nesta.org.uk/draw-the-internet/) rather than an embedded figure.
- **The hinge plate (Kodama 2017, "a creepy guy at Google"):** carries a note — the child's
  *intentional stance* (a person-with-motives behind the screen) is a **category error for a
  network but the correct stance for an agent** (Dennett). The one plate that turns the
  "metaphors mislead" argument into a *setup* for the information-agent thesis: *the drawing was
  early, not wrong.* (Populated as of 2026-06-02: 1998 Thatcher, 2017 Kodama, 2019 Nesta image,
  a 2019 link-card to Nesta's live gallery, 2025 Botturi & Addimando.)

## Beat 3 · Liberation + Proof MERGED → "liberation & proof" (added 2026-06-02)

The liberation thesis (the gate behind code dropped → you choose how information is presented)
and the SLT proof ("not one step is software engineering") are one beat: **the proof is the
thesis cashed.** The two emblem stations merged into one (`#liberation`), dropping the deck to
**13 stations**. Combined emblem: the **dropped gate** with a **pipeline → ∎ passing through
it** ("zero software engineering"). Landing: *"The gate behind code dropped — and not one step
is software engineering."*

**Deck renumbered cleanly** after the two merges (was getting gappy): beats are now **0–9 + II**
(skills & duality share 6). The emblem-station kickers and the `STATIONS` registry `n` fields
were updated together so the minimap, the map, and each station agree.

This merged beat is the natural home for the **borderline-earns "SLT pipeline" interactive**
(the "cook-while-you-talk" async proof) — not yet built; emblem for now.

**Next candidates** (designed one-by-one, then batch-built): the SLT pipeline (if it earns it) ·
Bootstrapping. Misnomer/Liberation/Hinge/Discussion stay emblem-only (distinctions, not
processes); MCP/side-tools owned by the live demo.

## Refinements (2026-06-02)

- **Beat indicators → single words**, AI-flourish removed ("the loop, left open / closing /
  sealed", "quietly", the long metaphor sub-clause). Kickers are now `Beat N · <word>`.
- **Explainer 00 (timeline) head** restyled to match the other explainers (the `.tl-head` div
  gained `prose`, so its kicker/h2 inherit the mono-blue-uppercase + bold-serif treatment).
- **Metaphor beat:** the "DPRK is democratic" landing was removed (verbal-only punchline, not a
  visual locus). Minimap label simplified to `metaphor`.
- **Liberation beat:** label → `liberation`; emblem **regenerated** as a single clean
  **open padlock** (the previous merged emblem read as two overlapping icons).
- **MCP beat — resolved as static, no interactive.** The USB-C analogy and the `N×M → N+M`
  pseudomath are dropped in favour of the **sensorimotor analogy**: an **eye (perceive) + hand
  (act) + the act→see→act loop**. It stays a static icon because the live Playwright demo and
  the spoken patter own the feedback-loop point (fails the "invisible to a demo" test).
  - **Self-referential staging:** the beat shows the *broken first draft* of this very icon
    (dim, "draft") → an orange **"saw it · fixed it"** transition → the corrected version
    ("fixed"), captioned *"the loop, on its own icon — drafted, looked at, corrected."* The
    act→see→act loop demonstrated by the act of fixing the icon that depicts it — the deck's one
    deliberately recursive moment.

## Consolidation, round 2 (2026-06-02)

- **Side tools beat removed.**
- **Bootstrapping → "procedural thinking."** The "surface area → zero" framing is reframed as a
  mindset beat: *every task can, in principle, be the last time you do it — skillify it, let the
  skills optimise and learn; personalising the agent yields dizzying leverage of personalised
  abstractions; choose to keep it a tool or grow it into a cognitive partner.* Emblem: a **lever**
  (small effort, large load). Landing: *"Do each task once — it pays to be lazy."*
- **Hinge + Discussion merged** into one close (`#discussion`, Act II). The hinge's line folds
  into the landing: *"What's left is judgment — so, what do you want?"* The ring motif is now
  two-stage: **open (1) → sealed (close)** (the half-closed hinge ring is gone).
- **Deck is now 11 stations, beats 0–7 + II.** The press-`M` map's row split is computed
  (`Math.ceil(n/2)`) and its row labels are **reading-flow** ("the talk →" / "→ to the close"),
  *not* act boundaries — the two rows are a layout wrap, and only `discussion` is Act II.

## Out of scope (YAGNI)

No per-beat notes (purest loci, by decision). No speaker-timer, no remote control, no
build tooling, no analytics.
