# Recommended Draft: AI Does Not Remove Expertise, It Moves It

## Why This Is The Best Version

This is the strongest draft for your podcast because it combines:

* Your real personal journey
* Your production AI experience
* A clear developer-facing thesis
* A broader memorable framing
* Practical, non-hype language

This version should make you sound like an AI engineer first, builder second, thinker third.

## Core Thesis

AI is not removing the need for expertise. It is changing where expertise is required. As intelligence and implementation become cheaper, the bottleneck moves toward judgment, architecture, workflow design, context, and ownership.

## Suggested Title

**AI Does Not Remove Expertise. It Moves It.**

## Opening Answer

**Host:** If you had to summarize your current view of AI in one idea, what would it be?

**You:**

My current view is that AI does not remove the need for expertise. It changes where expertise is required.

For a long time, software engineering was constrained by knowledge and implementation. You needed to know the language, the framework, the APIs, the ecosystem, and the patterns. That knowledge still matters, but AI is making parts of it more accessible.

So the bottleneck is shifting.

It is less often, "Can I write this code?" and more often, "Should this be built? What should the architecture be? What context does the system need? How do we evaluate whether the answer is good? Who owns the final outcome?"

The line I keep coming back to is: when coding becomes cheaper, thinking becomes more expensive.

## How You Started

**Host:** How did you get into AI?

**You:**

I started my career as a web developer in 2023, and my relationship with AI was not instantly enthusiastic in the way people might expect.

I was not using ChatGPT for everything at the beginning. I actually liked the traditional learning process: searching Google, reading Stack Overflow, going through documentation, and looking at community forums.

Part of me was cautious because I did not want AI to replace my thinking process. I was not worried that AI would replace me. I was more worried that I would stop thinking for myself.

But then I got into my first AI proof of concept, which was dynamic theming.

In WaveMaker, applications use theme variables. The idea was that a user could describe a theme, and an LLM would generate all the required theme variables so the application appearance could change automatically.

The concept was good, but the result was not very reliable. The model hallucinated. It gave inconsistent outputs. Small changes in the prompt could change the result dramatically.

That was a useful failure. It taught me early that AI is not magic. A demo can look impressive, but building something reliable requires much more than sending a prompt to a model.

## First Big Lesson: The Model Is Not The Whole Story

**Host:** What did you learn after that?

**You:**

The next major phase for me was RAG.

In 2024, I got exposure to an internal system called Pooch. I did not build Pooch, but I got a sneak peek into how it worked, saw parts of the code, and understood the architecture.

It worked over WaveMaker documentation, FAQs, and demo scheduling. That is where I started learning retrieval, grounding, and context augmentation in a practical way.

The biggest lesson was: the model is not the whole story. Context matters.

If the context is weak, even a strong model gives weak answers. If retrieval is noisy, the final response becomes unreliable. If chunking is bad, the model may miss the useful part. If the system does not know which source to trust, it may combine things incorrectly.

That experience changed my mental model. I stopped thinking only in terms of model capability and started thinking in terms of system capability.

## Exploration: Local And Domain-Specific Models

**Host:** Did you experiment with other kinds of models?

**You:**

Yes, I explored local models with Ollama, open-weight models, and domain-specific LLMs.

One exploration was around medical AI. I looked into MedLLaMA and healthcare-oriented models for a doctor-facing system. The idea was a system that could help with appointment management, report interpretation, and medical workflows.

That system was not fully built, but it taught me something important: bigger models are not always the answer.

In many domains, the real question is not just, "Which model is smartest?" It is, "Does the system understand the domain? Does it have the right context? Does it fit the workflow? Can it be trusted in the way this domain requires?"

That is especially true in sensitive domains like healthcare, but the lesson applies broadly.

## Production AI: Ecosystem Agent

**Host:** What was your first major production AI system?

**You:**

The first major production system was the Ecosystem Agent.

