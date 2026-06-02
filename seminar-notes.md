# Claude Code Seminar — Working Notes

**Venue:** Institute for Ethics in AI
**Audience:** philosophers and scholars (not engineers)
**Prep window:** ~2 days
**Status:** finding the through-line. This doc is a scratchpad — dump freely below.

---

## North star (one sentence, draft)

> Teach scholars *how to ride the bike* — the workflows for using a coding agent
> as a general-purpose information agent — rather than how the bike is built.

## Stance / posture (captured from VW)

- Don't spend too much time on raw technical mechanics.
- Give them **workflows** they can actually use, not architecture lectures.
- "Ride the bike" > "what the bike is made of / how it's made."
- Reframe **coding agents → general information agents**. Code is just one
  modality; the same agent reads, writes, searches, reasons over *any* corpus.

## Core content to convey (the "basics")

- **MCPs** = a USB port for tools. A standard way to *plug in* external
  capabilities (data sources, services, your files, the web) to the agent.
- **Skills** = a way to *modularize repeated procedural knowledge* into Claude.
  Reusable "how we do X here" packaged so the agent reaches for it on its own.
- The unifying move: an agent that (a) can plug into anything [MCP] and
  (b) accumulates reusable know-how [skills] is no longer a "coding tool" —
  it's a personal research/scholarship instrument.

## Deliverable idea

- A small **interactive website** built with **PreTeXt** (text rendering +
  interactive graphics) to teach the above. Self-paced, embeddable diagrams.
- Open question: live-demo vs. interactive site vs. both (site as leave-behind).

---

## Candidate through-lines (my contributions — react / kill / merge)

1. **"The agent as a research assistant you can extend."**
   Frame: you already know how to direct a capable RA. MCPs = giving the RA keys
   to the archives/labs; Skills = training the RA in your house style so you stop
   re-explaining. Everything technical hangs off this familiar relationship.

2. **"From asking to delegating."**
   Arc: chatbot (you copy-paste) → agent (it acts in your environment) →
   *extended* agent (MCPs widen what it can touch, Skills deepen what it reliably
   knows how to do). Through-line = a progression of *trust and reach*.

3. **"Procedural knowledge wants to be shared."**
   A philosophy-flavored spine: tacit/procedural knowledge (Ryle's "knowing-how")
   has historically been hard to transmit. Skills are an attempt to *externalize*
   knowing-how; MCPs externalize *access*. The talk becomes a case study in
   codifying tacit scholarly practice — which is itself philosophically loaded.

4. **"What's the smallest thing that changes your week?"**
   Ruthlessly practical spine: pick 3–4 concrete scholar workflows (lit triage,
   draft interrogation, building a personal reference tool) and show MCPs/skills
   only as they're needed to make those work. Concepts are scaffolding, not topic.

## Tensions to resolve

- **Concept-first vs. workflow-first.** "Ride the bike" pushes workflow-first,
  but MCP/skill are abstractions — some scaffolding is unavoidable. How much?
- **Ethics audience.** Do they want the *practical* tool, or are they also
  hungry for the *conceptual* implications (agency, delegation, automation of
  judgment)? A talk at an Ethics institute can probably earn a little of both.
- **Interactive site scope.** PreTeXt is powerful but has a learning curve and
  isn't installed. Is the site the star, or a companion to a live talk?

## Open questions for VW

(to be filled as we discuss — see chat)

---

## Dumping ground (raw, unsorted — add anything)

### Brain dump — round 1 (VW)

**1. Opening note for a room of scholars — the value-of-intelligence reframe.**
Everyone here is intelligent, and that *was* valuable in an outgoing paradigm:
an economy that had to build incentives to coax that kind of human capital to
the surface. That may no longer be so valuable. So the live question to open on:
**what is a knowledge worker supposed to do now?** (Provocation, not despair —
sets up why the workflows in this talk matter.)

**2. The humanities-distrust pattern — and why the timeline is the trap.**
Humanities scholars often don't like / use / trust these tools. Same *spirit* as
schoolteachers from our own school days warning "don't trust Wikipedia as a
source." That dynamic aged a particular way: Wikipedia is now a perfectly good
jumping-off point for most things — the warning didn't survive contact with the
tool maturing.
- The difference here is **the timelines have accelerated.** It's reasonable,
  from a humanities vantage, to have tried a model 6–12 months ago, drawn
  conclusions, and concluded "okay, I basically get it."
- But that is *not how this technology works.* **A three-month gap is a huge,
  huge difference** between model generations.
- General takeaway to plant: keep **a couple of personal use cases** in your
  back pocket and **re-run them every time a new model generation drops** — to
  recalibrate what the models can and can't do. The conclusion you drew last
  year has likely expired.

### Brain dump — round 2 (VW): conceptual history of coding agents

**The starting point: GPT-3.5.** The break from what came before — for the first
time you weren't dealing with an *autocomplete*. RLHF (reinforcement learning
from human feedback) was working, so the models could **follow natural-language
instructions.** That's the hinge.

