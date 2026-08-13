=================
ASSOCIATE LEVEL


=========================
=========================

#########################
NEW SECTION: What is AI
#########################

# understanding AI 

## What is AI, really?

Imagine you have a record of how much rain fell every day for the last ten years in your city. With enough of that data, you could probably guess whether tomorrow is likely to be rainy or dry, just from the patterns: the time of year, the recent weather, what usually follows a storm. Artificial intelligence (AI) is software that does this kind of guessing, but at a much larger scale and faster than a person could.

More precisely, AI is software that learns from data (examples of what has happened before) and uses what it learned to make predictions or produce something new. The data can be anything: numbers like rainfall amounts, text like emails, or images like x-rays. Often, the relationships between these data points are far too complex for a person to work out by hand — that complexity is exactly why we turn to AI to find them.

The idea is always the same: study many past examples, find the patterns, and use them to handle a new situation.

Once AI has learned those patterns, we put them to work in three ways.

----

## Pattern recognition

A customer service team might get hundreds of complaints a week. People describe the same problem in different words: "package never arrived," "shipping was late," "item still hasn't come." Reading all of them to see what is going wrong this month would take hours.

Pattern recognition is when AI does that grouping for you. Give it many examples (complaints, emails, survey responses) and it sorts them into themes based on what they mean, even when the wording is different. For the complaints above, it might report a single main theme: "late or missing deliveries."

The AI is only spotting what comes up often, not explaining why it happens. You still read the results and decide what they mean and what to do next. In practice, that might mean checking whether "late or missing deliveries" traces back to one carrier, one region, or one time of year before you decide whether to switch vendors or investigate a specific route.

---

## Prediction

Once patterns are visible, the next question is often "what is likely to happen next?" A finance team can look at thousands of past invoices — noting details like invoice size, each customer's payment history, and how many days overdue their past invoices went before being paid — and use that history to score this month's invoices for risk of late payment, so collections effort goes where it matters first.

That scoring is prediction. AI learns from past examples that include outcomes (paid vs late, churned vs stayed), then applies those patterns to a new case and produces a likelihood: a score, a ranking, or a category like "high risk." Either way it is a best guess based on similar past cases, not a guarantee.

---

## Assistance

Assistance is when AI produces a draft for you. You give it a request and some context, and it writes something back. For example, you hand it three bullet points and it returns a clean email, or you paste a long report and it gives you a one-paragraph summary.

The writing usually sounds fluent and professional. But the AI is producing what looks like a likely answer, not checking whether it is true for your situation, so it can be confidently wrong. Treat the draft as a starting point you review and fix, not a finished product.

A practical example is legal or compliance reporting. These reports are often extremely long and time-consuming to produce, and AI can drastically cut down the time it takes to write them. This does raise some data privacy concerns, though — uploading confidential information to an external organization's systems is a real issue, and we'll come back to that later.

---

## Putting AI's three jobs to work

Pattern recognition, prediction, and assistance are useful, but outcomes depend on how you use them. Three principles keep showing up: judge outputs by what they do, keep accountability with the human, and provide the context the tool needs.

- **Judge by behavior.** Ask what you would ask of any draft or analysis: do the themes match the underlying examples, do the prediction's drivers make sense now, does the draft include the right constraints?
- **Keep accountability with the human.** AI produces options, summaries, and first drafts; it does not own the decision. Ask for options rather than verdicts, then write the final call in language you could defend to a stakeholder.
- **Provide context.** Without your objective, audience, and constraints, the tool still produces a confident answer, just for a different situation than yours. Say what you want, who will read it, what to include, and what to avoid.

| AI job | What you give it | What you get back | What you still do |
| --- | --- | --- | --- |
| Pattern recognition | Many examples of text | Themes and clusters | Spot-check and interpret |
| Prediction | Past cases with outcomes | A risk score or ranking | Validate drivers and context |
| Assistance | A prompt plus context | Draft text or a summary | Verify facts and adjust judgment |

### Seeing the three jobs work together

These three jobs often show up together within a single function. Take a talent-acquisition team trying to reduce early attrition: pattern recognition might group hundreds of exit-interview comments into a handful of recurring themes, such as "unclear growth path." Prediction might then score current employees by how closely their situation resembles those who left, flagging a shortlist at elevated risk. Assistance might draft a first version of a check-in email for managers to send to the people on that list. Three different jobs, one connected problem — and at every step, a person is still deciding what the themes mean, whether the risk score is trustworthy, and whether the email is right for each individual.

=====

# Lesson 2: AI vs Machine Learning vs Data Science

---
**Associate · AI fundamentals**

### What you'll learn

After this lesson, you will be able to listen to a work conversation or read an article that uses "AI," "Machine Learning," and "Data Science," correctly identify what work is actually being described, and ask one clarifying question that reduces confusion and improves decision-making.

### Why this matters at work

Each concept opens with a concrete workplace situation before the term is named. You will start with **AI** as the big umbrella goal, then place **Machine Learning** (learning from past examples), then **Data Science** (turning data into decision-ready insight), and finally practice recognizing which term fits common workplace situations.

:::info How to use this lesson
Read each part, complete the activity, then click **Continue**. On the last part, use **Next** to finish the lesson.
:::

### The four ideas in this lesson

1. **AI is the broader field** — the umbrella goal
2. **Machine Learning** — systems that learn patterns from data
3. **Data Science** — extracting insight from data for decisions
4. **Putting the three terms to work** — telling them apart in real conversations

----

Imagine a director in three meetings the same week. One team wants "AI for customer support." Another wants "AI to predict churn." A third wants "AI to understand why retention is dropping." Same word — three very different kinds of work.

**Artificial intelligence (AI)** is the broad category for systems that perform tasks that normally require human intelligence: understanding language, recognizing patterns, making recommendations, or generating content. The label **AI** tells you *what the system is trying to do*. It does **not** tell you how it works, what data it needs, or how reliable it will be.

That gap is where teams get into trouble. A chatbot, a recommendation engine, and a churn predictor can all be called AI, but they have different inputs, risks, and success metrics. Treating them as one generic "AI project" usually leads to the wrong timeline, the wrong team, and the wrong success metrics.

:::info When someone says "AI"
Ask: **What exactly is the system supposed to do?** Predict something? Generate a draft? Sort tickets? Analyze patterns? Once that is clear, you can see whether ML, data science, or something else is really involved.
:::

----
:::warning Common mistakes
- **Myth:** AI is one technology that always works the same way.
  **Reality:** AI is a broad category; reliability and requirements vary widely.

