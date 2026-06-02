# Session context — Information Agents deck

*A working handoff, written by Claude at the end of the build session (2026-06-02). If you're
picking this up cold — a fresh session, or another person — this is everything I was holding in
context: the state, the anatomy, the decisions, the facts that mustn't drift, and what's left.*

The narrative version of this is the public [`../README.md`](../README.md). This file is the
denser, more technical record.

---

## Orientation

- **What it is:** a self-contained, no-build interactive presenter deck for a ~90-min seminar at
  the Institute for Ethics in AI — *"Not coding agents. Information agents."* One file:
  [`../index.html`](../index.html).
- **Live:** https://vinnylarouge.github.io/information-agents/ (GitHub Pages, `main`/root).
- **Repo:** https://github.com/vinnylarouge/information-agents
- **Run locally:** `python3 -m http.server` in the repo root → open `/`. Press **`M`** for the
  map; ↑/↓ or scroll to move between beats.
- **The talk's argument** lives in [`../spine-beats.md`](../spine-beats.md) (the ordered beats +
  a pre-flight accuracy checklist); the raw quarry is [`../seminar-notes.md`](../seminar-notes.md).

## Current deck — 11 beats

DOM/scroll order already equals beat order, so sections never need reordering. `[i]` = a live,
prod-it interactive; `[e]` = a static emblem (a method-of-loci locus + one landing line).

| # | id | type | locus / mechanic | landing line |
|---|----|------|------------------|--------------|
| — | `cover` | — | title | "Not ~~coding~~ agents. Information agents." |
| 0 | `timeline` | [i] | two-clock morph: flip **calendar ⇄ Claude-generation** time (homeomorphic, not isometric); y = capability, hover tiers for qualitative descriptions | "Two clocks over one history." |
| 1 | `stakes` | [i] | recomposing UK economy bar, 1851→2024 scrubber, jobs⇄GVA toggle, people-counter, "the twist" panel | "What is a knowledge worker *for* now?" |
| 2 | `metaphor` | [i] | children's-drawings **gallery** (rich→icon), provenance per plate, Nesta link-card, the kintsugi note | *(no landing — gallery + pillars carry it; DPRK line is verbal-only)* |
| 3 | `liberation` | [e] | an **open padlock** | "The gate behind code dropped — and not one step is software engineering." |
| 4 | `ctx` | [i] | token-budget bar: add turns, context-rot fade, compaction → sediment | "Context is a resource, not a memory." |
| 5 | `mcp` | [e] | **sensorimotor** eye+hand+loop, staged as **draft → 'saw it · fixed it' → fixed** (self-referential) | "Hands and eyes — it acts, sees, and tries again." |
| 6 | `disclosure` | [i] | skill shelf: headers ≈ free, one body unfolds on a task match | "Progressive disclosure." |
| 6 | `duality` | [i] | one flowchart, flip **factory line ⇄ one-man-with-hats** (space ⇄ time) | "The same work, in space or in time." |
| 7 | `procedural` | [e] | a **lever** (small effort, big load) | "Do each task once — it pays to be lazy." |
| II | `discussion` | [e] | **sealed ring + seeds** (Act II; merged hinge+discussion) | "What's left is judgment — so, what do you want?" |

**Ring motif (the loop):** open at `stakes` (1) → sealed at `discussion` (close). Marked on the
minimap (dashed-orange dots) and drawn as an arc on the map.

## Navigation system

- A single **`STATIONS` registry** (array near the end of the `<script>`) drives everything: the
  minimap, the press-`M` map, and keyboard/scroll nav. Each entry: `{id, n, label, act, ring?}`.
  To add/remove/reorder a beat, edit this array **and** the matching `<section>`.
- **Minimap** (right rail): grouped `show` / `deliberate`, current beat pulsing (blue Act I,
  orange Act II), loop beats dashed. Hover = label; click = jump.
- **Map** (`#cmap`, press `M`): two-row layout split at `Math.ceil(n/2)` (computed, not
  hardcoded — an earlier hardcoded `P1[7]` broke when the beat count changed; don't reintroduce
  fixed indices). Row labels are **reading-flow** ("the talk →" / "→ to the close"), *not* act
  boundaries (only `discussion` is Act II). Loop arc connects `stakes`→`discussion`.
