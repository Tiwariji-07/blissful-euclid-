# Developer-Focused Draft: What AI Changed About Software Engineering

## Positioning

This version is best if the podcast audience is mostly developers, senior engineers, and people who care about how software work is changing.

It is more practical than philosophical. The big idea is still present, but it is grounded in developer workflows.

## Core Thesis

AI is changing software engineering less by replacing developers and more by shifting the valuable part of the job. Implementation is becoming cheaper, so architecture, context, review, and product judgment become more important.

## Opening

**Host:** As someone building AI systems, what do you think developers are misunderstanding about AI?

**You:**

I think many developers are still framing the change too narrowly. They ask, "Can AI write code?" or "Will AI replace developers?" Those are understandable questions, but I do not think they capture the real shift.

The bigger shift is that implementation is becoming cheaper.

If implementation becomes cheaper, the valuable part of engineering moves. It moves toward understanding the problem, designing the architecture, deciding what should exist, reviewing the output, and making sure the system is maintainable.

So I do not think the only useful measure of a developer will be how much code they personally write. Increasingly, it feels like the work is about directing tools well, reviewing outputs, and making good system decisions.

## Your Starting Point

**Host:** How did your own AI journey start?

**You:**

I started as a web developer in 2023. Initially, I was not using ChatGPT heavily. I liked figuring things out through Google, Stack Overflow, documentation, and forums.

That might sound old-fashioned now, but it mattered to me because I did not want to lose the habit of thinking. My worry was not, "AI will replace me." It was, "If I rely on this too much, will I stop building my own problem-solving muscle?"

My first real exposure to OpenAI APIs came through a dynamic theming proof of concept. WaveMaker applications use theme variables, so the idea was: let a user describe a theme in natural language, and have the model generate all the theme variables.

It was a good idea, but the system was unreliable. It hallucinated. It was sensitive to prompts. Outputs were inconsistent. That was useful because it broke the illusion that AI is magic. It made me understand that practical AI is not just about calling an API.

## Lesson 1: Context Matters

**Host:** What changed after that?

**You:**

I got deeper into RAG systems.

One internal project, Pooch, worked over WaveMaker documentation, FAQs, and demo scheduling flows. I did not build it, but I got to see how it worked, read parts of the code, and understand the architecture.

That was where I started understanding retrieval, grounding, and context augmentation more practically.

The important realization was: the model is not the whole story. Context matters.

You can use the same model and get completely different results depending on the quality of retrieval, chunking, source selection, prompt structure, and how the system handles context.

This is why I think model comparisons can be misleading. Models matter, but the surrounding workflow often matters just as much. In coding environments too, the same underlying model can feel very different depending on how context is managed, how tools are exposed, and how feedback loops are designed.

Workflow intelligence is often more important than model intelligence.

## Lesson 2: Production AI Is Orchestration

**Host:** What did production AI teach you?

**You:**

The Ecosystem Agent was the big turning point.

It is a unified Ask AI experience across multiple sources: documentation, Storybook, Academy, and Marketplace. The architecture is not one giant knowledge base. Each source has its own MCP and its own retrieval behavior.

That matters because not every question should be answered the same way. A documentation question, a component question, a marketplace question, and a learning question may need different context.

The central orchestrator has to decide which sources to use, what strategy to apply, how much context to retrieve, and how to structure the final response. We used LangGraph for orchestration, and that made the system feel less like a chatbot and more like a coordinated workflow.

That is where I started thinking: the future of AI engineering is not only about prompts. It is about systems.

## Lesson 3: Language Is Less Of A Bottleneck

**Host:** How has AI changed your own development process?

**You:**

The clearest example for me was a mobile workflow application idea.

The concept was: users describe intent, and AI creates a workflow. For example, "Wake me up at 5 AM and do not stop the alarm until I walk 100 steps." The system would connect alarm APIs, step counter APIs, and device capabilities.

I did not know Kotlin well enough to confidently build that from scratch in the traditional way. But with AI, Kotlin was not the main blocker.

The hard parts became: what should the workflow model look like? How do actions connect? How do you represent device capabilities? What happens if permissions are missing? How do you make the generated workflow understandable and editable?

That experience made something very clear to me: the language is not the bottleneck anymore. Architecture is.

This does not mean languages do not matter. It means language knowledge is less often the limiting factor. The limiting factor is whether you understand the system you are trying to build.

## Lesson 4: Boring Planning Becomes More Valuable

**Host:** What changed in your own development process?

**You:**

I now try to spend more time before implementation.

A lot of us are tempted to skip the boring part and jump directly from idea to code. AI makes that temptation stronger because it can generate code immediately.

But that is exactly why planning has started to matter more in my own workflow.

My current workflow is more like:

1. Understand the problem.
2. Research the architecture.
3. Research best practices.
4. Understand scale and performance requirements.
5. Decide the shape of the system.
6. Then generate or write implementation.

When coding becomes cheaper, thinking becomes more expensive.

If I skip the thinking, AI will still produce something. That is the danger. It may produce code that looks plausible but has weak architecture underneath.

That connects to one idea from the transcripts we discussed: AI does not naturally care about laziness in the engineering sense. A good engineer wants the system to be simpler, easier to maintain, and easier for future people to understand. A model will happily generate more layers unless we guide it.

## What Developers Should Build

**Host:** What skills become more valuable?

**You:**

System design becomes more valuable.

Reviewing AI output becomes more valuable.

Understanding context becomes more valuable.

Product thinking becomes more valuable, because now you can build more things, but you still need to know what is worth building.

Taste becomes more valuable. If AI gives you five possible implementations, someone needs to know which one is clean, maintainable, and aligned with the product.

Communication becomes more valuable too. As AI helps produce more artifacts, the human role becomes connecting those artifacts to intent and aligning teams around the right direction.

## Closing

**Host:** How would you frame this for other developers?

**You:**

I would be careful about giving advice too confidently, because I am still early in my career too. But the pattern I have seen is that the field is changing, and we should take that seriously.

The main thing I would say is: do not reduce yourself to syntax.

If your identity as a developer is only "I know this language," AI will feel threatening. But if your identity is "I can understand problems, design systems, make tradeoffs, and own outcomes," AI becomes leverage.

Developers are not just being asked to code faster. More and more, we are being asked to think at a higher level.

AI does not remove expertise. It changes where expertise is required.
