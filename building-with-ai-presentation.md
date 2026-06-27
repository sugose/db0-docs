# Building with AI: What We Did, What We Learned, What It Means
## Conference Presentation — Slide Outline & Speaker Notes

**Target runtime:** 45–50 minutes  
**Audience:** AI conference — prospects to practitioners  
**Format:** Story-driven narrative with modular sections

---

> ### HOW TO USE THIS DOCUMENT
> Each slide is marked with an **[AUDIENCE TAG]**:
> - 🟢 **ALL** — works for every audience
> - 🔵 **PROSPECTS** — especially valuable for non-technical or AI-curious attendees
> - 🟠 **PRACTITIONERS** — especially valuable for technical or AI-experienced attendees
>
> For a shorter 25–30 minute version aimed at prospects: use slides marked 🟢 and 🔵, skip or compress 🟠 slides.  
> For a practitioner-heavy audience: keep all slides, spend more time on 🟠 sections.

---

## SECTION 1: THE HOOK
*Estimated time: 5 minutes*

---

### SLIDE 1 — Title Slide 🟢

**Visual:** Clean title slide  
**Text:**
> *Building with AI*  
> What We Did. What We Learned. What It Means.

**Speaker notes:**  
Good [morning/afternoon]. I want to start by asking you something. How many of you have used AI in the last week? Keep your hand up if you used it to ask a question and get an answer. Now keep your hand up if you used it as part of a structured, repeatable development process with defined roles, quality gates, and a PR review cycle.

That's the gap I'm here to talk about today.

---

### SLIDE 2 — The Glorified Google Search 🟢 🔵

**Visual:** Split image — old Google search box on left, AI chat interface on right  
**Text:**
> "For most people, AI is a smarter search box."  
> Ask. Answer. Move on.  
> *That's not wrong. But it's dramatically underselling what's available.*

**Speaker notes:**  
In practice, for the vast majority of users, AI has become a glorified Google search. A smarter prompt box that returns a better-formatted answer. You ask it to summarise something. You ask it to draft an email. You get the answer and move on.

That's useful. But the ceiling is far higher than that. And most people — including most people in this room — aren't using anywhere near what's available.

Today I'm going to show you one way to think about it differently.

---

### SLIDE 3 — The Question That Changes Everything 🟢

**Visual:** Single bold question on screen  
**Text:**
> *"Can AI help me do something I fundamentally cannot do alone?"*

**Speaker notes:**  
That was the question that drove everything I'm going to talk about today. Not "can AI make me faster." Not "can AI write this email for me." But: can it help me do something that would otherwise be completely out of reach?

That's a much harder question. And the answer — spoiler — is yes. But only if you're intentional about it.

---

## SECTION 2: WHO I AM AND WHY THIS MATTERS
*Estimated time: 5 minutes*

---

### SLIDE 4 — The Profile 🟢

**Visual:** Simple timeline — Developer → Team Lead → Product/Process → Here  
**Text:**
> - Background in programming  
> - Moved into process, teams, product management  
> - Knows what good looks like. Can't easily build it anymore.  
> *Sound familiar?*

**Speaker notes:**  
Let me tell you a bit about where I'm coming from, because it's relevant to whether any of this applies to you.

I started out as a developer. Over time I moved — as many people do — into leading teams, managing product development, working on process and organisation. The coding skills quietly rusted. The organisational judgment accumulated.

By the time I started these projects, I understood what good software development practice looks like from the inside. TDD, code review, PR cycles, architectural discipline — I'd managed teams that did these things. I just couldn't sit down and do them myself anymore.

There's a difference between not knowing what good looks like and not being able to produce it. I knew what good looked like. I had an execution gap. And AI became the way to fill it.

---

### SLIDE 5 — The Execution Gap 🟢 🔵

**Visual:** Simple diagram — "What you know" on one side, "What you can build" on the other, a gap between them  
**Text:**
> The execution gap:  
> *The space between understanding a principle and being able to implement it.*

