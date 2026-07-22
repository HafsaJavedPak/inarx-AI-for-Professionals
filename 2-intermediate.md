## Part 3 - Why similar prompts cant

### Variability is built into generation

```text
+ADD
As the previous section explained, an LLM builds its response one token at a time, each one chosen based on the tokens that came before it. Because that choice is made fresh at each step rather than read off a fixed answer key, the same prompt does not have to produce the same output twice.+
```

For most prompts, there is no single inevitable continuation. Many answers can be grammatically and contextually plausible.

Outputs can change because:

1. **Sampling:** the system may choose among several plausible next tokens. A setting often called **temperature** influences how conservative or varied that selection is.
2. **Framing:** words such as *risk*, *growth*, *urgent*, or *reassuring* activate different language patterns.
3. **Order:** information placed earlier can receive more emphasis.
4. **Constraints:** adding an audience, format, source rule, or prohibited commitment changes the solution space.

This variability is useful for brainstorming and scenario planning. It is risky when a team needs repeatable wording, auditable decisions, or tightly controlled commitments.

---

## Part 4 - How training data shapes behaviour

### The model's reading history

```text
+ADD
The previous section showed that a model can generate different outputs for the same prompt because it is choosing token by token rather than recalling a fixed answer. Where do those tokens and patterns come from in the first place? That comes down to training data.+
```

**Training data** is the large collection of examples from which a model learns language patterns. During training, it learns relationships such as common phrasing, tone conventions, argument structures, and which concepts often appear together.

This does **not** mean the model contains a neat, searchable library of every document it encountered. Its responses reflect a statistical imprint of the material rather than guaranteed recall of an authoritative source.

Training data influences:

```text
-REMOVE
| Area | Possible effect |
|---|---|
| Domain fit | Strong generic writing but weak specialist terminology |
| Regional fit | Assumptions that do not match local practice |
| Representation | Some voices or perspectives may be underrepresented |
| Currency | The model may not know recent changes unless current sources are supplied |
| Framing | Frequently seen narratives may appear more "normal" or important |
```

```text
+ADD
| Area | Possible effect | Example |
|---|---|---|
| Domain fit | The model has seen far more general business or casual writing than material from narrow specialist fields, so it can produce fluent prose while using specialist terms loosely or incorrectly | Asked to summarise a clinical trial report, it may use "significant" in the everyday sense rather than the precise statistical sense the field requires |
| Regional fit | The model's training examples skew toward the practices, laws, or conventions of the regions most represented in its data, so it may default to those norms rather than the user's local ones | Asked to draft an employment contract, it may include at-will employment language common in the US even though the user is in a country with different labour law |
| Representation | If a group, dialect, or viewpoint appeared less often in training material, the model has fewer patterns to draw on for it and may describe it less accurately or fall back on generic phrasing | Asked to write about a small regional dialect or a less-documented profession, the output may default to broad generalisations rather than specifics |
| Currency | The model's patterns are frozen at the point its training data was collected, so it cannot know about events, prices, or rules that changed afterward unless those are supplied in the prompt | Asked for "the current interest rate" or "this year's tax bracket," it may state an outdated figure with the same confidence as a current one |
| Framing | Some narratives or conclusions appeared so often in training material that the model treats them as the default, ordinary answer, even when a given situation calls for a different conclusion | Asked to evaluate a business plan, it may default to generic risk framing common in the source material and understate a genuinely unusual risk unique to the case |
```

:::info Better practice
When domain accuracy matters, provide approved policies, definitions, recent data, or excerpts and instruct the model to stay within them.
:::

---

## Part 5 - Generating Is Not the Same as Knowing

### Fluency can imitate certainty

```text
-REMOVE
**Generating** means producing text that fits learned patterns and the current context.

**Knowing**, in a workplace sense, means being anchored to verified facts, approved evidence, current systems of record, and accountable interpretation.

An LLM can imitate the form of a policy, calculation, citation, or expert explanation even when part of the content is unsupported. Confidence is also a language pattern; it is not evidence.
```

