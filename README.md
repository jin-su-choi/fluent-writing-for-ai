# Fluent Writing for AI

[English](README.md) | [한국어](README.ko.md)

Writing skills for AI assistants, designed for documents shared with others and for reviewing AI work. They guide the assistant to select the information a reader needs, explain it in a useful order, and retain the evidence and conditions needed to assess the results.

## Use cases

- **Documents shared with other people:** reports, proposals, design notes, and handovers for readers who did not participate in the work.
- **Documents for reviewing AI work:** explanations that let you assess an assistant's findings, methods, and decisions without reconstructing the conversation or inspecting every intermediate step.

## Skills

| Skill | Focus |
|---|---|
| [fluent-english](skills/fluent-english/SKILL.md) | Reader-focused document writing and revision in English |
| [fluent-korean](skills/fluent-korean/SKILL.md) | The same writing principles, with additional guidance on Korean wording and terminology |

Both apply to document drafting and editing, including drafts written in chat. They are not applied to ordinary conversation, simple Q&A, or progress updates solely because of the language used.

## Writing philosophy

The reader's questions determine which information belongs in the document and in what order. Both language versions address these recurring AI writing habits:

| Recurring AI habit | Writing principle |
|---|---|
| Organizing a report around the order of investigation and revision | Select the final findings and arrange them in the order the reader needs. |
| Assuming readers know the writer's background context | Use only the reader's established knowledge and the preceding text; introduce necessary premises first. |
| Inventing comparisons, contrasts, categories, or roles to sound convincing | Check whether each relationship is supported and useful; explain actual functions and behavior directly. |
| Using "not X but Y" for unnecessary emphasis | State the point affirmatively and use a contrast only when the distinction matters. |
| Appending feedback as separate "additional notes" | Integrate it into the relevant discussion and update summaries, conclusions, and tables together. |
| Moving essential conditions to the end or hiding them in collapsible sections | Keep the scope and conditions that determine a claim's meaning beside the claim in the main text. |
| Packing several conditions and explanations into one bullet | Separate the shared point from its details and use sub-bullets where needed. |
| Treating structural problems as sentence-polishing or table-formatting problems | Fix information selection and explanation order first, then refine wording and format. |

Keep facts, numbers, scope, uncertainty, and supporting evidence intact when condensing or revising the document.

## Practical methods

### Review without the work history

For a document presenting the final results of complex work:

1. Temporarily remove accounts of the investigation, experiments, implementation history, and rejected alternatives.
2. Read the draft as someone who did not follow that work. Identify specific gaps that prevent understanding or assessment.
3. Restore only the explanations needed to fill those gaps, where the reader needs them.

Keep the evidence and conditions supporting the central claims. The effort spent producing material and the amount of text removed are not reasons to restore entire sections.

### Context at the point of use

- Introduce necessary premises before relying on them.
- Place a claim's scope and conditions beside the claim, even when supporting details are collapsible.
- Keep evidence and alternatives for the same decision together so readers can assess them without assembling the explanation themselves.

### Format that follows the content

- Use short noun phrases for headings.
- Use lists for facts, conditions, and steps that readers need to check individually; use paragraphs for connected explanations.
- Give each bullet a clear main point, with subordinate conditions and examples in sub-bullets.
- Choose tables and collapsible sections when they help readers understand the relationships or inspect the details.

These are flexible writing practices. They do not require a fixed document outline or a rigid sentence count.

## Installation

In Codex, ask the built-in skill installer to install either or both skills:

```text
Use $skill-installer to install skills/fluent-english and skills/fluent-korean
from the GitHub repository jin-su-choi/fluent-writing-for-ai.
```

The installer supports skills from GitHub repositories. See the [Codex installation guidance](https://learn.chatgpt.com/docs/build-skills#install-curated-skills-for-local-use).

## Usage

Invoke the skill with a document-writing request:

```text
$fluent-english
Write a report from the findings in this conversation for teammates who did
not participate. Include the results, methods, and evidence they need to
evaluate the work and decide what to do next.
```

Use `$fluent-korean` for Korean documents. Each skill folder contains the writing instructions in `SKILL.md` and Codex interface metadata in `agents/openai.yaml`.