**Speaker notes:**  
This execution gap is more common than people admit. There are a lot of people in the world who understand what should be built and how it should work, but can't build it themselves. Product managers. Domain experts. Ex-developers who've moved into leadership. Entrepreneurs with great ideas and no technical co-founder.

AI doesn't eliminate the gap. But if you use it with enough structure and discipline, it can bridge it.

---

## SECTION 3: THE ORIGIN STORY
*Estimated time: 8 minutes*

---

### SLIDE 6 — It Started On A Lake 🟢

**Visual:** Photo of a lake — ideally Lake Mälaren or similar Scandinavian fishing scenery  
**Text:**
> Lake Mälaren, Sweden.  
> Pike. Perch. Zander.  
> Advanced sonar. Unreadable data.

**Speaker notes:**  
None of this was planned. It started with fishing.

I spend a lot of my free time on Lake Mälaren in Sweden, fishing from my boat. I'm the kind of angler who invests in equipment — my boat has advanced sonar gear that gives me data most anglers can't access. The problem isn't the data. The problem is interpretation. Reading a sonar screen is a skill that takes years to develop. The image is dense, noisy, ambiguous. Best described as static TV interference hacked into a boulder. Even with the best equipment, the difference between a promising reading and a false alarm is often invisible to anyone but an expert.

---

### SLIDE 7 — FOMO-f: Fear Of Missing Out Fish 🟢

**Visual:** Sonar screen image alongside the FOMO-t logo concept  
**Text:**
> *"What if AI could read the sonar for me?"*  
> **FOMO-f** — Fear Of Missing Out Fish  
> Part of **FOMO-t** — Fear Of Missing Out Tech

**Speaker notes:**  
With a summer vacation approaching and a growing awareness of what AI image analysis could do, the idea formed. Pattern recognition in noisy visual data is exactly what AI is good at. And I had two genuine fears: missing the fish right under my boat, and missing the AI wave entirely.

FOMO-f — Fear Of Missing Out Fish — was born. The first project of the imaginary tech group FOMO-t: Fear Of Missing Out Tech.

But something unexpected happened while building it.

---

### SLIDE 8 — The Scaffolding Was The Product 🟢 🔵

**Visual:** Scaffolding around a building under construction  
**Text:**
> Building FOMO-f required:  
> Agent roles. PR cycles. TDD discipline. Handoff documentation.  
>  
> *The process that emerged was more reusable than the product itself.*

**Speaker notes:**  
While building FOMO-f I found myself spending more time establishing how the project should work than building the product itself. And what emerged from that setup work looked increasingly like it had value beyond FOMO-f. The process — the agent roles, the PR cycle, the testing discipline, the documentation — was coding-language-agnostic. It worked the same way whether the implementation language was Python or JavaScript.

The scaffolding was reusable. That led to the ai-project-template repository.

---

### SLIDE 9 — Proving The Template: Blackjack 🟢

**Visual:** Playing cards — blackjack table aesthetic  
**Text:**
> A template nobody has tested is just a theory.  
>  
> **Project 2: Blackjack Casino Simulator**  
> *(The product was almost beside the point)*

**Speaker notes:**  
A template nobody has tested is just a theory. It needed proving. So we built a Blackjack Casino simulator. Not because the world needed another blackjack game, but because we needed a real project in a completely different domain to see if the template held up.

The bootstrap was remarkably painless. Minor adjustments, minimal friction. Before long the simulator had grown to the point where the next implementation epic was ChaosMode — a mode where AI players start tipping and bribing the house in exchange for extra drinks and card value deductions, with simulated intoxication levels causing escalating havoc at the table. Not a trivial feature. A genuinely fun one.

And then the World Cup started.

---

### SLIDE 10 — The World Cup Problem 🟢

**Visual:** Football stadium at night, or a TV showing a match  
**Text:**
> FIFA World Cup 2026. Middle of the night. Sweden playing.  
>  
> *What was I actually doing?*  
> Discussing drunk blackjack AI with Claude.