**Why code, and why agents — origin story.** Writing code is drudgery, so from
the very start the thought was "we should get these things to write code for
us." And crucially **it was coders building these tools**, scratching their own
itch — removing a small inconvenience they hit constantly. Instead of
copy-pasting code completions out of the chat interface every time, they asked:
*why don't we just have the agent write the code for us?* That's the move from
chat → agent.

**The "house" metaphor (the key conceptual difference).**
- **Chat interface = calling someone else's house.** When you use Claude /
  ChatGPT / any chat app, you're phoning a house that belongs to Anthropic or
  OpenAI, and they serve you the chat. Like **Netflix, YouTube, cloud computing,
  cloud gaming**: you do essentially **no local computation** — you send
  requests, you receive responses.
- **Consequence:** those responses can only be conditioned on **what's in
  *their* house**, plus **whatever you choose to send along** with your request.
- **Coding agent = the agent is in *your* house.** The useful case is that the
  agent lives in your own home, with **access to all your local files and
  data.** That's what changes the kind of thing it can do for you.

**The "coding agent" is a misnomer — an accident of authorship.** They're
called *coding* agents because **coders built them** (see origin story above);
the name records *who made the tool first*, not *what the tool is for*. They are
**no more necessarily about coding than the Democratic People's Republic of
Korea is actually democratic** — the label is inherited, not descriptive.
- **Better mental model: instruction followers.** What RLHF actually unlocked
  (round 2, top) was natural-language *instruction following*. Coding is one
  instruction among many.
- **Even better: information agents.** They work with, transform, and reason
  over *data / information* in whatever modality you hand them — prose, sources,
  spreadsheets, archives. Code is just the modality the builders happened to
  reach for first because it was their own drudgery.
- **This is the north-star reframe in miniature** (lines 20–21, 31): the move
  from "coding tool" → "general information agent" is the single most important
  perspective shift for this audience. Plant it early; everything practical
  (MCPs = plug into any information source; Skills = teach reusable know-how)
  hangs off it.

### Brain dump — round 3 (VW): "why still code-shaped?" → the liberation thesis

**Answering the objection ("if it's not about code, why the code aesthetics?").**
Don't let appearances fool you. What you actually have is a **liberation tool** —
one that frees you from the **modes in which you interact with information.** And
for scholars, *interacting with information is most of the job.* The code-shaped
surface is a costume, not the substance.

**Why the costume? — the "crystallizing metaphor" of computing.** New
technologies with an *amorphous* nature (computing above all) pass through a
process of **crystallizing into a dominant metaphor.** Computers *could have been
anything*, but we settled on the **graphical desktop metaphor**: files, folders,
a "desktop." That metaphor is **workspace-coded** — so computers *became* tools
of work, when they could have been many other things.
- **LLMs are crystallizing the same way — around the chat interface.** And chat
  has real **affordances** that draw you in: the flexibility of natural language,
  the ease of just *talking to a dogsbody.*
- **But the metaphor also hides things.** Chat is single-threaded dialogue; it
  doesn't naturally give you the **more multifaceted interaction structure** —
  the *organization* of multiple agents, delegation, parallel work. That whole
  dimension is invisible if "LLM = chat box" is your only mental image.

**The liberation thesis (the payoff).** Because there is now **near-zero friction
for writing code** — and code is the **de facto way we modify information** — you
**no longer have to accept how information is presented to you.** You can *choose*
how you want it presented. **Information agents are the instrument by which you
exercise that choice.** The agent removes the *skill barrier* to wielding code;
what's left is your judgment about how information should be shaped.

### Worked example — SLT (VW): the liberation thesis, end to end

*(Live artifact: `~/Desktop/tinkering/SLT/` — a real project, not a hypothetical.
This is the demo that cashes the "chat hides the organization of agents" check.)*