It is a unified Ask AI experience across multiple WaveMaker sources: documentation, Storybook, Academy, and Marketplace.

The important design decision was that each source is different. Documentation answers are not the same as Storybook answers. Academy content is not the same as Marketplace content.

So each source has its own MCP and retrieval behavior. Then a central orchestrator coordinates the sources.

That orchestrator has to decide which source is relevant, what retrieval strategy to use, how many chunks to retrieve, how to structure the response, and how to avoid giving a confident but poorly grounded answer.

We used LangGraph for orchestration, and that project made me see production AI very differently.

At that point, AI engineering stopped looking like "prompt plus model" and started looking like system design. You have tools, context, retrieval, orchestration, routing, response structure, and evaluation. The model is still important, but it is only one component.

People think the models are the story. I think the systems are the story.

## Strongest Personal Story: Kotlin Was Not The Limitation

**Host:** When did AI genuinely surprise you?

**You:**

Coding surprised me the most.

Not just because AI could generate code, but because it changed what felt like a blocker.

One example was an AI workflow mobile application idea. The idea was that a user could express an intent like, "Wake me up at 5 AM and do not stop the alarm until I walk 100 steps."

The AI would generate a workflow that connects alarm APIs, step counter APIs, and device capabilities.

I did not know Kotlin deeply. In the past, that alone would have made me stop or spend a long time learning before I could even start.

But with AI, Kotlin was not the limitation.

The real limitation became: how should the workflow system be designed? How should user intent be represented? How should device capabilities be modeled? What happens when permissions are missing? How does the user inspect, edit, and trust the generated workflow?

That experience made the abstraction shift obvious.

Developers are moving from "learn language, write code" toward "design systems, design workflows, orchestrate intelligence."

The language is not the bottleneck anymore. Architecture is.

## What The Transcripts Add

**Host:** Some developers argue AI may create more low-quality code. Do you agree?

**You:**

Yes, that risk is real.

One idea I like from the discussions around programmer laziness is that good engineers are lazy in a productive way. They do not want to maintain unnecessary complexity. They want cleaner abstractions, fewer repeated mistakes, and systems that are easier for future people to work with.

AI does not naturally have that instinct. It can generate code endlessly. It does not care whether the system is elegant or bloated. It does not care whether future maintainers will suffer.

So if we measure AI productivity only by how much code it generates, we are measuring the wrong thing.

The value is not more code. The value is better systems.

That is why judgment and review matter so much. AI can accelerate implementation, but humans still need to care about quality.

## What Remains Valuable

**Host:** Based on your experience, what has become more important?

**You:**

For me, judgment has become more important. AI can generate a thousand answers. It still cannot decide which problem is worth solving.

System thinking has become more important. Most useful AI products are not just a model. They involve context, tools, retrieval, workflows, memory, permissions, UI, and evaluation.

Taste has become more important. If AI gives you several possible designs or implementations, someone still needs to know what good looks like.

Communication has become more important. As building gets faster, alignment becomes more important. Teams still need people who can explain tradeoffs and bring clarity.

Ownership has become more important. AI can produce outputs, but it does not own outcomes. Humans still have to be responsible for whether the system works, whether users trust it, and whether it is maintainable.

## Closing Answer

**Host:** What is your final takeaway from everything you have seen so far?

**You:**

My takeaway is that I should not treat AI only as a shortcut for writing code.

I see it more as a shift in where the hard work lives.

If we use AI to skip thinking, we may ship faster but build weaker systems. If we use AI to explore, prototype, compare approaches, and test assumptions, it becomes powerful leverage.

At least from what I have seen, the useful skill is not simply generating the most code. It is directing intelligence toward the right problems and then reviewing the result with enough context.

For me, the journey started with models. Then it became RAG. Then MCP and orchestration. Now the bigger lesson is clear: AI engineering is system design around intelligence.

AI is making intelligence abundant. Judgment is becoming scarce.

AI does not remove expertise. It moves it.
