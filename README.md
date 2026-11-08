# Fluent Writing for AI

[English](README.md) | [한국어](README.ko.md)

Writing skills for AI assistants that turn research, analysis, and implementation work into documents people can understand and evaluate.

The central principle is simple: choose and organize information around what the reader needs to understand, decide, or do.

## Use cases

- **Documents shared with other people:** reports, proposals, design notes, and handovers for readers who did not participate in the work.
- **Documents for reviewing AI work:** explanations that let you assess an assistant's findings, methods, and decisions without reconstructing the conversation or inspecting every intermediate step.

In both cases, the document should stand on its own, with the context, evidence, and conditions needed to assess its conclusions.

## Skills

| Skill | Focus |
|---|---|
| [fluent-english](skills/fluent-english/SKILL.md) | Reader-focused document writing and revision in English |
| [fluent-korean](skills/fluent-korean/SKILL.md) | The same writing principles, with additional guidance on Korean wording and terminology |

Both apply to document drafting and editing, including drafts written in chat. They are not applied to ordinary conversation, simple Q&A, or progress updates solely because of the language used.

## Writing philosophy

- **The reader's purpose determines the content.** Select information that helps the reader understand, assess, or act on the result.
- **The final findings determine the explanation.** Distinguish current facts from hypotheses and abandoned options. Investigation order and source-file boundaries should not become the outline.
- **Relationships need a reason.** Use comparisons, contrasts, categories, stages, and divisions of responsibility when they are supported and useful. Do not invent them to make a sentence or document sound more convincing.
- **Concision retains meaning.** Keep the scope, conditions, uncertainty, and supporting evidence that determine what a claim means.
- **Revisions belong in the document.** Integrate feedback into the relevant discussion and update affected summaries, conclusions, and tables together.

## Practical methods

### Review without the work history

For a document produced after complex work:

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
