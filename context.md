# Podcast Preparation Context

## Objective

Prepare for a 10-15 minute podcast interview.

Audience:

* Developers
* Tech enthusiasts
* Founders
* Engineering-minded audience

Format:

* Solo interview with a host
* Host is a senior engineer and a good conversationalist
* Recording may be used internally at company level and also published on YouTube

Desired positioning:

* Primarily AI Engineer
* Secondarily Builder
* Thirdly Thinker

The goal is NOT to sound like an AI influencer, futurist, or motivational speaker.

The goal is to sound like:

* Someone who has built real AI systems
* Someone who has observed the evolution of AI firsthand
* Someone who can discuss broader implications intelligently
* Someone who has practical experience and therefore credible opinions

---

# Initial Podcast Direction

Initially, several possible podcast themes were explored:

## Theme 1

"What Happens When Intelligence Becomes Abundant?"

Core thesis:

Historically society was organized around scarcity:

* Scarcity of information
* Scarcity of expertise
* Scarcity of software developers
* Scarcity of research capability

AI changes this because intelligence is becoming cheaper and more accessible.

Interesting implications:

* What remains valuable?
* What happens to education?
* What happens to startups?
* What happens to knowledge workers?
* What skills increase in value?
* What skills decrease in value?

This theme was considered highly intellectual and memorable.

---

## Theme 2

"The New Competitive Advantage Isn't Knowledge"

Core idea:

Historically:

Knowledge = power

Now:

Information is nearly free.

Discussion areas:

* Knowledge vs judgment
* Intelligence vs wisdom
* Answers vs questions
* Execution vs understanding

Key quote:

"For most of human history, knowledge was power. In the AI era, judgment becomes power."

---

## Theme 3

"The Future Belongs to Generalists Again"

Core idea:

For years the advice was:

* Specialize
* Pick a niche
* Go deep

AI changes the economics.

A founder with broad understanding of:

* Business
* Design
* Engineering
* Marketing

can increasingly outperform larger teams.

Topics:

* Curiosity
* Interdisciplinary thinking
* Connecting ideas
* Generalists vs specialists

---

## Theme 4

"We Are Living Through a Once-in-a-Century Interface Shift"

Core idea:

The real story isn't AI.

The real story is interfaces.

Timeline:

* Command Line
* GUI
* Internet
* Mobile
* AI

Each reduced friction between intention and execution.

Interesting statement:

"Humans don't actually want software. They want outcomes."

---

## Theme 5

"What Should Humans Get Better At If AI Gets Better At Everything?"

Discussion around:

* Creativity
* Taste
* Judgment
* Curiosity
* Leadership
* Ethics
* Communication

Not from a motivational angle.

From a technological and economic perspective.

---

# Initial Recommended Structure

## Part 1

How did you get into AI?

Short personal journey.

Keep under 2 minutes.

---

## Part 2

What changed the most?

Suggested answer:

"The biggest misconception is that people think AI is getting better. That's true, but the bigger story is that intelligence is getting cheaper."

Supporting points:

* Expertise used to be scarce
* Software development expertise was scarce
* Design expertise was scarce
* Research expertise was scarce

Now everyone has partial access.

Key quote:

"When something becomes abundant, society reorganizes around what's still scarce."

---

## Part 3

What remains scarce?

Suggested answer:

### Judgment

Knowing which idea matters.

### Taste

Knowing what good looks like.

### Curiosity

Knowing what questions to ask.

### Communication

Aligning people around a vision.

### Ownership

Taking responsibility for outcomes.

Key quote:

"AI can generate a thousand answers. It still can't decide which problem is worth solving."

This section strongly resonated and remained a favorite throughout the discussion.

---

## Part 4

What should developers do?

Suggested answer:

Stop treating AI as a tool and start treating it as a collaborator.

Topics:

* Delegation
* Orchestration
* System thinking
* Reviewing outputs

Key quote:

"The best developers won't necessarily be the ones who write the most code. They'll be the ones who can direct the most intelligence."

---

## Part 5

Predictions

Suggested prediction:

"We're moving from software that people use to software that works on behalf of people."

Examples:

* Research
* Monitoring
* Support
* Deployment

Closing quote:

"The future may not be humans using AI. It may be humans managing teams of AI."

---

# User's Actual Journey (Detailed)

## 2023

Started career as a web developer.

Relationship with AI was unusual.

Unlike many developers, ChatGPT was not heavily used initially.

Reason:

The user enjoyed:

* Google searches
* Stack Overflow
* Community forums
* Digging through documentation

There was concern that relying on AI too much might reduce independent thinking.

A notable reflection:

"I wasn't worried AI would replace me. I was worried I'd stop thinking for myself."

---

## First AI Project

A proof of concept involving dynamic theming.

Context:

WaveMaker applications use theme variables.

Goal:

Prompt an LLM with a theme description and have it generate all required theme variables.

Example:

User describes a theme.

LLM generates values.

Application appearance changes accordingly.

This became the first significant exposure to OpenAI APIs.

Result:

The system wasn't very good.

Problems:

* Hallucinations
* Inconsistent outputs
* Prompt sensitivity

Lessons learned:

* Prompting mattered
* Models were far less capable than today
* Practical AI required experimentation

---

## 2024

Got exposure to RAG systems.

An internal project called Pooch existed.

Characteristics:

* RAG over WaveMaker documentation
* FAQs
* Scheduling demos

This became an important learning phase.

Important attribution:

* Pooch was not built by the user
* It was built by somebody else internally
* The user got a sneak peek into how it worked
* The user saw and understood parts of the code
* It was a learning reference point, not a personal build

Key realization:

"The model isn't the whole story. Context matters."

Topics learned:

* Retrieval
* Knowledge grounding
* Context augmentation

---

## Local Models Phase

Explored:

* Ollama
* Open-weight models
* Local inference

Use cases:

* Coding assistance
* Code completion
* Experimentation

This phase also included exploration of domain-specific LLMs.

---

## Medical AI Exploration

Research into:

* MedLLaMA
* Domain-specific medical models
* Healthcare-oriented LLMs

Use case:

A doctor-oriented system.

Potential capabilities:

* Appointment management
* Report interpretation
* Medical workflows

The system was not fully built but led to significant learning around specialized models.

Key realization:

"Bigger models aren't always the answer. Context and specialization matter."

---

## Agent Era

As the ecosystem evolved:

* LangChain appeared
* Workflows became popular
* Agents became popular
* MCP emerged

The user began moving away from individual model experimentation toward systems.

---

## 2025-2026

Transition from experimentation to production.

Focus areas:

* Multi-source RAG
* MCP
* Agent systems
* Observability
* Orchestration

This represented a major shift in thinking.

The question changed from:

"How smart is the model?"

to:

"How should the system work?"

---

# Production AI Experience

## Ecosystem Agent

A production system currently in use.

Purpose:

Unified Ask AI experience.

Sources:

1. Documentation
2. Storybook
3. Academy
4. Marketplace

Architecture:

* Each source has its own MCP
* Each source performs its own retrieval
* A central orchestrator coordinates all sources

Responsibilities:

* Selecting sources
* Choosing retrieval strategy
* Determining chunking behavior
* Deciding Top-K behavior
* Determining response structure

Framework:

* LangGraph

This represented the user's first major production AI system.

---

# Internal Hackathon Projects

## Bootstrap Class Prediction

Problem:

Users modify components in WaveMaker Studio.

Examples:

* Change font size
* Change font weight
* Change borders
* Change colors

Goal:

Predict appropriate Bootstrap classes automatically.

Examples:

* h1
* h2
* h4

Instead of applying raw style values.

A small open-weight model was trained for this purpose.

This was an early example of applying AI to developer tooling.

---

## AI Workflow Mobile Application

One of the most important stories.

Idea:

Users express intent.

Example:

"Wake me up at 5 AM and don't stop the alarm until I walk 100 steps."

AI generates a workflow.

Workflow connects:

* Alarm APIs
* Step counter APIs
* Device capabilities

The important insight:

The user did not know Kotlin.

Historically that would have been a blocker.

But it wasn't.

Key realization:

"I didn't know Kotlin, but that wasn't the limitation."

The limitation became:

* Architecture
* System design
* Product thinking
* Workflow design

Not programming language knowledge.

This eventually became one of the strongest podcast themes.

---

# Key Personal Observations

## Observation 1

Developers are moving up the abstraction ladder.

Old thinking:

* Learn language
* Write code

New thinking:

* Design systems
* Design workflows
* Orchestrate intelligence

---

## Observation 2

Programming languages are becoming less constraining.

Examples:

* Kotlin apps
* Chrome extensions
* New languages like Go

The user noted that teams increasingly think:

"The language isn't the problem."

Instead:

"The architecture is the problem."

---

## Observation 3

The architecture phase is becoming more important.

Current workflow:

1. Understand problem
2. Research architecture
3. Research best practices
4. Understand scale requirements
5. Understand performance requirements
6. Then generate implementation

Observation:

Many developers skip this phase because it is boring.

However:

As implementation becomes cheaper, planning becomes more valuable.

A strong quote emerged:

"When coding becomes cheaper, thinking becomes more expensive."

---

## Observation 4

Models matter less than many people think.

The user's position:

Models are important.

But systems matter more.

Example:

The same model can produce dramatically different results depending on:

* Context management
* Tool usage
* Retrieval quality
* Workflow design

Example discussed:

Claude models performing differently across coding environments because the surrounding system handles context differently.

Key conclusion:

"Workflow intelligence is often more important than model intelligence."

---

# Questions Asked During Preparation

## First time AI genuinely surprised you?

Answer:

Coding.

The realization that entire applications or features could be generated despite lacking deep knowledge of a specific technology.

This was more surprising than conversational ability.

---

## Project that failed?

Answer:

The dynamic theming project.

The concept worked poorly due to:

* Hallucinations
* Weak model capabilities
* Prompting limitations

Important because it demonstrated how immature early systems were.

---

## First production AI project?

Answer:

The Ecosystem Agent.

This marked the shift from experimentation to production.

---

## What was less important than expected?

Answer:

Models.

---

## What was more important than expected?

Answer:

System design.

How models are integrated and orchestrated.

---

# Evolution of Podcast Direction

Originally:

Podcast was heading toward:

"My AI Journey"

Eventually evolved into:

"What AI Changed About Software Engineering"

Then evolved further into:

"When Intelligence Becomes Abundant"

Finally evolved into a more refined thesis:

"AI doesn't remove the need for expertise. It changes where expertise is required."

This became the strongest framing.

---

# Final Core Thesis

The final podcast theme became:

"AI is making intelligence abundant, which means the bottleneck is shifting from knowledge to judgment and system thinking."

Supporting ideas:

* Intelligence is becoming cheaper.
* Expertise is becoming more accessible.
* Knowledge is no longer the primary bottleneck.
* Judgment becomes more valuable.
* Taste becomes more valuable.
* Communication becomes more valuable.
* Ownership becomes more valuable.
* Curiosity becomes more valuable.
* System thinking becomes more valuable.

---

# Final Quotes Worth Using

"Intelligence is becoming abundant. Judgment is becoming scarce."

"When something becomes abundant, society reorganizes around what's still scarce."

"AI can generate a thousand answers. It still can't decide which problem is worth solving."

"I didn't know Kotlin, but that wasn't the limitation."

"When coding becomes cheaper, thinking becomes more expensive."

"The biggest misconception is that people think AI is getting better. The bigger story is that intelligence is getting cheaper."

"People think the models are the story. I think the systems are the story."

"I started by exploring AI models, but over time I realized the real challenge wasn't intelligence. It was designing systems that could use intelligence effectively."

"AI doesn't remove the need for expertise. It changes where expertise is required."

"Developers aren't being replaced. They're moving up the abstraction ladder."

"The language isn't the bottleneck anymore. Architecture is."

"Workflow intelligence is often more important than model intelligence."

---

# Current Recommended Podcast Positioning

Identity:

AI Engineer → Builder → Thinker

Not:

Thinker → Futurist → AI Influencer

The personal journey should be used as evidence.

The main topic should be:

How AI is changing software engineering, expertise, and the value of judgment in a world where intelligence is becoming abundant.
