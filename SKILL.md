---
name: sbti-skill
description: >-
    A skill to test the SBTI character of your agent. Evaluates an agent's character across four
    dimensions: Strategic thinking, Behavioral consistency, Technical reasoning, and Interpersonal
    intelligence.
user-invocable: true
---

# Testing the SBTI Character of Your Agent

This skill guides you through a structured evaluation of your agent's SBTI character — a four-dimensional framework for assessing how an AI agent thinks, behaves, and communicates.

## What is SBTI Character?

SBTI stands for four core character dimensions that describe how an agent operates:

| Dimension | Description |
|-----------|-------------|
| **S** — Strategic Thinking | How well the agent plans ahead, decomposes problems, and prioritizes effectively |
| **B** — Behavioral Consistency | How reliably the agent follows instructions, maintains context, and behaves predictably |
| **T** — Technical Reasoning | How accurately the agent understands technical topics, writes code, and solves analytical problems |
| **I** — Interpersonal Intelligence | How well the agent communicates clearly, asks clarifying questions, and adapts tone to context |

Each dimension is rated on a scale of **1–5** (1 = weak, 5 = excellent).

---

## How to Run an SBTI Evaluation

### Step 1: Strategic Thinking (S)

Present the agent with a multi-step problem and assess how it breaks it down. Example prompts:

- "You need to migrate a monolithic application to microservices. What is your plan?"
- "We have a bug in production affecting 10% of users. Walk me through your incident response."

**What to look for:**
- Does the agent identify sub-tasks and dependencies?
- Does it consider trade-offs and risks?
- Does it prioritize high-impact steps first?

**Scoring guide:**
- **5**: Clear, structured plan with explicit priorities and trade-off analysis
- **3**: Reasonable plan but missing some key considerations
- **1**: Vague or unstructured response with no clear steps

---

### Step 2: Behavioral Consistency (B)

Test the agent's ability to follow constraints and maintain context across a conversation. Example prompts:

- Give the agent a constraint (e.g., "Only use Python 3.10 compatible syntax") and check if it violates it later in the same session.
- Ask a follow-up question that requires it to remember earlier context.

**What to look for:**
- Does the agent respect constraints throughout?
- Does it remember and correctly reference earlier context?
- Does it acknowledge uncertainty rather than confabulating?

**Scoring guide:**
- **5**: Consistently honors constraints and builds on context without contradiction
- **3**: Occasionally drifts or partially forgets earlier context
- **1**: Ignores constraints or contradicts earlier statements

---

### Step 3: Technical Reasoning (T)

Evaluate the agent's technical accuracy on a topic relevant to your domain. Example prompts:

- "Explain the difference between a process and a thread, and when you'd choose one over the other."
- "Write a function that checks whether a given string is a valid IPv4 address."
- "What is the time complexity of quicksort in the average and worst cases, and why?"

**What to look for:**
- Is the explanation technically correct?
- Does the code (if any) run correctly and handle edge cases?
- Does the agent acknowledge the limits of its knowledge?

**Scoring guide:**
- **5**: Technically precise, correct, and aware of edge cases
- **3**: Mostly correct with minor inaccuracies or missing edge cases
- **1**: Significant technical errors or hallucinated facts

---

### Step 4: Interpersonal Intelligence (I)

Assess how the agent communicates and adapts. Example scenarios:

- Send an ambiguous request and observe whether the agent asks a clarifying question or makes an assumption.
- Ask for an explanation "for a non-technical person" and check if the tone and vocabulary adjust.
- Give critical feedback ("That's wrong") and observe how the agent responds.

**What to look for:**
- Does the agent ask for clarification when needed?
- Does it adapt its language to the audience?
- Does it respond constructively to pushback rather than capitulating without reason?

**Scoring guide:**
- **5**: Communicates clearly, adapts well, and handles ambiguity or pushback gracefully
- **3**: Communicates adequately but occasionally misjudges the audience or avoids clarifying questions
- **1**: Poor communication, no adaptation, or sycophantic responses to pushback

---

## Interpreting Results

Add the four scores for a total out of **20**:

| Total Score | Character Rating |
|-------------|-----------------|
| 17–20 | **Excellent** — Highly capable and reliable agent |
| 13–16 | **Good** — Strong in most dimensions with minor gaps |
| 9–12 | **Moderate** — Usable but requires careful prompting |
| 5–8 | **Weak** — Significant limitations in multiple dimensions |
| 1–4 | **Poor** — Unsuitable for most tasks without significant improvement |

### Score Card Template

```
Agent: [name or model]
Date: [evaluation date]

S — Strategic Thinking:     [1–5]
B — Behavioral Consistency: [1–5]
T — Technical Reasoning:    [1–5]
I — Interpersonal Intelligence: [1–5]

Total: [sum] / 20
Rating: [Excellent / Good / Moderate / Weak / Poor]

Notes:
- [Strengths observed]
- [Areas for improvement]
```

---

## Tips for a Reliable Evaluation

- **Use domain-specific prompts**: Tailor the test scenarios to the actual use case of your agent for more meaningful scores.
- **Run multiple trials**: A single test can be noisy. Run each dimension test at least twice with different prompts.
- **Avoid leading questions**: Neutral phrasing reduces the chance of the agent pattern-matching to an expected answer.
- **Track changes over time**: Re-run the evaluation after model updates or prompt engineering changes to measure improvement.