**The problem (a scholar's problem, not a coder's).** I wanted to assess a
hype-y thread of theoretical ML — **singular learning theory (SLT)**. The
literature is **scattered, uncentralized, no survey**, and the **barrier to entry
is high.** The real question wasn't "learn SLT," it was the *triage* question:
**is engaging with this literature worth my effort at all?**

**The pipeline I ran through Claude Code (spread over ~2–3 days, multiple
sessions):**
1. **Scope.** "Do a little research — what are the main sources of literature,
   who's giving the talks?" Agent surveys the field.
2. **Acquire.** "Download them." *Human-in-the-loop* where needed — I help with
   anything paywalled, source textbooks if necessary. For talks: stand up a
   **local speech-to-text model** + **YouTube APIs** to pull and transcribe them.
3. **Synthesize.** Dump everything into an **Obsidian MD mind map**, organized by
   a **partial ontology** — *definitions, theorems, motivating examples* — and
   surface *the big ideas* and *the motivating questions.*
4. **Personalize.** "Now build a **curriculum** — here's where I am, here's what
   I want to know, here's how I think." → a personalized learning path.
5. **Produce.** Load the **Manim skill** (the animation package **Grant
   Sanderson / 3Blue1Brown** uses) → turn the curriculum into a **series of
   YouTube-style videos with proper math animations.**

**The result.** Total time I had to be *awake and monitoring*: **~1 hour.** Out
the other end: a stack of videos I watch 2–3 of at fast speed and go *"okay —
I get the idea."*

**Why this example earns its place in the talk:**
- **Not one step is "coding."** It's research → acquisition → synthesis →
  pedagogy → media production. *Pure information work.* It proves the misnomer
  (round 2) viscerally — you watch an "information agent," not a "coding agent."