**Speaker notes:**  
I had been looking forward to the World Cup. Sweden were in it. The games ran in the middle of the night — vacation schedule, no work the next morning, perfect setup for watching football. What actually happened was that I found myself deep in discussions about increasingly unhinged ChaosMode implementations, with total disregard for the matches on screen behind me.

The World Cup was on. I was talking to an AI about drunk blackjack dealers.

Something needed to change. And since I clearly wasn't going to stop building things, what needed to change was having a way to track the football while I did it.

---

### SLIDE 11 — titan-comptracker Is Born 🟢

**Visual:** Mobile phone mockup showing the app interface  
**Text:**
> **titan-comptracker**  
> Real-time football competition tracker  
> First ever mobile app. Third template bootstrap.  
>  
> *Could the template handle a fundamentally different tech stack?*

**Speaker notes:**  
titan-comptracker — a real-time football competition tracker — was the result. Built to solve a personal problem, and to answer a question: could the ai-project-template bootstrap a mobile app project as cleanly as it had bootstrapped the casino simulator? A completely different tech stack — React Native, TypeScript, Expo — not Python.

It could.

---

## SECTION 4: WHAT WAS ACTUALLY BUILT
*Estimated time: 5 minutes*

---

### SLIDE 12 — Three Projects, One Workflow 🟢

**Visual:** Three-column layout — FOMO-f | Casino Sim | titan-comptracker  
**Text:**
> | | FOMO-f | Casino Sim | titan-comptracker |
> |---|---|---|---|
> | Domain | Fishing / sonar | Gaming | Football |
> | Stack | Python | Python + web | React Native / TS |
> | Purpose | Product | Template proof | Template + mobile proof |

**Speaker notes:**  
Three projects. Three completely different domains. One workflow backbone.

FOMO-f: AI sonar analysis. Python. Where the workflow was born.
Casino simulator: Also Python, deliberately. Validate the template without adding the variable of a new language.
titan-comptracker: React Native, TypeScript, Expo. The deliberate step up in technical complexity — a fundamentally different stack to prove the template generalises.

That last point is worth dwelling on.

---

### SLIDE 13 — One Variable At A Time 🟢 🟠

**Visual:** Scientific experiment aesthetic — controlled variables  
**Text:**
> *"When proving something, change as few things as possible at once."*  
>  
> Fewer variables → cleaner cause and effect  
> This is agile thinking applied to workflow design.

**Speaker notes:**  
There's a principle behind those choices that runs through everything we did. When you're trying to prove or disprove something, change one thing at a time. If the process and the tech stack both change simultaneously and something breaks, you can't tell which one caused it.

This is the same principle behind short agile iterations. One meaningful change. Observe the result. Learn. Move forward. We applied it not just inside the projects but to the design of the project framework itself.

---

### SLIDE 14 — The Tech Stack (for the curious) 🟠

**Visual:** Technology logos — React Native, TypeScript, Expo, Reanimated  
**Text:**
> React Native + Expo SDK 54  
> TypeScript  
> React Native Reanimated (UI-thread animations)  
> AsyncStorage | expo-image | Gradle / Android SDK

**Speaker notes:**  
For those who want to know what was actually under the hood on titan-comptracker — this is a production-grade mobile stack. React Native for cross-platform native UI. TypeScript for type safety. Reanimated for smooth animations that run on the UI thread rather than the JavaScript thread. These aren't toy choices — they're the same stack you'd find in professional mobile development shops. And it was built by someone who couldn't write a line of it independently.

*(Skip or compress this slide for non-technical audiences)*

---

## SECTION 5: THE WORKFLOW
*Estimated time: 8 minutes*

---

### SLIDE 15 — The Team 🟢

**Visual:** Four boxes — Adam | Clead | Crog | Copi  
**Text:**
> **Adam** — Product Owner (human)  
> **Clead** — Tech Owner / Architect (Claude, chat)  
> **Crog** — Senior Developer (Claude Code CLI)  
> **Copi** — Automated PR Review (GitHub Copilot)

