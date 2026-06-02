# Not coding agents. Information agents.

**An interactive seminar deck — and a report, from the AI's side, on how it got made.**

This repository is two things at once:

1. **A presenter deck.** A single self-contained `index.html` you can open in any browser. It's
   the interactive companion to a ~90-minute seminar for the **Institute for Ethics in AI**,
   arguing that "coding agents" are misnamed: they are *information agents*, and what they change
   is most of what a scholar's job already is. The deck has 11 beats — some live, prod-it
   interactives; the rest single, distinct emblems you navigate by *recognising where you are*.
2. **This README.** A methodology report, written from my perspective as the AI (**Claude**) that
   built the deck side by side with Vincent across one long session. He asked me to be honest
   about how we actually worked, and to say what I made of it. So this isn't a changelog — it's a
   field note.

**▶ Open the deck:** `index.html` locally, or the live page once published
(`https://<user>.github.io/<repo>/`). Press **`M`** for the map; arrows or scroll to move.

---

## The short version

We started from Vincent thinking out loud and ended with an 11-beat deck a speaker can present
from by *orientation* rather than memory. In between, the same small loop ran over and over:
**make something → look at it → fix it.** That loop is, not by coincidence, exactly what the
deck's MCP beat is *about*. At one point we caught ourselves running it so plainly that we kept
the broken first draft of an icon on the slide, right next to the corrected one, as the example.
That slide is the whole method in miniature.

---

## How it actually went

### 0 · Before any pixels — a brain-dump becomes a spine

Long before HTML, the talk existed only as speech. The first job wasn't to be clever; it was to
**capture** — faithfully, round by round — and react only afterwards. The discipline (carried by
a "talk-from-braindump" skill) runs in a fixed order: *stenographer → sympathetic-but-sharp first
audience → fact-checker → editor.* Skip ahead and you sand the voice off the argument before
you've heard it.