- **It instantiates every concept already in these notes.** *(Correction — see
  round 7: the YouTube/STT step was NATIVE tool use — the agent writing+running a
  script — NOT an MCP. Use SLT to motivate the **need** for reaching outside the
  model; show a real MCP separately.)* The **Manim skill**
  is the textbook case of Skills-as-externalized-*knowing-how* (lines 27–28,
  through-line #3, Ryle): 3b1b's tacit animation craft, *packaged and reused.*
- **It IS the liberation thesis (round 3).** A scattered, high-barrier field was
  re-presented — by my choice — as a *personalized animated curriculum.* I
  refused the mode the information arrived in and picked a new one.
- **The "~1 hour awake" stat is the kill-shot.** It quantifies the friction
  collapse better than any abstract claim.
- **Honest about scope (disarms the "AI slop" objection).** The outcome was
  *orientation*, not mastery — it answered "is this worth my real effort?" The
  videos are a **map / jumping-off point, not a substitute for primary sources**
  — a direct callback to the round-1 Wikipedia point (lines 92–96).

### Brain dump — round 4 (VW): the delegation model + instrumental vs. constitutive (the ethical core)

**Bridge from SLT.** No software engineering was required of me for any of that —
which is a clean jumping-off point into *technique*. And note how modest the aim
was: I just wanted information **in a format I found palatable**, to make a
**triage decision.** Hold onto that modesty; it does a lot of defensive work.

**Diffusing the "slop" objection fast — the PI rebuttal.** If you're a **PI or a
senior researcher** with a couple of dogsbodies doing your literature review,
then *(VW's words — tune the heat for the room)* "you should shut the fuck up,"
because **this is already what happens.** The only differences: **no one's career
is on the line**, and I'm getting an AI to **play the role of a small research
team whose entire operation I design.**

**The productive mental model — you are directing a team.** Picture it: a bunch
of **fairly competent (if not deeply experienced) people, and as many of them as
you want.** The whole skill becomes two questions:
- *If I had them, what would I have to tell them to do to get the outcome I want?*
- *And how would they have to talk to each other?*
This is the **"organization of agents"** from round 3 and the SLT pipeline, named
explicitly. (Ties directly to through-line #2, "From asking to delegating.")

**The subtle, load-bearing point — management distances you from the work.**
Everyone senior here knows the end-stage of a scholarly career: you become a
**scientific manager**, and the activity devolves into the *activity of
management.* Some enjoy that — but it **necessarily distances you from the work
itself, which may be the pleasurable part.**

**The reframe of "skill" — the ethical payload.** Part of *liberation* is that it
matters **less what you know technically.** What matters most becomes a question
of **self-knowledge**: figure out, for yourself, which of your activities are
- **instrumental** → therefore **delegable**, and which are
- **constitutive** → the parts that actually give you **joy and meaning.**

You want to spend as much time as possible on the **constitutive** kind. *That* is
the answer to round 1's opening question — **"what is a knowledge worker supposed
to do now?"** Answer: do the constitutive work; delegate the instrumental.

### Brain dump — round 5 (VW): trust, provenance, and the ethics of asymmetric effort

**We already live with provenance double standards.** We aren't careful about how
our **pencils, toothbrushes, shoes, food** are made — the complexity of global
logistics is **too much for one person to hold, audit, and understand.** So we
**trust these things to just work** — and we're rational to, because there are
**incentives, feedback loops, and regulation** in place to correct them. The
"where did this come from?" purism we apply to AI output isn't applied evenly.

**What's phenomenologically new.** Coding agents let us **engage with far larger
swaths of information than before.** A language model is, in a sense, a **decent
compression of the entire internet**, and it has **enough common sense to use
tools.** So the **range and depth of information manipulation anyone can now
achieve is orders of magnitude greater** than ever before.

**The honest open question.** It's genuinely *unresolved* how to set these
pipelines up so they're **auditable and trustable.** But the answer is
**use-dependent**:
- For **triage / personal use** (the SLT case): **perfectly fine.** You bear the
  cost of your own shortcuts; the stakes are yours.
- For **writing an entire paper**: now there are real **ethical questions.** It's
  a **violation of basic conscientiousness** to produce something with very
  little effort of your own and then **force human peer reviewers to read it.**

**The unifying principle — the "reply all" ethics of information.** A reply-all
email costs *you* 30 seconds but can collectively **eat hours of everyone else's
time.** Same structure here: the wrong isn't *using the tool*, it's **offloading
your saved effort as a cost onto a non-consenting commons.** Cheap to produce,
expensive to absorb. Personal use **internalizes** the cost; slop-into-peer-review
**externalizes** it. *That* is where the ethical line actually falls — not at
"did a machine help?" but at **"who pays for the effort you skipped?"**

### Brain dump — round 6 (VW): the technical basics — and how few there are

**Reassurance first (the bike metaphor, sharpened).** Now for the technical
details I promised — *but don't worry if you're not technical.* **Knowing how to
*fix* a bike is a different skill set from knowing how to *ride* one.** If all you
want is to ride, you don't need to know how everything works in full detail; only
at a **very high level of riding** does it start to help to know how bikes are
*made.* (This is the cleanest statement yet of the north star, lines 12 & 18–19 —
it defines *what this talk chooses to teach*.)

**The good news — the surface area is tiny.** There aren't many things to know to
capture **~90% of the use cases** you'd want, *especially* if your goal is just
the **freedom to manipulate information.** In no particular order, the core is:
- **MCPs** — *(the "USB port for tools," line 25)*
- **Agent skills** — *(modularized, reusable procedural knowledge, line 27)*

**"And honestly, that's about it."** Two concepts carry the bulk of the value.

**Two small side things (supporting cast, not the core):**
- **Interfaces — what you choose to build.** Very often you'll just **spin up a
  local website** for the maximum amount of freedom. *(This is itself the
  liberation thesis in action — you pick the presentation mode; round 3. And it's
  exactly the PreTeXt deliverable idea, lines 35–38: the talk's own artifact is an
  instance of the technique it teaches.)*
- **Local information organization / bookkeeping — for your own ability to
  audit.** Something **richer than folders.** VW uses **Obsidian MD**; alternatives
  are **Logseq** *(transcribed "FogSec" — confirm)* and **Notion.** *(This is a
  partial, personal-level answer to round 5's auditability question — provenance
  you build into your own workspace, not something you wait on regulation for. The
  SLT pipeline already used Obsidian, so this isn't new tooling — it names what the
  demo quietly did.)*

### Round 7 (VW + Claude): the MCP mental model — done precisely

**Verdict on the SLT YouTube step: NOT an MCP.** Pulling videos + local
speech-to-text was the agent using its **native powers** (read/write files, run
any program on your machine — i.e. it wrote and ran a script like `yt-dlp` +
Whisper). That's **tool use**, not MCP. *Diagnostic:* did you *install/configure
an MCP server*, or did the agent *just run a script*? If the latter, it's not MCP.

**The agent's NATIVE powers (out of the box):** generate text, and — for a coding
agent — **read/write your files** and **run any program on your machine.** Lots of
"reaching outside" is just this. MCP is for something more specific.

**What MCP is — the precise USB-C metaphor:**
- *Before USB:* every peripheral had a proprietary connector. Connecting **N
  devices × M computers** needed bespoke cables/drivers per pair — a mess.
- *USB:* standardized the **port + handshake.** Any device plugs into any port,
  declares itself, host knows how to talk to it. **N×M → N+M.**
- **MCP = USB-C for agents.** Same problem (N agents × M services: email, Drive,
  databases, web search, Zotero…), same fix: a vendor writes **one MCP server**;
  **any** MCP-speaking agent can use it.
- **THE load-bearing distinction:** *MCP is the connector standard, not the
  device.* "Was the YouTube data an MCP?" ≈ "is my hard drive a USB?" No — the
  drive is the device, USB is how it connects. The **MCP server** = the standard
  plug on a capability; the **agent** = the standard port; the **capability**
  (Gmail/Drive/DB/web/Zotero) = the device.

**How to use SLT on stage (honest + stronger): demo-first, name-second.**
1. *Motivate* with SLT: "the agent had to step outside itself to fetch from the
   world" — the recurring need. ✔
2. *Name the problem:* "for a service you'll reuse, you want a standard plug, not
   a bespoke script each time."
3. *Show a REAL MCP this room cares about:* a **Zotero MCP** (their reference
   library!), or note that a live session can have **Gmail / Google Drive /
   Google Calendar** plugged in via MCP — "find me that paper in my Drive" just
   works because Drive is *in the port.* (These were live MCPs in this very
   session — viable live demo.)

### Round 8 (VW): MCPs as virtual hands AND eyes — the feedback/iteration point

**Working definition (VW).** MCPs are **USB dongles for tools** you plug into your
coding agent. If there's *other software* you want your agent to use, the agent
needs **virtual hands and virtual eyes** to operate it and get feedback — that's
what an MCP provides.

**The acronym, as a mnemonic.** *Model Context Protocol* — model = the coding
agent; context = the tool you hook in; protocol = how the two interact. *(Note —
useful teaching gloss, but slightly off the official sense: "context" really
means the data/capabilities surfaced* to *the model, not the tool itself. Fine to
use as a mnemonic if you flag it as one; a sharp attendee may quibble.)*

**Examples, simple → complex.**
- *Simple:* the agent reads/writes/sends your **email** via an email client.
- *Complex:* **computer-aided design** — the agent talks to the CAD tool directly.

**The opinionated core — feedback enables iteration (the real value).** It's not
just *reach.* When the agent uses the tool, the MCP feeds back results it can
**learn from and iterate on.** Flippant example: ask the agent to **build you a
website.**
- *Without eyes:* it's a **blind expert** hoping its output matches what you
  pictured. You say "move that component left," and it has to infer the visual
  result **by staring at formatting code.**
- *With an MCP (Puppeteer / Playwright):* it gets **richer feedback** — *take a
  screenshot and look*, or actually **drive the browser, click, move the cursor**
  like a human.
- **Punchline:** once there's feedback, the agent can **iterate until it hits the
  goal.** *No feedback → no iteration.*

**Refinement (Claude) — so the talk doesn't overclaim:**
- *Sharpening "reach":* an MCP is best described as a **sensorimotor channel** —
  *hands* (act on the tool) **and** *eyes* (perceive the result). That upgrades
  the earlier "reach" word (round 7) and pairs cleanly with **Skill = know-how.**
- *Feedback→iteration is the general agentic loop, not MCP-exclusive.* Native tool
  use already iterates (the agent reads a script's error output and tries again).
  The precise MCP claim: it **adds a sensor/actuator the tool otherwise lacks** —
  e.g. *vision* onto a rendered webpage. The loop is the engine; MCPs wire new
  senses into it.
- **Demo gift:** a **Playwright MCP is live in THIS session.** The website-iteration
  story is directly demoable — the most visceral "watch the agent get *eyes*"
  moment you can give the room.

### Round 9 (VW): DEMO PLANNING — feedback-fixing-a-website (shape TBD)

**The candidate demo.** A small live demo of **feedback in action** — agent fixes
up a little website using *eyes* (screenshot/Playwright) and iterates. Directly
illustrates round 8 (hands + eyes → iteration).

**Open decision (deferred on purpose).** Maybe run this *here* (right after the
MCP segment), **or** save a single bigger demo for **later** that showcases *all*
the principles at once. Decide the shape after more dumping.

**The meta-move worth not missing — "cook while you talk."** Vibe coding is
**async**: you can kick off a build and *keep talking while it cooks in the
background.* That's not just a convenience — it's **itself a demonstrable
principle** (background/asynchronous agentic work; the "organization of agents
across time" from rounds 3–4). Strong staging idea: **start a demo cooking at the
top of the talk, keep speaking, and reveal the finished artifact at the end** —
the talk's structure *becomes* a proof of the async claim. (Pairs with the
"~1 hour awake" SLT stat — both make the friction-collapse visceral.)

### Round 10 (VW): agent skills via the orchestration duality (one-man play)

**Background — the delegation story.** Obvious early idea: if one model is good,
**teams of models** talking among themselves and delegating in organized ways
could get more done. But only **fairly recently** did models get strong enough to
actually reap **dividends from delegation.**
- *Early failure mode (good anecdote):* models would delegate **trivial** tasks —
  "write this function" → delegate → the delegate re-delegates → **infinite chain
  of delegation.**
- Hence a back-and-forth over **orchestrations** (industry term) / **"agencies"**
  (Hylab's term — *local jargon, flag as such*): structured model-to-model comms.

**The duality (the mental model).** A skill is, loosely, **a script/protocol
folded into instructions given to a *single* model.** So:
- Any **organization of people** passing messages can be re-staged as a
  **one-man play**: one person with a **pile of hats** + a set of **instructions
  per hat.** They put on a hat, do that role's bit, take it off, **check the
  mailbox**, put on the next hat, and so on.
- The **only** real difference is **parallelism** — how much happens *at once*
  (orchestration, many agents) vs. **sequentially** (one agent, many hats).
- **Skills ≈ the sequential one-man play** (first approximation) — *but* a skill
  can **also dispatch sub-agents**, so the parallel/sequential line is a spectrum,
  not a wall. *(VW: "I'll get into skills in a bit" — this is setup.)*

**Connections:** concretizes round 4 ("if I had a team, what would I tell them &
how would they talk?"); sits opposite MCP in the **reach/know-how** pair (rounds
7–8) — *MCP bolts on a sense/limb; a skill installs a habit/role.*

**Claude — calibrations to keep it accurate (for when you "get into skills"):**
- *Two complementary lenses on "skill," don't let them blur:*
  (1) **packaged, reusable know-how** — externalized tacit procedure / "house
  style" (lines 27–28, through-line #3); (2) **the single-agent embodiment of
  what a team would orchestrate** (this round). Compatible: a skill is reusable
  packaged procedure, and *one kind* of procedure it can hold is a multi-role
  workflow a team would otherwise parallelize. The hats are the bridge, not the
  definition.
- *The "one instruction" gloss undersells it.* A real Claude **agent skill** is a
  **named, on-demand-loaded bundle** (a `SKILL.md` with a *description that
  triggers it automatically* + optional **scripts/resources**), which the agent
  **reaches for on its own** when relevant — not just text you paste once. Nail
  the auto-trigger + reusable-bundle properties when you define it.
- *"Duality" = elegant intuition, not a formal one.* Boundary blurs both ways
  (skills spawn sub-agents; an orchestration can be collapsed into one skill).
  Present it as a *way to see it*, and you're bulletproof.

### Round 11 (VW): context as short-term memory — windows & compaction

**Demo aside.** For *both* MCPs and agent skills, worth a **small website that
visually demonstrates** the concepts (ties to round 9 + the deliverable site,
lines 35–38). And here's the minimal "how the bicycle works" needed: **context.**

**Context = short-term (working) memory.** As the conversation continues, the
agent builds up **chat context.** For any new turn, it looks back over that
accumulated memory to produce its response. Think of it as **working memory**, not
permanent storage.

> ⚠️ **FACTUAL CORRECTION — fix before any slide.** VW said context windows are
> *"about a billion tokens."* **That's wrong by ~1000×** — and it contradicts the
> ~200k figure VW gives two sentences later. Real numbers (2026): **Claude
> standard ≈ 200k tokens** (1M-token beta on some tiers); **Gemini / GPT-4.1
> frontier ≈ 1M** (Gemini ~2M experimental). So: *"a couple hundred thousand,
> up to about a million at the frontier."* **Never say "a billion."**

**Degradation — "models get a bit dumb" as context fills.** Too much context →
too many interrelationships to attend to at once → quality drops. For Claude,
rough order **~200k tokens.** *(Calibration: this is also ~the window size, so VW
is really saying "it degrades near its limit." More precisely, "context rot" is
**progressive** — quality can erode well before the hard limit, not just at the
edge. Worth saying it's a gradient, not a cliff.)*

**Managing context (accurate).**
- **Manual:** clear the context yourself (`/clear`) when starting something new.
- **Automatic — compaction:** when context gets large, the model "takes a break,"
  **summarizes** its working memory into a small chunk, and **starts afresh** from
  that summary.
- **Repeated compaction → "sedimentary layers":** nested/telescoping summaries
  that compress the deeper past more aggressively. *(Nice metaphor, and accurate —
  each compaction summarizes a context that may already contain prior summaries.)*

**Why this belongs in the talk:** it's the setup for *why* skills load **on
demand** (progressive disclosure — don't burn working memory holding every
procedure at once) and why context hygiene is a real workflow skill. Keep it to
the *minimum* needed — bike mechanics only insofar as they help you ride.

### Round 12 (VW): three ways to live within the context limit (skills = the middle ground)

*Given the context/working-memory limit (round 11), there are a few strategies:*

**1. Orchestration (spatial modularization).** Multiple agents, each with a
**fixed instruction upfront** (fixed role), receiving **variable context as
input** and emitting **output** along the orchestration. **No compaction tricks
needed** — you've **modularized**: each agent is on a **factory line**, applying
its one fixed instruction to a small bit of new context it **doesn't have to hold
onto.** *(Concretizes the round-10 duality — the parallel side.)*

**2. Offload context to the file system (long-term memory).** Have the coding
agent **push context into files.** Frame: **file system = long-term memory** vs.
**context = short-term memory.** Short-term memory carries a pointer: *"if you
need to know about X, look in long-term memory (the files)."*
- This is roughly what **`CLAUDE.md`** does: general per-project instructions,
  **including where to look** for long-term memory that needn't live in
  short-term context. *(Accurate — and note the subtlety VW gets right:
  CLAUDE.md is the always-loaded **index/pointer**; the files it points to are the
  **on-demand** long-term store.)*

**3. Skills = the elegant middle ground.** *(Dump cut off at "This…" — payoff
pending.)* Reading ahead: a skill behaves like **(2)** — *loaded on demand*, so it
doesn't sit in working memory until needed (progressive disclosure, round 11) —
but it carries **active procedure / a role**, like **(1)**'s fixed-instruction
agent — *without* the overhead of spinning up a separate agent. So skills =
**progressive-disclosure memory + role**, minus the cost of either extreme. *(VW
to confirm/extend.)*

**Structure note:** rounds 10–12 now form a clean arc — *the context limit (11)*
→ *two extremes for coping (orchestration / file-offload, 12)* → *skills as the
synthesis.* This is a strong teaching order.

### Round 13 (VW): how skills actually work — the progressive-disclosure mechanism

**The payoff to round 12's cliffhanger.** A skill keeps instructions in **long-term
memory** yet lets them be **invoked on demand as if they were in flexible
short-term memory — without taxing the context window.** Mechanism:

**A skill is just a Markdown (`.md`) file, with a twofold structure:**
1. **A small header — the firing conditions.** Indicates *when* the skill should
   be used. E.g. a web-design skill: *"if the user wants to make a website / do
   the thing this skill pertains to → use this skill."* Carries a **short
   description** + **positive and negative examples** (what it should and
   shouldn't do).
2. **The body — procedural knowledge, of essentially any form.** "Present the
   user a questionnaire," "do these steps with these serial dependencies," "use
   these tools," "heuristics to follow," "heuristics to avoid," "musts and
   must-nots," etc.

**The clever bit (the whole point).** The working agent's context only needs to
hold the **tiny header** up front. So you can load **many, many skills at once** —
all the headers together take **very little space**, sitting where the agent can
attend to them. When a task **pertains to** a skill, the agent recognizes it
("oh, you're doing X — I have a skill for that"), **pulls up the full body**, and
works according to it — **relativized to whatever task you're doing.**

**Claude — sharpenings (enhancements, not corrections; this round is accurate):**
- *Name the parts so they can find them:* the "header" is the **YAML frontmatter**
  (`name` + `description`); the **`description` is the trigger string** the model
  matches against. (Real examples in *this* session use explicit "**Use when… /
  SKIP when…**" — your positive/negative examples, in the wild.)
- *It's about **size**, not position.* Headers are cheap because they're **small**
  (only metadata loads up front), not because they're "near the beginning." Frame
  it as: 50 skills' worth of descriptions ≈ trivial context; 50 full bodies ≈
  would blow the window. That's *why* on-demand loading matters.
- *Bodies can bundle **runnable scripts/resources**, not just prose* — and those
  load even more lazily (referenced files pulled only if needed). A skill can ship
  *tools*, not only instructions. (Deeper progressive disclosure.)
- *Beautiful closure:* a skill **is** the round-11/12 **"index + archive" pattern,
  self-contained** — the header is the always-loaded *pointer* (like CLAUDE.md's
  role), the body is the *on-demand long-term store*. Skills mechanize the exact
  thing you taught two rounds earlier.

**Demo tie-in (round 9/11 aside):** this is the single most *visualizable*
concept — *many small headers loaded → task arrives → one body expands into
context → collapses again.* A 20-second animation of that teaches progressive
disclosure better than any paragraph. Strong candidate for the explanatory site.

### Round 14 (VW): the bootstrapping payoff — agents build their own MCPs & skills

**The clean two-liner mental model (final form):**
- **MCPs = reach** — tie your model into another tool + give it **sensorimotor
  feedback** on that tool (rounds 7–8).
- **Skills = packaged procedural knowledge** for your agent (rounds 10–13).

**The liberating part — the agent makes these *for* you.**
- *Novel tool, no MCP yet?* Your coding agent can **build the MCP** — and *you
  work with it* to determine how it should behave. (Note the collaboration; not
  push-button magic — but the barrier collapses.)
- *Skills?* **You don't write them by hand.** There's an **information-expansion
  effect**: **skills that write skills**, and **skills that optimize skills.**

**Concrete, verifiable example — `skill-opt`** (in the tinkering folder; *loaded &
confirmed live in this very session*). It **ports Microsoft's open-source SkillOpt
research.** Originally an **orchestration** — VW **used the round-10 duality to
collapse it into a single skill** — and now it's **a skill that optimizes other
skills** (a rollout→reflect→edit→gate→memory loop that treats a `SKILL.md` as a
trainable document, model frozen).

**Why this round matters (the arc closes):**
- **The duality (round 10) was not just pedagogy — VW *used* it in anger** to turn
  a multi-agent orchestration into one skill. Real artifact > clever analogy.
  *This is the credibility moment: "I didn't just theorize the duality, here's me
  shipping it."*
- **Round 4 fully cashed.** "It matters less what you know technically" → now even
  *making the tools* is delegated. The technical surface area shrinks toward zero;
  what remains is **judgment about what you want** (the constitutive/instrumental
  discernment). The last excuse — *"but there's no skill/MCP for my niche thing"* —
  is removed: the agent builds it.
- **Reflexivity worth one beat (don't overcook):** tools that operate on tools,
  a system that extends its own capabilities. Mildly Gödelian; a philosophy room
  will feel it. Keep the round-1 anti-hype posture — *real, but you still steer.*

### Round 15 (VW): the close — manager trap, do-what-makes-you-happy, and "why are we necessary?"

**Demo cooking.** A **Pure Data (Pd) MCP** is being built on the side as a demo
vehicle. *(Links to the existing Pd-MCP project — Pd as the visible instrument.
This is the second live demo alongside the Playwright website-feedback one.)*

**"That's all the big points."** The rest of the talk is **live / whatever comes
to mind.**

**The philosophical landing (closes the round-1 frame):**
- **The manager trap.** Using these, you'll be tempted to open a **second**, then
  a **third** agent — and you'll be **naturally drawn into just *managing* what
  they do.** *(This is the round-4 "scientific manager distances you from the
  work" point — now about managing the **agents themselves**. The automation can
  re-inflict the very alienation it promised to remove.)*
- **So do what makes you happy.** Deliberately. Because —
- **The blunt version (closes round 1).** *It's not clear why any of us are
  necessary anymore.* We're plausibly **here** — selected, employed — because we
  were **particularly good at handling cognitive friction.** But **that's no
  longer a skill that needs to be tied to humans** for a lot of knowledge work.
  → Resolution = round 4: when the friction-justification is gone, optimize hard
  for the **constitutive** (meaning/joy), not the **instrumental.**

**NEXT STEPS (VW's stated plan):**
1. **Go through all the points again** (review pass). ✔ done as the spine doc.
2. **Separate document → work out the spine beats.** → see **`spine-beats.md`.**
3. **Then:** scaffolding for a **website with visual interactive explainers** for
   the technical concepts. *(Phase 3 — queued; confirm scope before building.)*

---
*Brain dump complete (rounds 1–15). Spine synthesis → `spine-beats.md`.*