- **When not to lean on "AI":** High-stakes decisions that need clear human accountability (hiring, discipline, sensitive eligibility) unless there is a defined human-led process.
:::

:::info Connects to the rest of this lesson
AI is the **goal**. **Machine Learning** is one common way systems learn patterns to support AI behavior. **Data Science** is how teams understand data before building or trusting those systems.
:::

**Reflect:** Where in your organization do people use "AI" as a shortcut — and what important details get lost?

----

## Machine Learning enables systems to learn from data

AI names the destination — a system that behaves intelligently. Machine Learning is one of the most common routes there: teaching a system to learn patterns from examples instead of writing rules by hand.

Picture a bank with ten years of loan applications: approved, declined, paid on time, defaulted. The team wants a **risk score** for new applications without writing hundreds of rules by hand — rules that go stale as lending patterns shift.

**Machine Learning (ML)** builds systems that improve by learning patterns from **examples**, not from hand-written rules. The system studies past data with known outcomes, adjusts to match those examples, then produces a **best guess** on new cases — usually a score, likelihood, or category, not a guaranteed answer.

ML can scale repeating decisions (routing, prioritizing, forecasting, flagging). It also has limits: it is only as good as the patterns in its training data. When markets or products change, a model can keep producing confident outputs that no longer match reality.

:::info ML vs AI
**ML is not the same as AI.** ML is one common *method* inside AI solutions. The business goal (AI) can be broader than the learning method (ML). In the loan example above, the ML model is the scoring engine itself; the bank's broader "AI initiative" might also include the software that shows loan officers the score and lets them override it — that surrounding system is AI, even though the scoring underneath is ML.
:::

### Workplace scenario

**High-stakes interaction**

A branch manager prepares for a meeting after a rise in defaults. Central teams propose an "ML risk model" to tighten approvals. The manager must explain declines to customers. If the model was trained mainly on data from before a regional downturn, for instance, it may start flagging long-standing, reliable customers as high risk simply because their current numbers resemble those of applicants who defaulted years earlier. Understanding that ML **learns from past patterns** and outputs a **probability-style guess** helps the manager ask: what data was it trained on? how often is it updated? what human review is required before a customer-facing decision?

---

### How professionals use this

- **Scale repeating judgments** — triage, prioritization, routing — when past examples exist and conditions are relatively stable.
- **Support forecasting** — demand, churn risk, fraud flags — with explicit monitoring when the world changes.
- **Pair with governance** — define who can override the model and when.

:::warning Pitfalls
- Treating ML output as **truth** instead of a **pattern-based guess**.
- Using ML where decisions must be **fully explainable** to regulators or the public, without a strong interpretability and oversight plan (for example, declining a loan application without being able to explain the specific factors behind the decision).
:::

:::info Connects forward
ML often needs **clean, well-defined data** — work that frequently starts as **Data Science** (next section).
:::

**Reflect:** Think of a repeating decision in your work. What would need to be true about your past data for ML to be trustworthy?

---

## Data Science extracts insight from data

Picture a retail category manager: profits are dropping even though sales volume looks steady. Dashboards disagree. Suppliers say prices are stable. Store teams report more out-of-stocks. Nobody can explain why.

An analyst pulls inventory, promotion, supplier cost, and return data into one place. Product codes do not match across systems — the first job is **cleaning** so numbers can be compared honestly. Then they look for what changed: a recent promotion drove higher returns and stockouts in the highest-margin sizes. Volume looked fine; **profit quietly eroded**. The insight reshapes the next promotion plan — and stops the team from blaming sales staff or switching suppliers based on incomplete dashboards.

**Data Science** is the work of collecting the right data, cleaning it, finding patterns, and presenting conclusions decision-makers can act on — with clear assumptions about what the data can and cannot tell you.

:::info Data science vs reporting
Reporting summarizes **what happened**. Data science explains **patterns**, tests plausible explanations, and guides decisions with stated limitations.
:::

----

### A simple investigation flow

1. **Define the question** — "Why did margin drop if volume is flat?"
2. **Gather and align data** — fix definitions and product codes.
3. **Explore and test explanations** — promotions, returns, stockouts.
4. **Recommend action** — change the plan with evidence, not anecdotes.

:::warning When analysis is not the first move
Do not substitute data science for **urgent operational fixes** when the issue is obvious and time-critical (outage, safety, compliance breach). Contain first; analyze when stable.
:::

:::info Connects to ML and AI
Data science often **feeds** ML with clean, labeled data — and many "AI projects" fail because that groundwork gets skipped. Recall the loan risk model from the previous section: it is only as trustworthy as the historical loan records behind it. If those records use inconsistent definitions or don't match across systems, the model quietly learns the wrong patterns, and nobody notices until it starts producing bad scores.
:::

**Reflect:** In your last data-driven decision, what definition or data-quality disagreement slowed you down?

----

A program manager must draft a one-page "AI initiative" proposal by Friday. Stakeholders disagree:

- One leader imagines a **chatbot** (customer questions).
- Another wants a **churn predictor** next quarter.
- A third wants to know **why churn has been rising** for six months.

All three say "AI." All three ask for **different work**.

### Listen for the main output

| If the deliverable is… | The term is usually… |
|------------------------|----------------------|
| A system that behaves intelligently — drafts, routes, recommends | **AI** (capability) |
| A score or prediction learned from past examples | **Machine Learning** |
| An explanation, trend, or decision-ready insight from data | **Data Science** |

The label drives **resourcing**: ML needs training data and monitoring; data science needs metric definitions and access; AI implementations need workflow and accountability decisions.

:::info One question that saves meetings
**"What will the deliverable look like, and who will use it to make what decision?"**
:::

### Structuring the proposal

| Option | Label | Deliverable | Decision it supports |
|--------|-------|-------------|----------------------|
| A | AI assistant | Chat/workflow experience | Faster, consistent support handling |
| B | ML prediction | Churn risk scores | Prioritize retention outreach |
| C | Data science | Investigation report | Fix root causes of rising churn |

----
:::warning Pitfalls
- Assuming every "AI" tool includes ML and full automation — many are mainly **interfaces and workflows**; the real gap may be data quality or change management.
- Correcting terminology in the meeting when the team is already aligned on deliverable, decision, and risk — **speed beats labels** in that case.
:::

**Reflect:** Think of a recent "we need AI" moment at work. Do you now suspect they needed an AI capability, an ML prediction, or a data science insight? What question would you ask to confirm?

---
=========

# Benefits and Trade-offs of Using AI

----
## AI as an Accelerator, Not a Replacement

