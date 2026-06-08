# Podcast Script — 10–15 Minutes

**Gayathri** and **Vivek** — two developers, just talking. Keep it loose. The bold lines are Gayathri's; treat them as openers, not a script. `[~time]` markers are just to keep half an eye on the clock. Drop the _(follow-up)_ lines if you're running long.

---

## 1 — Where you're at now (0:00–1:30)

**Gayathri:** So, big question to start — what's your actual take on AI right now? Like the one thing you'd say if someone asked.

**Vivek:**

That AI doesn't remove the need for expertise. It just changes where the expertise is needed.

For a long time, the constraint in software was knowledge and implementation — you had to know the language, the framework, the APIs, the patterns. That still matters, but AI is making a lot of it more accessible.

So the bottleneck moves. It's less "can I write this code" and more "should this be built, what's the architecture, what context does the system need, how do I know the answer is any good, who owns the outcome."

The line I keep coming back to is: when coding gets cheaper, thinking gets more expensive.

---

## 2 — How you got into it (1:30–3:30)

**Gayathri:** Rewind a bit — how'd you even get into AI?

**Vivek:**

I started as a web developer in 2023, and honestly I wasn't the early adopter you'd expect.

I wasn't using ChatGPT for everything. I actually liked the old way — Googling, Stack Overflow, reading docs, forums. I was a little cautious about leaning on AI too much.

It wasn't that I thought AI would replace me. I was more worried I'd stop thinking for myself.

**Gayathri:** _(follow-up)_ And looking back — was that the right instinct, or were you overthinking it?

**Vivek:**

Bit of both. The instinct was right — I've seen people outsource their thinking completely and lose the thread. But I held onto it too long. What I landed on eventually was: use AI to go fast on things I already understand, go slow and deliberate on things I don't. Leverage, not avoidance.

**Gayathri:** So what pulled you in?

**Vivek:**

My first real AI project — a dynamic theming proof of concept.

In WaveMaker, apps use theme variables. The idea was you'd describe a theme in plain language and an LLM would generate all the theme variables, so the app's look would just change.

Good idea, not reliable. It hallucinated, gave inconsistent output, and tiny prompt changes blew up the results.

But it was a useful failure. Taught me early that AI isn't magic — a demo looks great, but reliable is a completely different problem from sending a prompt to a model.

---

## 3 — The context lesson (3:30–5:30)

**Gayathri:** So after that flopped, what'd you learn?

**Vivek:**

The next phase was RAG.

In 2024 I got exposure to an internal system called Pooch. I didn't build it, but I got to see how it worked, read parts of the code, understand the architecture. It ran over our docs, FAQs, demo scheduling.

That's where it clicked: the model isn't the whole story. Context is.

Weak context, even a strong model gives weak answers. Noisy retrieval, unreliable output. Bad chunking, it misses the useful part. If the system doesn't know which source to trust, it just blends things wrong.

That flipped my mental model — I stopped thinking about model capability and started thinking about system capability.

**Gayathri:** _(follow-up)_ Give me a real example. What does "bad context" actually look like when it breaks?

**Vivek:**

Classic one — someone asks a version-specific question, and retrieval pulls three docs from three different product versions. The model gets confident and blends them. Each piece is true on its own, but the answer as a whole is wrong. The model didn't fail. The context did. That's what made me stop blaming the model for everything.

**Gayathri:** Did you mess around with different kinds of models too?

**Vivek:**

Yeah — local models with Ollama, open-weight stuff, some domain-specific LLMs.

One thing I looked into was medical AI — MedLLaMA and healthcare-oriented models, for a doctor-facing system. Appointments, report interpretation, that kind of workflow.

Never fully built it, but it taught me something: bigger models aren't always the answer. In a lot of domains the question isn't "which model is smartest," it's "does the system understand the domain, does it have the right context, does it fit the workflow, can it be trusted the way this domain needs." Especially somewhere like healthcare.

---

## 4 — Going to production (5:30–7:30)

**Gayathri:** When did this stop being experiments and become something real?

**Vivek:**

The Ecosystem Agent. That was the first proper production system.

It's a unified Ask AI experience across our sources — docs, Storybook, Academy, Marketplace.

The key call was that each source is genuinely different. A docs answer isn't a Storybook answer, Academy isn't Marketplace. So each source has its own MCP and its own retrieval. Then a central orchestrator coordinates them — picks the relevant source, the retrieval strategy, how many chunks, how to shape the response, how not to give a confident but badly grounded answer.

We used LangGraph for the orchestration. That project changed how I see production AI completely. It stopped being "prompt plus model" and became system design — tools, context, retrieval, routing, response structure, evaluation. The model's still important, but it's one piece.

People think the model is the story. I think the system is the story.

**Gayathri:** _(follow-up)_ What was the hard part — the bit that doesn't show up in the demo?

**Vivek:**

Knowing when *not* to answer, honestly. It's easy to build something that always says something. Much harder to build something that knows when its grounding is weak and says "I'm not sure" or routes to the right source instead of guessing. The logic around uncertainty was harder than any single retrieval step. Users forgive "I don't know." They don't forgive confident and wrong.

---

## 5 — The Kotlin story (7:30–9:30)

**Gayathri:** When did AI actually surprise you? Like, change-how-you-work surprise you.

**Vivek:**

