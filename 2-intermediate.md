# How Large Language Models Work

## Part 3 - Why similar prompts cant

### Variability is built into generation

For most prompts, there is no single inevitable continuation. Many answers can be grammatically and contextually plausible.

Outputs can change because:

1. **Sampling:** the system may choose among several plausible next tokens. A setting often called **temperature** influences how conservative or varied that selection is.
2. **Framing:** words such as *risk*, *growth*, *urgent*, or *reassuring* activate different language patterns.
3. **Order:** information placed earlier can receive more emphasis.
4. **Constraints:** adding an audience, format, source rule, or prohibited commitment changes the solution space.

This variability is useful for brainstorming and scenario planning. It is risky when a team needs repeatable wording, auditable decisions, or tightly controlled commitments.

> the previous section talks about how LLMS generate content - they predict one token at a time based on previous token. this section is just a jump that variablity is built into generation. a few lines in the start of the section should have some context that relates previous section to current section.

---

## Part 4 - How training data shapes behaviour

### The model's reading history

**Training data** is the large collection of examples from which a model learns language patterns. During training, it learns relationships such as common phrasing, tone conventions, argument structures, and which concepts often appear together.

This does **not** mean the model contains a neat, searchable library of every document it encountered. Its responses reflect a statistical imprint of the material rather than guaranteed recall of an authoritative source.

Training data influences:

| Area | Possible effect |
|---|---|
| Domain fit | Strong generic writing but weak specialist terminology |
| Regional fit | Assumptions that do not match local practice |
| Representation | Some voices or perspectives may be underrepresented |
| Currency | The model may not know recent changes unless current sources are supplied |
| Framing | Frequently seen narratives may appear more "normal" or important |

:::info Better practice
When domain accuracy matters, provide approved policies, definitions, recent data, or excerpts and instruct the model to stay within them.
:::

> add few liner context in start relating current section to text generation and prompt output variability.
> the explainers in possible effect column are too generic , not good explainations - need to make a bit more clear. also add another column called Example where you give a simple, practical example of each effect

---

## Part 5 - Generating Is Not the Same as Knowing

### Fluency can imitate certainty

**Generating** means producing text that fits learned patterns and the current context.

**Knowing**, in a workplace sense, means being anchored to verified facts, approved evidence, current systems of record, and accountable interpretation.

An LLM can imitate the form of a policy, calculation, citation, or expert explanation even when part of the content is unsupported. Confidence is also a language pattern; it is not evidence.

A practical task split is:

- **Language work:** structure, tone, clarity, summarization, option generation, and audience adaptation.
- **Truth work:** facts, figures, legal meaning, policy requirements, contractual commitments, and causal claims.

:::warning Risk signal
The more polished and authoritative a draft sounds, the easier it is to skip verification. Review the claims, not just the prose.
:::

> facts / content sentences are very disconnected from each other. there should be coherency / flow.

---

## Part 6 - A Safer Workplace Workflow

### Use the model for what it does well—and add controls

A reliable workflow does not ask the LLM to be both ghostwriter and final authority.

1. Define the goal, audience, constraints, and required format.
2. Supply the minimum approved context needed for the task.
3. Ask for visible assumptions, options, risks, or source boundaries.
4. Review assumptions before polishing the language.
5. Verify every factual or consequential claim.
6. Obtain accountable human approval before high-impact use.

This approach preserves the speed of generation while reducing the chance that plausible text becomes an unverified business decision.

> Give some example.

---

## Part 7 - Final Decision Check

### Apply the mental model

An operations manager gives an LLM backlog notes and asks for three headcount-prioritization options. The response is clear, detailed, and persuasive. One option assumes a team has six available people, but the current capacity plan shows only four.

The useful part of the output is the rapid generation of structured options and trade-offs. The unsafe part would be treating its plausible assumption as an organizational fact.

> Make example a bit more detailed. Right now it is way too concise. Don't make it unncessary complex/complicated but do add more detail so the entire scenario can be undertood better

---

---

# What is an AI Agent


## Part 2 - A Tool Answers; an Agent Pursues a Goal

### One instruction versus one goal

The clearest way to tell an agent apart from a regular AI tool is to notice how much you have to steer it.

With a regular tool, you drive every step. You ask it to summarise a report, read the result, then ask it to draft an email, read that, then ask it to shorten the email. Each request stands alone, and the tool waits for you in between. It has no sense of where the whole effort is heading.

With an agent, you describe the destination once — *research our top three competitors' pricing and send me a one-page comparison* — and it decides what to do first, what to do next, and when it is finished. You move from **instructing** to **delegating**.

### Key Idea: Using a regular tool is like asking a colleague one question at a time. Using an agent is like handing that colleague the whole task and asking them to report back when it is done.

> the use cases of AI here have different end goals / objectives. a better way to explain diff btw regular AI  and agentic AI is to use the same end goal/scenario / objective for both and then in each topic explain how the workflow would look different for both.

---

# What Are Custom AI Assistants — GPTs, Gems, and Similar Tools