**Speaker notes:**  
Here's who was in the room. And I use that phrase deliberately — these feel like roles in a team, because they function like one.

Adam is the human. Product Owner. Defines what gets built, makes final calls, never gets bypassed.

Clead is Claude in the chat interface. Tech Owner and architect. Reviews every pull request. Maintains the architectural vision. Wrote the document this presentation is based on.

Crog is Claude Code CLI — the command-line agent that does the actual implementation. Writes the code, runs the tests, manages Git, opens pull requests.

Copi is GitHub Copilot, providing automated review as an additional quality layer.

---

### SLIDE 16 — The PR Cycle 🟢 🟠

**Visual:** Circular flow diagram of the 7 steps  
**Text:**
> 1. Spec defined (Adam + Clead)  
> 2. Failing test written (Crog)  
> 3. Implementation until tests pass (Crog)  
> 4. PR opened with full diff summary  
> 5. Clead reviews → approve or reject with exact instructions  
> 6. Adam relays to Crog  
> 7. Merge confirmed  
>  
> *Every change. No exceptions.*

**Speaker notes:**  
Every change — no matter how small — goes through this cycle. A one-line fix goes through this cycle. There are no shortcuts.

Why? Because the discipline is the point. TDD is non-negotiable. No code gets written before a failing test exists. No merge happens without review. The human is in the loop at every decision point of consequence.

For practitioners in the room: yes, this is more ceremony than a solo developer needs. That's intentional, and I'll explain why in a moment.

---

### SLIDE 17 — Why So Much Process? 🟢

**Visual:** Safety net under a tightrope walker  
**Text:**
> An experienced developer has internalised the checks.  
> Their experience *is* the safety net.  
>  
> *The process replaces what competence provides.*

**Speaker notes:**  
This is the question I always get. Isn't this over-engineered for a solo project?

Here's the answer: it depends entirely on who the solo developer is.

A seasoned developer working alone carries the checks and balances in their head. They know when to write tests. They catch their own architectural mistakes. They know what they don't understand. Their experience is the safety net.

I don't have that safety net for implementation. So the process becomes the safety net instead. The workflow is calibrated to the person, not to an abstract standard of efficiency. The right question isn't "is this over-engineered?" It's "over-engineered for whom?"

---

## SECTION 6: WHAT AI MADE POSSIBLE
*Estimated time: 5 minutes*

---

### SLIDE 18 — Five Years Ago, This Wasn't Possible 🟢 🔵

**Visual:** Timeline — 2021 vs 2026  
**Text:**
> 2021: To do this, you'd need to hire:  
> → A tech lead  
> → A developer  
> → A QA engineer  
>  
> 2026: One person. One summer. Three projects.

**Speaker notes:**  
Five years ago, this project would not have been possible for someone in my position. The execution gap was unbridgeable without people. You'd need to hire a tech lead for architectural decisions, a developer to write the code, maybe a QA engineer to enforce the testing discipline. For a passion project or early-stage idea, that cost — financial and organisational — is prohibitive.

The AI tools collapsed that requirement. Not by removing the need for good judgment, but by providing the execution capability that judgment couldn't previously unlock.

---

### SLIDE 19 — A Genuine Collaboration, Not A Magic Box 🟢

**Visual:** Two-column table — What Adam brought | What Claude brought  
**Text:**
> | Adam brought | Claude brought |
> |---|---|
> | Product sense | Technical execution |
> | Process knowledge | Architectural reasoning |
> | Organisational discipline | Quality enforcement |
> | Domain decisions | Implementation |

**Speaker notes:**  
This is a more interesting use of AI than "write me a function." It's using AI as a genuine collaborator in a structured system, with roles, responsibilities, and accountability. Not a magic box that spits out code. A collaborator that you direct, review, and hold to a standard.

