# Technical Design Skill

A Codex skill for turning product requirements and a frontend repository into a focused, visual-first frontend technical design in one HTML file. It adapts the writing principles in the user's source document, *如何写好技术文档*, to design reviews.

## Install

Clone the repository into the Codex skills directory, then start a new Codex session:

```bash
git clone https://github.com/jsspace/technical-design-skill.git ~/.codex/skills/technical-design-skill
```

## Use

Provide the requirement, the relevant frontend repository, and the desired output path. For example:

> Use $technical-design-skill with this product requirement and the current frontend repository. Write a Chinese technical design for the advertising strategy settings page to `docs/ad-strategy-design.html`. The requirement URL is `https://example.com/requirements`.

The skill chooses design subsections from the feature rather than following a fixed flow/components/code template. It keeps the top-level reading path at **Background → Benefits → Design**, uses short numbered design headings, and emphasizes the key problem and target. The starter uses a restrained warm-neutral reading style; a compact hierarchical contents control sits outside a wider centered article. Diagrams show only decisive relationships, with every branch checked against its explanation. Supporting lists carry details. API integration is included where needed without turning the document into a backend design.

## Files

- [`SKILL.md`](SKILL.md): Instructions used by Codex.
- [`references/writing-principles.md`](references/writing-principles.md): Editorial and visual decisions.
- [`assets/technical-design-template.html`](assets/technical-design-template.html): Optional HTML styling starter. Its design subsection is an example pattern, not a required outline.

The source Word file and screenshots are not redistributed in this repository.