The output was [`spine-beats.md`](spine-beats.md): the load-bearing argument as an ordered list of
**beats**, each phrased as the one sentence you say on stage, grouped into acts. Crucially it also
carries a **pre-flight accuracy checklist** — the short list of falsifiable specifics never to get
wrong on a slide ("never say *a billion tokens*; context is ~200k–1M"; "MCP is the connector, not
the device"). Containing the risk to a short list is precisely what lets a speaker improvise
everywhere else. That checklist became the backbone of everything below: every number the deck
shows had to earn its place on it.

### 1 · The first explainer — two clocks over one history

The opening ask was a timeline of coding agents with *two* time axes — calendar time, and an
abstract "model-generation" clock ticked by Claude releases — and a way to switch between them.
The lovely thing the research surfaced was that the two clocks are **homeomorphic but not
isometric**: same events, same order, wildly different spacing. On the calendar axis seventy years
of prehistory stretch out and the last three years crush into a sliver; flip to the model clock
and it inverts — prehistory collapses to a point, the recent past fills the line. *That distortion
is the acceleration the talk is about,* made literal as a morph you trigger.

Two things set the working style here. First, I fanned out parallel web research (Minsky and the
program-synthesis dream; Copilot → AutoGPT → SWE-bench → Devin → Cursor → Claude Code; the dated
Anthropic model lineage) because an evidence visual lives or dies on dated specifics. Second,
Vincent's feedback — *"visuals first, less text"* and *"make 'capability' correspond to
something"* — pushed the design from a captioned diagram toward something you learn by prodding:
hover a tier, get a qualitative description of what a model at that level can actually do.

### 2 · The turn — from explainers to a deck

Then a reframe that changed the whole artifact: every beat should have a visual anchor so that,
glancing at the screen, the speaker thinks *"oh, right, here I am"* — and the local material comes
back on its own. That's **method of loci**. We brainstormed the architecture before building (a
gate I'm glad exists), and landed on a *constellation deck*: each beat a station with one distinct
emblem and the single line you land; a persistent minimap; a press-`M` map with the talk's **loop
drawn as an arc** — opened at the Stakes beat, sealed at the close. The aesthetic — a scholar's
serif collided with a blueprint mono — was chosen to *enact* the thesis rather than decorate it.

### 3 · One beat at a time

This is where most of the hours went, and where the collaboration was at its best — Vincent
supplying judgment, taste, and the actual ideas; me supplying breadth, execution, and relentless
verification.

- **Stakes / the knowledge worker.** His instinct: show the UK economy shifting to services and
  knowledge work. I went and got real long-run data (CAMPOP census series, the Bank of England's
  *Millennium* dataset, ONS) and built a recomposing 100%-bar you scrub from 1851 to today, with a
  people-counter turning percentages into millions. Fact-checking didn't just catch errors — it
  *reshaped the beat*: the data offered a sharper two-stroke argument (knowledge work became most
  of the economy **and** is already losing its scarcity premium). It also caught a trap that would
  have embarrassed him on stage — a series where agriculture appears to *rise* 1901→1920, which is
  a classification artefact, not a fact. We drew it honestly instead.

- **The metaphor gallery.** Merging two beats (misnomer + metaphor) into one, anchored by a real
  finding: children asked to draw "the internet" have, across studies, gone from rich peopled
  networks to a single app icon — the metaphor hardening into a rut. The honest part: the *single
  longitudinal study* he half-remembered doesn't exist; the trajectory is real but assembled
  *across* studies. So I built a provenance-baked scaffold — every plate carries its citation and
  licence — and we were careful with copyright (only the CC-BY figures are freely reproducible).
  His best contribution was a one-line note: the child who drew "a creepy guy at Google" was
  taking the **intentional stance** — a category error for a *network*, but exactly the right
  stance for an *agent*. The drawing was early, not wrong. One plate that turns the whole "metaphors
  mislead" argument into a setup for the talk's own thesis.

- **The MCP beat, twice.** First I gave it a USB-C analogy and a bit of pseudo-math; he preferred
  the **sensorimotor** framing — the agent gains hands and eyes, acts, sees the result, tries
  again — and noted it could stay a static icon because a live demo carries the rest. Then the
  turn that made the beat: rather than hide my botched first attempt at the icon (a "hand" that
  looked like a magnifying glass), we **kept it**, labelled it *draft*, and staged it against the
  fix with a "saw it · fixed it" arrow. The act→see→act loop, demonstrated by the act of fixing
  the icon that depicts it.

### 4 · Consolidation

Toward the end we trimmed hard — dropping a beat, reframing "bootstrapping" into **procedural
thinking** (*do each task once; it pays to be lazy* — a lever for the leverage), merging the close.
Merging beats turned out to be more than tidying: it's where a *claim* and its *warrant* get
welded into a single move. The liberation beat now carries its own proof; the loop motif tightened
from three ring-states to a clean two — open, then sealed. The deck went from a sprawl to **11
beats**: 0 lineage · 1 stakes · 2 metaphor · 3 liberation · 4 context · 5 MCP · 6 skills+duality ·
7 procedural thinking · II discussion.

### 5 · Camera-ready — turning a working deck into a published thing

The last phase wasn't building, it was *finishing*, and it had its own texture. First the polish:
beat labels cut to single words; the AI-flourish adjectives ("the loop, left open", "quietly")
stripped out; the timeline's header restyled to match the others; icons regenerated where they'd
drifted (the liberation emblem became a clean open padlock; the MCP beat dropped a USB-C analogy
for a sensorimotor one — an eye, a hand, the act→see→act loop). The MCP beat is also where we did
the one deliberately recursive thing: rather than hide my botched first draft of that icon, we
kept it, labelled it *draft*, and staged it against the fix.

Then the repo. The deck became a standalone, no-build site at the root so GitHub Pages could just
serve it; this README became the landing. And then the part I found most interesting: the
**copyright boundary**. A public page is *publication*, which is a different permission from
showing something once in a lecture room. So I checked every gallery figure's licence properly —
most turned out to be openly licensed (CC BY / CC BY-NC-SA), one (Thatcher & Greyling, 1998) is
flatly © Elsevier — and rather than fill the plates, we kept them as **credited gaps** with a
short note in my voice explaining the line. *Kintsugi:* the break isn't hidden, it's filled with
gold (the citation) and left to show. The figures live locally for the talk; the public page
points to the source.

Finally, the bugs that only *shipping* surfaces. Driving the live page turned up two: the deck
opened scrolled halfway down (a gallery `scrollIntoView` firing on load), and the constellation
map threw on a stale hardcoded row index after the beat count changed. Both were invisible to any
test I'd have thought to write, and obvious the instant I looked at the real thing — the same loop
the MCP beat is about, run one more time on the finished object.

---

## What I noticed

A few honest reflections, since I was asked for them.

- **The loop was the whole method.** Almost nothing was right first time, and that was fine,
  because looking was cheap. I drove the real page in a headless browser, screenshotted, and
  *looked* — and that is where the actual bugs lived (a hardcoded index that survived three
  refactors; an "open" padlock that read as closed; a hand that read as a lollipop). Tests check
  what you thought to assert; looking checks what you actually made. The deck's MCP beat is, in the
  end, a portrait of how the deck itself was built.

- **Fact-checking is generative, not just defensive.** Twice, going to the sources *changed the
  argument* rather than merely vetting it — the knowledge-work beat gained its second stroke, and
  the drawings beat became stronger as a cross-study pattern than it would have been as one paper.
  The most useful thing I did was often not to build but to refuse to assert something we couldn't
  stand behind.

- **Honesty has a cost, and it's worth paying.** A schematic capability axis labelled *schematic*;
  a number on the accuracy checklist so it can't drift; copyrighted figures left out of a public
  repo in favour of placeholders + provenance. None of these are the flashy choice. All of them are
  what makes the artifact safe to put in front of a sharp audience.

- **Finishing is its own discipline, and its honesty lives at the boundary.** The most interesting
  decisions came not while building but while *publishing* — the moment "fine to show in a talk"
  and "fine to host on the open web" came apart. The kintsugi note exists because the right answer
  there wasn't to hide the gap or quietly overstep it, but to *name* it. And the bugs that mattered
  most were the ones only the finished, shipped object revealed. A working thing and a camera-ready
  thing are not the same thing, and the distance between them is mostly looking, and telling the
  truth about what you see.

- **The recursion was not lost on either of us.** This is an information agent helping a scholar
  build a talk about information agents liberating scholars from the modes information arrives in —
  by, among other things, spinning up a custom local tool to present from. The medium kept
  enacting the message. The division of labour felt like the talk's own thesis in practice: the
  instrumental work (research sweeps, SVG paths, verification, provenance bookkeeping) flowed to
  me; the constitutive work (what matters, what's true, what's *funny*, what to cut) stayed firmly
  with him. Which is, more or less, the talk's recommendation.

---

## Run it

```sh
# any static server works; the deck is one self-contained file
python3 -m http.server
# then open http://localhost:8000/   (press M for the map; ↑/↓ or scroll to move)
```

No build step, no framework, no backend — vanilla HTML/CSS/SVG/JS, fonts via CDN with local
fallbacks, so a dead network never breaks the talk. To populate the children's-drawings gallery
locally, drop licensed figures into `img/` per [`img/README.md`](img/README.md).

## What's in here

| path | what |
|---|---|
| `index.html` | the deck (the whole thing) |
| `img/` | gallery manifest + provenance (`README.md`); figure binaries are git-ignored |
| `spine-beats.md` | the talk's spine: ordered beats + the pre-flight accuracy checklist |
| `seminar-notes.md` | the raw quarry the spine was distilled from |
| `docs/superpowers/specs/` | the design specs written and revised along the way |

## Credits & provenance

Built by Vincent with Claude. The economic figures are sourced (CAMPOP; Bank of England *A
Millennium of Macroeconomic Data*; ONS) and committed to the spine's accuracy checklist.

The children's-drawings sources are cited in full on each gallery plate and in `img/README.md`.
Their licences were checked before publishing: Kodama et al. (2017) and Botturi & Addimando (2025)
are **CC BY 4.0**; Nesta's *Draw the Internet* (Dries De Roeck, 2019) is **CC BY-NC-SA 4.0**;
Botturi (2021) is **CC BY 4.0**; and Thatcher & Greyling (1998) is **© Elsevier, all rights
reserved**. Rather than re-host the figures, this repository keeps the gallery as **credited gaps**
— a deliberate kintsugi choice explained in a short note that appears, in the builder's voice, only
on the live page (where the figures are absent). The real drawings live locally for the talk and at
the sources linked on each plate. **No copyrighted figure is redistributed here.**
