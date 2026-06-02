# Interactive Explainers — Design Spec

**Date:** 2026-06-01 · **Project:** Claude Code seminar (Institute for Ethics in AI)
**Source of truth for content:** `../../../spine-beats.md` (the talk skeleton)
**Status:** approved for build.

## Purpose

A small set of *interactive* visual explainers for the two load-bearing technical
concepts of the talk, for an audience of philosophers/scholars. They run as a
self-contained local website the speaker can project and **prod live**.

## Selection principle (why these and not others)

An animation earns a slot only when the concept is **(a) invisible to a live demo
AND (b) resists a static diagram**. The Pd/Playwright demos already *show* MCP
feedback (fails a). The ethics beats are *distinctions*, not processes (fails b).
What survives are things that happen **inside the context window**, where no camera
can point:

| Explainer | Status | Why it qualifies |
|---|---|---|
| 0. The lineage (two-clock timeline) | core | the *morph between two time-parameterisations* is motion a static diagram can't show; no live demo of "the history of coding agents" exists |
| 1. Context as a resource | core | invisible; it is accumulation + decay over time |
| 2. Progressive disclosure | core | invisible; the cost asymmetry is the whole lesson |
| 3. Orchestration ⇄ skill duality | stretch | parallel-vs-sequential *is* motion |

## Aesthetic: microtype × paperclip-punk