Imagine receiving a request at 4 PM for a report that normally takes half a day to prepare. A few years ago, you might have spent hours organizing notes, identifying key points, and drafting recommendations from scratch. Today, AI can help generate a first draft in minutes.

This speed is why AI has become a valuable workplace tool. It can help professionals organize information, generate ideas, summarize large amounts of content, and create structured drafts much faster than manual methods.

However, there is an important trade-off. AI can accelerate work, but it cannot take responsibility for decisions. The more useful and polished AI becomes, the easier it is to forget that someone still needs to evaluate whether the output is accurate, appropriate, and relevant to the situation.

AI can help you move faster, but you remain accountable for what you decide, share, approve, or implement.

----

## Productivity Means More Options, Not Just Speed

One of the biggest benefits of AI is productivity. Productivity gains occur when a tool helps you reach a useful outcome more efficiently.

Many people assume productivity means doing the same work in less time. While that is partly true, AI often creates value in a different way: it allows professionals to explore more possibilities before making a decision.

Instead of spending thirty minutes creating a single outline, you can generate three different approaches and compare them. Instead of staring at a blank page, you can begin with a structured draft and spend your energy improving it.

The result is not simply faster work. It is often better-informed work because more alternatives can be considered before committing to a course of action.

----

## Reducing Manual Effort — and What Goes With It

Not every valuable activity at work requires deep thinking. Many tasks involve organizing information, formatting documents, identifying themes, or converting raw notes into a structured format.

These activities are important, but they can consume significant time and attention.

AI is particularly effective at reducing manual effort. It can summarize meeting notes, organize survey responses, extract action items, and transform messy information into more usable formats.

This allows professionals to spend more energy on activities that require judgment, context, creativity, and relationship management.

Yet reduced effort creates another trade-off. When manual steps disappear, some natural quality checks disappear with them. The process may become faster, but opportunities to notice inconsistencies or missing information can also be reduced.

----

## How Over-Reliance Creeps In

Over-reliance does not usually happen because someone deliberately decides to stop thinking.

Instead, it often develops gradually.

A person uses AI once and receives a useful answer. The next time, they trust it a little more. Under pressure, they stop checking certain details. Eventually, the tool begins shaping decisions that should still be guided by human judgment.

This becomes especially dangerous when AI produces confident, polished language. A well-written response can feel trustworthy even when important facts, assumptions, or context are missing.

The core problem is accountability. If an AI-generated recommendation creates problems, responsibility does not belong to the tool. It belongs to the person who acted on it.

-----

## The Fix Is Verification, Not Avoidance

The solution to over-reliance is not avoiding AI.

The solution is verification.

Verification means treating AI output as a strong draft rather than a final answer. It is the habit of pausing before acting and asking whether important facts, assumptions, and recommendations have been checked.

Think of AI as a very fast junior colleague. You may appreciate the speed and effort, but you would still review important work before presenting it to others.

Verification protects credibility because it ensures that the final decision reflects both AI assistance and professional judgment.

---
Steps
1.
Review key facts

Are important details accurate?
2.
Check assumptions

Does the output rely on assumptions that may not apply?
3.
Confirm organizational fit

Does the recommendation align with policies and priorities?
4.
Consider consequences

What happens if this recommendation is wrong?

----

AI offers substantial benefits in modern workplaces. It can help professionals generate ideas faster, reduce repetitive effort, and explore multiple options before making decisions.

At the same time, convenience creates risk. The easier AI becomes to use, the easier it becomes to rely on it too heavily.

Successful professionals recognize both sides of this trade-off. They use AI to accelerate their work while maintaining ownership of decisions and outcomes.

The most valuable habit you can develop is a simple verification checkpoint: before acting on AI output, decide what should be accepted, what should be changed, and what should be independently verified.

This approach preserves the speed of AI without surrendering professional judgment.

----


=========================
=========================

#########################
NEW SECTION: PRompting fundamentals
#########################

# Writing Clear and Simple Prompts

Many people assume AI will automatically understand what they want. They type a short request, receive a generic answer, and then spend time rewriting the prompt or editing the response.

The difference between a weak prompt and a strong prompt is usually clarity. Effective prompts tell the AI:

- What outcome you need
- What context matters
- What boundaries it should follow
- What format the answer should take

A simple structure can turn vague requests into useful, work-ready outputs.

----

The first thing AI needs to know is what you are trying to achieve.

Compare these prompts:

"Help me prioritize my work."

"Recommend a priority order for these tasks and provide a short explanation I can share with stakeholders."

The second prompt gives the AI a clear destination. Instead of guessing what "help" means, it knows exactly what outcome to produce.

-----

**Weak Goal**
"Help me with this project."

**Better Goal**
"Create a project plan for the next two weeks."

**Strong Goal**
"Create a two-week project plan with priorities, deadlines, and risks."

---

Once the goal is clear, provide the information that shapes the answer.

Context helps AI understand your situation instead of relying on assumptions. Useful context might include:

- Who the audience is
- What has already happened
- Existing constraints
- Important background information

The key is relevance. Include details that change the answer, not every detail you know.

----

AI often tries to be helpful by filling in missing information. Sometimes that can lead to assumptions, speculation, or unnecessary detail.

Boundaries act as guardrails. They tell the AI what it should avoid and how far it should go.

Examples include:

- Do not make assumptions
- Use only the provided information
- Ask questions if information is missing
- Keep the response under 200 words
- Avoid legal or medical advice

Good boundaries often make responses more reliable and easier to use.

---

A reliable prompt usually follows the same sequence:

1. State the goal.
2. Provide context.
3. Set boundaries.
4. Request an output format.

Following this order makes prompts easier to write and easier for AI to understand.

Here's the sequence applied to one real request — a manager preparing a note for their team:

----
Steps
1.
Define the Goal

State what outcome you need.
Example: "Write an update for my team about the vendor delay."
2.
Add Context

Provide relevant facts and constraints.
Example: "The delay is two weeks, caused by a shipping issue, and the team already knows the vendor's name."
3.
Set Boundaries

Explain what should and should not happen.
Example: "Don't speculate about who's at fault. Keep it factual and reassuring."
4.
Request the Output

Specify the format you want.
Example: "Keep it under 150 words, as a short email."

Put together, that becomes: "Write a short email update for my team about a two-week vendor delay caused by a shipping issue. Don't speculate about fault — keep it factual and reassuring. Keep it under 150 words."

----

Consider this prompt:

"Help me run a meeting."

Now compare it with:

