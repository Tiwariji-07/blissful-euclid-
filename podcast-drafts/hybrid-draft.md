# Hybrid Draft: AI, Developers, And The Shift From Code To Judgment

## Positioning

This version balances your personal journey with the larger idea. It is probably the safest version for a 10-15 minute podcast because it gives the audience both credibility and a clear takeaway.

It uses your projects as evidence, then expands into what AI is changing about software engineering.

## Core Thesis

AI is making intelligence and implementation more accessible. The result is not that expertise disappears. The result is that expertise moves from writing every line of code to deciding what should be built, how systems should work, and how AI should be orchestrated.

## Opening

**Host:** What should this conversation about AI really be about?

**You:**

I think the conversation should be less about whether AI can write code and more about what happens when intelligence becomes more abundant.

For most of software history, knowledge and implementation were major bottlenecks. If you knew the language, the framework, the APIs, and the architecture, you had a big advantage.

AI changes that. It does not remove the need for expertise, but it changes where expertise is required.

The best way I can summarize my current view is: when coding becomes cheaper, thinking becomes more expensive.

That is the shift I have felt personally over the last few years.

## Personal Journey

**Host:** How did you first get into AI?

**You:**

I started as a web developer in 2023. At that time, I was not using ChatGPT as heavily as many developers around me.

I liked the process of searching, reading Stack Overflow, going through documentation, and learning from community discussions. I was slightly cautious about using AI too much because I did not want to stop thinking for myself.

But then I worked on a dynamic theming proof of concept, and that became my first serious exposure to OpenAI APIs.

In WaveMaker, applications use theme variables. The idea was that a user could describe a theme in natural language, and the LLM would generate all the required theme variables. In theory, the application could visually change based on a prompt.

That project was exciting, but it did not work very well. The model hallucinated. It produced inconsistent outputs. It was very prompt-sensitive.

That failure was important because it taught me that practical AI is not just about calling a model. You need structure, constraints, evaluation, and system design.

## The RAG Phase

**Host:** What was the next step?

**You:**

In 2024, I got exposure to RAG systems through an internal project called Pooch. I did not build it, but I got a chance to see how it worked, read parts of the code, and understand the architecture.

It worked over WaveMaker documentation, FAQs, and demo scheduling.

That was the phase where I learned that context is often more important than people think.

At first, people focus on the model. Which model is smarter? Which model has the best benchmark? But when you build actual systems, you realize the model is only one part.

The same model can perform very differently depending on what context you give it, how retrieval works, how chunks are selected, how tools are exposed, and what workflow surrounds it.

That became one of my core beliefs: people think the models are the story, but I think the systems are the story.

## Exploration Phase

**Host:** Did you explore beyond RAG?

**You:**

Yes. I spent time with local models, Ollama, open-weight models, and domain-specific LLMs.

One area I explored was medical AI. I looked into MedLLaMA and healthcare-oriented models. The idea was a doctor-oriented assistant that could help with appointment management, report interpretation, and medical workflows.

That system was not fully built, but the exploration taught me something important: bigger models are not always the answer.

In specialized domains, context and domain alignment matter a lot. A general model may be powerful, but if the system around it does not understand the workflow, the result can still be weak.

## Production Shift

**Host:** When did this move from experimentation to production?

**You:**

The biggest production shift was the Ecosystem Agent.

It is a unified Ask AI experience across documentation, Storybook, Academy, and Marketplace. Each of these sources has different structure and different user intent.

So instead of treating everything as one flat knowledge base, each source has its own MCP and retrieval strategy. Then a central orchestrator coordinates the sources.

That orchestrator has to make decisions: which source should answer, what retrieval strategy makes sense, how much context is enough, what response structure is appropriate.

We used LangGraph for this, and that changed how I thought about AI engineering. It felt less like prompt engineering and more like building a distributed system where intelligence is one of the components.

That is when the question changed for me from "How smart is the model?" to "How should the system work?"

## The Developer Shift

**Host:** How does this affect software developers?

**You:**

I think developers are moving up the abstraction ladder.

Earlier, the path was often: learn a language, learn a framework, write code. That still matters, but it is no longer the whole picture.

One of the strongest examples for me was an AI workflow mobile application idea. A user could say, "Wake me up at 5 AM and do not stop the alarm until I walk 100 steps." The system would generate a workflow connecting alarm APIs, step counters, and device capabilities.

I did not know Kotlin deeply. Historically, that would have stopped me.

But with AI, Kotlin was not the real limitation. The real limitation was designing the workflow architecture. How do you represent user intent? How do you map intent to device capabilities? How do you handle permissions? How do you let users inspect and edit the workflow?

That made the shift very clear to me: the language is not the bottleneck anymore. Architecture is.

## What Remains Valuable

**Host:** If AI can help with knowledge and code, what remains valuable?

**You:**

Judgment remains valuable. AI can generate options, but it cannot decide which problem is worth solving.

Taste remains valuable. You still need to know what good looks like.

System thinking remains valuable because most real AI products are not one prompt. They are workflows, tools, context, memory, retrieval, permissions, evaluation, and user experience.

Communication remains valuable because someone has to align people around what the system should do and why.

Ownership remains valuable because AI does not care about the outcome. It does not care whether the system is maintainable or whether users trust it. Humans still have to care.

## Closing

**Host:** What is the most important thing you want people to take away?

**You:**

I do not think of AI as removing expertise. I think of it as moving expertise.

If implementation gets cheaper, the premium moves to choosing the right problem, designing the right system, and reviewing the result with taste and judgment.

That is why I think the developer role is becoming broader than just coding. It is moving closer to orchestration: combining tools, models, context, workflows, and human judgment into systems that actually work.

AI can generate a thousand answers. It still cannot decide which problem is worth solving.
