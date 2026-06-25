# Building with AI: What We Did, What We Learned, What It Means

*A reflection on the titan-comptracker project, the workflow that led to it, and the workflow that emerged from it*

---

## The Question That Started It

Most people approach AI tools as productivity shortcuts. You ask, it answers, you move on faster than before. In practice, for the vast majority of users, AI has become little more than a glorified Google search — a smarter prompt box that returns a better-formatted answer. That's useful. But it's also a dramatically narrow interpretation of what's actually available, and most people simply aren't aware that the ceiling is far higher than that.

The question that drove titan-comptracker was different: not "can AI help me work faster," but "can AI help me do something I haven't done in a long time and can no longer easily do alone?" Specifically — can someone whose programming days are well behind them build a real, production-quality mobile app, end to end, by structuring AI collaboration deliberately enough that quality doesn't get sacrificed along the way?

That's a harder question. And the answer, it turns out, is yes — but only if you're intentional about it.

---

## Who Was In The Room

Adam came to this project with a specific and unusual profile. He has a background in programming, but over time moved away from active development into process, teams, and product management in product development settings. That trajectory is more common than people acknowledge — developers who grow into leadership roles, accumulating organisational and product judgment while their hands-on coding skills quietly rust.

What he retained was substantial: he understood what good software development practice looks like, from the inside. He knew the vocabulary not as an outsider who'd read about it, but as someone who'd lived in those environments. TDD, code review, architectural discipline, PR cycles, technical debt — these weren't abstract concepts. He'd managed teams that practised them. He just couldn't sit down and implement them himself anymore.

That distinction matters. There's a difference between not knowing what good looks like and not being able to produce it yourself. Adam knew what good looked like. The problem was the execution gap — the space between understanding a principle and being able to implement it in code, a gap that had widened over years of moving away from the keyboard.

The hypothesis was: what if you could fill that gap with AI, while keeping the discipline and process intact? What if the checks and balances that an experienced developer carries in their head could instead be baked into the workflow itself — enforced by mechanics rather than personal competence?

---

## How It Actually Started: A Fisherman, A Sonar, And A Fear Of Missing Out

None of this was planned. It started on a lake.

Adam spends a significant part of his free time on Lake Mälaren in Sweden, fishing for pike, perch, and zander from his boat. He's the kind of angler who invests in the equipment — his boat carries advanced sonar gear that gives him information about what's happening underwater that most anglers simply can't access. The problem isn't the data. The problem is interpretation. Reading a sonar screen is a skill that takes years to develop. The image is dense, noisy, and ambiguous — best described as static TV interference hacked into a boulder. Even with the best equipment, the difference between a promising reading and a false alarm is often invisible to anyone but an expert.

With a summer vacation approaching and a growing awareness of what AI image analysis could do, the idea formed: what if AI could help interpret the sonar stream in real time? Pattern recognition in noisy visual data is exactly the kind of problem AI is well suited to. And so **FOMO-f** was born — Fear Of Missing Out Fish — the first project of the imaginary tech group **FOMO-t** (Fear Of Missing Out — Tech). The name captured two genuine anxieties: not catching the fish that's right there under the boat, and not being on the AI train when it leaves the station.

FOMO-f was where the workflow took shape. Building a sonar analysis tool required real infrastructure — API integrations, image processing, a structured development process. Adam found himself spending more time establishing how the project should work than building the product itself. And what emerged from that setup work was something that looked increasingly like it had value beyond FOMO-f. The process — the agent roles, the PR cycle, the TDD discipline, the handoff documentation — was coding-language-agnostic. It would work the same way whether the implementation was Python or JavaScript. The scaffolding was reusable.

That realisation led to the **ai-project-template** repository: a framework for structuring AI-assisted development projects, extracted from the FOMO-f work and generalised. But a template nobody has tested is just a theory. It needed proving.

The proof of concept was a **Blackjack Casino simulator**. The product itself was almost beside the point — what mattered was bootstrapping a new project from the template and seeing how it held up. The answer was: remarkably well. Minor adjustments, minimal friction, and before long the simulator had developed to the point where the next implementation epic was going to be **ChaosMode** — a mode where AI players begin tipping and bribing the house, trading favours for extra liqueur and card value deductions, with the simulated intoxication levels of the AI players causing escalating havoc at the table. Not a trivial feature. A genuinely fun one.

