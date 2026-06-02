# Claude Code Seminar — Spine & Beats

**Venue:** Institute for Ethics in AI · **Audience:** philosophers/scholars (non-engineers)
**Source:** distilled from `seminar-notes.md` rounds 1–15. This is the *skeleton* — the
ordered argument. The notes are the quarry; this is the load-bearing structure.

**One-sentence north star (promoted from round 3):**
> These are not coding tools. They are *information agents* that **liberate you from the
> modes in which information is presented to you** — and as a scholar, that's most of the job.

**Pedagogical contract (the "bike" promise — state it early, keep it):**
> Knowing how to *fix* a bike ≠ knowing how to *ride* one. You'll leave able to ride.
> We touch the mechanics only where they help you ride. Two concepts do ~90% of the work.

---

## LOCKED RUNNING ORDER (2026-06-01) — 90 min, demos woven in

> **Present from the deck.** `site/index.html` is now a full **constellation deck**: one
> station per beat, each a distinct **emblem (locus)** + the single landing line — so you
> navigate by *where you are*, not by memory. The recurring **ring** opens at Beat 1, goes
> half-closed at the Hinge, seals in the Discussion. A persistent minimap shows "you are
> here"; **press `M`** for the full map (with the loop drawn) and click any beat to jump.
> Spec: `docs/superpowers/specs/2026-06-02-presenter-deck-design.md`.
>
> **Deck consolidation (2026-06-02):** merges — *misnomer + costume* → **metaphor** (the
> children's-drawings gallery); *liberation thesis + proof* → **liberation**; *hinge +
> discussion* → the **close**. *Side tools* dropped; *bootstrapping* reframed as **procedural
> thinking** ("do each task once — it pays to be lazy"; tool vs cognitive partner). Deck is now
> **11 stations, beats 0–7 + II**: 0 lineage · 1 stakes · 2 metaphor · 3 liberation · 4 context ·
> 5 MCP · 6 skills+duality · 7 procedural thinking · II discussion. Ring motif: **open (1) →
> sealed (close)**. (The numbered beat sections below are kept as the content quarry.)

**Two halves.** The talk *shows* (reframe → proof → working tech); the last ~30 min
*deliberates* (ethics, freeform). The split itself enacts the instrumental/constitutive
argument: demonstrable work goes to slides+demos, judgment work is reserved for live dialogue.

**MAIN TALK (~60 min)**
0. **Open on the lineage timeline** (`site/index.html` → Explainer 00) — flip calendar ⇄
   model-generation time; the morph *is* the acceleration. Lands the Stakes beat visually.
1. Stakes — open the loop, leave it open (now cued by the timeline)
2. Misnomer (DPRK)
3. Costume (why still code-shaped)
4. Liberation thesis
5. PROOF — SLT worked example
6. Context — **prod the explainer live** (`site/index.html`)
7. MCP = reach — **woven Playwright demo** (~90s)
8. Skills = packaged know-how + duality — **prod the explainer live**
9. Side tools (local site; Obsidian-style bookkeeping) — Beat 4 in action
10. Bootstrapping payoff — **play the Pd MCP the agent built**; `skill-opt` is real; surface area → ~0
11. HINGE — re-pose the loop ("what's left is judgment about what you want — let's discuss") → hand off

**FREEFORM DISCUSSION (~30 min)** — ethics seeds, not scripted (see Beats 4–5 below for the material):
delegation & the research-team model · instrumental vs constitutive · "who pays for the effort
you skipped?" · the manager trap → collectively closes Beat 1.

> Open and close are the **same question** (round 1 ⇄ round 15): *what is a knowledge worker
> for now?* The main talk earns it; the discussion answers it together.

*Note: the sections below keep the original numbering as the **content quarry**. The old
"BEAT 4 / BEAT 5" (ethics) now live in the discussion half, not the linear talk.*

---

## OPENING — the stakes (round 1)

- **Hook:** Everyone here is intelligent, and intelligence *was* the scarce, prized thing in
  the outgoing economy. That may no longer hold. Live question: **what is a knowledge worker
  supposed to do now?** (Provocation, not despair.)
- **Disarm the distrust:** humanities scepticism ≈ "don't trust Wikipedia" from school. That
  warning didn't survive the tool maturing. *But the timelines have accelerated* — a 3-month
  model gap is a generation. **Conclusions you drew 6–12 months ago have expired.**
- **Takeaway to plant:** keep 2–3 personal use-cases in your back pocket; **re-run them every
  model generation** to recalibrate.
- **PROD THE LINEAGE EXPLAINER HERE** (`site/index.html` → Explainer 00): the two-clock
  timeline *is* this beat. Flip calendar ⇄ model-generation time: prehistory collapses, the
  last three years explode — the clocks are *homeomorphic, not isometric*, and **that
  distortion is the acceleration**. Use it to make "a 3-month gap is a generation" visible.

## BEAT 1 — The misnomer (round 2)

- "Coding agent" is an **accident of authorship** — coders built them, named them after their
  own first use. **No more about coding than the DPRK is democratic.** *(Deliver as setup, then
  cash immediately — the name records who built it, not what it's for.)*
- Better model: **instruction-followers → information agents.** Code is one modality.
- *House metaphor:* chat = phoning **someone else's house** (their data + what you send); a
  coding agent lives in **your** house, with your files. That's what changes what it can do.

## BEAT 2 — The costume: why it still looks like code (round 3)

- New amorphous computing tech **crystallizes into one metaphor.** Computers *could* have been
  anything → we got the **desktop metaphor** (files/folders) → computers became "work."
  *(Anchors: Xerox PARC / Alan Kay; skeuomorphism; affordances — Gibson→Norman; McLuhan.)*
- LLMs are crystallizing around **chat.** Chat's affordances (natural language, a dogsbody to
  talk to) draw you in — **but the metaphor hides** the multi-agent / organizational dimension.
- **You are present at the crystallization, and you can refuse the default.** (Agency-restoring.)

## BEAT 3 — The liberation thesis (rounds 2–3)

- Near-**zero friction to write code** = the de-facto way machines modify information. So you
  **no longer have to accept how information is presented** — you *choose*. Information agents
  are the instrument of that choice.
- *Calibration (say it):* "code modifies information" = *machine*-modification was always gated
  behind code; that gate just dropped. (Pre-empts "I modify info without code all day.")

## PROOF — the SLT worked example (the QED)

- Real artifact (`~/Desktop/tinkering/SLT/`). Scattered, hype-y field, high barrier. Goal was a
  **triage decision**, not mastery.
- Pipeline: **scope → acquire (human-in-loop for paywalls; local STT + YouTube for talks) →
  synthesise into an Obsidian ontology (defs/theorems/examples) → personalised curriculum →
  Manim videos.** **~1 hour awake**, spread over 2–3 days.
- **Not one step is software engineering.** Pure information work. ← proves Beat 1 viscerally.
- **Honest scope = the "slop" defence:** it's a **map / jumping-off point**, not a substitute
  for primary sources (callback to Wikipedia). The tool didn't automate understanding; it
  **lowered the cost of deciding what's worth understanding.**

## BEAT 4 — Ethics I: delegation & the instrumental/constitutive cut (round 4)

- **You direct a small research team** — competent, inexperienced, as many as you want. The
  whole skill becomes: *what would I tell them, and how would they talk to each other?*
- **PI rebuttal** (aim heat at the *position*, not the people): you already delegate lit review;
  the agent just removes the career-stakes and the headcount cap.
- **The deep point:** scholarship's end-stage is becoming a **manager** — which *distances you
  from the work*, the pleasurable part.
- **The reframe of skill = self-knowledge:** decide which of your activities are **instrumental**
  (→ delegable) vs **constitutive** (→ joy/meaning). Spend your life on the latter.
  *(This answers the opening question.)*
- *Anchors:* Aristotle praxis/poiesis; the autotelic (flow); **Marx on alienation** — and the
  inversion: automation usually *deepens* alienation; here it can *reverse* it.
- *Pre-empt your own thesis:* the line isn't given — sometimes drudgery is where understanding
  is **forged**. Deciding well *is itself* the new core skill.

## BEAT 5 — Ethics II: trust, provenance & asymmetric effort (round 5)

- **Provenance double standard:** we don't audit how pencils/food are made (**"I, Pencil"**,
  Leonard Read; **Giddens/Luhmann** on trust in abstract systems). We trust via **feedback loops
  & regulation** — which AI pipelines don't *yet* have. *(State the analogy's limit yourself.)*
