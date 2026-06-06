# Big Idea Draft: When Intelligence Becomes Abundant

## Positioning

This version is the most intellectual and memorable. It is useful if the host wants a broader conversation about AI, society, developers, and knowledge work.

You should sound like an AI engineer who has seen the shift firsthand, not like a futurist making predictions from the sidelines.

## Core Thesis

AI is making intelligence more abundant. When something important becomes abundant, the bottleneck moves somewhere else. In software, the bottleneck is shifting from knowledge and implementation toward judgment, architecture, taste, communication, and ownership.

## Opening

**Host:** You have worked on AI systems over the last few years. If you had to describe the biggest shift you are seeing, what would it be?

**You:**

The biggest shift is not just that AI is getting better. That is true, but I think the bigger story is that intelligence is getting cheaper.

For a long time, a lot of society was organized around scarcity. Information was scarce. Expertise was scarce. Software development skill was scarce. Research ability was scarce. If you knew how to find the right answer, or if you had access to the right expert, that itself was a major advantage.

AI changes that equation. It does not make everyone an expert, but it gives many more people partial access to expertise. It lowers the cost of asking questions, exploring ideas, writing code, summarizing documents, and testing possible solutions.

When something becomes abundant, society reorganizes around what is still scarce. So the important question becomes: if intelligence is more available, what remains valuable?

My answer is judgment. Taste. System thinking. Communication. Ownership. Curiosity. AI can generate a thousand answers. It still cannot decide which problem is worth solving.

## Personal Entry Into AI

**Host:** How did you personally enter this space?

**You:**

I started my career as a web developer in 2023. My relationship with AI was a little unusual because I was not immediately using ChatGPT for everything.

I actually enjoyed the older way of learning: searching Google, reading Stack Overflow, going through documentation, reading community discussions. I liked the process of figuring things out. So my initial hesitation was not that AI would replace me. It was more that I did not want to stop thinking for myself.

But then I got pulled into practical AI work, and that changed how I saw it.

One of my first AI projects was a proof of concept around dynamic theming. In WaveMaker apps, themes are controlled through variables. The idea was simple: a user gives a theme description, and an LLM generates the required theme variables so the application appearance changes automatically.

The idea was exciting, but the system was not very good. It hallucinated. Outputs were inconsistent. Small prompt changes affected results a lot. That was my first real lesson: AI demos are easy, but reliable AI systems are hard.

## From Model Excitement To System Thinking

**Host:** What did that failure teach you?

**You:**

It taught me that the model is only one part of the story.

At first, it is natural to ask, "How smart is the model?" But once you build real things, the question changes. You start asking, "What context does the model have? What tools can it use? How do we constrain it? How do we evaluate the result? How do we recover when it is wrong?"

In 2024, I got exposure to RAG systems through an internal project called Pooch. I did not build Pooch, but I got a sneak peek into how it worked, saw parts of the code, and understood the architecture at a practical level.

It worked over WaveMaker documentation, FAQs, and demo scheduling flows. That was the phase where I started to understand context augmentation and retrieval beyond the surface level.

The model was important, but context was often the difference between a generic answer and a useful answer. That realization shaped a lot of my later thinking.

I also explored local models with Ollama and open-weight models, including domain-specific models. I looked into medical AI models like MedLLaMA and healthcare-oriented use cases. I did not fully build the doctor-oriented system, but the exploration was useful because it showed me that bigger is not always the answer. Sometimes context and specialization matter more.

## Production Experience

**Host:** What was your first major production AI system?

**You:**

The major production shift for me was the Ecosystem Agent. It is a unified Ask AI experience across multiple knowledge sources: documentation, Storybook, Academy, and Marketplace.

The interesting part is that each source has its own MCP and retrieval behavior. Documentation is not the same as Storybook. Marketplace is not the same as Academy. Each source has different structure, different user intent, and different retrieval needs.

So the central system is not just "ask a model a question." It has to orchestrate. It has to decide which sources matter, what retrieval strategy to use, how much context to bring back, how to structure the answer, and how to avoid mixing irrelevant information.

We used LangGraph for orchestration, and that project changed how I think about production AI. It made me much less model-obsessed and much more system-obsessed.

People think the models are the story. I think the systems are the story.

## What Becomes Scarce

**Host:** If intelligence becomes more abundant, what becomes scarce?

**You:**

Judgment becomes scarce.

Knowledge is easier to access now. Syntax is easier to generate. Boilerplate is easier to produce. But deciding what matters is still hard.

Taste becomes scarce, because someone still has to know what good looks like. If AI generates five designs, five architectures, or five implementations, you still need to choose. And choosing well requires experience.

Communication becomes scarce, because AI can produce artifacts, but teams still need alignment. Someone has to explain why the system should work a certain way.

Ownership becomes scarce, because AI does not truly own outcomes. It can produce work, but it does not care whether the product is maintainable, whether the user experience is coherent, or whether the business problem was actually solved.

Curiosity becomes scarce too. The best results often come from asking better questions, not just asking for faster answers.

## Developer Shift

**Host:** What does this mean for developers?

**You:**

Developers are moving up the abstraction ladder.

Earlier, a lot of development identity was tied to language knowledge. You learn JavaScript, Java, Kotlin, Go, or Python, and then you build. That still matters, but it is less constraining now.

I had one project idea for a mobile workflow app where a user could say, "Wake me up at 5 AM and do not stop the alarm until I walk 100 steps." The AI would generate a workflow connecting alarm APIs, step counter APIs, and device capabilities.

I did not know Kotlin deeply. Historically, that would have been the blocker. But in that project, Kotlin was not the limitation. The real limitation was architecture, product thinking, workflow design, and understanding how the system should behave.

That is the shift. The language is less often the bottleneck. Architecture is.

When coding becomes cheaper, thinking becomes more expensive.

## Closing

**Host:** What is your final takeaway from your experience so far?

**You:**

The main thing I have learned is that cheaper implementation does not automatically mean cheaper thinking.

AI can help us build faster, but in my experience the quality of what we build still depends heavily on judgment. If we skip architecture, context design, and problem selection, AI can help us produce more output, but not necessarily better systems.

The developer role seems to be moving beyond only writing code. More of the work is becoming about directing intelligence, reviewing outputs, designing workflows, and taking responsibility for the result.

So I would not frame this as a simple replacement story. From what I have seen, developers are moving up the abstraction ladder.

AI does not remove the need for expertise. It changes where expertise is required.