```text
+ADD
**Generating** means producing text that fits learned patterns and the current context. That is a different act from **knowing**, which, in a workplace sense, means being anchored to verified facts, approved evidence, current systems of record, and accountable interpretation. Because generating and knowing are different processes, an LLM can imitate the form of a policy, calculation, citation, or expert explanation even when part of the content is unsupported — the fluency of the output tells you nothing about whether it is anchored to fact. This matters because confidence is also a language pattern; it is not evidence, so a polished tone is not a signal you can rely on to tell the two apart.
```

A practical task split is:

- **Language work:** structure, tone, clarity, summarization, option generation, and audience adaptation.
- **Truth work:** facts, figures, legal meaning, policy requirements, contractual commitments, and causal claims.

:::warning Risk signal
The more polished and authoritative a draft sounds, the easier it is to skip verification. Review the claims, not just the prose.
:::

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

```text
+ADD
For example, a manager asking an LLM to draft a client-facing project update might: (1) state the goal is a two-paragraph status update for a non-technical client, (2) paste in the actual sprint report as the only source of facts, (3) ask the model to flag any assumption it made and list which figures came from the sprint report versus its own phrasing, (4) check that the flagged assumptions are reasonable, (5) confirm the dates and numbers against the sprint report itself before sending, and (6) have the account lead sign off before it goes to the client. Each step keeps a plausible-sounding draft from quietly becoming an approved commitment.
```

---

## Part 7 - Final Decision Check

### Apply the mental model

```text
-REMOVE
An operations manager gives an LLM backlog notes and asks for three headcount-prioritization options. The response is clear, detailed, and persuasive. One option assumes a team has six available people, but the current capacity plan shows only four.

The useful part of the output is the rapid generation of structured options and trade-offs. The unsafe part would be treating its plausible assumption as an organizational fact.
```

```text
+ADD
An operations manager is behind on a product launch and needs to decide how to reassign staff for the next two weeks. She pastes her backlog notes — a list of open tasks, deadlines, and rough time estimates — into an LLM and asks it to generate three headcount-prioritization options, each showing which tasks get covered and which get delayed.

The response comes back clear, detailed, and persuasive: three named options, each with a short rationale, a list of tasks covered, and a projected completion date. Option 2 is framed as the strongest choice, since it finishes the most tasks on time. It does this by assuming the QA team has six available people to pull from. The manager's actual current capacity plan, however, shows only four QA people available that week — two are out on approved leave, which never appeared in the backlog notes because that file only tracks tasks, not staffing.

The useful part of the output is the rapid generation of structured options and trade-offs — it saved her the time of drafting three scenarios by hand. The unsafe part would be approving Option 2 on the strength of its confident write-up, without checking its staffing assumption against the capacity plan. If she skipped that check, she could commit the team to a schedule that is short two people from day one.
```

---

## What is an AI Agent

## Part 2 - A Tool Answers; an Agent Pursues a Goal

### One instruction versus one goal

The clearest way to tell an agent apart from a regular AI tool is to notice how much you have to steer it.

```text
-REMOVE
With a regular tool, you drive every step. You ask it to summarise a report, read the result, then ask it to draft an email, read that, then ask it to shorten the email. Each request stands alone, and the tool waits for you in between. It has no sense of where the whole effort is heading.

With an agent, you describe the destination once — *research our top three competitors' pricing and send me a one-page comparison* — and it decides what to do first, what to do next, and when it is finished. You move from **instructing** to **delegating**.
```

```text
+ADD
Take a single objective: *research our top three competitors' pricing and send me a one-page comparison.*

With a regular tool, you drive every step of that same objective yourself. You ask it to look up Competitor A's pricing page and summarise it, read the result, then ask it to do the same for Competitor B, read that, then ask for Competitor C, then ask it to combine the three summaries into a comparison, read that, then ask it to trim the comparison to one page. Each request stands alone, and the tool waits for you in between. It has no sense of where the whole effort is heading — you are holding the destination in your head and feeding it one step at a time.

With an agent, you describe that same destination once — *research our top three competitors' pricing and send me a one-page comparison* — and it decides what to do first, what to do next, and when it is finished: looking up each competitor, drafting the comparison, trimming it to length, and sending it, without you approving each intermediate step. You move from **instructing** to **delegating**.
```