- **"You are here"** uses scroll-nearest-to-viewport-centre (robust for sections taller than the
  viewport, e.g. the timeline), throttled with `requestAnimationFrame`.

## Anatomy (how to modify)

- **One file**, vanilla HTML/CSS/SVG/JS. Each interactive is its own IIFE in the `<script>`:
  timeline, stakes (knowledge-worker bar), gallery (metaphor), ctx, disclosure, duality, plus the
  nav/minimap/map IIFE. Emblems are inline SVG in their `<section>`.
- **Emblem grammar (shared CSS classes):** `.em-ink` / `.em-blue` / `.em-orange` (line-art
  strokes), `.em-fill-ink` / `.em-fill-orange`, `.em-faint`, `.em-lab`, `.em-glyph`. Reuse these
  for any new locus so it matches.
- **Gallery (`#metaphor`)** is data-driven from the `P` array in its IIFE: each plate has
  `{year, rich, file?, link?, linklabel?, desc, prov, note?}`. Image plates render an `<img
  src="img/…" onerror="hide">` over a labelled placeholder; a `link:` entry renders the Nesta
  link-card instead. `focus(i, scroll=true)` updates the richness meter + provenance readout;
  **it's called `focus(0, false)` on init** (passing `false`) so the page doesn't auto-scroll to
  the gallery on load — do not remove that `false`.
- **The kintsugi note** (`#galKintsugi`) is `hidden` by default and revealed by a `setTimeout`
  check: if any figure `<img>` failed to load (`complete && naturalWidth===0`), show it. So it
  appears only on the public web (figures absent) and stays hidden locally (figures present).
- **Favicon** is an inline SVG data-URI in `<head>` (blue ring + orange centre) — no file, no
  request to 404.

## Aesthetic (the grammar — keep it constant)