"Create a 30-minute project kickoff meeting agenda [Goal] for a team of six people, starting next week [Context]. Don't include icebreakers or background context the team already knows — focus only on assigning responsibilities [Boundaries]. Present it as a checklist under one page [Format]."

The second prompt gives the AI a clear goal, relevant context, explicit boundaries, and a usable output format — the same four-part sequence from above, applied to a different situation. As a result, the response is far more likely to be useful on the first try.

----

Whenever you write a prompt, remember these four questions:

- What outcome do I need?
- What information does the AI need to know?
- What limits or guardrails should it follow?
- What format would be most useful?

Look back at the meeting-agenda prompt above: it answers all four of these in a single sentence. That's the target — not a longer prompt, but one where nothing important is left for the AI to guess. Using this simple framework consistently will help you create prompts that produce clearer, more practical, and more dependable results.

=====

# Common Prompting Mistakes

### When a Reasonable Request Still Disappoints

You type a request that feels perfectly clear, press enter, and the response comes back generic, off-target, or missing the point. It is tempting to decide the tool simply is not very good.

More often, the prompt gave the AI less to work with than you thought. A request that makes complete sense in your head can still leave out the very things the tool needs to get it right.

Almost all weak results trace back to a small number of common, fixable habits. This lesson walks through four of them. The aim is not to point out that you have been doing it wrong, but to help you recognise your own habits and see the small adjustments that make a surprising difference.

----
### Instructions Too General to Act On

A vague prompt is one that reads clearly to you, because you already hold all the background in your head, but gives the AI nothing specific to aim at.

Imagine typing: "Write something about our new project for the team." At a glance this looks like a reasonable request. Look closer and almost every word is open: "something" could be an announcement, a summary, or a status update; "our new project" means nothing to a tool that has never heard of it; and "for the team" gives no sense of what they actually need to know.

The fix is rarely to write more. It is to name three things: what you want produced, what it is about, and why it is needed. "Write a short announcement introducing the new records-digitisation project to our field staff, so they know it starts next month" points the tool at a real target.

---
### Leaving Out Context, Audience, and Format

Sometimes the instruction is specific enough, yet the result still feels flat. Usually that is because the prompt left out the details that shape a good answer. Three matter most.

**Context** is the background the tool needs: what changed, why, and any facts it cannot know on its own. **Audience** is who will read the result, which sets the tone and the level of detail. **Format** is the shape you want back: length, structure, and style.

Consider: "Draft an email announcing the policy change." As an instruction it is clear, but the tool has no idea what the policy actually changes, who receives the email, or how long and formal it should be. Add those three details and the same request produces something you could almost send as-is.

----
### Too Many Asks in One Prompt

When several things need doing, it feels efficient to ask for them all at once. But a single prompt crammed with instructions often produces a response that does each part shallowly, blends them together, or quietly drops some of them.

A request like this looks productive: "Summarise this report, translate the summary into Urdu, turn it into a slide outline, write talking points for each slide, and suggest three questions the audience might ask, all under 200 words." That is at least five separate jobs competing for attention in one breath.

The tool handles a chain of focused requests far better than one overloaded one. Ask for the first thing, check it, then build on it. Working step by step also lets you catch a problem early, before it flows into everything that follows.

---
### Asking for What AI Cannot Reliably Do

Some prompts are clear, detailed, and focused, and still fail, because they ask for something outside what the tool can actually do. AI generates language by predicting patterns; it does not have live access to your systems, it cannot see confidential information, and it cannot promise how the future will turn out.

Each of these looks reasonable at first: "How many people used our service last week?" expects live data the tool cannot see; "Guarantee this contract is legally watertight" asks for a promise it cannot responsibly make; "Tell me exactly how many customers we will win next quarter" demands a precise prediction no one can give.

The fix is to match the request to the tool's real strengths. Use AI to draft, structure, rephrase, and think through options, and verify anything factual, current, or high-stakes yourself before you rely on it.

---
### Recognising the Four Mistakes in the Wild

Now that you can name the four mistakes, the useful skill is spotting them in prompts that look fine at a glance. Reading a request with these four in mind is exactly the habit that lets you catch your own before you press enter.

A quick reminder of the difference between the first two, since they are easy to confuse: a **vague** prompt leaves you unsure what the tool is even meant to produce, while a prompt with **missing details** names a clear deliverable but leaves out the specifics that would make it good.

Sort each request below by the single mistake it shows most clearly.

----
Buckets (categories)
Vague instructions
Missing details
Overly complex request
Unrealistic expectation

Items (assign each to its correct bucket)
Fix this document. → Vague instructions
Draft the announcement about the office move. → Missing details
Research the topic, write the report, build the slides, and prepare my answers, all at once. → Overly complex request
Tell me the exact resale value my car will have in five years. → Unrealistic expectation
Pull today's live figures straight from our internal dashboard. → Unrealistic expectation

----
### A Few Words Are Usually All It Takes

The reassuring part is that fixing these mistakes almost never means writing a longer or more technical prompt. It usually means adding a few words that were missing, or splitting one request into two.

The most reliable habit is a quick check before you send. It takes a few seconds and catches most weak prompts before they cost you a round of disappointing output.

----
Steps
1.
Name the deliverable

Is it clear what you want the tool to produce, and what it is about?
2.
Add the essentials

Have you given the context, the audience, and the format you need?
3.
Do one thing at a time

Is this a single, focused ask rather than five jobs in one?
4.
Check it is answerable

Is this something AI can actually do well, or should you verify it yourself?

----
### Judge the Prompts

Use what you have learned to judge the prompts below and choose the adjustment that would help most.

[some MCQS etc are here]

---

Most disappointing AI results come not from a weak tool but from a handful of common, fixable habits in how we ask.

Vague instructions are too general to act on; missing details leave out the context, audience, and format that shape a good answer; overly complex requests cram too many jobs into one prompt; and unrealistic expectations ask for things the tool cannot reliably do.

The habit that guards against all four is a quick check before you send: name the deliverable, add the essentials, keep it to one focused ask, and make sure it is something AI can actually do well.

None of these fixes takes long. Often a few added words are the difference between output you rewrite from scratch and output you can build on. The next time a prompt disappoints you, you will be able to look at what you wrote, name exactly what is weak, and know what to change.

=====

# Prompting vs Searching

You already know how to write a decent prompt. The next skill is knowing **when to bother** — should you ask an AI tool, or should you search?

Pick wrong and you pay for it: you polish an AI draft that can't be cited in an audit, or you burn twenty minutes searching for something an AI could have drafted in one pass.