Together, these two columns cover the full stack of what a small development team would provide. One human. Multiple AI agents. Real software. That's new.

---

## SECTION 7: CONCLUSIONS & IMPLICATIONS
*Estimated time: 10 minutes*

---

### SLIDE 20 — The Template Adapts To You 🟢 🔵

**Visual:** The ai-project-template GitHub repo  
**Text:**
> The template is self-documented.  
> Rule sets, checks, agent roles — all inside the repo.  
>  
> *Fork it. Talk to Clead. Adapt it to your situation.*  
> It's a starting point with a built-in advisor.

**Speaker notes:**  
One of the most important properties of the ai-project-template is that it's self-documented. The rule sets, the PR conventions, the agent roles — they're all written down inside the repository. That means someone new doesn't have to accept it as-is.

You fork the repo. You talk to Clead — Claude in the chat interface — explain your situation, your competence level, your goals. And you collaboratively adapt the ruleset to fit. More experienced developers strip back ceremony. Less experienced ones add more guardrails. Teams adapt the agent roles. Different domains need different quality gates.

The template is a starting point with a built-in advisor. That's what makes it genuinely transferable rather than just theoretically reusable.

---

### SLIDE 21 — The Sweet Spot 🟢

**Visual:** A spectrum — Complete beginner ←→ Expert developer, with a marker in the middle-left zone  
**Text:**
> Too inexperienced: can't evaluate AI output  
> Too expert: loses sight of the system  
>  
> *Sweet spot: knows what good looks like, doesn't get lost in implementation*

**Speaker notes:**  
Who does this work best for? There's a sweet spot.

Complete inexperience makes it impossible to know whether the AI's output is good or terrible. You can't direct it usefully because you don't know what you're aiming for.

Deep current technical expertise can make it hard to step back and think about workflow and process — there's always a more elegant algorithm, a better abstraction. You get lost in the details.

The sweet spot is someone with domain knowledge, process judgment, product sense, and enough technical literacy to evaluate output without getting sucked into implementation debates. That's more people than you'd think.

---

### SLIDE 22 — The Demand Is Latent 🟢 🔵

**Visual:** Iceberg — small visible tip labelled "people searching for this", large submerged mass labelled "people who need this but don't know it exists"  
**Text:**
> They're not searching for "multi-agent development templates."  
> They're asking: *"Can AI help me build my idea?"*  
> And hitting a wall.

**Speaker notes:**  
There are people who could benefit from this approach who don't know it exists. They're not searching for "multi-agent development workflow templates" — they don't know to search for that. They're asking more basic questions: "can AI help me build my idea?" and hitting a wall when the answer requires more setup than they know how to do.

The proof that this works — three projects, working software, repeatable process — is the thing that might eventually reach those people. Not as a product to sell, but as a demonstration that the possibility exists. You don't need a technical co-founder if you're willing to be intentional about how you structure your AI collaboration.

---

### SLIDE 23 — What Started As An Experiment 🟢

**Visual:** Split — fishing boat on left, mobile app on right  
**Text:**
> Started: "Can I build a sonar analysis tool?"  
> Discovered: A reusable development methodology  
>  
> *The answer to the question nobody was explicitly asking.*

**Speaker notes:**  
None of this was planned. The original goal was to answer one question: can I build a sonar tool with AI? That led to a template. The template needed proving. The proof of concept got interrupted by the World Cup. The World Cup produced a mobile app.

Three projects later, the more interesting answer isn't about any of the products. It's about the workflow. A structured, disciplined, human-in-the-loop approach to AI-assisted development can produce real quality at a level that shouldn't be achievable for someone without a technical background. And it can do it consistently, across completely different domains.

That conclusion wasn't designed. It emerged from doing the work and being honest about what it produced.

---

### SLIDE 24 — The Honest Caveat 🟢 🟠

**Visual:** Scales — value vs. overhead  
**Text:**
> An experienced developer working alone would find much of this overhead.  
> That's fine. It's not for them.  
>  
> *The workflow is right-engineered for its context, not universally optimal.*