### Key Idea: Using a regular tool is like asking a colleague one question at a time. Using an agent is like handing that colleague the whole task and asking them to report back when it is done.

---

## What Are Custom AI Assistants — GPTs, Gems, and Similar Tools

## Part 1 - From Repeated Prompts to a Configured Assistant

### From repeated prompts to a configured assistant

By now you have used a general AI tool by typing a prompt, reading the reply, and refining it. That works, but every conversation starts from nothing. The tool does not know who you are, what your organisation expects, or how you handled the same task last week. For a one-off question that is fine. For a task you repeat every week, re-explaining the context each time is slow and produces inconsistent results.

There is a more powerful option: an AI assistant configured for a single purpose. Instead of a blank tool you steer from scratch, it already knows its role, the material it should rely on, the limits it must respect, and the format its answers should take.

```text
+ADD
For example, a support team that answers the same kinds of billing questions every day could configure an assistant once with the company's refund policy, standard reply tone, and a rule to always ask for the order number first. From then on, any agent can hand it a customer's message and get a reply that already follows policy — instead of every agent re-typing the same policy details into a blank prompt each time.
```

By the end of this lesson, you should be able to:

- explain how a custom AI assistant differs from a general AI tool;
- describe what Custom GPTs and Google Gems are and which platform each belongs to;
- decide when a custom assistant is worth building instead of writing another prompt; and
- recognise real professional tasks where a custom assistant is more reliable than repeated prompting.

---

## Identifying Tasks Suitable for AI in Your Role

## Part 2 - Two Dimensions That Decide Fit

### A simple test for any task

You do not need a long checklist to judge whether a task suits AI. Two questions do most of the work.

First: *how repetitive and structured is it?* A structured task has clear inputs, a predictable shape, and a recognisable finished result — drafting a standard reply, reformatting data, cutting a document down to a set length. The more each instance looks like the last, the more pattern there is for AI to work with.

Second: *how much human judgment does it demand?* Judgment is what you bring that a pattern cannot: weighing competing interests, reading a room, deciding what is fair, and owning the consequences. The more a task turns on judgment, the less of it you can safely hand over.

Plot any task against those two dimensions and its suitability comes into focus. Highly structured with low judgment sits in the strong-candidate corner; unstructured and judgment-heavy sits firmly with you. Most work lands somewhere between — which is exactly why the test is worth running deliberately rather than on gut feel.

```text
+ADD
For example, formatting a weekly sales figures spreadsheet into a standard summary table is highly structured and low on judgment — a strong candidate. Deciding which of two underperforming employees to place on a performance improvement plan is unstructured and judgment-heavy — squarely your call, not AI's. Drafting a first response to a routine customer complaint sits in between: the reply itself is fairly structured, but deciding how much goodwill credit to offer a frustrated long-term customer still needs your judgment.
```

---

## Part 3 - What makes a task a strong candidate

### The shape of AI-friendly work

Strong candidates tend to share a family of traits. Learning to spot them lets you recognise a good fit quickly, even for a task you have never thought of handing over.

The common thread is that the work is mostly *language or pattern work* with a result you can check. When a task has clear inputs, a repeatable structure, and an output you can verify quickly, AI can take a first pass and you can confirm it in a fraction of the original time. The stakes of any single output are usually modest, so a mistake is easy to catch before it travels far.

```text
+ADD
For example, drafting a first-pass meeting summary from raw notes is language work with a checkable output: you already know what was discussed, so you can scan the draft and confirm it matches in a minute or two. Similarly, converting a list of expense entries into a standard reimbursement format is pattern work — the correct format is well defined, and a wrong entry is easy to spot by comparing it against the original receipts.
```

None of these traits means 'hand it over and look away'. They mean the task is worth *trying* with AI — because the effort of drafting is high and the effort of checking is low, which is exactly the trade AI is good at.

---

## Part 6 - Deciding What to Tackle First

### Not all good candidates are equal

Your 'good fit' pile is still a list, not a plan. Some of those tasks will repay AI effort far more than others and starting in the right place builds both real time savings and your own confidence.