The two references are the two halves of the thesis wearing clothes — the **scholar**
(microtype: Latin Modern, justified prose, "it's a paper") collided with the
**information agent** (paperclip-punk: blueprint readouts, mono, "interacting teaches
the meaning"). The page *performs* the talk.

- **Type, two registers, deliberately collided.**
  - Prose: `'Latin Modern Roman'` (CDN: `https://cdn.jsdelivr.net/gh/sugina-dev/latin-modern-web@1.0.1/style/latinmodern-roman.css`), justified, ligatures. Fallback: `Georgia, 'Times New Roman', serif`.
  - Machine layer (tokens, labels, counters, code): `'JetBrains Mono'` (Google Fonts). Fallback: `ui-monospace, Menlo, monospace`.
- **Light only, no darkmode** (paperclip-punk tenet). bg `#FAF9F6`, ink `#111`.
- **Semantic accents (recur across every explainer so the audience learns the code once):**
  - blueprint blue `#0050FF` = *structure / index / cheap*
  - engineering orange `#F38020` = *loaded body / cost / expensive*
- Exploded-view, hairline-ruled diagrams; hover tooltips; an explicit **"› prod me"** affordance on each interactive.

## Stack

**One self-contained `site/index.html`** — vanilla JS + SVG/DOM, no build step, no
framework, no PreTeXt. Rationale: zero friction; projects/embeds anywhere; and the
artifact is itself an instance of the talk's Beat 3 ("spin up your own local site").
Fonts via CDN `<link>` with robust local fallbacks so a dead network never breaks the
talk.

## Shared component: the token-budget bar

Build **once**, reuse in every explainer. A fixed-width bar = the context window,
labelled `200k` with a **hard right edge**, and an off-canvas marker
`a million → (at the frontier)` — the honest upper bound, never a billion (checklist #1).
The hard edge makes "a billion" *visually unsayable*. Fill segments: blue =
cheap/structural, orange = loaded body.

## Explainer 0 — The lineage (two-clock timeline)

The opening visual. A single set of ~19 curated nodes — the load-bearing history of
"machines that write code / agents that follow instructions" — plotted on a wide,
flat band. Reuses the page grammar: blue = structural/enabling (architecture, models,
benchmarks), orange = the agent itself (and, dashed + struck-through, the *failure
modes*); prehistory = hollow ink dots.

- **The whole point is two temporal parameterisations of the same ordered events.**
  A **flip toggle** (the duality idiom, reused) morphs each node's *x* between:
  - **Calendar time** (linear 1956→now): seventy years of prehistory spread the page;
    the modern story *crushes* into the right-hand sliver.
  - **Model-generation time** (ticked by representative Claude releases — Claude 1 → 2 →
    3 → 3.5 → 3.7 → 4 → 4.5 → Opus 4.8): prehistory *collapses* into a "deep time ·
    pre-Claude" band on the left; the last three years *expand* to fill the line.
  The morph is a CSS transform transition — a literal **continuous deformation**. The
  clocks are **homeomorphic** (same points, same order) but **not isometric** (spacing
  inverted); *that distortion is the acceleration* the opening beat asserts. The
  homeomorphism payload lives only in the post-flip caption (earned by interaction, not
  front-loaded).
- **Vertical axis = capability**, and it must *mean something*: the y-axis carries four
  tier landmarks (**pre-model · Haiku · Sonnet · Opus**), each a full-width **hover zone**
  that surfaces a qualitative description of what that capability level can actually do.
  The axis title hover notes the "ruler slides" (today's Haiku ≈ last year's Opus).
  Capability height also de-clutters the crushed calendar view (nodes at different
  heights stay separable). Framed as *rough, schematic — not a measured score*.
- **Failure modes are first-class nodes** (dashed orange ring, struck through): AutoGPT
  loops ("endlessly plan, never finish"), **"lazy" GPT-4** ("// ... rest of code here" =
  infinite lazy delegation), Devin's hype-vs-13.86%, reward hacking (Goodhart, agentic).
- **Prehistory** (richer arc, per speaker): Dartmouth/Minsky 1956, Perceptrons 1969 (the
  field bets against neural nets), SHRDLU 1970, Society of Mind 1986, Programmer's
  Apprentice 1988 (Copilot dreamed early), Naturalness of Software 2012 (code is
  statistical).
- **Interaction:** hover any node → quick tooltip; click → pins its dated story in a
  readout (orange when it's a failure). `▶ walk the eras` steps a playhead through in
  chronological order. `↺ reset` returns to calendar time. Research-grounded, dated, and
  cross-checked against Anthropic's own release notes.
- Sits first, after the cover: it *is* the opening beat (stakes + acceleration) made
  visible.

## Explainer 1 — Context as a resource

- Bar fills left→right as **turns** are added (button + optional autoplay).
- Past a threshold the **leftmost segments desaturate** — context rot rendered as an
  **alpha gradient, not a wall** (checklist #4).
- **Compact** button: the oldest **live** turns crush into one narrow dark **sediment**
  block (`§1`); tokens readout drops, space reopens. Each compaction lays down a small
  layer that **persists** — compact again and `§2`, `§3` form beside it; **prior sediment
  is never re-crushed**. *Sedimentary layers, made literal.*
- Readouts (mono): `tokens 147k / 200k`, `coherence ●●●○○`.
- Tooltip on sediment: "this layer now sticks around, untouched by later compactions."

## Explainer 2 — Progressive disclosure

- A shelf of ~12 skill cards; collapsed each shows mono `name` + one-line `description`
  + tiny cost chip `~30 tok`. A global budget bar shows total ≈ sum of headers ≈ tiny
  (blue).
- `[+ add skill]` piles on more headers → budget **barely moves** (the point).
- A **task** prompt with preset chips ("fix this website", "format a bibliography",
  "debug a test"). On send, the matching card **unfolds** its body (steps + a bundled
  script glyph); budget jumps an **orange** segment (`body loaded 1,800 tok`).
- `[clear]` collapses it; orange segment removed; budget returns to baseline.
- Lesson: N headers ≈ free; 1 body = the cost, paid only on match.

## Explainer 3 — Duality (stretch)

- One **conditional flowchart** (SVG) shared by both modes: `scope` fans out to two
  parallel gathers (`papers` ∥ `talks`) → merge → `draft` → `review?` decision diamond,
  which either `pass → ship` or loops back (`retry`) to `draft`. Not a linear sequence —
  it branches, merges, and loops.
- Toggle `factory line ⇄ one-man-with-hats` over the **same** graph:
  - Factory line: the whole team is staffed at once (all role nodes lit blue, parallel) —
    work distributed in **space**.
  - One-man: a single agent (orange highlight) walks the same graph one node at a time —
    papers then talks, and round the retry loop — distributed in **time**. The taken
    decision edge (`pass`/`retry`) pulses.
- Caption states the space/time contrast.

## Navigation / structure

- Full-viewport scroll-snap sections: `cover → ctx → disclosure → duality`.
- Each explainer: two columns — microtype prose (scholar's voice) | interactive diagram
  (machine's voice). Stacks on narrow screens.
- Keyboard: ↑/↓ / space move between sections; section dots top-right.

## Accuracy guardrails (from spine-beats checklist)

1. Context bar capped at `200k`; "a billion" only ever appears as the struck-through
   off-chart marker.
2. No claim that the SLT YouTube/STT step is an MCP — not depicted here at all.
3. Rot is a gradient, not a cliff.
4. Copy frames "agent builds your MCP/skill" as collaboration, not magic (only if
   mentioned in prose).

## Out of scope (YAGNI)

No MCP-feedback animation (the live demo owns it). No ethics "sorter" gimmick. No
backend, no analytics, no build tooling.