:::info What this lesson gives you
- What AI is genuinely better at
- What search is genuinely better at
- A quick way to classify any question
- A repeatable habit so you stop guessing under pressure
:::

---

## AI is a synthesis engine, not a lookup engine

An AI model doesn't fetch a web page — it generates a response by predicting likely text based on patterns it learned, shaped by your instructions. That makes it strong when the job is **thinking support**: summarizing messy inputs, comparing options, drafting, restructuring.

:::info Analogy
Think of AI as a capable colleague in the next seat. They can't cite a source for every line, but hand them your notes and your goal and they'll turn it into a clear brief fast.
:::

**Use AI first when you need to:**
- Turn constraints into options or scenarios
- Draft something from your own messy notes
- Compare tradeoffs across a structured format
- Get a first pass, then critique it yourself

:::warning Watch for this
Confident and well-structured is not the same as accurate. Verify any specific numbers, dates, or policy claims with search before you rely on them.
:::

---

## Search is built for traceability

Search engines index existing documents and rank them by relevance. Your goal isn't to generate new text — it's to find the right document and confirm what it actually says.

:::info Analogy
Asking a colleague to guess what a rule 'probably means' versus opening the official handbook and reading the exact paragraph you're accountable to.
:::

**Use search first when you need:**
- An exact policy, price, or legal requirement
- A quote or clause you can defend if challenged
- The current, correctly-versioned answer
- Something with an owner and a date attached

:::warning Watch for this
Stopping at the first result without checking the version, owner, or date is how teams end up following outdated guidance.
:::

----

Narrow before you trust it

Use exact phrases, domain filters, and date filters so you land on the right *version* of a document, not just the right topic.

Capture provenance as you go

Save the quote, the link, the owner, and the last-updated date. When someone asks 'where did that come from,' you answer instantly.

Let AI translate, not invent

Once you have the authoritative source, AI can rewrite it in plain language for your audience — but keep the original wording on hand for reference.

The misconception to drop

Search isn't just for 'basic' questions. It's often the senior-professional move, because it produces evidence you can stand behind when stakes are high.

----
## Diagnose before you choose

Before opening either tool, classify the question:

| Type | What you need | Start with |
|---|---|---|
| A | An authoritative fact or source | Search |
| B | To transform/structure your own materials | AI |
| C | Both | Two-step: draft, then verify (or vice versa) |

Many real questions are mixed — cluster themes from messy comments with AI, then confirm the competitor detail with search. Keep **what you can cite** and **what you're deciding** as two separate things in your notes, so a hypothesis never gets mistaken for a verified fact.

Sort each item below into where it belongs.

---
Buckets (categories)
Search first (need a citable source)
AI first (need synthesis of your own material)

Items (assign each to its correct bucket)
Confirming the exact effective date of a new expense policy → Search first
Turning call transcripts and survey comments into churn hypotheses → AI first
Finding a competitor's current published pricing page → Search first
Drafting a first-pass options table from your own constraints spreadsheet → AI first
Verifying whether an expense category is allowable under internal policy → Search first
Rewriting a verified policy clause into plain language for frontline staff → AI first

---
## Build the instinct, not the memory

A good habit removes decision friction so you're not 'thinking about thinking' when you're already under deadline pressure.

:::info Analogy
A pilot's pre-flight checklist. Experienced pilots still use it — it prevents predictable mistakes when things are busy.
:::

Walk through the four-step routine below in order.

----
Steps
1.
1. Diagnose

Ask: what's the deliverable? Do I need a citable source? Do I need to transform my own materials? What's the risk if I'm wrong?
2.
2. Act

Based on the diagnosis, go search-first, AI-first, or two-step. Use a standard prompt template so you're not starting from a blank page.
3.
3. Verify

Flag anything that sounds like a fact — numbers, dates, policy language — and confirm it before it goes in front of stakeholders.
4.
4. Quality gate

Before sending: What's a fact and where's the source? What's my recommendation and why? What would a skeptical stakeholder challenge?


=========================
=========================

#########################
NEW SECTION: limitations ethics and prviacy
#########################

# Why AI Can Be Wrong

### Confidence worth deepening

You have already learned to work with AI tools and to write prompts that get useful results. This lesson is designed to sharpen that skill, not shake it.

Here is the idea worth holding onto: the professionals who get the most from AI are not the ones who trust it blindly, and not the ones who avoid it. They are the ones who understand *why* it sometimes gets things wrong. Knowing where errors come from lets you catch them early and act with confidence.

AI does not fail at random. Most wrong answers trace back to a few predictable causes. In this lesson you will look closely at three of the most common:

- Information that is **out of date**
- **Assumptions** the tool made because your prompt left something out
- Conclusions built on **missing or incomplete data**

By the end, you will have a short mental checklist you can run before you rely on anything an AI tells you.

----
### When the world has moved on

Imagine you ask an AI assistant to summarise the rules for claiming a particular business expense. It gives you a clear, confident answer in seconds. It reads well and sounds authoritative. And it is wrong, because the regulation changed last year and the version the tool learned from is the old one.

This is one of the most common reasons AI outputs can be wrong: **outdated information**. An AI model learns from a large collection of text gathered up to a certain point in time. Anything that changed after that point, such as a new law, an updated policy, a revised price, or a staff change, may simply not be part of what it knows.

The tricky part is that the tool rarely warns you. It does not say 'this might be out of date.' It answers with the same confidence whether the information is current or five years stale.

### Key idea

The more a topic changes over time, whether rules, prices, people, or technology, the more important it is to check the AI's answer against a current, trusted source before you act on it.

----
What it looks like

A confident, well-written answer that quietly relies on an old rule, price, or fact, usually about something that has changed recently.

Why it happens

The model learned from information gathered up to a fixed point in time. Events after that point may be missing, so it answers using the version of the world it was trained on.

Where it bites hardest

Fast-moving topics: regulations, tax and compliance rules, prices, product features, and anything about specific people or their current roles.

How to catch it

Ask yourself when this last changed, and confirm anything time-sensitive against an up-to-date official source before you rely on it.

---
### Filling in the blanks

Ask an AI tool to 'write a short update for the team about the project delay,' and it will happily produce one. But to do that, it had to guess a great deal: which project, how long the delay is, what caused it, how formal the tone should be, and what the reader already knows.

When your prompt leaves something out, the tool does not stop and ask. It fills the gap with an assumption, usually the most common or generic one, and then writes as if that assumption were a fact. This is the second common cause of wrong output: **incorrect assumptions**.

The result can look completely finished and still miss your actual situation. The tone might be wrong for your audience. It might invent a reason for the delay that is not true. It answers the question it assumed you asked, not the one you meant.

