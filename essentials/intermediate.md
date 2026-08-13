# Overall Level Analysis — Intermediate: "AI Essentials for Professionals"

This level has a clear, sensible arc: **Section 1** opens the hood on how AI actually generates answers (LLMs → embeddings → RAG → synthesis), **Section 2** turns that mental model into applied prompting and tool-selection skill, and **Section 3** moves from individual use to designing AI into team workflows. That's a good progression for "Intermediate" — it builds on Associate's foundations (what AI is, why it's wrong, privacy) without repeating them, and it's appropriately more systems-level than Associate's individual-practitioner focus.

A few cross-cutting issues worth flagging before the lesson-by-lesson review:

**A real coherence/accuracy bug: the missing "deployment" lesson.** The synthesis lesson "What This Means for How You Use AI" opens by referencing "four parts of modern AI... how these systems are deployed and run," and later has a whole section built on "The deployment lesson showed that an AI feature is more than the model itself." No such lesson exists anywhere in the material provided — you flagged this yourself with a `> CHANGE`. Rather than inventing a new deployment lesson (which would bloat an already substantial section and drift toward infrastructure detail non-technical professionals don't need), I've removed the deployment references. This also fixes a **real redundancy**: the vendor-evaluation questions in that section ("Where does our data go... what does it cost") are covered more thoroughly by the dedicated "Evaluating and Choosing the Right AI Tool for Your Work Problem" lesson later in the course. Cutting the section here removes overlap rather than creating a gap.

**Two `> CHANGE` requests I'm declining, and why it matters.** You asked twice for specific, named, current AI tools/vendors to be added as examples (the CBA case study, and the Tool A/B comparison). I'm declining both — not because the instinct is wrong, but because a named current product is exactly the kind of **time-sensitive fact** your own "Why AI Can Be Wrong" lesson warns learners to distrust: vendors change, features change, products get discontinued, and I have no way to verify current details here. Baking a real vendor name into a course meant to stay usable for a few years is a liability, not a strength. I've explained my reasoning in each case and offered an alternative that keeps the pedagogical value without the staleness/accuracy risk.

**Section 1's module separators are inconsistent.** Sections 2 and 3 use a clean `=====` between modules, matching your defined syntax. Section 1 instead uses varying-length double lines of `=` (`========`, `=========`, `===============`) between its four modules. I've preserved these exactly as given rather than "fixing" them, but flagging it in case it's unintentional drift.

**Two section-title typos:** "how ai systems **atually** work" and "DESIGNING **RELAIBLE** AI WORKFLOWS." Not touching these since they're your section titles, just flagging.

**CMS authoring artifacts** ("Editing: Categorization," "Delete block," "Add item," "Add option," "Points per match") appear throughout the activity blocks. These are leftover editor UI text, not learner-facing content. I've stripped them wherever I was already revising a module, and flagged them separately for the two modules that needed no other change.

**Scope check on the mechanics content (LLMs/embeddings/RAG):** I want to flag this explicitly since it's the most "technical" material in the course. I think it earns its place — none of it drifts into architecture, math, or engineering detail; every mechanism is immediately tied to a workplace consequence (why outputs vary, why fluency isn't proof, why org-specific answers need retrieval). This is appropriately scoped for professionals *evaluating and directing* AI use, not building it.

Now, module by module, in order, using your exact separator syntax.

---

```
=========================
=========================

#########################
NEW SECTION: how ai systems atually work
#########################
```

## Module: "How Large Language Models Work"

### ORIGINAL

*(As given — four `> CHANGE` markers evaluated below; "The model's reading history" and "Apply the mental model" had no CHANGE flagged and needed none.)*

> # How Large Language Models Work
> ## What happens after you press Enter?
> A large language model (LLM) is best understood as a **pattern-based text generator**...
> `> CHANGE: make the initial definition of LLM bit more detailed and simple`
>
> ## Prediction, one token at a time
> The model does not usually compose a complete answer and then reveal it...
> `> CHANGE: give an detailed example of this related to a professional context`
>
> ## The model's reading history
> [training data table — no change]
>
> ## Fluency can imitate certainty
> **Generating** means producing text that fits learned patterns...
> `> CHANGE: give some real world example.`
>
> ## Use the model for what it does well—and add controls
> [6-step workflow + manager example]
> `> CCHANGE: add some example prompt as well after stating each point in this... example`
>
> ## Apply the mental model
> [operations manager scenario — no change]

### MODIFICATIONS

1. **LLM definition — accepted.** Added a phone-autocomplete analogy (intuitive, non-technical) before the tokens explanation, and a one-clause gloss on what a "token" actually is.
2. **Prediction example — accepted.** Added a concrete professional scenario (a payment-deadline justification) showing how token-level branching produces different, sometimes contradictory, explanations for the same request.
3. **Fluency example — accepted.** Added a policy-citation scenario that also sets up the hallucinations concept from Associate level nicely.
4. **Manager-scenario prompt examples — accepted, scoped.** Added illustrative prompt fragments after steps 1–3, since those are the steps that actually involve prompting the AI. Steps 4–6 are human review/approval actions — no AI prompt applies there, so I've labeled them as such rather than inventing one to force a pattern.

### UPDATED CONTENT

# How Large Language Models Work

## What happens after you press Enter?

A large language model (LLM) is best understood as a **pattern-based text generator** — think of the predictive text on your phone's keyboard, but trained on a vastly larger and more varied body of text, and far better at tracking what you actually mean across a whole paragraph rather than just the last couple of words. It takes the text in your prompt, converts it into small units called **tokens** (roughly word-sized pieces of text), and predicts a plausible next token. It then repeats that prediction process, one token at a time, until it has built a full response.

A useful workplace analogy is an extremely fast ghostwriter who has read a vast amount of text. The ghostwriter can produce a polished memo, plan, or explanation because it has learned common language patterns. However, polished writing is not the same as verified knowledge of your organization.

:::info Core mental model
An LLM generates a statistically plausible continuation from the context you provide. It does not automatically retrieve a verified answer from a database.
:::

By the end of this lesson, you should be able to:

- explain how an LLM generates text;
- identify why similar prompts may produce different outputs;
- describe how training data shapes model behaviour; and
- separate **language work** from **truth work** before using an output.

---

## Prediction, one token at a time

The model does not usually compose a complete answer and then reveal it. It builds the answer incrementally.

At each step, it estimates which tokens are plausible given:

- your instructions;
- the words already generated;
- examples or source material in the prompt; and
- patterns learned during training.

Several continuations may be reasonable. The model selects or samples one, appends it to the context, and predicts again.

For example, suppose you ask an AI tool to draft a short justification for extending a client's payment deadline. At the point where it needs to explain *why*, several next words are almost equally plausible — "because," "given," "due" — and following one path over another can lead to a justification that cites cash-flow timing in one draft and a shipping delay in another, even though you never mentioned either. Neither reason is necessarily true; both were simply plausible continuations. This is exactly why asking the same question twice can produce two different, sometimes contradictory, explanations.

:::warning Practical implication
A fluent answer should be treated as a **well-formed suggestion**, not as proof that the underlying facts, calculations, policies, or assumptions are correct.
:::

---

## The model's reading history

The previous section showed that a model can generate different outputs for the same prompt because it is choosing token by token rather than recalling a fixed answer. Where do those tokens and patterns come from in the first place? That comes down to training data.

**Training data** is the large collection of examples from which a model learns language patterns. During training, it learns relationships such as common phrasing, tone conventions, argument structures, and which concepts often appear together.

This does **not** mean the model contains a neat, searchable library of every document it encountered. Its responses reflect a statistical imprint of the material rather than guaranteed recall of an authoritative source.

Training data influences:

| Area | Possible effect | Example |
|---|---|---|
| Domain fit | The model has seen far more general business or casual writing than material from narrow specialist fields, so it can produce fluent prose while using specialist terms loosely or incorrectly | Asked to summarise a clinical trial report, it may use "significant" in the everyday sense rather than the precise statistical sense the field requires |
| Regional fit | The model's training examples skew toward the practices, laws, or conventions of the regions most represented in its data, so it may default to those norms rather than the user's local ones | Asked to draft an employment contract, it may include at-will employment language common in the US even though the user is in a country with different labour law |
| Representation | If a group, dialect, or viewpoint appeared less often in training material, the model has fewer patterns to draw on for it and may describe it less accurately or fall back on generic phrasing | Asked to write about a small regional dialect or a less-documented profession, the output may default to broad generalisations rather than specifics |
| Currency | The model's patterns are frozen at the point its training data was collected, so it cannot know about events, prices, or rules that changed afterward unless those are supplied in the prompt | Asked for "the current interest rate" or "this year's tax bracket," it may state an outdated figure with the same confidence as a current one |
| Framing | Some narratives or conclusions appeared so often in training material that the model treats them as the default, ordinary answer, even when a given situation calls for a different conclusion | Asked to evaluate a business plan, it may default to generic risk framing common in the source material and understate a genuinely unusual risk unique to the case |

:::info Better practice
When domain accuracy matters, provide approved policies, definitions, recent data, or excerpts and instruct the model to stay within them.
:::

---

## Fluency can imitate certainty

**Generating** means producing text that fits learned patterns and the current context.

That is a different act from **knowing**, which, in a workplace sense, means being anchored to verified facts, approved evidence, current systems of record, and accountable interpretation.

Because generating and knowing are different processes, an LLM can imitate the form of a policy, calculation, citation, or expert explanation even when part of the content is unsupported — the fluency of the output tells you nothing about whether it is anchored to fact. This matters because confidence is also a language pattern; it is not evidence, so a polished tone is not a signal you can rely on to tell the two apart.

For example, ask an AI tool to summarise your company's expense policy and cite the relevant clause, and it may return a clean, specific-sounding answer — "Per Section 4.2, receipts are required for expenses over $25." The sentence reads exactly like something pulled from your actual policy. Whether Section 4.2 exists, or says anything of the kind, is a separate question the fluency of the sentence cannot answer for you.

A practical task split is:

- **Language work:** structure, tone, clarity, summarization, option generation, and audience adaptation.
- **Truth work:** facts, figures, legal meaning, policy requirements, contractual commitments, and causal claims.

:::warning Risk signal
The more polished and authoritative a draft sounds, the easier it is to skip verification. Review the claims, not just the prose.
:::

----

## Use the model for what it does well—and add controls

A reliable workflow does not ask the LLM to be both ghostwriter and final authority.

1. Define the goal, audience, constraints, and required format.
2. Supply the minimum approved context needed for the task.
3. Ask for visible assumptions, options, risks, or source boundaries.
4. Review assumptions before polishing the language.
5. Verify every factual or consequential claim.
6. Obtain accountable human approval before high-impact use.

This approach preserves the speed of generation while reducing the chance that plausible text becomes an unverified business decision.

For example, a manager asking an LLM to draft a client-facing project update might:

1. State the goal is a two-paragraph status update for a non-technical client.
   *Prompt fragment: "Write a two-paragraph project status update for a client who isn't technical."*
2. Paste in the actual sprint report as the only source of facts.
   *Prompt fragment: "Use only the sprint report below as your source of facts — do not add details that aren't in it."*
3. Ask the model to flag any assumption it made and list which figures came from the sprint report versus its own phrasing.
   *Prompt fragment: "List any assumption you made, and mark which numbers came directly from the report versus your own wording."*
4. Check that the flagged assumptions are reasonable. *(a human review step — no further prompt needed)*
5. Confirm the dates and numbers against the sprint report itself before sending. *(a human review step — no further prompt needed)*
6. Finally, have the account lead sign off before it goes to the client. *(a human approval step — no further prompt needed)*

Each step keeps a plausible-sounding draft from quietly becoming an approved commitment.

---

## Apply the mental model

An operations manager is behind on a product launch and needs to decide how to reassign staff for the next two weeks. She pastes her backlog notes, a list of open tasks, deadlines, and rough time estimates, into an LLM and asks it to generate three headcount-prioritization options, each showing which tasks get covered and which get delayed.

The response comes back clear, detailed, and persuasive: three named options, each with a short rationale, a list of tasks covered, and a projected completion date.

When compared with the options generated, AI suggests option 2 as the strongest choice, since it finishes the most tasks on time. It does this by assuming the QA team has six available people to pull from. The manager's actual current capacity plan, however, shows only four QA people available that week — two are out on approved leave, which never appeared in the backlog notes because that file only tracks tasks, not staffing.

The useful part of the output is the rapid generation of structured options and trade-offs — it saved her the time of drafting three scenarios by hand. The unsafe part would be approving Option 2 on the strength of its confident write-up, without checking its staffing assumption against the capacity plan. If she skipped that check, she could commit the team to a schedule that is short two people from day one.

```
========
========
```

## Module: "What Are Embeddings and Why They Matter"

### ORIGINAL

*(As given — five `> CHANGE` markers; "Three questions every retrieval result must survive" and "Apply the model" had no CHANGE and needed none.)*

> # What Are Embeddings and Why They Matter
> ## Why embeddings matter
> [intro, core mental model, objectives — no change]
>
> ## What is an embedding?
> [vector explanation + "staffing capacity" example]
> `> CHANGE: make example a bit more detailed`
>
> ## Matching ideas, not just strings
> [keyword vs embedding retrieval + churn example]
> `> CHANGE: give somme detailed example.`
>
> ## The near-miss problem
> [Product A/B refund example]
> `> CHANGE: make the example more detailed.`
>
> ## Three questions every retrieval result must survive
> [no change]
>
> ## Embeddings inherit the quality of the source
> [weak vs stronger practice table]
> `> CHANGE: the purpose of the table... isn't that detailed or comprehensive... it also should be clear`
>
> ## Combine discovery, verification, and maintenance
> [7-step routine]
> `> CHANGE: create a professional scenario and then give examples for all of these defined points`
>
> ## Apply the model
> [risk analyst scenario — no change]

### MODIFICATIONS

1. **Embedding example — accepted.** Added the "so what" — what a search tool would actually surface given those two related sentences.
2. **"Matching ideas" example — accepted.** Added a concrete analyst scenario showing which real documents get surfaced and why keyword search would have missed them.
3. **Near-miss example — accepted.** Spelled out the actual differing clause between Product A and B's refund policies, so the "one sentence that changes everything" is visible rather than asserted.
4. **Table — accepted, format-preserving.** Rather than expanding each cell into prose (which would break the table's scannability — a stated course priority), I added a third "Example" column so each row stays concrete without losing the compact reference format.
5. **7-step routine — accepted.** Built one running scenario (a compliance analyst investigating late-fee complaints) mapped across all seven steps.

### UPDATED CONTENT

# What Are Embeddings and Why They Matter

## Why embeddings matter

Modern AI search tools often need to find information even when the query and the source use different words. To do this, they convert text into **embeddings**: numeric vectors that represent patterns of meaning and context.

A useful analogy is a map. Each sentence or document receives coordinates in a high-dimensional space. Texts about similar ideas tend to appear closer together, while unrelated texts tend to appear farther apart.

:::info Core mental model
An embedding is a numeric representation used to compare the meaning of text. It is not a human-readable definition, a verified fact, or an exact record identifier.
:::

By the end of this lesson, you will be able to:

- explain how text becomes a vector;
- distinguish meaning-based retrieval from keyword and exact lookup;
- identify when a semantic near-match is unsafe; and
- improve documents so AI retrieval becomes more accurate.

---

## What is an embedding?

An AI system can convert a word, sentence, paragraph, or document into a long list of numbers called a **vector**. The individual numbers are usually not meaningful to a person. What matters is the overall pattern.

When two pieces of text express related ideas, their vectors often point in similar directions or occupy nearby regions of the model's meaning space.

For example:

- "staffing capacity is constrained"
- "we do not have enough people for the workload"

These sentences share few exact words, yet they communicate a similar operational problem. Their embeddings may therefore be close — which means a search tool built on embeddings could surface both in response to a query like "team is short-staffed," even though neither sentence shares an exact word with that query.

:::clarification Important distinction
Embeddings represent learned language patterns. They do not prove that the system understands your organization, knows whether a statement is true, or has found the authoritative source.
:::

---

## Matching ideas, not just strings

Traditional keyword search looks for literal words or close textual matches. Embedding-based retrieval converts the query and stored content into vectors, then looks for items that are **semantically nearby**.

A query for **"reasons customers leave"** might retrieve documents containing:

- churn drivers;
- renewal risk;
- cancellation patterns;
- poor retention;
- account attrition.

For example, a customer-success analyst investigating why enterprise accounts aren't renewing might search "reasons customers leave" and, thanks to embedding retrieval, land on a support ticket about "renewal risk flagged by account manager" and a survey response about "poor retention experience" — documents a literal keyword search for "leave" would have missed entirely, because neither one contains that word.

This can reveal evidence the user would miss if they searched only for one phrase.

| Search mode | Best at | Main limitation |
|---|---|---|
| Keyword search | Literal terms and known wording | Misses synonyms and alternate phrasing |
| Embedding retrieval | Related concepts and language variants | Can return relevant-looking near-misses |
| Exact lookup | Known IDs, values, clauses, and records | Requires the exact field or identifier |

:::info Professional value
Meaning-based retrieval is strongest during discovery: gathering a landscape, finding adjacent evidence, and connecting language used by different teams.
:::

---

## The near-miss problem

Embedding retrieval selects items that are close in meaning. Two documents can be highly similar yet differ on one constraint that changes the correct decision:

- region;
- product version;
- effective date;
- customer tier;
- policy threshold;
- contract status.

For example, Product A's refund policy might read: "Refunds are issued within 14 days of purchase, provided the item is unused." Product B's policy might be nearly identical in wording, except for one added clause: "Refunds are issued within 14 days of purchase, provided the item is unused and the customer has not already redeemed a promotional credit on this order." An embedding search for "refund eligibility" could easily return Product B's policy as the top match for a Product A question, because the two documents are semantically almost twins — right up until the one sentence that actually decides the case.

:::warning Reliability boundary
Semantic similarity answers, "What looks related?" It does not answer, "What is definitively the correct record, version, clause, or value?"
:::

Use embedding retrieval to investigate. Switch to an authoritative exact lookup when a near-miss could change money, compliance, customer rights, safety, or reporting.

---

## Three questions every retrieval result must survive

A highly similar result can still be unsafe. Before using it in a consequential decision, check:

1. **Authority:** Is this an approved source, or merely a draft, summary, email, or old procedure?
2. **Completeness:** Could a less common exception or missing document change the conclusion?
3. **Scope:** Does the result match the required region, product, audience, date, and version?

A top-ranked result is the nearest result according to the retrieval method. It is not automatically the most authoritative or complete result.

:::checklist High-impact retrieval check
- Open the source document.
- Confirm title, owner, status, version, and effective date.
- Validate hard filters and identifiers.
- Check for exceptions.
- Record or cite the authoritative source used.
:::

----

## Embeddings inherit the quality of the source

An embedding is built from the text and context supplied to the model. If a document mixes several unrelated processes, hides its scope, or switches terminology, its semantic signal becomes blurred.

A retrieval-ready document should make its **aboutness** and applicability explicit.

| Weak document practice | Stronger alternative | Example |
|---|---|---|
| Vague title | Title that matches the process or question | "Notes" → "Refund Eligibility – Product A – Updated Jan 2026" |
| Several processes in one long file | One process per document or clearly independent sections | Split a single "Customer Policies" file into separate refund, warranty, and shipping documents |
| Missing region or product scope | Scope stated near the beginning | Add "Applies to: EU customers, Product A only" as the first line |
| Inconsistent labels | Primary term plus accepted synonyms | State "churn (also called attrition or cancellation)" once, up front |
| No version information | Owner, status, version, and effective date | Add a header line: "Owner: Legal · v3 · Effective 1 March 2026" |
| Key rule buried in prose | Explicit heading, definition, or decision rule | Pull "no refund after 14 days" out of a paragraph into its own labeled rule |

:::info Root-cause insight
Poor AI search is often partly a knowledge-management problem. Changing tools cannot compensate for unclear, stale, or contradictory source material.
:::

----

## Combine discovery, verification, and maintenance

A reliable workflow uses embeddings for their strength without pretending that similarity is certainty.

Take a compliance analyst investigating a rise in complaints about "unexpected late fees":

1. **Define whether the task is concept discovery or exact verification.** She starts in discovery mode — she wants to see the landscape of related complaints, not yet confirm a specific policy clause.
2. **Phrase a concept-focused query for discovery.** She searches "unexpected fees" rather than the exact phrase customers used, so she also catches complaints about "surprise charges" and "hidden costs."
3. **Review retrieved sources and identify relevant themes.** Most complaints cluster around one theme: fees applied after a grace period customers didn't know existed.
4. **Narrow by hard filters such as date, region, product, version, or ID.** She filters to the last two quarters and to the specific product line generating most complaints.
5. **Confirm critical claims in an authoritative system or document.** She opens the actual current fee schedule — not a summary or draft — to confirm the grace period length and when it last changed.
6. **Improve weak source documents revealed by failed or misleading searches.** She notices the fee schedule buries the grace period in a footnote and flags it to be pulled into its own labeled section.
7. **Retest using realistic queries and accepted synonyms.** She re-runs her original search after the fix, using customers' own wording, to confirm the right document now surfaces first.

This turns AI search from an answer engine into a **research accelerator supported by governance**.

---

## Apply the model

A risk analyst asks an AI assistant to find complaints related to "misleading fee disclosure." The system retrieves several useful cases, but mixes two regions with different legal requirements and two product versions with different customer notices.

The retrieved set is valuable for identifying a possible pattern. It is not yet decision-ready. The analyst must validate region, product code, policy version, and authoritative disclosure requirements before reporting a trend or recommending action.

```
=========
=========
```

## Module: "Understanding RAG — How AI Uses Your Documents"

### ORIGINAL

*(As given — four `> CHANGE` markers; "Grounding reduces guessing" and "Manage RAG like a fast research assistant" had no CHANGE and needed none.)*

> # Understanding RAG — How AI Uses Your Documents
> ## General fluency is not company-specific knowledge
> [intro + RAG definition]
> `> CHANGE: add context to previous section. also make the concept of RAG a bit more detailed and simple.`
>
> ## Retrieve first, generate second
> [retrieval + generation explanation, librarian/writer analogy]
> `> CHANGE: also write the answer can also be wrong if the writer isnt good or skilled enough... both matter`
>
> ## How your documents enter the answer
> [chunking + embedding explanation]
> `> CHANGE make a soft of text based flowchart to show the process.`
>
> ## The answer is only as strong as the briefing pack
> [retrieval quality table]
> `> CHANGE: for each row in the table, give a short example.`
>
> ## Grounding reduces guessing
> [no change]
>
> ## Manage RAG like a fast research assistant
> [prompt pattern + checklist — no change]

### MODIFICATIONS

1. **Intro — accepted.** Added a direct bridge back to the embeddings lesson (RAG is where that matching gets *used*), plus a plainer one-sentence gloss on what RAG actually does.
2. **Retrieve/generate warning — accepted.** Your point is correct and was genuinely missing: bad generation can ruin a good retrieval just as easily as bad retrieval ruins good generation. Added a sentence to the existing warning box rather than a new section, since the point fits naturally there.
3. **Flowchart — accepted.** Added a simple text-based flow showing documents → chunks → embeddings → index, and question → embedding → match → answer.
4. **Table — accepted.** Added a short "Example" column, same approach as the embeddings table, keeping the row format scannable.

### UPDATED CONTENT

# Understanding RAG — How AI Uses Your Documents

## General fluency is not company-specific knowledge

The previous lesson introduced embeddings as a way to match meaning rather than exact words. RAG is where that matching gets put to practical use: it's the technique that lets an AI tool search your own documents for relevant passages before it writes an answer, instead of relying only on what it learned during training.

A general-purpose language model can write fluent explanations, emails, and plans, but it does not automatically know your organization's current policies, procedures, contracts, or product rules.

This creates a professional risk: the model may generate an answer based on how organizations **typically** operate rather than what your organization has actually approved.

**Retrieval-Augmented Generation**, usually shortened to **RAG**, addresses this problem by adding a document-retrieval step before the answer is generated — in effect, handing the model a short, relevant packet of your own material to work from, on the spot, before it starts writing.

:::info Core mental model
RAG gives the language model a temporary briefing pack of relevant passages from your documents while it writes its answer.
:::

By the end of this lesson, you will be able to:

- explain why RAG exists;
- describe the retrieval-and-generation process;
- identify how RAG improves organization-specific answers;
- recognize where RAG can still fail; and
- use source-grounded AI answers with appropriate professional judgment.

----

## Retrieve first, generate second

A RAG system performs two linked jobs:

1. **Retrieval:** locate passages from an approved collection of documents that appear relevant to the question.
2. **Generation:** provide those passages to a language model so it can compose an answer grounded in the retrieved material.

RAG does not usually mean the model has permanently memorized your documents. The material is typically searched at the time of the question and inserted into the model's working context.

A useful analogy is a professional writer working with a librarian:

- the **librarian** finds relevant source excerpts;
- the **writer** turns those excerpts into a clear response.

:::warning Important limitation
A polished answer can still be wrong if the librarian retrieves the wrong passages, misses an exception, or supplies an outdated document. It can also be wrong even with perfect retrieval, if the writer misreads, oversimplifies, or overgeneralizes what the source actually said — good retrieval does not guarantee good generation, and both stages need scrutiny.
:::

----

## How your documents enter the answer

Before users ask questions, documents are usually prepared for retrieval. Long files may be divided into smaller **chunks**, and each chunk may be converted into an embedding — a numeric representation of its meaning.

When a question is submitted, the system compares the question with the indexed document chunks, selects the most relevant passages, and places them in the prompt sent to the language model.

```
Your documents → split into chunks → each chunk converted to an embedding → stored in an index
                                                                                    ↓
Your question → converted to an embedding → compared against the index → most relevant chunks selected
                                                                                    ↓
                            Selected chunks + your question → sent to the language model → answer generated
```

:::clarification Two separate quality stages
A RAG answer can fail during **retrieval** or during **generation**. Strong writing cannot repair missing or irrelevant evidence.
:::

----

## The answer is only as strong as the briefing pack

Imagine asking an analyst to prepare an urgent policy briefing. Even an excellent writer will struggle if the research pack contains the wrong region, an outdated policy, or only half of the relevant exception.

The same principle applies to RAG.

Retrieval quality depends on:

- how clearly the question is scoped;
- whether the correct repository is searched;
- how documents were divided into chunks;
- document titles, labels, and metadata;
- whether current and superseded versions are distinguishable; and
- whether the relevant information exists in the indexed sources.

| Retrieval problem | Likely result | Example |
|---|---|---|
| Question is vague | Broad or generic passages | Asking "what's our leave policy" instead of "how much annual leave do new hires in Germany get in their first year" |
| Wrong repository searched | Related but non-authoritative material | Searching a shared drive of draft HR proposals instead of the approved policy repository |
| Old and new versions coexist | Conflicting guidance | Both the 2023 and 2026 expense policy are indexed, and the system can't tell you which is current |
| Exception stored elsewhere | Accurate-looking but incomplete answer | The general refund policy is retrieved, but a separate "promotional order exceptions" document never gets pulled in |
| Passage is split badly | Missing context or distorted meaning | A chunk boundary cuts a sentence in half, so "not eligible" gets separated from the condition that explains why |

:::info Troubleshooting principle
When a RAG answer seems wrong, inspect what was retrieved before repeatedly asking the model to rewrite the prose.
:::

---

## Grounding reduces guessing

Without RAG, a model may answer an internal question using general patterns from similar organizations. With RAG, the model can use your actual terminology, timelines, thresholds, procedures, and exceptions.

This often improves:

- organization-specific relevance;
- consistency with documented procedures;
- traceability through citations;
- access to current documents without retraining the model; and
- comparison across multiple internal sources.

However, RAG does not eliminate hallucinations or professional responsibility. The model can still:

- add a detail that is not in the source;
- misunderstand or overgeneralize a passage;
- merge conflicting documents incorrectly;
- cite a passage that does not support its claim; or
- miss a source that was never retrieved.

:::warning Accuracy is bounded
RAG improves the probability that an answer is grounded. It does not transform generated prose into automatically approved guidance.
:::

----

## Manage RAG like a fast research assistant

A reliable user does more than ask a question and accept the answer. The user defines the scope, checks the evidence, and decides whether the situation requires escalation.

A strong RAG prompt includes:

- **decision context:** why the answer is needed;
- **scope:** team, region, product, timeframe, or customer type;
- **source boundary:** which repository or document set to search;
- **output requirement:** answer, citations, excerpts, and exceptions; and
- **uncertainty instruction:** identify missing, conflicting, or unavailable evidence.

Example prompt pattern:

> Using only the approved HR policy repository, identify the offboarding requirements for permanent employees in Malaysia effective this year. Provide the document title, section heading, supporting excerpt, exceptions, and any uncertainty. Do not infer requirements that are not stated in the sources.

:::checklist Trust checklist
- Open the cited source.
- Confirm owner, approval status, and effective date.
- Check that the excerpt supports the claim.
- Verify critical deadlines, thresholds, and exceptions.
- Obtain human sign-off where required.
:::

```
===============
================
```

## Module: "What This Means for How You Use AI"

### ORIGINAL

*(As given. Flagging a structural issue, not a `> CHANGE`: the intro and "From user to informed evaluator" reference a "deployment" lesson that does not exist in the material provided. The one explicit `> CHANGE` sits on that same section.)*

> # What This Means for How You Use AI
> ### The payoff of everything so far
> You have now looked inside **four** parts of modern AI: how a large language model generates text, how embeddings capture meaning, how retrieval-augmented generation (RAG) brings in outside information, **and how these systems are deployed and run**...
> [objectives list, including "ask sharper questions when your organization is evaluating an AI product"]
>
> ### The wording is the input
> [no change]
>
> ### Meaning comes from what surrounds the words
> [no change]
>
> ### When a general chatbot is the wrong tool
> [no change]
>
> ### From user to informed evaluator
> The deployment lesson showed that an AI feature is more than the model itself...
> `> CHANGE: there is no deployment method lesson - give some example`
>
> ### One habit that ties it all together
> [no change]

### MODIFICATIONS

1. **Your CHANGE is correct, and I'd push the fix further than "give some example."** There genuinely is no deployment lesson anywhere in the material — this isn't a missing example, it's a reference to content that doesn't exist. Rather than inventing a deployment lesson (which would add real length to an already substantial section, and drift toward infrastructure/vendor-ops detail that's arguably the least essential of the four for this audience), I've removed the deployment references.
2. **Removed "From user to informed evaluator" entirely**, not just patched it. Its actual content — questions to ask a vendor about data handling, retrieval, uncertainty, and cost — is covered in more depth by the dedicated "Evaluating and Choosing the Right AI Tool for Your Work Problem" lesson later in this section. Keeping both would be redundant; cutting this one removes both the accuracy problem and the overlap. Added one forward-pointing sentence to the closing instead, so the reader knows that ground is coming, not missing.
3. **Adjusted "four parts" to "three parts"** in the intro and removed the deployment clause.
4. **Dropped the "ask sharper questions... evaluating an AI product" objective**, since this lesson no longer teaches that directly — promising an outcome and then not delivering it is its own coherence problem.

### UPDATED CONTENT

# What This Means for How You Use AI

### The payoff of everything so far

You have now looked inside three parts of modern AI: how a large language model generates text, how embeddings capture meaning, and how retrieval-augmented generation (RAG) brings in outside information. Each of those lessons answered a "how does it work" question. This lesson answers a different one: what should any of that change about the way you actually work?

The short answer is that understanding the machinery makes you a sharper, safer, and more confident user. You stop treating AI as a mysterious oracle and start treating it as a tool whose behaviour you can anticipate and shape.

By the end of this lesson you should be able to:

- explain why the exact wording of a prompt changes the result;
- describe why adding relevant context improves an answer; and
- decide when an organization-specific question needs a retrieval-based tool rather than a general chatbot.

We will introduce no new technology here. Instead, we will turn what you already know into concrete professional habits.

----

### The wording is the input

In the first lesson you saw that a language model works by predicting likely text, one piece at a time, from the words it has been given. That single fact has a direct consequence for your day: the words in your prompt are not a loose description of what you want — they are the raw material the model builds from.

When you change the wording, you change the patterns the model reaches for. Asking for "a short, cautious update for senior leadership" pulls in different language than "a quick note to the team." Naming the audience, the tone, the length, and the purpose narrows the range of plausible continuations, so the result lands closer to what you intended on the first try.

This is why vague prompts produce generic results and specific prompts produce useful ones. You are not persuading the model; you are steering it. A professional who understands this writes a prompt the way they would brief a capable new colleague: state the goal, the audience, the constraints, and the format up front, rather than hoping the model guesses correctly.

---

### Meaning comes from what surrounds the words

The lesson on embeddings showed that these systems represent meaning by placing related ideas near each other, so the model can tell that "quarterly revenue" and "three-month sales figures" point to the same thing. That is why context is so powerful: when you add relevant background to a prompt, you give the model more of the right meaning to work with, and it can connect your request to the ideas that actually matter.

A general model knows a great deal about the world in general and very little about your world in particular. It has never seen your policy, your product names, or last week's decision. When you paste in the approved definition, the relevant paragraph, or a short example of the style you want, you close that gap. You are not making the model smarter; you are pointing its existing ability at the specific meaning of your situation.

In practice this changes a habit. Instead of asking a bare question and correcting a generic answer, you supply the few sentences of context that let the model get it right the first time — the audience, the source text, the constraint, or a sample of the outcome you have in mind.

----

### When a general chatbot is the wrong tool

The RAG lesson explained that some AI systems retrieve relevant documents first and then generate an answer grounded in them. Knowing this gives you a practical decision rule: match the question to the tool that can actually answer it.

A general chatbot is well suited to open-ended language work — drafting, summarizing, brainstorming, or explaining a widely known concept. But when the answer depends on your organization's own current information — a specific policy clause, this quarter's figures, an internal procedure — a general model has no reliable way to know it. That is exactly the situation a retrieval-based tool is built for: it looks up the approved source and answers from it, and it can usually show you where the answer came from.

So before you trust an answer, ask where the correct information lives. If it lives in general knowledge, a standard model is fine. If it lives in your documents, systems, or records, you want a tool that retrieves from those sources — or you supply the source yourself. Recognising which kind of question you are asking prevents the most common professional mistake: trusting a confident general answer to a question only your internal records can settle.

----

### One habit that ties it all together

Each idea in this module points to the same underlying move: before you rely on an AI output, decide what kind of work it is and where the right answer lives. That single habit draws on everything you have learned.

A dependable routine looks like this. Be specific in the prompt, because the wording is the input. Supply the relevant context, because meaning comes from what surrounds the request. Check whether the question depends on your organization's own information, and if it does, use a tool that retrieves from your sources or paste the source in yourself. Separate the parts the model is good at — structure, tone, drafting — from the facts and figures that need checking. And keep accountable human judgement on any decision that carries real consequences.

A later lesson in this course builds a full framework for evaluating and choosing AI tools — what you've learned here is the mental model that makes those questions make sense.

None of this slows you down once it becomes automatic. It simply means the speed of AI is working for you, instead of quietly introducing errors you did not think to check.

---

```
=========================
=========================

#########################
NEW SECTION: APPLIED PROMPTING AND TOOL CHOICE
#########################
```

## Module: "Role-Based and Context-Aware Prompting"

### ORIGINAL

*(As given — one `> CHANGE`.)*

> [intro, role/audience section with deadline-risk example, tone/boundaries section]
> `> CHANGE: give an example for a same question/scenario but how the above two tones defined in examples would change the output.`
> [context section, closing synthesis]

### MODIFICATIONS

**Accepted.** The tone/boundaries section names two tone options ("warm and reassuring" vs. "concise, lead with the bottom line") but never shows them applied to the same content, unlike the role/audience section just above it, which does have a paired before/after. Added a matched pair — same underlying fact (a project delay), two tone treatments — so the reader can see the difference rather than infer it.

### UPDATED CONTENT

# Role-Based and Context-Aware Prompting

You already know how to ask an AI tool a question, and that alone can be useful. But most people stop there, and they never discover how much better the results can get.

Two small instructions change almost everything: telling the AI **who to be**, and telling it **who the answer is for**. The same question, asked with a role and an audience attached, can go from generic and forgettable to genuinely useful.

In this lesson you will learn to add those two ingredients on purpose, so that a strong answer becomes your normal result rather than a lucky one.

----

A role decides who is speaking. The **audience** decides who is listening, and it shapes how the AI explains things just as strongly.

Compare:

- "Explain what a deadline risk is."
- "Explain what a deadline risk is to a brand-new employee in their first week."

The first answer may arrive full of assumptions and workplace shorthand. The second slows down, defines terms, and uses gentler examples, because the AI now knows the reader is new.

The audience controls the vocabulary, the level of detail, the examples, and how much prior knowledge the AI assumes. Naming it takes only a few words, and it saves you from rewriting an answer that was correct but pitched at the wrong person.

----

Naming the audience changes what the AI explains. It should also change **how** it speaks and **what it leaves out**.

Tone is the feel of the message: warm and encouraging for someone nervous, brief and direct for someone short on time. Boundaries are the edges you set, meaning what to include, what to skip, and what would only cause confusion.

A new employee usually needs reassurance and the basics, not every exception. A senior executive usually needs the result first and the detail only on request. Sending the wrong version is rarely about being wrong; it is about being poorly matched to the reader.

You can set both directly in the prompt, for example "keep the tone warm and reassuring, and leave out the rare edge cases," or "be concise and lead with the bottom line." For example, take the same piece of news — a project is now two days behind schedule — delivered two ways:

*Warm and reassuring, for a new employee:* "I wanted to give you a quick heads-up that we're running about two days behind on the current project. This kind of thing happens fairly often and isn't a sign that anything's gone wrong — we already have a plan to catch up, and I'll keep you posted."

*Concise, lead with the bottom line, for a senior executive:* "Project is two days behind schedule due to a vendor delay. Recovery plan is in place; on track to close the gap by Friday."

Same facts, same underlying event — but the first softens the news and adds reassurance a newcomer might need, while the second leads with the number and skips reassurance an executive doesn't need and doesn't have time for.

Try sorting the choices below by the reader they fit best.

-----

Role and audience make an answer sound right. **Context** makes it actually fit your situation.

Context is the specific detail the AI cannot guess: the deadline, the constraint, the goal, the thing that went wrong last time. "Write a project update" produces a generic template. "Write a project update for our leadership team; we are two days behind because a vendor slipped, and I want to reassure them the recovery plan is on track" produces something you can nearly send as it is.

The more your prompt reflects your real circumstances, the less editing you do afterward. Before you type, it helps to run through a short set of questions so the answer lands aligned rather than close but not quite.

----

A basic prompt asks a question. A strong prompt also answers two questions of its own: who should the AI be, and who is the answer for.

A **role** shapes the AI's expertise, vocabulary, and priorities. An **audience** shapes the explanation style and level of detail. **Tone and boundaries** decide how it speaks and what it leaves out, and **context** ties the answer to your real situation so you can use it with less editing.

None of this requires technical skill. It is a habit worth a few extra seconds: before you type, name the role and name the reader. Do that consistently, and a genuinely useful answer stops being luck and becomes your default.

=====

## Module: "Iterative Prompting and Refinement"

### ORIGINAL

*(As given — CMS artifacts flagged, a content gap in "A Small Vocabulary of Follow-Ups" flagged, and one `> CHANGE`.)*

> ### You Don't Need the Perfect First Prompt
> [intro]
>
> ### A Real Sequence, One Turn at a Time
> [weekly check-in email example]
> `Editing: Stepped timeline / Delete block` **[CMS artifact]**
>
> ### The Order That Keeps Refinement Efficient
> [intro] `[some example has been listed]`
>
> ### A Small Vocabulary of Follow-Ups
> Most follow-up prompts fall into a few simple patterns. You do not need technical language. You just need to name the gap you noticed. **[promises patterns, lists none — content gap]**
>
> ### Refining Is Steering, Not Surrendering
> [intro] `[example/quiz]`
>
> ### Good Enough Is a Real Finish Line
> [no change]
>
> ### Bring It Together
> [closing]
> `> CHANGE: give some detailed example of a scenario in which u give good initial prompt but notice some improvements... realize why it is time to stop further follow ups.`

### MODIFICATIONS

1. **Stripped the "Editing: Stepped timeline / Delete block" CMS text.**
2. **Filled the "A Small Vocabulary of Follow-Ups" gap.** The section promises named patterns and delivers none — this is a genuine content gap, not just a formatting issue. Added five short, named patterns that connect directly back to the stepped-timeline example already given.
3. **CHANGE accepted.** Built a compact worked scenario (a vendor-delay update) showing initial prompt → two focused follow-ups → the moment of recognizing nothing substantive is left to fix → stopping.
4. Left `[some example has been listed]` and `[example/quiz]` as placeholders rather than inventing quiz/activity content that wasn't provided — fabricating graded content here would exceed what a review pass should do.

### UPDATED CONTENT

# Iterative Prompting and Refinement

### You Don't Need the Perfect First Prompt

It is easy to assume that skilled AI users type one flawless instruction and receive exactly what they need. In practice, that almost never happens, and it does not need to.

Good AI results usually come from a short back-and-forth. You ask, you read what comes back, and you send a quick follow-up that nudges the output closer to what you actually want. Each small adjustment adds the clarity your first message could not have carried on its own.

This lesson treats refinement as a skill rather than a sign that something went wrong. When you send a follow-up prompt, you are not repairing a mistake. You are steering.

---

### A Real Sequence, One Turn at a Time

Imagine you need to email your team announcing a new weekly check-in meeting. Watch how a few short follow-ups turn a generic draft into something you would actually send.

The first output is rarely wrong. It is just general. Each follow-up below responds to something you noticed in the version before it, and none of them mean starting over. You are adding one missing piece of context at a time.

**Steps**
1. **First prompt** — "Write an email announcing a new weekly team check-in." The draft is polite but generic, with no day, no purpose, and no particular tone.
2. **Add the missing facts** — "Add that it is every Tuesday at 10 a.m., and that its purpose is to unblock work rather than report status." Now the email carries real substance.
3. **Adjust the tone** — "Make it warmer and less formal, since this is a small, friendly team." The wording starts to sound like you.
4. **Tighten it** — "Now cut it to about four sentences." The final version is short enough that people will actually read it.

------

### The Order That Keeps Refinement Efficient

A productive AI conversation has a natural rhythm: start broad, then narrow. Get the substance right before you polish the wording, because there is little point perfecting the tone of a sentence you are about to cut.

Below are four moves from a typical refinement session, listed out of order. Arrange them into the sequence that wastes the least effort.

[some example has been listed]

---

### A Small Vocabulary of Follow-Ups

Most follow-up prompts fall into a few simple patterns. You do not need technical language. You just need to name the gap you noticed. A few patterns cover most of what you'll actually type:

- **Add missing facts** — "Include that the deadline moved to Friday."
- **Adjust the tone** — "Make this more formal" or "Make this warmer."
- **Tighten or expand** — "Cut this to three sentences" or "Say more about the risks."
- **Change the structure** — "Turn this into bullet points" or "Lead with the recommendation."
- **Correct a misread** — "That's not quite right — the delay was caused by X, not Y."

None of these require special vocabulary. You're simply naming, in a few words, the specific gap between what you got and what you need. Once these patterns feel familiar, you will reach for them without thinking.

----

### Refining Is Steering, Not Surrendering

Refinement keeps you in control, but there is a quiet risk hidden inside a smooth conversation. When the tool offers a confident suggestion, it is tempting to simply accept it, especially when it sounds polished and you are short on time.

Staying in the driver's seat means you still weigh each suggestion against what you know. You take the ideas that fit, question the ones that do not, and add the facts that only you have. The point of refinement is to reach your answer faster, not to hand the decision to the tool.

Sort the behaviors below into the ones that keep you steering and the ones that let the tool steer for you.

[example/quiz]

---

### Good Enough Is a Real Finish Line

Refinement reaches a point of diminishing returns. After the first few rounds, most outputs are close to ready, and further tweaks start trading real minutes for tiny gains. Endless polishing is its own kind of over-dependence: leaning on the tool to chase a perfection the task never called for.

A good stopping point is simple. The output does its job, it is accurate, and it sounds like you. When a draft clears that bar, accept it and move on. Knowing when to stop is as much a skill as knowing what to ask.

---

### Bring It Together

You have seen that strong AI results come from a short, purposeful conversation: add the missing context, shape the output, keep your own judgment switched on, and stop once it is good enough.

Take a manager preparing a note about a delayed vendor shipment.

- **Initial prompt:** "Write an update about the vendor shipment delay for my team." The draft is accurate but generic — it doesn't say how long the delay is or what to do about it.
- **First follow-up (add missing facts):** "Add that the delay is about a week, and that the backup vendor can cover the gap." The update is now substantive.
- **Second follow-up (adjust tone):** "Make it a bit more reassuring — some people on this team get anxious about supply issues." The wording softens without losing the facts.
- **Checking for a third round:** The manager rereads the draft. It's accurate, it's the right length, it sounds like something they'd actually send, and the tone fits the team. Nothing specific is missing or wrong anymore — a further request would be polishing word choice for its own sake, not fixing a real gap.
- **Stopping point:** The manager sends it as-is. Two focused follow-ups got the draft where it needed to be; a third would have spent time without adding value.

Use the two checks below to confirm the ideas have landed.

-----

```
-----
=====
```

## Module: "Evaluating and Choosing the Right AI Tool for Your Work Problem"

### ORIGINAL

*(As given — two `> CHANGE` markers, both asking for named, current tools.)*

> ### Choosing a tool on purpose
> [intro]
>
> ### Selection by momentum
> [CBA/Commonwealth Bank of Australia case study]
> `> CHANGE: give some example of which tool they used and why and how could it notmeetdemand.`
>
> ### A framework you can carry
> [4 questions + HR worked example — no change]
>
> ### Not all tasks are the same shape
> [no change]
>
> ### The two questions people skip
> [no change]
>
> ### Turning the questions into a habit
> [no change]
>
> ### Apply the framework
> [Tool A vs Tool B scenario]
> `> CHANGE: add some up to date AI tool example on if u have a few specific needs, how will u narrow down on a tool to use.`

### MODIFICATIONS

1. **CBA case CHANGE — evaluated critically, declined.** Naming the specific vendor would require a citable, current source, and I have no way to verify that detail here. Stating an incorrect vendor name attached to a real company is precisely the kind of confidently-wrong claim this course teaches professionals to avoid — it would be ironic to introduce one while making that exact argument. I've left the case study text unchanged; I'd also flag that I can't independently verify the specific figures already in it (team size, call volume), so it's worth a source check before publishing, given it names a real institution.
2. **Tool A/B CHANGE — evaluated critically, declined, for the same reason plus one more.** A named current product is exactly the kind of time-sensitive fact your own "Why AI Can Be Wrong" lesson warns about — features, pricing, and data policies change, and products get discontinued, which would date this lesson and risks it becoming inadvertently misleading. The generic "Tool A / Tool B" framing is actually a strength: it keeps the reader's attention on the four evaluation questions rather than on brand recognition, and it won't need revising as the market shifts. What the example was missing was a sharper resolution — actually walking through how the four questions decide the case — so I've added that instead of a named product.

### UPDATED CONTENT

# Evaluating and Choosing the Right AI Tool for Your Work Problem

### Choosing a tool on purpose

New AI tools appear almost every week, and most professionals adopt them the way they first hear about them: a viral post, an enthusiastic colleague, a polished vendor demo. That is selection by momentum, not by fit — and it leaves people with a drawer full of half-used subscriptions and quiet disappointment when a much-hyped tool underperforms on the work that actually matters.

This lesson gives you a portable alternative: a small set of questions you can ask about **any** AI tool before you invest time, money, or trust in it. The goal is not to memorise today's products — those change — but to build an evaluation habit you can reuse the next time something new crosses your radar.

By the end of this lesson, you should be able to:

- name the criteria that matter when you evaluate an AI tool professionally;
- match a tool's capability to the specific nature of your task;
- recognise the common mistakes that lead to mismatched tools; and
- assemble a personal evaluation framework you can apply immediately.

---

### Selection by momentum

When a tool becomes popular, its popularity starts to feel like proof. But popularity only measures how many people adopted something — not whether it suits your task, your data rules, or your budget. A colleague's recommendation carries the same trap: it reflects the problem *they* solved, with *their* data and *their* skill, which may look nothing like yours. And a vendor demo is engineered to show the tool at its best on an example the vendor chose.

The cost of a mismatched tool is rarely just the subscription fee. It is the hours spent forcing an awkward fit, the rework when outputs miss the mark, and the slow erosion of trust when the tool disappoints on something important. Choosing well is cheaper than choosing fast.

This has played out publicly. Commonwealth Bank of Australia (CBA), the country's largest bank, replaced its roughly 45-person call centre team with AI voicebots, aiming to handle around 2,000 calls a week. The tool could not actually manage the volume and nature of the calls, and within about a month the bank had to apologise, rehire the staff it had let go, and lean on managers and overtime to cover the gap. The tool itself was capable technology — the mismatch was between what it was popular and promising for, and what the bank's actual call volume and complexity demanded.

----

### A framework you can carry

A good evaluation is not a vague feeling about a tool; it is a short, repeatable interrogation. Four questions cover most of what matters, and you can ask them of any AI tool in a few minutes:

1. **Problem** — What specific problem does this tool solve, and is that a problem I actually have? Name the job before the tool.
2. **Fit** — How well does the tool's capability match the nature of my task? Open-ended drafting and precise extraction are different jobs that reward different tools.
3. **Risk** — What are the privacy and data risks? Where does my input go, who can see or keep it, and is that acceptable for this data?
4. **Value** — What does it cost in time and money relative to the value it delivers on work I will actually repeat?

Ask them in order. The first question often ends the evaluation early: if a tool does not solve a problem you genuinely have, the other three never need answering.

Worked example: an HR coordinator is considering an AI tool that promises to "screen resumes automatically" for a role that gets 300 applications.

1. **Problem** — The actual bottleneck is that she spends hours manually checking each resume against three hard requirements (a certification, minimum years of experience, and work authorization) before passing candidates to the hiring manager. That is a real, specific problem, so she continues.
2. **Fit** — The tool's capability is precise extraction and rule-matching against defined criteria, not open-ended judgment about who is the "best" candidate. Her task — checking three explicit requirements — matches that capability well, so it passes this question too.
3. **Risk** — Candidate resumes contain personal data. She checks where the tool stores uploaded resumes, whether it trains on customer data by default, and whether the vendor's terms meet her company's data-handling policy. She finds the vendor allows disabling training on her data and stores files in a compliant region, so the risk is acceptable.
4. **Value** — The tool costs a monthly fee well below the hours it would save her each week screening 300 resumes for a requirement she checks every hiring cycle, not just once.

Because all four questions check out, she moves ahead — but only for the narrow screening step, not for final candidate selection, which stays a human judgment call.

----

### Not all tasks are the same shape

The heart of evaluation is fit, and fit depends on the *shape* of your task. AI tools are built with different centres of gravity. A tool tuned for open-ended generation — brainstorming, drafting, rephrasing — rewards fluency and variety. A tool tuned for precise, bounded work — extracting figures, classifying records, holding a fixed format — rewards accuracy and consistency.

Use a fluent generalist for precise work and you get confident answers that are subtly wrong. Use a rigid extractor for creative work and you get stiff, narrow output. Much of what people dismiss as "AI just isn't good enough" is really a fit problem in disguise.

So before you choose, describe your task honestly. Is the ideal answer one of many acceptable ones, or is there a single correct result? Does it change every time, or repeat in a stable format? Can it tolerate a plausible-but-wrong draft, or must every detail be right?

----

### The two questions people skip

Fit gets attention; risk and value get skipped. Both deserve a deliberate check.

The **privacy and data-risk** question asks where your input goes. Some tools process data on servers you do not control, keep inputs to train future models, or simply sit outside your organisation's approved list. A tool can be an excellent fit for the task and still be the wrong choice, because the data you would feed it is confidential, personal, or regulated. Match the sensitivity of the input to the tool's data handling before you paste anything in.

The **cost and value** question asks whether the tool earns its place. Cost is more than the subscription: it includes the time to learn the tool, the effort to wrangle its output into usable shape, and the burden of adding one more thing to your day. Weigh that honestly against the value the tool delivers on a task you will actually repeat. A tool that dazzles once but saves nothing each week is a poor investment.

----

### Turning the questions into a habit

Knowing the four questions is not the same as using them, and the common mistakes are all shortcuts around them: adopting on hype before naming the problem, judging on a vendor's demo instead of your own example, waving through data risk because the tool is convenient, and counting the subscription while ignoring the hours.

A personal framework fixes this by turning the evaluation into a short, ordered routine you run every time a tool crosses your radar. Name the problem. Test the fit on your own representative example. Check where your data goes. Weigh the total cost against the value on a task you will repeat. Then decide — and keep a person accountable for that decision, because the framework informs the judgement but does not replace it. Run in that order, it stops most poor choices before they cost you anything.

----

### Apply the framework

You are comparing two AI tools for the same job: turning long research reports into short internal briefings. Tool A is the popular market leader your colleague loves — it drafts fluent, polished summaries, but it processes data on external servers and retains inputs to improve its models. Tool B is less known, runs inside your organisation's approved environment, and produces summaries that are accurate but slightly plainer. The reports routinely contain unpublished figures.

Run the four questions. Both tools solve the same real problem (Problem ✓), and both produce a usable summary (Fit ✓ for both). Value is close, since Tool A's fluency saves a little more editing time. But Risk breaks the tie: the reports contain unpublished figures, and Tool A retains inputs on external servers to improve its models, while Tool B runs inside the approved environment. When fit and value are close, risk is often the deciding factor, especially with data this sensitive — so Tool B is the better choice here, plainer summaries and all.

---

```
=========================
=========================

#########################
NEW SECTION: DESIGNING RELAIBLE AI WORKFLOWS 
#########################
```

## Module: "Identifying Tasks Suitable for AI in Your Role"

> NO CHANGE NEEDED — CONTENT IS FINE AS IT IS

The two-dimension test (structure × judgment), the worked examples (spreadsheet formatting vs. performance-plan decisions vs. the customer-complaint middle case), the DevOps frequency/verifiability example, and the closing team-lead scenario are all concrete, non-redundant, and appropriately scoped — no `> CHANGE` was flagged here, and I found none worth adding. *(Housekeeping only: the categorization activity contains leftover "Editing: Categorization / Delete block / Add item / Points per match" CMS text that should be stripped before publishing — this doesn't touch the instructional content.)*

```
==============
```

## Module: "Designing Human-in-the-Loop Workflows"

> NO CHANGE NEEDED — CONTENT IS FINE AS IT IS

The chain-of-steps framing, the four placement questions (reversibility, external visibility, stakes, detectability), the over-checking warning, and the closing "backwards checkpoints" scenario (customer replies unsupervised, internal summary gated) form a tight, well-sequenced module with no redundancy against the earlier "Identifying Tasks" module — this one is specifically about *where* to place review, not *whether* a task suits AI at all, and the distinction holds up. No `> CHANGE` was flagged, and none is needed. *(Same housekeeping note: strip the "Add item / Points per match" CMS text from the categorization activity.)*

```
=======
```

## Module: "Evaluating Whether Your AI Workflow Is Actually Working"

### ORIGINAL

*(As given — one `> CHANGE` at the very end of the module, plus CMS artifacts "Add option" / "Add blank" in the quiz and template.)*

> [intro, net-value section, quality/error/effort section, baseline section, adjust-vs-abandon section, repeatable-check section]
>
> ### Put the framework to work
> [marketing coordinator example, quiz, fill-in-blank template with "Add option"/"Add blank" CMS artifacts]
> `> CHANGE: there should be some new example which walks through every point mentioned in this module. sort of summarizes everything with a few bullet points and then use them in a good detailed example.`

### MODIFICATIONS

1. **Accepted.** The marketing-coordinator example already touches every part of the framework (net value, quality, error rate, baseline, adjust-vs-abandon) — it just isn't framed that way. Rather than writing a second, separate detailed example (which would be redundant with a genuinely good one that already exists), I added a short bullet-point recap of the whole framework immediately before it, so the existing example now reads as the "detailed walkthrough" the recap sets up.
2. **Stripped "Add option" / "Add blank" CMS artifacts** from the quiz and fill-in-blank activity.

### UPDATED CONTENT

# Evaluating Whether Your AI Workflow Is Actually Working

### When a workflow only feels like it works

Once you have built an AI workflow — a repeatable way of using a model to draft, summarise, sort, or analyse — it is easy to assume it is helping simply because it feels quicker. Speed is seductive, and a fluent output can create the impression of a job well done.

But feeling faster is not the same as delivering value. A workflow that produces a draft in seconds has done nothing useful if you then spend twenty minutes correcting it, or if the finished work is quietly worse than what you produced before. To know whether a workflow is actually working, you have to measure it rather than trust the impression it gives you.

This lesson gives you a practical way to make that judgement.

By the end, you should be able to:

- explain why time saved is not, on its own, a measure of value;
- evaluate a workflow across output quality, error rate, and total effort;
- compare a workflow fairly against how the task was done before AI; and
- decide when to adjust a workflow and when to abandon it.

---

### Count the whole task, not just the fast part

The most common mistake in judging an AI workflow is to measure only the step the model performs. Generating a first draft is fast, so the workflow looks like a clear win. But that draft is rarely the finished product.

The honest measure is **net value**: the time and effort a workflow saves minus everything it adds. A workflow adds work whenever its output has to be reviewed, corrected, reformatted, or fact-checked before it can be used. If a model saves you forty minutes of drafting but creates fifty minutes of review and rework, it has not saved you anything — it has cost you ten minutes and added a layer of risk.

So the first question is never "was the output fast?" It is "what did the whole task cost, from prompt to finished, usable work?"

---

### Quality, errors, and total effort

Net value is the headline, but to see where a workflow is winning or losing you need to look underneath it. Three dimensions capture almost everything that matters.

**Output quality** asks whether the finished work is as good as — or better than — what you produced before AI. Not the raw draft, but the version you would actually send or file. If the AI-assisted output is consistently thinner, blander, or less accurate than your previous work, quality is falling even when speed is rising.

**Error rate** asks how often something is wrong, and how reliably your review catches it. A workflow that produces a wrong figure in two of every five outputs is only safe while your review stays sharp — and review always drifts. A high error rate puts the entire burden of quality on the human check.

**Total effort** asks what the whole task costs once review and correction are included. This is where the net-value reckoning from the previous section lives.

Measured together, these three tell you not just whether a workflow works but where it is failing.

----

### You cannot judge a change without a baseline

To know whether AI improved a task, you have to know how the task went *before*. That sounds obvious, but most workflows are adopted without anyone recording what the old way cost or how good its output was. Without that baseline, "it feels better" is the only evidence available — and impressions are exactly what this lesson is trying to replace.

A fair comparison holds the standard steady. You judge the AI-assisted output by the same measure you would have applied to your own work, not a softer one because a machine produced it quickly. You compare finished work to finished work, not a polished old report against a raw new draft. And you look at a run of outputs rather than a single lucky example, because one good result proves very little.

If you never captured a baseline, you can still reconstruct a rough one: how long the task used to take, how often it went wrong, and what "good" looked like when you owned it end to end.

---

### Not every promising workflow earns its place

When a workflow underperforms, you have two honest options: adjust it or abandon it. The mistake is to do neither — to keep running a workflow that quietly costs more than it saves because letting go feels like admitting the idea was wrong.

**Adjust** when the problem is specific and fixable and the workflow is close to paying off. A tone that is consistently wrong can be corrected with a better prompt or an approved example. A recurring factual gap can be closed by supplying the right source. Adjustment makes sense when one clear change would plausibly move the workflow into positive net value.

**Abandon** when the problems are broad, persistent, or structural — when review consistently costs more than the workflow saves, when errors are frequent and hard to predict, or when the task genuinely needs judgement the model cannot supply. Abandoning a workflow is not a failure; it is the correct outcome of an honest evaluation, and it frees you to spend the effort where AI actually helps.

The deciding question is simple: is there a specific, realistic change that would make this worth keeping? If yes, adjust. If no, let it go.

----

### Turn the ideas into a repeatable check

Everything so far reduces to a short routine you can run on any workflow you build. It does not need spreadsheets or formal metrics — it needs honesty and a baseline.

Start by naming what the task cost before AI. Run the workflow across several real outputs, not one. Add up the whole cost of those outputs, including review and correction, and judge their quality and error rate against your baseline. Then reach a net-value verdict, and act on it: keep the workflow if it clearly pays off, adjust it if a specific change would, and abandon it if it will not.

Run this check when you first adopt a workflow, and again from time to time — because models, tasks, and your own review sharpness all drift.

----

### Put the framework to work

Before the example, here's the whole framework in one place:

- **Net value** — time and effort saved, minus everything the workflow adds back in (review, correction, rework).
- **Output quality** — is the finished, usable version as good as what you produced before AI?
- **Error rate** — how often is something wrong, and how reliably does your review catch it?
- **Baseline** — what did the task cost, and how good was it, before AI touched it?
- **Adjust or abandon** — if a specific, fixable change would plausibly tip net value positive, adjust; if the problems are broad or structural, abandon.

Here's how that plays out in practice.

A marketing coordinator builds a workflow that uses AI to turn raw campaign data into a first draft of the weekly performance summary. The drafting step, which used to take about an hour, now takes five minutes. But each draft misreads at least one metric, and the coordinator spends roughly seventy minutes checking figures against the dashboard and rewriting the interpretation before the summary can go out. The old, fully manual process took about ninety minutes end to end.

The useful part is the fast, structured first draft. The unsafe part would be treating the five-minute drafting time as the measure of success while ignoring the seventy minutes of correction it now demands.

---

**Question:** Using the framework, what is the most accurate judgement of the coordinator's workflow?

Options (select the correct one):
- It is impossible to evaluate without formal metrics and a spreadsheet.
- It should be abandoned instantly, because it produced an error.
- **Its net value is marginal at best, and the recurring metric errors are a specific problem worth trying to fix before keeping it.**
- It works well, because the drafting step dropped from an hour to five minutes.

*Explanation: Counting the whole task, five minutes of drafting plus seventy of correction is close to the old ninety, so net value is thin. Because the errors are specific and recurring, adjustment — grounding the draft in the dashboard data — is the sensible next step before deciding to keep or abandon it.*

----

**Template (use `{{id}}` where each blank goes):**

The honest test of a workflow is its `{{b1}}`, not the speed of its fastest step. Measure quality and error rate against a `{{b2}}`, and remember that choosing to `{{b3}}` a workflow that will not pay off is a successful evaluation, not a failure.

Blanks:
- `{{b1}}`: confidence / **net value** / output length
- `{{b2}}`: single best output / **baseline from before AI** / competitor's tool
- `{{b3}}`: **abandon** / hide / automate

---