And then the FIFA World Cup 2026 started.

Adam had been looking forward to it. Sweden were in it. The games were running in the middle of the night — vacation schedule, no work the next morning, perfect conditions for watching football. What actually happened was that he found himself in the middle of the night discussing increasingly unhinged ChaosMode implementation ideas with total disregard for the matches happening on the screen behind him. The World Cup was on and he was talking to an AI about drunk blackjack dealers.

Something needed to change. And since he clearly wasn't going to stop building things, the thing that needed to change was having a way to track the football while he did it. **titan-comptracker** — a real-time football competition tracker, his first ever mobile app — was the result. Built to solve a personal problem, and also to answer a question: could the ai-project-template bootstrap a mobile app project as cleanly as it had bootstrapped the casino simulator?

It could.

---

## What We Built

Three projects, three domains, one workflow. But what was actually produced technically?

**FOMO-f** is a Python-based AI sonar analysis tool. The **Blackjack Casino simulator** is also Python-based, with web components handling the presentation layer — deliberately so. This reflects a general strategy that runs through all of this work: when proving or disproving something, change as few things as possible at once. The fewer variables in play, the cleaner the cause and effect. If the process and the tech stack both change simultaneously and something goes wrong, you can't tell which one caused it. It's the same principle that underpins agile thinking — short iterations, one meaningful change at a time, learn from the result, then move forward. When bootstrapping a project from the template for the first time, introducing a different coding language on top of an untested process would have muddied the results. Python kept the focus on validating the workflow. The deliberate step up in technical complexity came with **titan-comptracker** — the focus here — is an Android-first mobile application covering twelve football competitions via the football-data.org API, built around the FIFA World Cup 2026.

titan-comptracker is a real, installable app — distributed as a standalone APK built from a proper release pipeline — with animated UI, persistent user preferences, live match data, and a codebase that has gone through dozens of reviewed, tested pull requests. The tech stack is not trivial: React Native with Expo SDK 54, TypeScript throughout, React Native Reanimated for smooth UI thread animations, AsyncStorage for local persistence, expo-image for SVG rendering, and a Gradle-based Android build pipeline. These aren't toy choices — they're the same stack you'd find in professional mobile development shops.

---

## The Workflow

The multi-agent system that runs this project is built on the `ai-project-template` framework and has four participants:

**Adam** is the Product Owner. He defines what gets built, makes the final calls on architecture and priorities, and is the human relay between agents. Critically, he never gets bypassed — every decision of consequence goes through him.

**Clead** is Claude in the chat interface, acting as Tech Owner and architect. Clead reviews every pull request, produces the exact prompts that drive implementation, maintains the architectural vision, and is the author of documents like this one.

**Crog** is Claude Code CLI — the command-line agent that does the actual implementation work. Crog writes the code, runs the tests, manages Git, and opens pull requests.

**Copi** is GitHub Copilot, providing automated PR review as an additional quality layer.

The PR cycle that connects them is strict and has no exceptions:

1. Adam and Clead define a spec and the test criteria
2. Crog writes a failing test — no implementation before the test exists
3. Crog implements until the tests pass
4. A PR is opened with a `pr_dump` comment capturing the full diff context
5. Clead fetches and reviews the diff, then produces either an approval with an exact merge command, or a rejection with a specific fix prompt
6. Adam pastes the output into Claude Code
7. Crog executes; Adam confirms the merge

Every change goes through this cycle. A one-line fix goes through this cycle. There are no shortcuts.

---

## Why So Much Process For A Solo Project?

This is the question worth examining honestly. A seasoned developer working alone would find this overhead unnecessary — probably even counterproductive. They'd commit directly, trust their own judgment on tests, merge their own PRs. And they'd be right to, because they carry the checks and balances internally. Their experience is the safety net.

Adam doesn't have that safety net. Without the PR cycle, there's no guarantee a change was reviewed. Without the TDD requirement baked into the workflow, tests might get skipped when things feel obvious. Without Clead reviewing architecture, decisions might get made for the wrong reasons or without understanding the downstream implications.

The process isn't overhead. It's infrastructure. It replaces the things an experienced developer provides through competence, with mechanics that work regardless of competence level. The workflow is calibrated to the person, not to an abstract standard of efficiency.