- **What's new:** an LLM ≈ a decent compression of the internet + common sense to use tools →
  information manipulation **orders of magnitude** more reachable.
- **The unifying ethical principle (your most quotable line):** the wrong isn't *"did a machine
  help?"* — it's **"who pays for the effort you skipped?"** Personal/triage use **internalises**
  the cost; slop-into-peer-review **externalises** it onto a non-consenting commons.
  *(Reply-all ethics; Brandolini's law — refuting costs 10× producing.)*

## TECHNIQUE — the two concepts (the "basics"; bike: ride, don't build)

Order matters: **demo-first, name-second.** Introduce each only after the problem is felt.

- **Minimal mechanics — context (round 11):** context = **short-term/working memory.** ⚠️ window
  is **~200k (Claude), up to ~1M frontier — NOT a billion.** Degradation is a **gradient, not a
  cliff** ("context rot"). Manage via `/clear` + **compaction** ("sedimentary summaries").
  *Context = scratchpad; files = archive.*
- **Coping trichotomy (round 12):** orchestrate (many fixed-role agents, factory line) /
  offload to **files = long-term memory** (`CLAUDE.md` = always-loaded **index** pointing at the
  archive) / **skills = the elegant middle ground.**

### MCP = reach (sensorimotor) — rounds 7–8
- **USB-C for agents.** Standard plug; one server, any agent (N×M → N+M). **The connector
  standard, not the device** ("is my hard drive a USB?").
- Value isn't only reach — it's **virtual hands AND eyes**: feedback → **iteration**.
  Website example: without eyes, a **blind expert** editing by staring at code; with
  Playwright, it **screenshots, sees, fixes, repeats.**
- *Calibrations:* the M/C/P acronym gloss is a **mnemonic**; iteration is the **general agentic
  loop** — MCP adds a *new sense* (vision) the tool lacked.
- **LIVE DEMO candidate:** Playwright MCP fixing a small site (eyes → iterate).

### Skills = packaged know-how — rounds 10, 13
- A skill is a **Markdown file**: **frontmatter header** (`name` + `description` = the **trigger**;
  positive/negative "use when / skip when") + **body** (procedure: steps, tools, heuristics,
  musts/must-nots; can **bundle runnable scripts**).
- **Progressive disclosure (the whole trick):** only the **tiny headers** load up front — many
  skills cost ~nothing; the **big body loads on demand** when a task matches. *Asymmetry of cost.*
- A skill **is** the index+archive pattern, self-contained (header = pointer, body = store).
- *Duality (round 10):* anything a **team** does by message-passing, **one agent** can do by
  swapping **hats** sequentially. Parallel vs sequential — a spectrum (skills can spawn sub-agents).

## BOOTSTRAPPING PAYOFF (round 14)

- **The agent builds its own MCPs and skills.** Novel tool → it builds the MCP (a *collaboration
  with iterations*, not push-button — keep that audible). Skills that **write** skills; skills
  that **optimise** skills (**information-expansion effect**).
- **Verifiable credibility moment:** `skill-opt` — ports Microsoft's SkillOpt; VW used the
  round-10 **duality in anger** to collapse an orchestration into a single skill that now tunes
  other skills. *The abstraction predicted a real artifact.*
- **Round 4 fully cashed:** technical surface area → ~0 and **self-extending**; what remains is
  judgment about what you want. *(One beat of reflexivity — Gödel/Hofstadter overtone — don't
  sermonise.)*

## CLOSE — the blunt landing (round 15, closes round 1)

- **The manager trap:** you'll open a 2nd, 3rd agent and be drawn into **managing them** — the
  Beat-4 alienation, re-inflicted by the very tool.
- **So do what makes you happy** — deliberately.
- **Bluntly:** it's unclear why any of us are *necessary* now; we were prized for handling
  **cognitive friction**, and that's **no longer a human-tied skill** for much knowledge work.
- **Resolution = Beat 4:** with the friction-justification gone, optimise hard for the
  **constitutive**. *That* is what a knowledge worker is for now.

---

## Side tools (round 6 — weave in, or short appendix)
- **Local website** for presentation freedom (you pick the mode — Beat 3 in action; also the
  talk's own PreTeXt leave-behind).
- **Obsidian-style bookkeeping** (alts: Logseq, Notion) = your **personal audit layer** — a
  partial answer to Beat 5's trust question you don't wait on regulation for.

## Demos (round 8/9/15)
- **Inline:** Playwright MCP fixes a small site (reach + feedback + iteration in ~90s).
- **Headline:** **Pure Data MCP** (cooking) — Pd as the visible instrument.
- **Staging move — "cook while you talk":** start a long demo at the top, lecture, **reveal the
  finished artifact at the end.** The talk's *form* proves the async claim. (Pairs with SLT's
  "~1 hour awake.")

## ⚠️ Pre-flight accuracy checklist (fix before any slide)
1. **NEVER say "a billion tokens."** Context ≈ **200k–1M.**
2. **MCP = connector, not the device.** The SLT YouTube/STT step was **native scripting, NOT an
   MCP** — use it to *motivate the need*; show a real MCP (Zotero/Drive/Playwright/Pd) separately.
3. **"Model/Context/Protocol → agent/tool/interaction" is a mnemonic**, not the spec's meaning.
4. **Degradation is a gradient**, not a 200k cliff.
5. **"Agent builds your MCP" = collaboration with iterations**, not magic.
6. **Confirm "Logseq"** (notes transcribed "FogSec").
7. **Duality = intuition, not a theorem.** PI rebuttal: aim at the position, not the people.
8. **Knowledge-worker stakes figures (UK)** — committed numbers for the Beat-1 explainer
   (`#stakes`), so they never drift on a slide:
   - Services: **~31% of jobs (1851) → ~84% (2024)**; **~46% of output (1851) → ~80% of GVA (2023)**.
   - Agriculture: **23.5% of jobs / 20.3% of national income (1851) → ~1% / 0.6% (2024)**.
   - Knowledge-intensive services: **~20% of jobs but ~29% of GVA** (ONS, 2015), **~2× output per head**.
     By occupation (SOC top-3) ≈ **46% of jobs** (Census 2021). *"Knowledge worker" is definitionally
     contested* — say so; it rests on a degree-share proxy.
   - Graduate wage premium **falling** ~50%→36% working-age (2007→2024, ONS/NIESR) — the "de-pricing."
   - **Honesty seams:** sources are stitched (CAMPOP census 1851–1911; BoE "Millennium"/ONS 1920–2024);
     early years approximate; the 1901→1920 agriculture bump is a *classification artefact* (mining
     folded into "primary") — the explainer uses an agriculture-only basis to avoid showing a fake
     reversal. **Top-1% income stats are NOT "knowledge workers"** (capital/finance) — don't conflate.

9. **Misnomer + Metaphor beat (now MERGED in the deck) — committed figures & provenance:**
   - **iPhone misnomer:** ~**3.5 hrs/day** on the device vs ~**3–6.5 min/day** on voice calls (Ofcom 2023)
     → telephony is **under ~5%** of use; UK mobile call minutes have been in **absolute decline since 2021**.
   - **Desktop metaphor:** Xerox **Alto (1973) → Star (1981)**, folders/icons/trash (David Canfield Smith).
     **Do NOT say "introduced 1970."** Use Alto 1973 / Star 1981.
   - **"Horseless-carriage syndrome"** exact phrase is **UNVERIFIED** as McLuhan's — attribute the
     *rear-view-mirror idea* to McLuhan (*Understanding Media*, 1964); treat the "syndrome" wording as a
     later popular coinage.
   - **Children's "internet" drawings = a CROSS-STUDY trajectory, NOT a single longitudinal cohort.**
     Say "across studies, rich/spatial networks → app icons" (Thatcher & Greyling 1998 → Botturi 2021/2025;
     Botturi frames it as *generational* evolution). **Provenance/licence:** Botturi 2021 & 2025 are
     **CC BY 4.0** (reproduce with credit); Thatcher & Greyling © Elsevier (institutional access); **Nesta
     "Draw the Internet" is an outreach project, not peer-reviewed** — credit Nesta / Dries De Roeck.
     Figure manifest in `site/img/README.md`.

## Open decisions (yours)
- [ ] Demo shape: one inline (Playwright) + one headline (Pd)? Or a single big finale?
- [ ] Where do the side tools live — woven through, or an appendix?
- [ ] How much ethics vs. how much practice — the line is yours to set (Ethics venue earns both).
- [x] Phase 3: scope of the interactive explainer website. Now **four** explainers:
  **00 the lineage** (opening two-clock timeline) · 01 context · 02 progressive disclosure ·
  03 duality. **The lineage timeline OPENS the talk** (decided 2026-06-02) — it carries the
  Stakes beat (acceleration made visible) before the spoken hook lands.
