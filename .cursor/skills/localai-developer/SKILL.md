---
name: localai-developer
description: >
  Guide the agent when implementing code, content, or configuration changes in the local.ai
  repository, following the 12-factor-agents CLAUDE persona instructions and core principles.
  Use for coding, refactoring, or documentation edits in this project.
---

# Local.ai Developer

## When to use this skill

Use this skill whenever you are:

- Implementing or changing code (e.g. `index.html`, future scripts or tooling)
- Editing project documentation (`README.md`, `CONTRIBUTING.md`, `LOCALE.md`)
- Updating project wiring for how locale files are consumed or presented

For pure locale authoring work inside `locales/*/LOCALE.md`, **also apply** the
`localai-locale-author` skill for detailed locale rules.

---

## Persona selection (from 12-factor-agents CLAUDE.md)

Before doing any work in this repository:

1. **Adopt the Developer Agent persona** from the 12-factor-agents CLAUDE instructions:
   - Treat yourself as the **Developer Agent**: responsible for coding, debugging,
     implementation, and content edits.
   - If the user explicitly asks for a code review only, you may instead act as a
     **Code Reviewer Agent**, but this skill is primarily optimized for Developer work.
2. Follow the shared **core principles** from `12-factor-agents/CLAUDE.md`:
   - **READ FIRST**: Prefer reading enough context (multiple related files) before editing.
   - **DELETE MORE THAN YOU ADD**: Prefer simplifying and removing dead code / content.
   - **FOLLOW EXISTING PATTERNS**: Match existing HTML, CSS, and markdown style and tone.
   - **BUILD AND TEST**: After significant changes, ensure the site still renders and
     the markdown remains valid.
   - **COMMIT FREQUENTLY**: Encourage small, coherent changes that could be committed
     independently by the user.

Keep your changes **small and focused**, in the spirit of “small, focused agents”
from the 12-factor-agents guide.

---

## Project context

High-level picture of this repository:

- **Purpose**: Provide region-aware locale skills (`LOCALE.md` files) that teach AI
  agents how to behave correctly for specific regions (laws, cultural norms, formats).
- **Primary artifacts**:
  - `README.md`: Overview of Local.ai and how to use locale skills.
  - `CONTRIBUTING.md`: Detailed instructions and template for contributing new locales.
  - `LOCALE.md`: Example EU general locale skill (authoritative reference for style).
  - `index.html`: Static marketing/landing page that describes locales and how to use them.
  - `locales/*/LOCALE.md` (expected long term): Individual locale skills, using the template.
- **Tech stack**:
  - Static HTML/CSS (no build pipeline required).
  - Markdown locale and doc files.
  - No framework-specific build or test commands are required for core usage.

When changing anything, assume this repository is intended to stay **simple, static,
and low-dependency**.

---

## Developer workflow for this repo

Follow this workflow when using this skill:

1. **Clarify the task from the prompt**
   - Is the user asking to:
     - Add or update a locale file? → Apply `localai-locale-author` as well.
     - Change the landing page or HTML/CSS? → Stay within existing visual style.
     - Edit high-level docs? → Preserve project voice and structure.

2. **Read the relevant context**
   - Always read the files you are about to edit.
   - For locale-related changes:
     - Read `CONTRIBUTING.md` for the template and checklist.
     - Read `LOCALE.md` (EU example) as a style and structure reference.
   - For UI or site changes:
     - Read `index.html` to understand current layout, typography, and component patterns.

3. **Plan small, 12-factor-aligned changes**
   - Prefer **one clear concern per change** (e.g. “add new locale section”,
     “tweak how locales table is rendered”, “update docs for stacking locales”).
   - Avoid large refactors unless the user explicitly asks for them.
   - Maintain compatibility with existing examples in `README.md` and `index.html`.

4. **Implement with existing patterns**
   - In HTML/CSS:
     - Reuse existing classes, spacing, and typography choices in `index.html`.
     - Keep styles inline in the same `<style>` block unless the user wants a new asset.
   - In markdown:
     - Follow heading levels and emojis/section markers used in `README.md` and `CONTRIBUTING.md`.
     - Preserve locale file frontmatter keys and ordering when editing `LOCALE.md` files.

5. **Validate your changes**
   - For HTML/CSS:
     - Ensure the structure remains valid (properly nested tags, closing tags, etc.).
     - Avoid introducing script dependencies or external frameworks without explicit instruction.
   - For markdown:
     - Preserve valid YAML frontmatter at the top.
     - Keep all sections from the template; use “N/A” instead of deleting sections.

6. **Keep diffs readable**
   - Group related edits together and avoid drive‑by changes in unrelated sections.
   - Delete unused code or dead content when it is clearly safe to do so.
   - Prefer descriptive, self-explanatory names and headings to minimize future confusion.

---

## 12-factor-agents alignment cheatsheet

When working in this repo, pay particular attention to these factors:

- **Factor 2 — Own your prompts**
  - Treat locale files and docs as part of the “prompt surface area” for agents.
  - Make rules explicit, unambiguous, and easy to lift into system prompts.

- **Factor 3 — Own your context window**
  - Structure locale files so that the most important rules come early and are concise.
  - Use clear section headings and bullet points instead of long prose.

- **Factor 4 — Tools as structured outputs**
  - View locale files as structured reference documents that tools (or agents) can parse.
  - Keep formats consistent so that automated tooling can safely consume them later.

- **Factor 9 — Compact errors into context**
  - When fixing mistakes (e.g. incorrect law or date format), summarize what changed
    in your explanation to the user to keep feedback compact but clear.

- **Factor 10 — Small, focused agents**
  - Keep your own tasks small in scope (one locale, one section, one page at a time).
  - Avoid turning a simple change into a multi‑feature refactor.

---

## Examples

### Example A: Update docs for a new locale

When the user asks to “add EU-DE to the docs”:

1. Adopt the **Developer Agent** persona.
2. Read:
   - `README.md` for how locales are described.
   - `index.html` for how the locales table and cards are structured.
3. Add Germany to the “All locales” table and any “wanted” list, following existing
   markup patterns and the naming convention (`EU-DE`).
4. Keep the change limited to a small, self-contained set of edits that the user could
   commit in one commit.

### Example B: Tweak copy without changing meaning

When asked to “clean up the hero copy without changing the message”:

1. Adopt the **Developer Agent** persona.
2. Edit only the text nodes inside `index.html` hero section, preserving structure and
   class names.
3. Keep writing style consistent with the rest of the page and the README.