**Speaker notes:**  
I want to be honest about the limits. A seasoned developer working alone would find a lot of this ceremony unnecessary. And they'd be right — for them. They don't need the PR cycle enforced by mechanics because they enforce it through competence.

This isn't a universal prescription. It's a proof of concept that the right workflow, for the right person, in the right context, can produce something that couldn't exist otherwise. That's the claim. Not that everyone should work this way.

---

## SECTION 8: CLOSE
*Estimated time: 4 minutes*

---

### SLIDE 25 — What This Means For You 🟢

**Visual:** Three paths — for prospects, for practitioners, for everyone  
**Text:**
> **If you're new to AI:** The ceiling is higher than you think. Structure is everything.  
> **If you're an AI practitioner:** The methodology matters as much as the tools.  
> **For everyone:** The question isn't "can AI help me?" It's "how do I organise that help?"

**Speaker notes:**  
So what does this mean for you?

If you're new to AI and wondering what it can do beyond search: the ceiling is far higher than most people use. But you need structure. Asking better questions is not enough. Building a system around AI collaboration is what unlocks it.

If you're an experienced AI practitioner: the tools aren't the differentiator anymore. Everyone has access to the same models. What matters is how you organise the work. The methodology is the competitive advantage.

For everyone: the question has shifted. It's no longer "can AI help me?" — the answer to that is obviously yes. The question is "how do I organise that help so it produces something real?"

---

### SLIDE 26 — The Repository 🟢

**Visual:** GitHub repo URL prominently displayed  
**Text:**
> **github.com/sugose/ai-project-template**  
> **github.com/sugose/titan-comptracker**  
>  
> Fork it. Adapt it. Build something.

**Speaker notes:**  
Both repositories are public. The ai-project-template has everything you need to start: the bootstrap process, the agent role definitions, the PR cycle documentation, the TDD conventions. Fork it. Talk to Clead about your situation. Adapt it to fit.

titan-comptracker is the live proof of concept — a working Android app built by one non-developer, one summer, three projects in.

---

### SLIDE 27 — Closing 🟢

**Visual:** Simple. Lake photo, or just text on a dark background.  
**Text:**
> *"None of this was planned. It started on a lake."*  
>  
> Thank you.

**Speaker notes:**  
I started this talk by asking how many of you had used AI as more than a smarter search box. I hope by now the answer looks more possible than it did 45 minutes ago.

None of this was planned. It started with a fisherman who wanted to catch more pike, got curious about AI, and ended up spending his World Cup vacation building a mobile app.

If that's possible — it's probably possible for you too.

Thank you.

---

## APPENDIX: TIMING GUIDE

| Section | Slides | Estimated Time |
|---------|--------|----------------|
| The Hook | 1–3 | 5 min |
| Who I Am | 4–5 | 5 min |
| Origin Story | 6–11 | 8 min |
| What Was Built | 12–14 | 5 min |
| The Workflow | 15–17 | 8 min |
| What AI Made Possible | 18–19 | 5 min |
| Conclusions | 20–24 | 10 min |
| Close | 25–27 | 4 min |
| **Total** | **27 slides** | **~50 min** |

---

## APPENDIX: AUDIENCE VARIANTS

### Prospect-focused (25–30 min)
Remove or compress: slides 13, 14, 17, 24  
Spend more time on: 6–11 (origin story), 20, 22  
Tone: inspirational, accessible, "this is possible for you"

### Practitioner-focused (45–50 min)
Keep all slides  
Spend more time on: 13, 14, 16, 17, 21, 24  
Tone: honest, rigorous, "here's what we learned and why it matters"

### Mixed audience (45–50 min, recommended)
Full deck as written. Story carries the prospects; the technical depth satisfies the practitioners.

---

*Presentation developed by Clead (Claude) in collaboration with Adam, June 2026*

... and if you appreciated this session, you can get me for next year's conference to tell you about v2 :)