### Key idea

Missing context does not produce a blank or a follow-up question. It produces a confident guess. The more context you give, the fewer guesses the tool has to make.

----
### A confident answer from half the picture

Suppose you paste last quarter's sales figures into an AI tool and ask which region is performing best. It names one, with a tidy explanation. What it does not tell you is that two regions were missing from the data you pasted, and one of those was the real top performer.

This is the third common cause: **missing or incomplete data**. When an AI tool has only part of the picture, it does not leave a gap in its answer. It draws a conclusion from whatever it was given and presents it just as confidently as if it had everything.

The danger here is not a strange or obviously broken answer. It is a reasonable, well-argued conclusion that happens to be built on an incomplete foundation. Because the reasoning looks sound, it is easy to accept without asking the most important question: *was anything left out?*

### Key idea

An AI tool answers based on what it can see. If the inputs are incomplete, the conclusion can be confidently, convincingly wrong.

----
Steps
1.
Partial input

You give the tool some of the information: a few files, one quarter, the data that was easy to gather.
2.
No flag for the gap

The tool does not know what it was not given, so it never warns you that anything is missing.
3.
A tidy conclusion

It reasons over what it has and produces a clear, confident answer that looks complete.
4.
Acted on as fact

Because the answer reads well, it gets shared and used, and the missing piece only surfaces later, if at all.

-----
### Naming the cause

Once you know the three common causes, you can usually spot which one is at work, and that matters, because the fix is different each time. Outdated information calls for checking against a current source. An incorrect assumption calls for adding context to your prompt. Missing data calls for confirming that the inputs are complete.

Read each situation below and sort it into the cause most likely behind it.

----
### From knowing to doing

Understanding the causes helps only if it changes what you do before you act. You do not need a long process. A quick, repeatable habit catches most errors, and it takes far less time than fixing a mistake after it has spread.

Put the four steps of that habit in the order that makes them work.

-----
You do not need to remember everything in this lesson. You need three questions, ready to ask before you rely on any AI answer.

### Before you act, ask

- **Could this be out of date?** If the topic is a rule, a price, a product, or a person's role, confirm it against a current, trusted source.
- **What did it have to assume?** If your prompt left out context, the tool guessed. Check that its guess matches your real situation, or add the missing context and ask again.
- **Was anything left out?** If the answer rests on data you provided, make sure that data was complete before you trust the conclusion.

Notice what this checklist is not. It is not a reason to distrust every answer or to stop using AI. It is the opposite. It is what lets you move quickly *and* confidently, because you know exactly where to look when something matters. Understanding why AI can be wrong is what makes you good at using it when it is right.

=====

# Understanding AI hallucinations

### When AI Sounds Sure but Isn't

The previous lesson looked at why AI can be wrong when it's working from outdated information, unstated assumptions, or incomplete data. This lesson looks at a related but different failure: hallucination, where the tool doesn't just misjudge from imperfect inputs — it invents information that was never there at all.

An AI hallucination is a confident, well-written answer that happens to be wrong. The tool does not signal any doubt. It does not flag the parts it invented. It produces the same fluent, professional language whether the information is accurate or completely made up.

This is what makes hallucinations the most dangerous failure mode for professionals. A spelling mistake is easy to catch. A hallucination is not, because the output looks correct. It reads like something a knowledgeable colleague would say, so it slips past a quick review.

In this lesson you will learn how hallucinations show up in everyday work, how to catch them, and what is at stake when one goes unnoticed.

---

### Confidence Is Not Accuracy

Ask an AI tool a factual question and it will almost always give you an answer. It rarely says "I am not sure." Instead, it fills the gap with the most plausible-sounding response it can produce, stated with the same certainty it uses for facts it has right.

Imagine asking which regulation governs a particular reporting deadline. The tool replies with a specific section number and a clean summary. It sounds authoritative. But the confidence in the wording tells you nothing about whether the answer is true. The tone of an AI response is not evidence.

Treat certainty in the output as a writing style, not a signal of correctness. A wrong answer and a right answer can look exactly the same.

-----

Invented statistics

A precise-looking number, such as "37% of firms," presented with no source you can actually trace.

Fake citations

A named report, law, or study that sounds authoritative but does not exist when you go looking for it.

Made-up policy references

A specific section or clause number that cannot be found anywhere in the actual document.

Misattributed quotes

Words confidently assigned to a person or organisation that never said them.

-----

### A Paragraph You Might Actually Approve

Suppose you're pulling together a quarterly update for your director. You've got scattered notes on a new workplace policy, so you ask an AI tool to turn them into a summary paragraph. It returns this line:

"The updated policy, introduced under Section 14(b), has already reduced processing delays by 42% across participating departments."

Read quickly, it is a strong sentence. It is specific, confidently worded, and would look convincing in the report you're about to send up the chain. But two parts of it were never verified. The section number may not exist. The 42% figure may have been generated to sound credible rather than measured from any real data.

Neither claim announces itself as invented. That is the whole problem. Before this line goes anywhere near your director, you'd want to know: does Section 14(b) actually exist, and where did 42% come from? The sentence that reads best is often the one that needs checking most.

---
### Three Habits That Catch Most Hallucinations

You do not need to distrust everything an AI tool produces. You need a few reliable habits for the moments that matter.

First, cross-check facts against a trusted source. If a claim will appear in something you send, sign, or present, confirm it in the original document, on a reliable website, or with a colleague who knows.

Second, be suspicious of overly specific claims that arrive with no citation. A precise statistic or a named regulation with nothing to trace it back to is a signal to slow down, not to speed up.

Third, verify anything you would be embarrassed to get wrong. If an error would damage your credibility, a client relationship, or a decision, the few minutes it takes to check are always worth it.

----
Steps
1.
Flag the claims

Mark every fact, number, name, and reference in the output.
2.
Ask for the source

For each flagged claim, can you point to where it actually comes from?
3.
Check the risky ones

Confirm anything specific, official, or consequential against a trusted source.
4.
Decide what to keep

Use what you verified; remove or rewrite what you could not confirm.

----
### Match the Effort to the Risk

Checking every word of every AI output would undo the time the tool saves you. The skill is knowing which claims earn a closer look and which are low-stakes.

Specific facts, figures, legal or policy references, and anything you will present as evidence belong in the verify-first group. Broad framing, general explanations, and rough drafts you plan to rewrite anyway carry far less risk if a detail is imperfect.

Sorting claims this way keeps you fast where speed is safe and careful where a mistake would cost you.