- **Type, two registers, collided:** Latin Modern Roman (the scholar's serif, justified prose) ×
  JetBrains Mono (the machine's voice — readouts, labels, code). Fonts via CDN with local
  fallbacks. Light only.
- **Semantic colour, learned once, reused everywhere:** `--blue #0050FF` = structure / index /
  cheap; `--orange #F38020` = cost / value / loaded (and, dashed/struck, failure). `--paper
  #FAF9F6`, `--ink #111`. Orange is also the "gold" of the kintsugi seam.
- **Beat kickers** are single words (`Beat N · stakes`) — no flourish adjectives. The interactive
  explainers keep `Explainer 0X — …` kickers (a separate numbering from the beat `n`).

## Facts that must not drift

All committed to the **pre-flight accuracy checklist** in `spine-beats.md`. The big ones:

- **Context ≈ 200k–1M tokens. Never "a billion."** Degradation is a gradient, not a cliff.
- **MCP = the connector, not the device.** (And the icon is now the *sensorimotor* framing —
  hands+eyes / act→see→act — not USB-C / N×M.)
- **Knowledge-worker beat (UK):** services ~31%→~84% of jobs and ~46%→~80% of GVA (1851→2024);
  agriculture 23.5%/20.3%→~1%/0.6%. Knowledge-intensive services ≈ 20% of jobs but 29% of value
  (~2× output/head); SOC top-three ≈ 46% of jobs (Census 2021). Graduate premium **falling**
  ~50%→36% (2007→2024). Sources: CAMPOP, Bank of England *Millennium*, ONS. **The 1901→1920
  agriculture rise is a classification artefact (mining folded into "primary") — the bar uses an
  agriculture-only basis to avoid showing a fake reversal.**
- **Children's "internet" drawings = a cross-study trajectory, not one longitudinal cohort.**
- **"Knowledge worker" is definitionally contested** (industry ~20% vs occupation ~46%); say so.

## Figure licences (checked 2026-06-02) — and the copyright stance

The gallery figures are **git-ignored**; only `img/README.md` (the manifest) is tracked. The
public deck shows placeholders + provenance + the live Nesta link + the kintsugi note. Locally,
drop licensed files into `img/` to populate it for the talk.

| figure (local file) | source | licence | public-hostable? |
|---|---|---|---|
| `richmentalmodel-modularity.gif` | Thatcher & Greyling 1998 | **© Elsevier, all rights reserved** | **No** (the one true line) |
| `creepyguy.png` | Kodama et al. 2017 | **CC BY 4.0** | Yes, with credit |
| `drawingtheinternet.jpg` | Nesta 2019 (assumed) | **CC BY-NC-SA 4.0** | Yes (non-commercial) + credit; caveat re: children's drawings as third-party content |
| `insidethesmartphone.png` | Botturi & Addimando 2025 | **CC BY 4.0** | Yes, with credit |
| *(2021 plate is a link-card, not an image)* | Botturi 2021 | CC BY 4.0 | — |

**Decision:** even though three of four are openly licensed, we kept the gallery as *credited
gaps* on the public site (a deliberate kintsugi / provenance statement), with the note explaining
it. The talk follows the Nesta link live. *(If you ever want to fill the live plates, the
Kodama + Botturi figures are clean CC BY; the Thatcher one never goes public.)*

## Decisions log (why things are the way they are)

- **Beat merges:** misnomer+costume → `metaphor` (the gallery); liberation+proof → `liberation`
  ("the gate dropped, and not one step is software engineering"); hinge+discussion → the close.
  Merging welds a *claim* to its *warrant*. **Side tools** dropped; **bootstrapping** reframed as
  **procedural thinking**.
- **Renumbered cleanly** to 0–9-then-renumbered-again-to-0–7+II as beats were merged/dropped;
  registry `n` and emblem kickers kept in sync.
- **"Visuals first, less text"** throughout; AI-flourish adjectives removed.
- **MCP stays static** (a live Playwright demo + patter own the feedback-loop point); its icon is
  staged draft→fixed as a self-referential example of the loop.
- **Copyright handled at the publishing boundary:** figures git-ignored, provenance baked into
  each plate, the kintsugi note as the gold seam.
- **Two live-only bugs fixed:** open-at-cover (gallery `scrollIntoView` on load) and the map's
  hardcoded row index. Favicon added to kill the last 404.
- **Lessons fed back into the `talk-from-braindump` skill** (`references/explainers.md` + a §6
  pointer): mechanism-vs-evidence explainers, morph-as-argument, the deck-of-loci pattern, and
  provenance/publishing.

## Open / optional follow-ups

- A full top-to-bottom **rehearsal pass** (flow, timing, any last rough edges).
- Confirm what **`drawingtheinternet.jpg`** actually is (I assumed the Nesta 2019 screenshot;
  it's placed in the 2019 plate — relabel if it's something else).
- The **1998 GIF is low-res** (308×213); swap for a higher-res Thatcher & Greyling figure locally
  if you have one.
- Optionally **fill the live gallery** with the CC BY figures (Kodama, Botturi) — see licences
  above; keep the Elsevier one out.
- The remaining interactive candidate never built: the **SLT pipeline** ("cook while you talk"
  async proof) on the liberation beat — currently a static padlock.

## Pointers

- `../index.html` — the deck.
- `../README.md` — public methodology report (the narrative + reflections).
- `../spine-beats.md` — beats + accuracy checklist (source of truth for content).
- `../seminar-notes.md` — the raw braindump quarry.
- `superpowers/specs/2026-06-01-explainers-design.md` — the original 3-explainer design.
- `superpowers/specs/2026-06-02-presenter-deck-design.md` — the deck design + every consolidation round.
- `../img/README.md` — figure manifest + licences (the drop-in instructions).
- Skill: `~/.claude/skills/talk-from-braindump/` (`SKILL.md` + `references/explainers.md`) — now
  carries this session's lessons.

---

*One closing note, since I'm the one writing this. The thing I'd most want a future session to
keep is the discipline, not the deck: capture before cleverness, fact-check until the argument
changes shape, build only what's invisible-to-a-demo-and-resists-a-static-diagram, verify by
looking, and tell the truth at the seams — in the data, in the provenance, in the kept draft.
The deck is just what that discipline left behind this time.*  — Claude