## Part 1 - From Repeated Prompts to a Configured Assistant

### From repeated prompts to a configured assistant

By now you have used a general AI tool by typing a prompt, reading the reply, and refining it. That works, but every conversation starts from nothing. The tool does not know who you are, what your organisation expects, or how you handled the same task last week. For a one-off question that is fine. For a task you repeat every week, re-explaining the context each time is slow and produces inconsistent results.

There is a more powerful option: an AI assistant configured for a single purpose. Instead of a blank tool you steer from scratch, it already knows its role, the material it should rely on, the limits it must respect, and the format its answers should take.

By the end of this lesson, you should be able to:

- explain how a custom AI assistant differs from a general AI tool;
- describe what Custom GPTs and Google Gems are and which platform each belongs to;
- decide when a custom assistant is worth building instead of writing another prompt; and
- recognise real professional tasks where a custom assistant is more reliable than repeated prompting.

> give some simple example here.

---

# Identifying Tasks Suitable for AI in Your Role


## Part 2 - Two Dimensions That Decide Fit

### A simple test for any task

You do not need a long checklist to judge whether a task suits AI. Two questions do most of the work.

First: *how repetitive and structured is it?* A structured task has clear inputs, a predictable shape, and a recognisable finished result — drafting a standard reply, reformatting data, cutting a document down to a set length. The more each instance looks like the last, the more pattern there is for AI to work with.

Second: *how much human judgment does it demand?* Judgment is what you bring that a pattern cannot: weighing competing interests, reading a room, deciding what is fair, and owning the consequences. The more a task turns on judgment, the less of it you can safely hand over.

Plot any task against those two dimensions and its suitability comes into focus. Highly structured with low judgment sits in the strong-candidate corner; unstructured and judgment-heavy sits firmly with you. Most work lands somewhere between — which is exactly why the test is worth running deliberately rather than on gut feel.

> Give examples here as well.

---

# Part 3 - What makes a task a strong candidate

### The shape of AI-friendly work

Strong candidates tend to share a family of traits. Learning to spot them lets you recognise a good fit quickly, even for a task you have never thought of handing over.

The common thread is that the work is mostly *language or pattern work* with a result you can check. When a task has clear inputs, a repeatable structure, and an output you can verify quickly, AI can take a first pass and you can confirm it in a fraction of the original time. The stakes of any single output are usually modest, so a mistake is easy to catch before it travels far.

None of these traits means 'hand it over and look away'. They mean the task is worth *trying* with AI — because the effort of drafting is high and the effort of checking is low, which is exactly the trade AI is good at.

> Give examples.

---

## Part 6 - Deciding What to Tackle First
### Not all good candidates are equal

Your 'good fit' pile is still a list, not a plan. Some of those tasks will repay AI effort far more than others and starting in the right place builds both real time savings and your own confidence.

Two things push a task up the queue. The first is *frequency*: a task you do many times a week returns far more for the same set-up effort than one you do twice a year. The second is *how easy the result is to check*: when verifying an output is quick and reliable, you capture the saving safely; when checking is slow or uncertain, the gains shrink. A high-frequency, easy-to-verify, low-risk task is the ideal place to begin. Prove the approach there, learn what good supervision looks like, then extend to the next candidate.

> Give example here. make it mroe technical since previous sections have already given a lot of related responses. give some practical, industry relevant example.

---

# Evaluating and Choosing the Right AI Tool for Your Work Problem



## Part 2 - Why Most Tool Choices Go Wrong
### Selection by momentum

When a tool becomes popular, its popularity starts to feel like proof. But popularity only measures how many people adopted something — not whether it suits your task, your data rules, or your budget. A colleague's recommendation carries the same trap: it reflects the problem *they* solved, with *their* data and *their* skill, which may look nothing like yours. And a vendor demo is engineered to show the tool at its best on an example the vendor chose.

The cost of a mismatched tool is rarely just the subscription fee. It is the hours spent forcing an awkward fit, the rework when outputs miss the mark, and the slow erosion of trust when the tool disappoints on something important. Choosing well is cheaper than choosing fast.

> give some example of such a use case which actually happened in any real industry / company. make sure to verify and fact check ur source and facts

---

## Part 3 - The Four Evaluation Questions

### A framework you can carry

A good evaluation is not a vague feeling about a tool; it is a short, repeatable interrogation. Four questions cover most of what matters, and you can ask them of any AI tool in a few minutes:

1. **Problem** — What specific problem does this tool solve, and is that a problem I actually have? Name the job before the tool.
2. **Fit** — How well does the tool's capability match the nature of my task? Open-ended drafting and precise extraction are different jobs that reward different tools.
3. **Risk** — What are the privacy and data risks? Where does my input go, who can see or keep it, and is that acceptable for this data?
4. **Value** — What does it cost in time and money relative to the value it delivers on work I will actually repeat?

Ask them in order. The first question often ends the evaluation early: if a tool does not solve a problem you genuinely have, the other three never need answering.

> give some worked out example with the entire steps.
