# Day 3 — Role-Based Prompting
**60-Day Claude AI Mastery Challenge**
*Phase 1: Foundation & Prompt Engineering*

---

## What is Role-Based Prompting?

Role-based prompting means giving Claude a specific persona or expert identity in the system prompt (or at the start of your message) before asking a question. Instead of asking a general assistant, you're asking a specialist.

**Without a role:**
> "Explain inflation."

**With a role:**
> "You are a university economics professor with 20 years of teaching experience. Explain inflation using real-world examples and precise economic terminology."

The same question — but the second produces a fundamentally different response in tone, vocabulary, depth, and structure.

---

## Why It Works

Role-based prompting shifts which patterns Claude weights most heavily when generating a response. The persona restructures the entire answer strategy:

- **Vocabulary** — an economist says "demand-pull inflation"; a teacher says "when too much money chases too few goods"
- **Tone** — a doctor is careful and caring; a lawyer is precise and hedged
- **Depth** — a software engineer gives code examples; a chef gives technique and flavour context
- **Framing** — the same concept is explained differently depending on who the expert is

---

## Task 2 — Comparing With vs Without a Role

**Question asked:** *"What causes inflation?"*

### Without a role (general assistant)
Claude gives a balanced, textbook-style answer covering supply and demand, monetary policy, and government spending. It's accurate but generic — suitable for anyone, specialized for no one.

### With role: Economics Professor
The response opens with aggregate demand and supply frameworks, references historical examples like the 1970s oil shock and post-COVID supply chain disruptions, uses terms like "demand-pull," "cost-push," and "monetary expansion," and ends with a nuanced discussion of central bank responses. It reads like a lecture.

### Key observation
The role doesn't just change tone — it changes **what information gets prioritized**, **how deep the answer goes**, and **what the reader is assumed to already know**.

---

## Task 3 — Two Personas Compared

### Persona 1: Economics Professor

**System prompt used:**
```
You are a university economics professor with 20 years of teaching experience.
Explain concepts clearly using real-world data and examples.
Use precise economic terminology.
```

**Sample question:** What causes inflation?

**Response characteristics:**
- Used technical terms: demand-pull, cost-push, monetary expansion, CPI
- Referenced historical events as case studies
- Structured like an academic explanation with clear sections
- Assumed the reader has basic economics literacy

---

### Persona 2: Primary School Teacher

**System prompt used:**
```
You are a friendly, enthusiastic primary school teacher.
Explain things simply using analogies, stories, and relatable examples
suitable for young learners. Keep it fun and encouraging.
```

**Same question:** What causes inflation?

**Response characteristics:**
- Used the analogy of a school tuck shop running out of snacks
- No technical jargon — "prices go up" instead of "cost-push pressure"
- Encouraging and conversational tone
- Short sentences, simple vocabulary, relatable scenario

---

### What This Demonstrates

| | Economics Professor | Primary School Teacher |
|---|---|---|
| Vocabulary | Technical, precise | Simple, everyday |
| Examples | Historical events, data | Everyday analogies |
| Assumed knowledge | Intermediate economics | None |
| Tone | Academic, analytical | Warm, encouraging |
| Ideal for | Students, professionals | Beginners, children |

The same underlying knowledge — completely different communication style. That's the power of role-based prompting.

---

## Task 4 — Claude Usage Counter

Claude Usage Counter is a browser extension that tracks your API token usage and conversation counts across Claude sessions.

**How to install:**
1. Search "Claude Usage Counter" in the Chrome Web Store
2. Click Add to Chrome
3. The extension icon appears in your toolbar and shows live usage stats

**Why it's useful:**
- Helps you understand how much of your context window you're using
- Useful for staying within plan limits on claude.ai
- Gives insight into which prompt styles are more token-efficient

---

## Key Learnings

1. **Role = context, not decoration.** The persona fundamentally changes the response structure, not just the tone.
2. **Be specific in your role.** "You are a doctor" is weaker than "You are a general practitioner with 15 years of clinical experience who explains things in plain language."
3. **Match the role to your audience.** A teacher persona is better for learning; an engineer persona is better for technical problem-solving.
4. **Roles can stack with tasks.** "You are a chef. Write a recipe card for..." combines persona with format instruction for even more targeted output.
5. **Compare outputs deliberately.** Running the same question with and without a role is the fastest way to understand the impact.

---

## Prompts Practiced Today

```
# Persona prompt template
You are a [role] with [years/type] of experience in [domain].
[Communication style instruction].
[Any constraints or caveats].

# Example 1 — Economics Professor
You are a university economics professor with 20 years of teaching experience.
Explain concepts clearly using real-world data and examples.
Use precise economic terminology.

# Example 2 — Primary School Teacher
You are a friendly, enthusiastic primary school teacher.
Explain things simply using analogies, stories, and relatable examples
suitable for young learners. Keep it fun and encouraging.

# Example 3 — Software Engineer
You are a senior software engineer with 15 years of experience across
web, systems, and AI. Be precise, technical, and opinionated.
Prefer examples and code snippets over abstract explanations.
```

---

## Resources

- [GeeksforGeeks — Role-Based Prompting](https://www.geeksforgeeks.org/artificial-intelligence/role-based-prompting/)
- [Learn Prompting — Role Prompting](https://learnprompting.org/docs/advanced/zero_shot/role_prompting)
- [Anthropic Docs](https://docs.anthropic.com)

---

*Day 3 of 60 — 60-Day Claude AI Mastery Challenge*