This is the insight that took a while to arrive at clearly: the right question isn't "is this over-engineered?" It's "over-engineered for whom?" For a different person in a different situation, the answer would be yes. For this project, with this product owner, it's right-sized.

---

## What The AI Made Possible

Five years ago, this project would not have been possible for someone in Adam's position. The execution gap was unbridgeable without people. You'd need to hire a tech lead to make the architectural decisions, a developer to write the code, maybe a QA engineer to enforce the testing discipline. The cost — financial and organisational — would be prohibitive for a passion project or early-stage idea.

The AI tools collapsed that requirement. Not by removing the need for good judgment, but by providing the execution capability that judgment was previously unable to unlock. Adam brought the product sense, the process knowledge, the organisational discipline, and the domain decisions. Claude brought the technical execution, the architectural reasoning, and the quality enforcement. Together they covered the full stack of what a small development team would provide.

This is a more interesting use of AI than "write me a function." It's using AI as a genuine collaborator in a structured system, with roles and responsibilities and accountability — not as a magic box that spits out code.

---

## The Conclusions We Reached

### The template adapts to the person, not the other way around

A critical property of the ai-project-template that makes this practical is that it is self-documented. The rule sets, checks and balances, agent roles, and PR conventions are all written down inside the repository itself. This means that someone bootstrapping a new project from the template doesn't have to accept it as-is. Through conversation with Clead — the Tech Owner role, fulfilled by Claude in the chat interface — they can walk through what exists, explain their own situation, competence level, and goals, and collaboratively modify the ruleset to fit. More experienced developers can strip back ceremony. Less experienced ones can add more guardrails. Teams can adapt the agent roles. Different domains might call for different quality gates.

The template is a starting point with a built-in advisor, not a rigid prescription. That's what makes it genuinely transferable rather than just theoretically reusable.

The `ai-project-template` repository documents everything: the PR cycle, the TDD conventions, the agent roles, the handoff process. Someone else could fork it and follow it. But the more important insight is that the *template is not the point* — the principle behind it is.

A more experienced developer would adapt the workflow significantly. Fewer formal handoffs, less ceremony, more autonomy for the implementation agent. Someone with even less experience than Adam might need more structure, not less. The value is in understanding that the workflow should be designed to fill *your* specific gaps — not copied wholesale from someone else's project.

### The sweet spot is knowing enough to leverage without getting lost in the implementation

Adam identified his own position accurately: experienced enough to know what good looks like, having come from a programming background before moving into process and product management, but no longer close enough to active development to execute it independently. That turns out to be close to ideal for this kind of AI-assisted development. Deep current technical expertise can make it hard to step back and think about workflow and process — there's always a more elegant way to write the function, a more efficient algorithm to consider. Complete inexperience makes it impossible to know whether the AI's output is good or terrible.

The middle ground — domain knowledge, process knowledge, product judgment, and enough technical literacy to evaluate output without getting lost in implementation details — is where this approach delivers the most. You can direct the AI usefully, evaluate its output against known standards, and keep the product vision coherent, without getting sucked into debates about code style.

### The demand is latent

There are people who could benefit from this approach who don't know it exists. They're not searching for "multi-agent development workflow templates" because they don't know to search for that. They're asking more basic questions: "can AI help me build my idea?" and hitting a wall when the answer requires more setup than they know how to do.

The proof that this works — three projects, working software, repeatable process — is the thing that might eventually reach those people. Not as a product to sell, but as a demonstration that the possibility exists. You don't need a technical co-founder if you're willing to be intentional about how you structure your AI collaboration. That's a meaningful shift in what's available to non-technical founders and builders.

### What started as an experiment answered a question nobody was explicitly asking

The original goal was to answer one question: can I build a mobile app with AI? The answer was yes. But the more interesting answer that emerged along the way wasn't about the app at all — it was about the workflow. A structured, disciplined, human-in-the-loop approach to AI-assisted development can produce real quality at a level that shouldn't be possible for someone without a technical background. And it can do it consistently, across different domains, without the wheels coming off.

That conclusion wasn't planned. It emerged from doing the work, reflecting on it honestly, and being willing to scrutinise whether what had been built was genuinely valuable or just an elaborate way of making a solo developer feel better about their process.

The answer is: it's genuinely valuable. Not for everyone, not in every context. But for the right person, asking the right question, with the discipline to follow through — it works.

---

*Written by Clead (Claude) in collaboration with Adam, June 2026*
