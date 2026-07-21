## Part 1 — What is AI, really?

Imagine you have a record of how much rain fell every day for the last ten years in your city. With enough of that data, you could probably guess whether tomorrow is likely to be rainy or dry, just from the patterns: the time of year, the recent weather, what usually follows a storm. Artificial intelligence (AI) is software that does this kind of guessing, but at a much larger scale and faster than a person could.

More precisely, AI is software that learns from data (examples of what has happened before) and uses what it learned to make predictions or produce something new. The data can be anything: numbers like rainfall amounts, text like emails, or images like x-rays.
```
+Often, the relationships between these data points are far too complex for a person to work out by hand — that complexity is exactly why we turn to AI to find them.+
```
The idea is always the same: study many past examples, find the patterns, and use them to handle a new situation.

Once AI has learned those patterns, we put them to work in three ways.

## Flip cards  why are the new concepts mentioned here? like pattern recog etc when they werent in the previous module. the flip cards should be introduced after the lessons have been taught.
---

## Part 4 — Assistance

Assistance is when AI produces a draft for you. You give it a request and some context, and it writes something back. For example, you hand it three bullet points and it returns a clean email, or you paste a long report and it gives you a one-paragraph summary.

The writing usually sounds fluent and professional. But the AI is producing what looks like a likely answer, not checking whether it is true for your situation, so it can be confidently wrong. Treat the draft as a starting point you review and fix, not a finished product.

```
+A practical example is legal or compliance reporting. These reports are often extremely long and time-consuming to produce, and AI can drastically cut down the time it takes to write them. This does raise some data privacy concerns, though — uploading confidential information to an external organization's systems is a real issue, and we'll come back to that later.+
```

---

## Part 1 — The Three Ways AI Gets Used

Ready-made tools are the fastest way to start using AI.

Examples include AI assistants, writing tools, meeting-note generators, and spreadsheet copilots. The vendor handles the infrastructure, maintenance, and updates, allowing users to focus on the task itself.

```
-Imagine an operations team that needs to process customer requests faster. Instead of waiting for a new software project, they use a ready-made AI tool to draft summaries and recommendations. Within weeks, they see measurable time savings.-

+Imagine a 20-person customer support team at a software company, where agents spend most of their day answering repetitive questions about billing, password resets, and account setup. Instead of waiting for a new software project, an agent copies a customer's question into a ready-made AI writing tool, which drafts a reply in seconds. The agent reviews it, tweaks a line or two, and sends it — cutting average reply time from ten minutes to two. Within weeks, the team clears its ticket backlog and frees up time for harder cases.+
```

The tradeoff is that these tools offer convenience rather than complete control.

---

## Part 5

An API acts like a controlled doorway between systems.

Instead of employees manually copying information into an AI tool, software sends requests automatically and receives results within an existing workflow.

```
-For example, a customer service platform could automatically generate case summaries directly inside the CRM. Employees never leave the system they already use.-

+For example, that same customer support team no longer has to copy each question into a separate AI tool. The helpdesk software calls the AI directly through an API, so a draft reply appears next to the ticket the moment it comes in. Agents never leave the system they already use.+
```

APIs help organizations scale AI across teams while maintaining consistency and oversight.

---

## Part 7

Sometimes organizations have needs that standard tools cannot meet.

A custom model can be trained or tailored using proprietary data, specialized terminology, or unique business rules.

For example, a finance organization might need an AI system that understands its internal chart of accounts and can identify unusual spending patterns.
```
+A general-purpose tool has never seen that company's specific account codes, vendor names, or spending history, so it can't tell a routine transaction from an unusual one. A custom model trained on years of the organization's own transaction data, labeled by its internal auditors, learns what "normal" looks like for that specific business and can flag deviations a generic tool would miss.+
```
General-purpose tools may not perform consistently enough for that task.

Custom models offer greater control and specialization, but they also require:

- Significant data
- Technical expertise
- Ongoing maintenance
- Long-term ownership

Custom models are powerful, but they should not be the default starting point.

---

## Part 9

When evaluating
```
-AI opportunities-
+a potential AI use case+
```
, start with a simple question:

"Can a ready-made tool solve this problem?"

If yes, begin there.

Move toward APIs when you need AI integrated into workflows and scaled across teams.

Consider custom models only when simpler approaches cannot meet business requirements.

This mindset reduces cost, speeds adoption, and avoids unnecessary complexity.

---

## Part 11

Think about a real process in your workplace or studies.

```
-Could a ready-made tool improve it today?-
+Could a ready-made tool improve it today — and if so, what's stopping you from trying it this week?+

-Would integration into an existing system provide greater value?-
+Would integration into an existing system provide greater value than a standalone tool — would the time saved from not switching between systems outweigh the setup effort?+

-Is there a genuinely unique requirement that might justify a custom model?-
+Is there a genuinely unique requirement — proprietary data, specialized terminology, or a rule no generic tool could learn — that might justify a custom model?+
```

The goal is not to choose the most sophisticated option. The goal is to choose the option that delivers the best outcome with the least unnecessary complexity.