Coding. Not just that it could generate code — that it changed what felt like a blocker.

There was this mobile workflow app idea. You'd say something like "wake me up at 5 AM and don't stop the alarm until I walk 100 steps," and the AI would generate a workflow wiring up alarm APIs, the step counter, device stuff.

I didn't know Kotlin well. Normally that's where I'd stop, or spend ages learning before I could even start.

But Kotlin just... wasn't the limitation.

The real limitation became the design. How do you represent intent? How do you model device capabilities? What happens when permissions are missing? How does the user inspect and trust the generated workflow?

That's when the shift got obvious to me. We're moving from "learn the language, write code" to "design the system, design the workflow, orchestrate the intelligence." The language isn't the bottleneck anymore. The architecture is.

**Gayathri:** _(follow-up)_ Doesn't that scare you a bit though? If the language stops being the moat, what stops anyone from doing what you do?

**Vivek:**

It'd scare me if my value was the syntax. But what's left when the syntax gets cheap is the actually-hard part — knowing what to build, catching when the output's wrong, owning whether it really works. More people can start now, which is great. Fewer people can finish well. The value moved into that gap. It didn't disappear.

---

## 6 — New devs and laziness (9:30–11:30)

**Gayathri:** You came into this recently yourself. If someone's starting out today, in a world where AI writes half the code — how should they actually learn?

**Vivek:**

Use AI to kill the boring part, not the understanding part.

It's so tempting to paste a problem, get a working answer, move on. But if you never sit with *why* it works, you get this fragile confidence — fine until something breaks and you've got no model of what's underneath.

What worked for me was treating the AI like a really fast senior who's occasionally wrong. I'd have it do something, then make myself explain back why it did it that way and poke at where it might be lying. You still have to put in the reps. AI just changes which reps matter.

**Gayathri:** There's that old line that good engineers are "lazy" in a good way. Some people worry AI makes us lazy in the bad way — more code, worse quality. You buy that?

**Vivek:**

Yeah, that risk is real.

The good kind of lazy is wanting cleaner abstractions, fewer repeated mistakes, systems the next person can actually work with. AI doesn't have that instinct. It'll generate code forever. It doesn't care if the system's elegant or bloated, or whether whoever maintains it later suffers.

So if you measure AI by how much code it produces, you're measuring the wrong thing. The win isn't more code. It's better systems. That's why review and judgment still matter — AI speeds up the building, humans still have to care about the quality.

**Gayathri:** _(follow-up)_ Has it changed how you actually start a task now?

**Vivek:**

A lot. I spend more time before writing anything — understand the problem, look at the architecture, the constraints, the scale and performance needs — then generate. The trap with AI is jumping straight from idea to code, because it'll happily give you something. Something plausible, with weak architecture underneath. So I front-load the thinking more than I used to.

---

## 7 — What stays valuable (11:30–13:00)

**Gayathri:** So with everything you've built — what's actually become *more* important?

**Vivek:**

Judgment. AI can generate a thousand answers. It still can't tell you which problem's worth solving.

System thinking — because most real AI products aren't a model, they're context, tools, retrieval, workflows, memory, permissions, UI, evaluation.

Taste — if AI hands you five designs, someone still has to know what good looks like.

Communication — building gets faster, so alignment matters more. You still need people who can explain tradeoffs and bring clarity.

And ownership. AI produces outputs, it doesn't own outcomes. A human's still on the hook for whether it works, whether people trust it, whether it's maintainable.

**Gayathri:** _(follow-up)_ If you had to bet on one of those being the rarest in five years — which one?

**Vivek:**

Judgment, easily. The others you can partly train or systematize. But deciding what's worth doing, under uncertainty, with taste — that stays stubbornly human. Intelligence is getting abundant. Judgment's getting scarce.

---

## 8 — Close (13:00–14:30)

**Gayathri:** Last one. What's the takeaway from all of it?

**Vivek:**

That I shouldn't treat AI as just a shortcut for writing code. It's a shift in where the hard work lives.

Use it to skip the thinking and you ship faster but build weaker systems. Use it to explore, prototype, compare approaches, test assumptions — and it's real leverage.

The useful skill isn't generating the most code. It's pointing intelligence at the right problems and then reviewing the result with enough context to know if it's any good.

For me it went models, then RAG, then MCP and orchestration. And the bigger lesson now is clear — AI engineering is system design around intelligence.

Intelligence is getting abundant. Judgment's getting scarce. AI doesn't remove expertise. It moves it.

**Gayathri:** Good place to stop. Thanks, man.

**Vivek:** Anytime.

---

## Pacing cheatsheet

| # | Topic | Target | Cut first if long |
|---|-------|--------|-------------------|
| 1 | Where you're at now | 1.5 min | — |
| 2 | How you got in | 2 min | the "was the caution right" follow-up |
| 3 | Context lesson | 2 min | the medical-AI bit |
| 4 | Production | 2 min | the "hard part" follow-up |
| 5 | Kotlin story | 2 min | keep all of it |
| 6 | New devs + laziness | 2 min | the "how you start a task" follow-up |
| 7 | What stays valuable | 1.5 min | trim the list to 3 |
| 8 | Close | 1.5 min | keep |

Target ~14 min. Drop _(follow-up)_ lines first to land near 10. Keep section 5 and 8 no matter what.
