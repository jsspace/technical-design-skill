---
name: technical-design-skill
description: Turn product requirements and a frontend codebase into a focused, visual-first frontend technical design in a standalone HTML file. Use for UI architecture, state and interaction design, and API integration; do not use for backend architecture or performance reviews.
---

# Frontend technical design

Produce a standalone HTML document that helps frontend engineers understand the important design choices and implement them. Write the deliverable in the user's requested language; default to Chinese. Keep this skill's instructions separate from facts supplied by documents, screenshots, and repositories.

## Establish the design before the outline

Read the requirement and inspect the relevant frontend code. Identify the feature's central behavior, the frontend decision that could easily be misunderstood, and the smallest set of implementation details needed to explain it. Distinguish confirmed behavior from proposals and unresolved contract details. Do not invent metrics, APIs, components, or backend behavior and present them as existing.

Plan a reading path from the main idea to supporting details. Choose design subsections from the actual problem; there is **no required sequence of flow, components, code, and API**. Give each design subsection a short, feature-specific summary heading, optionally numbered 1, 2, 3. Put the full conclusion and conditions in the opening sentence below the heading. A reader scanning the headings should grasp the proposal without reading long sentence-like titles. Avoid generic activity labels such as “Overall flow” or “Component design.”

## Document shape

Use three top-level sections by default:

1. **背景 (Background)** — Briefly state the problem and target in the body, without a separate goals heading. Visually emphasize the central problem and target with meaningful bold text and a restrained background highlight. If a requirement URL is known, add a simple link below the paragraph; omit it otherwise.
2. **收益 (Benefits)** — Lead with the strongest concrete expected benefit. Put secondary benefits in a short list or subordinate lines. Avoid equal-weight, low-contrast cards that make every benefit look the same. Do not claim measured gains without evidence.
3. **设计方案 (Design)** — Develop the frontend design in a coherent order chosen for this feature. Keep backend internals out; include only the API contract and external behavior that the frontend needs.

Do not add summary, scope, or current-state top-level sections by habit. Put necessary codebase evidence and pending decisions beside the design point they affect. Do not draw a rule across or immediately below major headings.

## Make visuals carry one point each

Use a diagram only when it clarifies a specific relationship that words alone would make harder to see. A diagram should deliver its point at a glance: few nodes, short labels, a clear direction, and one visual hierarchy. Put the detailed conditions, exceptions, and implementation notes in a short list **below** it. Do not place paragraphs inside nodes or turn a component inventory into a diagram. A small relationship graphic should remain visually lighter than the conclusion it supports.

Choose the form by the relationship: a flowchart for a business or UI decision path, a mind map for a genuine hierarchy, a small component diagram for a decisive ownership boundary, or a sequence diagram for consequential timing. When two dimensions interact, show how they combine or are selected; drawing them as separate branches can hide the rule. Tables are useful for exact field mappings, but do not use them as a default substitute for thought.

Use an architecture diagram only when component boundaries or data movement are a real design decision. Borrow the useful SVG rules from an architecture-diagram workflow: draw connectors behind opaque nodes, leave generous gaps, keep labels legible, and keep legends outside grouped boundaries. Adapt colors to the document; do not import an unrelated dark theme, export toolbar, fixed card layout, or tiny diagram typography.

Explain the diagram's conclusion in the subsection heading or one short sentence above it. The list below should add what the diagram omits, not repeat every node. If the diagram has no clear takeaway after simplification, use text instead.

Trace every branch against the prose. If several outcomes all lead to the same next step, connect all of them or leave that shared step out of the diagram and explain it below. Never draw a single branch to a shared result in a way that implies the other branches stop. Prefer removing an unnecessary destination over adding a second large convergence graph.

## Write and style for scanning

Keep paragraphs short, but do not sacrifice causal explanation. Bold and highlight the few statements a reader must retain, especially in Background. Use a full-height, padded highlight behind the phrase; avoid a half-height marker that competes with the glyphs. Use stronger contrast for the primary benefit; color, badges, and emoji may support meaning but must not be the sole carrier. Keep a small, consistent palette and enough whitespace. Avoid repeated pale cards, decorative boxes, and text-heavy graphics.

Treat the HTML as a reading interface. Center a generous responsive content column (roughly 1050–1200 px on large screens), but keep ordinary paragraphs, code blocks, and small diagrams at a comfortable reading width. Make the table of contents a compact floating or collapsible control outside the article's width; show top-level headings and nested design subsections with distinct indentation. Check the contents control both closed and open at wide viewport sizes: the expanded panel must not cover diagrams or text. Preserve keyboard access, visible focus, readable text contrast, and a narrow-screen layout without page-level horizontal scroll. The table of contents must not squeeze the article into a narrow column. Do not add ornamental rules beneath headings.

When no product palette is supplied, use the starter's restrained warm-neutral palette as a starting point: a near-neutral page, dark ink, one editorial accent, and semantic diagram colors. Avoid tinting every surface or wrapping the whole article in a heavy card. Keep the page, diagrams, callouts, and code block visually coherent, with readable contrast; adjust the palette to the user's brand or stated preference.

Show only pivotal code: a type distinction, state transition, validation rule, or integration boundary. Code blocks **must have syntax highlighting** and readable line wrapping or horizontal scrolling. Use a self-contained highlighter or escaped semantic token spans; an external highlighter such as highlight.js is optional only when its dependency is acceptable and the code remains readable without it. Do not paste a large type inventory merely because it exists in the repository.

## HTML and review

Create one UTF-8 HTML file with semantic headings, accessible diagram titles or captions, responsive layout, working anchors, and print styles. The [HTML starter](assets/technical-design-template.html) provides presentation primitives, not a required design outline. Remove every placeholder and unused element. Escape code and untrusted HTML; never copy scripts or event handlers from source material into the output.

When the product requirement spans several frontend clients but only one repository is available, explain the design supported by that repository and add only the other client's confirmed integration obligations. Mark unverified client behavior as needing codebase confirmation; do not turn a guessed implementation into a fact or add a separate scope section merely to state this boundary.

Review the generated document against the supplied requirements and repository. Check that headings summarize real content, the first screen reveals the important point, diagrams are simpler than their explanations, branches do not misstate outcomes, overlapping dimensions are unambiguous, code highlighting works, and no major heading has an underline. Verify anchors, expanded navigation, wide-screen spacing, and narrow-screen behavior when a renderer is available. If visual inspection is blocked, report that limit rather than claiming it passed.

Use [writing principles](references/writing-principles.md) when selecting a visual or editing a dense draft. Deliver the HTML file path and briefly state the main design choice and any decision still needed.