----
Buckets (categories)
Verify before using
Lower risk

Items (assign each to its correct bucket)
A specific statistic in a report → Verify before using
A cited law or policy section number → Verify before using
A named source or a direct quote → Verify before using
A brainstormed list of topic ideas → Lower risk
A rough first-draft outline you will rewrite → Lower risk
A general explanation of a familiar concept → Lower risk

----
### The Cost of Missing One

A hallucination that slips through does not stay small. It travels. A fabricated figure copied into a draft becomes a figure in a report, which becomes a claim in a meeting, which becomes the basis for a decision. By the time someone questions it, the error is several steps downstream and much harder to walk back.

The professional cost is real, and it lands on you rather than the tool. A client, a manager, or a regulator sees your name on the work. Decisions built on invented data can waste budget, break rules, or damage trust that took years to earn.

This is why detection is not optional. The output is fast, but the responsibility for it stays with you.

---
Sequencing — list items in the correct order (students see them shuffled)
1.
The AI invents a confident but false figure
2.
The figure is copied into a draft without checking
3.
The draft is shared and used to make a decision
4.
The error surfaces publicly and damages credibility

=====

# Bias and Fairness in AI

---

When professionals hear "bias in AI," many picture something distant: a research debate, a headline about a large technology company, a problem that affects millions of strangers but not the email, summary, or report they are working on this afternoon.

That assumption is comfortable, and it is mistaken. The same tools that help you draft, summarise, and decide can quietly carry bias into your ordinary, everyday work. It usually arrives looking perfectly reasonable — and unlike a hallucination, it isn't inventing a fact out of nowhere. It's often reporting a real pattern from real data; the pattern itself is just an old unfairness, not a neutral truth.

In this lesson you will see where that bias comes from, how it shows up in normal-looking outputs, and how to notice it before you rely on it.

---
### What Bias and Fairness Really Mean

When people imagine AI bias, they expect an obvious mistake. In practice it is usually quiet and systematic: a consistent tilt that favours some people or viewpoints over others without a good reason. Fairness is the opposite, where comparable people and perspectives are treated comparably, so no group is routinely advantaged or overlooked.

The useful thing to remember is that bias can live in two places: in the data a tool learned from, and in the outputs that tool produces. Naming these clearly makes the rest of the lesson easier to follow, because each one shows up differently in your work.

---
### Bias Starts in the Data

AI tools learn by finding patterns in large amounts of past information: documents, records, and decisions that people already made. If that history under-represents some groups, or carries old imbalances, the tool treats those imbalances as normal.

This part matters: the tool is not malfunctioning. It is faithfully copying the world it was shown, including the unfair parts. A few forms of this show up often in professional settings:

- **Historical decision records** — if past promotions or approvals mostly went to one kind of candidate, a tool trained on that record learns to expect and prefer the same outcome.
- **Unrepresentative samples** — customer or survey data skewed toward one region, age group, or language leaves the tool with a distorted picture of "typical."
- **Language patterns** — text data that reflects common stereotypes or assumptions can pass those same assumptions into summaries or drafts without anyone intending it.

That is data bias, and it rarely stays hidden in the data. It travels forward into the outputs you actually see.

### From Hidden Data to Visible Output

Decision bias is what happens when an imbalance in the data becomes visible in what the tool actually produces. It seldom announces itself. The output usually looks polished, confident, and reasonable, which is exactly why it is so easy to accept without a second thought.

For example, a writing tool might consistently sound natural and warm for one audience while coming across as flat or overly formal for another — the same underlying imbalance can take several recognisable shapes in everyday professional work. Once you have seen them, they become much harder to miss.

----
Tone that does not fit everyone

An AI writing tool produces communication in a tone that represents some groups well and others poorly, defaulting to language that suits one audience while subtly diminishing another.

Perspectives left out

A summarisation tool consistently drops certain viewpoints, condensing a long discussion but repeatedly omitting the objections, minority positions, or contributions of particular people.

History mistaken for merit

A hiring-support tool ranks or recommends candidates by how closely they resemble people hired before, rewarding familiarity rather than who is genuinely best suited to the role.

----
### Why This Matters for Your Work

When biased outputs go unquestioned, small tilts add up. An unfair tone slowly erodes trust and leaves some people feeling unseen. Missing perspectives lead to decisions based on an incomplete picture. Skewed recommendations quietly shape who gets noticed and who gets passed over.

The risk is highest wherever an AI output touches people, or a judgment about them, and it is lower where the task is mechanical. Learning to sense that difference is the first practical skill in working fairly with these tools.

----
### A Habit for Catching Bias Before You Use an Output

You do not need to audit an algorithm to work fairly. You need a short pause before you rely on an output, especially one that affects people or speaks for a group.

The goal is not to distrust every result, which would undo the time these tools save you. It is to build a simple habit of questioning the outputs that matter, so a hidden bias does not travel any further than your screen.

----
### Key Takeaways

Bias in AI is not a distant problem. It can enter your daily work through the very tools that make you faster.

It begins in data that carries past imbalances, and it surfaces in polished outputs: a tone that excludes, perspectives left out, or recommendations that reward history over merit. Wherever those outputs touch people, the impact is real.

Your job is not to fix the algorithm. It is to recognise when an output might be reflecting a bias and to question it before you use it. That short pause keeps the final judgment, and the fairness, with you.

=====

# Privacy, Confidentiality, and Professional Responsibility

### When the Tool Becomes Part of Your Job

Bias is one way AI's use of data can create risk for the people it affects. Privacy is a related but different risk — this time about what data you put into the tool in the first place.

When you use AI to draft an email or summarize a report, it can feel like a private, personal choice — just you and a helpful tool. But the moment that work involves your organization's information, your clients, or your colleagues, the stakes change.

Using AI at work is not only a question of productivity. It is also a question of responsibility: for the information you handle, for the confidentiality others trust you to protect, and for the rules your organization has set.

This lesson looks beyond personal tool habits. It is about the professional responsibility that comes with using AI as part of your job — and the difference between being careful on your own and being accountable to the people and organization around you.

---
### Personal Caution Is Only Half of It

It is easy to think of AI safety as a personal skill: be careful what you type, double-check the output, and don't overshare. That personal caution matters, and it is where responsible use begins.

But at work you carry a second kind of responsibility that has nothing to do with your own preferences. Your organization has interests, obligations, and often formal rules about how AI may be used. You are responsible not only for your own good habits, but for understanding what your organization allows and acting within those limits.

It helps to keep two questions separate:

- **Personal caution:** Am I handling this information sensibly?
- **Organizational obligation:** Am I using AI in the way my organization actually permits?

A professional can have excellent personal habits and still cause a serious problem by ignoring the second question. The rest of this lesson builds on both.

----
### Treat the Input Box as a Public Space

Many popular AI tools run on external servers. Depending on the tool and its settings, what you type may be stored, reviewed to improve the service, or kept far longer than you expect. With a public, general-purpose tool, the safest assumption is simple: anything you paste in could be seen by someone outside your control.

That does not make AI unusable. It means you should think before you paste, and keep genuinely sensitive information out of tools that are not approved for it.

Sensitive data is any information that could cause harm — to a person, a client, or your organization — if it were exposed. Common examples include personal identifiers, financial and health details, unreleased business plans, and anything that would let someone access a system.

The exercise below asks you to sort common workplace content. Notice the pattern as you go: material that is already public or fully generic is low-risk, while anything that identifies a real person or reveals private business information should stay out of a public tool.

----
Buckets (categories)
Generally safe for a public AI tool
Keep out of a public AI tool

Items (assign each to its correct bucket)
An already-published press release → Generally safe for a public AI tool
A generic meeting-agenda template → Generally safe for a public AI tool
Wording for a standard out-of-office reply → Generally safe for a public AI tool
A draft of a public product FAQ → Generally safe for a public AI tool
A customer's national ID number → Keep out of a public AI tool
Employee salary and performance details → Keep out of a public AI tool
An unreleased product roadmap → Keep out of a public AI tool
A system password or access key → Keep out of a public AI tool

----
### Confidentiality Is a Duty, Not a Preference

Much of the information you touch at work does not belong to you. It belongs to a client who trusted your organization with it, to a colleague whose personal details sit on file, or to the organization itself in the form of plans and know-how that competitors would value.

Confidentiality is the duty to protect that information. It often comes with real obligations — contracts with clients, laws protecting staff records, and regulations covering certain kinds of data. Pasting such material into an unapproved AI tool can breach those obligations even when nothing visibly goes wrong and no one seems harmed.

A useful habit is to ask, before sharing any content with a tool: whose information is this, and did they trust it to us for this purpose? If it belongs to someone else, treat it with extra care.

The categories below show the kinds of confidential information you are most likely to encounter.

----
Client and Customer Data

Contact details, contracts, account information, and the specifics of a client's business. They shared it with your organization for a defined purpose — not for a public tool.

Colleague and Personnel Information

Salaries, performance reviews, disciplinary records, health accommodations, and personal contact details. This information is protected by policy and often by law.

Proprietary and Competitive Information

Unreleased plans, pricing strategies, internal financials, and processes that give your organization an edge. Exposure can cause direct commercial harm.

Regulated and Contractual Data

Information covered by specific regulations or confidentiality agreements. Here the rules come from outside your organization, and breaking them can carry legal or contractual consequences.

-----
### Small Steps Toward a Big Mistake

Most confidentiality problems are not the result of someone deciding to leak information. They build up quietly.

Someone pastes a lightly sensitive document into a convenient tool and nothing bad happens. Encouraged, they do it again with something more sensitive. The habit becomes normal, the caution fades, and eventually a client's confidential file ends up in a tool no one approved. By then the risky behavior feels routine.

Recognizing this pattern is what lets you interrupt it early. The exercises below check whether you can spot the safer choice and put the stages of a typical slip in order.

----
### Not Knowing Is Not an Excuse

Personal caution protects you from obvious mistakes. But your organization may permit some tools and forbid others, require that certain data never leave approved systems, or expect you to disclose when AI helped produce your work. These rules are not always obvious, and "I didn't know the policy" rarely counts as a defense.

The responsible move is to find out. Many organizations now have an AI or acceptable-use policy, and those that don't yet are usually working on one. Either way, it is your job to ask rather than assume.

If you are not sure where your organization stands, the questions below are a practical place to start. Knowing the answers turns vague caution into clear, defensible action.

----
Is there an approved list of tools?

Ask which AI tools are sanctioned for work and whether a paid or enterprise version is required. Approved tools often come with stronger data protections than free consumer ones.

What information is off-limits?

Find out which categories of data must never be entered into an AI tool — typically client data, personnel records, and anything regulated.

Do we disclose when AI is used?

Some organizations expect you to note when AI assisted with a document or decision. Know the expectation before you send or publish AI-assisted work.

Who is accountable for the output?

Confirm that responsibility for AI-assisted work stays with you and your team, not the tool, and understand the review steps expected before it is used.

Where do I go with questions?

Identify the person or team who owns the policy, so you have somewhere to check an unusual case instead of guessing.

----
### A Routine You Can Apply Every Time

Understanding the risks and the rules only helps if it changes what you actually do. A short, repeatable routine turns the ideas in this lesson into a habit you can run in a few seconds before using AI on any work task.

The point of the routine is not to slow you down. It is to make the safe choice the automatic one, so that speed and responsibility work together rather than against each other.

Walk through the steps below. With practice, they become second nature.

----
Steps
1.
Pause and classify

Ask what kind of information this is. Is any of it sensitive, or does it belong to a client, a colleague, or the organization?
2.
Check the policy

Confirm the tool is approved and that this type of data is allowed in it. When you are unsure, ask before you paste.
3.
Strip or anonymize

Remove names, identifiers, and confidential specifics wherever the task allows. Share the least the tool needs to help.
4.
Use an approved tool

Prefer a sanctioned, protected tool over whatever is most convenient in the moment.
5.
Own the output

Review the result, verify anything important, and take responsibility for what you share or act on.

----
### Bringing It Together

Responsible AI use at work rests on two habits working side by side: your own caution with sensitive and confidential information, and your commitment to understand and follow what your organization allows.

[Note: the original file promises "The questions below check that both are clear" but no check/activity follows in the source — likely a content gap from export. Recommend confirming with the source file rather than me inventing filler here.]

---
### What to Carry Forward

AI can make your work faster, but it does not reduce your responsibility for the information you handle. That responsibility has two sides.

The personal side is caution: treat a public tool's input box as visible to others, keep genuinely sensitive data out of unapproved tools, and protect confidential information that belongs to clients, colleagues, and your organization.

The organizational side is obligation: find out whether your organization has an AI policy, learn which tools are approved and which data is off-limits, and act within those rules rather than assuming. Not knowing the policy is not a defense.

If you remember one thing, let it be the habit: before using AI on any work task, pause to classify the information, check what is allowed, share the least you can, and take ownership of the result. The judgment about what is safe and appropriate stays with you.
