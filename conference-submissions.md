# Conference Submission Letters

Three versions: joint submission (both talks), and one per talk.
All are placeholder-ready — swap in conference name, dates, and email address.

---

## A) Joint Submission — Both Talks

**To:** [Conference Program Committee]
**From:** Adam Smolowicz, Divbyzero Consulting AB
**Re:** Speaker Submission — Two Sessions

Dear [Program Committee],

I'd like to submit two sessions for consideration at [Conference Name]. They cover the same body of work from different angles, and can be booked independently or as a pair.

Before I describe them, I should be honest about the scope: this is not groundbreaking research. The complexity of my findings sits somewhere between tying my shoes and launching a rocket — closer to the shoes. But I've documented the shoe-tying so thoroughly that you can pick up the process, understand exactly why each step exists, adapt it to your own feet, and walk confidently without tripping. Which, if you've ever watched someone try to use AI in a development workflow without any process at all, you'll know is rarer than it sounds.

---

**Session 1: Building with AI — What We Did, What We Learned, What It Means**
*45–50 minutes | Prospects to practitioners*

Over the course of a week, I built three projects across three completely different domains — a Python sonar analysis tool, a blackjack casino simulator, and an Android-first mobile football tracker — using a structured multi-agent AI workflow. Same pattern, different stacks, each one proving the template generalises.

This talk covers who I am and why this worked for me (background in agile and product, years away from active development, knew what good looked like but couldn't easily produce it), what the workflow actually is, and what it taught me about structuring AI collaboration so quality doesn't get sacrificed. The conclusions are honest: this isn't a prescription for everyone. It's a proof of concept that the right workflow, for the right person, fills the right gaps.

The template is open source. The talk ends with an invitation to fork it, adapt it, and make it fit your situation — not ours.

---

**Session 2: Controlling the Uncontrollable — Lessons from Building a Production AI Development Workflow**
*45 minutes | Engineering practitioners and leaders*

A case study in what happens when you try to use GitHub Copilot seriously — not as a convenience tool, but as part of a structured, automated review process with defined roles, quality gates, and real accountability. Three specific problems, three documented solutions, four failure modes we'll never make again.

This talk covers the re-review reliability problem (and the label-based automation model that fixed it), what Copilot actually does versus what most people think it does, and the multi-agent coordination rules that emerged from watching things go wrong. It's an engineering talk for people who've hit these problems or are about to.

---

Both sessions are self-contained. Either works independently. If your programme has room for both, they complement each other without overlap. If you'd like to discuss which fits your audience better, I'm happy to talk it through.

I contributed the things I'm good at. Claude contributed the things it excels at. Together we can tie almost any shoes — and this submission is proof of that.

*Adam Smolowicz*
*Divbyzero Consulting AB*
*[email] | github.com/sugose/ai-project-template*

---

## B) Submission — "Building with AI"

**To:** [Conference Program Committee]
**From:** Adam Smolowicz, Divbyzero Consulting AB
**Re:** Speaker Submission — Building with AI: What We Did, What We Learned, What It Means

Dear [Program Committee],

I'd like to submit a session for consideration at [Conference Name].

I should open with an honest disclaimer: the complexity of what I'm presenting sits comfortably in shoe-tying territory. Not rocket science. But I've documented the shoe-tying so thoroughly — why each step exists, what breaks if you skip it, how to adapt it for your own feet — that someone else can pick it up, make it their own, and walk without fumbling. In a world where most AI development advice is either "just ask ChatGPT" or "here are 47 architectural principles," I'd argue there's a gap for something practical in the middle.

**Session: Building with AI — What We Did, What We Learned, What It Means**
*45–50 minutes | Prospects to practitioners*

Over the course of a week, I built three projects across three completely different domains using a structured multi-agent AI workflow: a Python sonar analysis tool, a blackjack casino simulator, and an Android-first mobile football tracker. The workflow was the same across all three. The stacks were not.

My background: agile coach, scrum master, team lead, product owner, product manager. Programming background, but years away from active development. I know what good software development looks like from the inside. I just can't easily produce it alone anymore. The question that drove this work was: can AI fill that gap, if you're intentional enough about how you structure the collaboration?

The answer is yes. But only if you build the right process around it.

This talk covers:
- The origin story (it started with fishing, got derailed by the World Cup, and ended with a mobile app)
- The multi-agent workflow that made it possible
- Why the process is heavier than a solo developer needs — and why that's the right call for this situation
- The honest conclusions about who this works for and what the template actually is

The template is open source. The talk ends with an invitation: fork it, adapt it, make it yours. The shoe-tying technique is documented. Whether you need it exactly as written is your call.

I contributed the things I'm good at. Claude contributed the things it excels at. Together we can tie almost any shoes — and this talk is the story of how we figured that out.

*Adam Smolowicz*
*Divbyzero Consulting AB*
*[email] | github.com/sugose/ai-project-template | github.com/sugose/titan-comptracker*

---

## C) Submission — "Controlling the Uncontrollable"

**To:** [Conference Program Committee]
**From:** Adam Smolowicz, Divbyzero Consulting AB
**Re:** Speaker Submission — Controlling the Uncontrollable: Lessons from Building a Production AI Development Workflow

Dear [Program Committee],

I'd like to submit a session for consideration at [Conference Name].

Fair warning: I'm going to describe some shoe-tying. Specifically, I'm going to describe what happens when you try to automate the shoe-tying and the automation fails in ways that are undocumented, inconsistent, and mildly infuriating. And then I'm going to describe what we built instead — and why it works.

**Session: Controlling the Uncontrollable — Lessons from Building a Production AI Development Workflow**
*45 minutes | Engineering practitioners and leaders*

This is a case study in what happens when you try to use GitHub Copilot seriously — not as a convenience tool, but as a component in a structured, automated development workflow with defined roles, quality gates, and real accountability.

Three problems. Three solutions. Four documented failure modes.

**The re-review problem:** With "Review new pushes" enabled, Copilot reviews a PR once and then goes quiet. The REST API, GraphQL, and GitHub CLI all fail to trigger re-review after the first pass. We investigated the failure mode, formed a hypothesis about Copilot's internal baseline tracking, posted our findings to the GitHub community forum, and redesigned the trigger model entirely — label-based, interrupt-driven, with explicit lifecycle invariants. Credit consumption dropped by approximately 70%.

**The diff-bounded review problem:** Copilot reviews the PR diff. It does not review the codebase. We caught a cross-file interface bug that Copilot missed because the dependent file wasn't in the diff. The result: a formal three-layer review architecture with a documented depth policy — and a clearer understanding of what automated review can and cannot be trusted to catch.

**The multi-agent coordination problem:** What happens when an AI developer agent starts acting on reviewer comments without human oversight. The answer is spec drift that compounds silently and surfaces three PRs later. The result: the hard stop rule, single-task prompt structure, and session hygiene requirements that now govern every iteration.

The process that emerged from these failures is transferable. The label model works for any team. The review depth policy works for any tech lead. The hard stop rule works for any developer agent. The session hygiene works for any context-limited AI.

I contributed the things I'm good at. Claude contributed the things it excels at. Together we can tie almost any shoes — and the laces have held across three projects, three domains, and one very eventful World Cup.

The work is open source: github.com/sugose/python-blackjack and github.com/sugose/ai-project-template.

*Adam Smolowicz*
*Divbyzero Consulting AB*
*[email] | github.com/sugose/ai-project-template*
