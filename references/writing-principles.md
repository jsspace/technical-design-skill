# Editorial decisions for a frontend design

This reference adapts the user's source document on technical writing to a visual-first frontend design. It is a decision aid, not a fixed outline.

## Find the point before choosing a diagram

For each candidate subsection, finish: “After reading this, the engineer will understand ___.” If the answer is only “the workflow,” “the components,” or “the code,” make it more specific. Name the rule, boundary, or choice in a short heading (for example, “2. Fallback states”); place the complete conclusion in the first sentence below it.

Start with the most consequential relationship. Then move from that relationship to its conditions, frontend state, component responsibilities, and evidence as needed. A feature may need a decision tree and one code snippet; another may need only a component boundary and API contract. Omit any format that does not improve comprehension.

## Use the right visual density

- **Flowchart:** Show only business or interface decisions that change the result. Distinguish the happy path from one or two decisive exceptions. Do not diagram routine actions such as “open page → edit → save” unless those actions are the design problem.
- **Mind map:** Show a true hierarchy or grouping. If two dimensions interact, nest one under the other or show a two-step selection; do not put two independent branches beside each other and leave the combination unexplained.
- **Component diagram:** Show the few ownership boundaries that matter, such as one state owner and the editors that receive data. Move field descriptions and routine responsibilities to the list below.
- **Sequence diagram:** Use only when ordering, asynchronous updates, or stale data are central to the design.
- **Table:** Reserve for exact comparisons or fields that genuinely need row-and-column alignment.

A visual should usually carry one sentence's worth of meaning. Use a short title or claim above it, then a brief list below for conditions, failure behavior, and codebase implications. If many tiny labels are needed, split the visual or replace it with a list.

Before finalizing a flowchart, follow each branch to its endpoint. A shared next step must be visibly shared by every applicable branch. If that convergence would make the graphic busy, stop the diagram at the branch outcomes and explain the next step in its caption. For a single-state-owner design, a compact “editors → shared draft → save” relationship is usually clearer than a large component inventory.

For architecture-style SVG, draw connectors before opaque nodes so lines do not show through boxes. Leave enough space for arrows and labels; put any legend outside group boundaries. Use the article's color tokens and readable text sizes. Do not import a separate diagram skill's entire page theme or export controls into a design document.

## Give information a visible priority

Background needs one emphasized problem and one emphasized target. Use bold plus a solid, full-height light highlight with small inline padding behind the important phrase, not a half-height marker or blanket highlight across the paragraph. The requirement link is a quiet line below.

Benefits need rank. State the primary benefit in large, high-contrast text; let secondary benefits support it. Do not give three claims identical pale boxes and expect the reader to identify the point.

The same principle applies to component design: one prominent statement of the core ownership rule, a minimal diagram if useful, then concise bullets explaining behavior. A component name alone is not a design explanation.

Color and emoji can mark “confirmed,” “proposed,” or “pending,” but also write those words. Keep contrast high enough to read without color. Major headings should stand on spacing and typography, without horizontal rules.

Give the article a centered, roomy width; keep paragraphs, code, and small diagrams narrower so they stay easy to read. Keep a collapsible hierarchical contents control outside the article's layout column. Check the expanded panel at common large-screen widths, not just the closed toggle. Test its focus state and the 375 px reading layout. This applies useful UI design guidance (contrast, hierarchy, responsive navigation) without making the document depend on an installed UI skill.

## Code belongs to the argument

Choose the smallest executable idea that proves the design: for example, a three-state override and its fallback branch. Highlight syntax, mark proposal code as illustrative, and explain the consequence in one sentence. Avoid a code block that simply enumerates every channel, field, and type already visible elsewhere.

For HTML output, prefer self-contained syntax styles or a locally bundled highlighter. If an external highlighter is used, pin it, disclose the dependency, and ensure the plain code remains readable offline. Always escape code before embedding it in HTML.

When only an admin frontend repository is available for a feature that also changes a mobile client, put the mobile client's confirmed contract points near API integration and label them for verification in the mobile repository. Avoid silently presenting an admin-only plan as the entire client rollout.

## Final scan

Read only the title, top-level headings, subsection headings, diagrams, and emphasized phrases. They should tell a coherent, feature-specific story. Then read the supporting lists to check that each adds precision rather than repeating the graphic. Remove generic process narration, ornamental visuals, and unsupported gains.