Two things push a task up the queue. The first is *frequency*: a task you do many times a week returns far more for the same set-up effort than one you do twice a year. The second is *how easy the result is to check*: when verifying an output is quick and reliable, you capture the saving safely; when checking is slow or uncertain, the gains shrink. A high-frequency, easy-to-verify, low-risk task is the ideal place to begin. Prove the approach there, learn what good supervision looks like, then extend to the next candidate.

```text
+ADD
For example, a DevOps engineer might have two candidates on their good-fit list: (1) writing a plain-language summary of each day's failed CI/CD pipeline runs from the build logs, and (2) drafting the annual disaster-recovery runbook. The pipeline summary happens dozens of times a week, and checking it is fast — the engineer just compares the summary against the actual error codes in the log, which takes seconds. The disaster-recovery runbook is done once a year, and checking it properly means walking through every failover step against the live infrastructure, which takes days. Even though the runbook feels like the more "important" task, the pipeline summary is the better place to start: the same set-up effort pays off dozens of times a week instead of once a year, and mistakes surface almost immediately instead of surfacing only during a real disaster.
```

---

## Evaluating and Choosing the Right AI Tool for Your Work Problem

## Part 2 - Why Most Tool Choices Go Wrong

### Selection by momentum

When a tool becomes popular, its popularity starts to feel like proof. But popularity only measures how many people adopted something — not whether it suits your task, your data rules, or your budget. A colleague's recommendation carries the same trap: it reflects the problem *they* solved, with *their* data and *their* skill, which may look nothing like yours. And a vendor demo is engineered to show the tool at its best on an example the vendor chose.

The cost of a mismatched tool is rarely just the subscription fee. It is the hours spent forcing an awkward fit, the rework when outputs miss the mark, and the slow erosion of trust when the tool disappoints on something important. Choosing well is cheaper than choosing fast.

```text
+ADD
This has played out publicly. Commonwealth Bank of Australia (CBA), the country's largest bank, replaced its roughly 45-person call centre team with AI voicebots, aiming to handle around 2,000 calls a week. The tool could not actually manage the volume and nature of the calls, and within about a month the bank had to apologise, rehire the staff it had let go, and lean on managers and overtime to cover the gap. The tool itself was capable technology — the mismatch was between what it was popular and promising for, and what the bank's actual call volume and complexity demanded.
```

---

## Part 3 - The Four Evaluation Questions

### A framework you can carry

A good evaluation is not a vague feeling about a tool; it is a short, repeatable interrogation. Four questions cover most of what matters, and you can ask them of any AI tool in a few minutes:

1. **Problem** — What specific problem does this tool solve, and is that a problem I actually have? Name the job before the tool.
2. **Fit** — How well does the tool's capability match the nature of my task? Open-ended drafting and precise extraction are different jobs that reward different tools.
3. **Risk** — What are the privacy and data risks? Where does my input go, who can see or keep it, and is that acceptable for this data?
4. **Value** — What does it cost in time and money relative to the value it delivers on work I will actually repeat?

Ask them in order. The first question often ends the evaluation early: if a tool does not solve a problem you genuinely have, the other three never need answering.

```text
+ADD
Worked example: an HR coordinator is considering an AI tool that promises to "screen resumes automatically" for a role that gets 300 applications.

1. **Problem** — The actual bottleneck is that she spends hours manually checking each resume against three hard requirements (a certification, minimum years of experience, and work authorization) before passing candidates to the hiring manager. That is a real, specific problem, so she continues.
2. **Fit** — The tool's capability is precise extraction and rule-matching against defined criteria, not open-ended judgment about who is the "best" candidate. Her task — checking three explicit requirements — matches that capability well, so it passes this question too.
3. **Risk** — Candidate resumes contain personal data. She checks where the tool stores uploaded resumes, whether it trains on customer data by default, and whether the vendor's terms meet her company's data-handling policy. She finds the vendor allows disabling training on her data and stores files in a compliant region, so the risk is acceptable.
4. **Value** — The tool costs a monthly fee well below the hours it would save her each week screening 300 resumes for a requirement she checks every hiring cycle, not just once.

Because all four questions check out, she moves ahead — but only for the narrow screening step, not for final candidate selection, which stays a human judgment call.
```
