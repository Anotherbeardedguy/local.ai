---
name: localai-locale-author
description: >
  Help the agent add or update locale LOCALE.md files in the local.ai repository using
  the official template, research standards, and quality checklist. Use whenever the user
  asks to create, edit, or review a locale file.
---

# Local.ai Locale Author

## When to use this skill

Use this skill whenever you are:

- Creating a new `locales/ID/LOCALE.md` file for a region, country, or sub-region.
- Updating an existing locale file to fix or expand its rules.
- Reviewing a locale file for completeness, accuracy, or consistency.

Combine this with `localai-developer` for broader project work or when locale changes
are part of a larger change set.

---

## Locale file structure (CONTRIBUTING.md)

Locales follow a consistent, markdown-based structure:

- Each locale lives in its own folder under `locales/`:

  - `locales/EU/LOCALE.md` (EU general)
  - `locales/EU-FI/LOCALE.md` (Finland, extends EU)
  - `locales/EU-UK/LOCALE.md` (United Kingdom)
  - `locales/US-CA/LOCALE.md` (United States & Canada)
  - `locales/YOUR-LOCALE/LOCALE.md` (new locale)

- The `LOCALE.md` file contains:
  - YAML frontmatter with metadata.
  - A set of standardized sections (Date & Time, Currency & Numbers, Legal, etc.).

**Never invent a new structure.** Always follow the template from `CONTRIBUTING.md`.

---

## Frontmatter template

All locale files must start with frontmatter like this:

```markdown
---
name: locale-{id-lowercase}
description: >
  One or two sentences describing when an agent should use this locale.
  Include the region name and key distinguishing factors.
locale: {LOCALE-ID}
region: {Full Region Name}
language: {language codes, e.g. en-GB / fr-FR}
version: 1.0.0
extends: {parent locale ID if applicable, e.g. EU}
---
```

Guidelines:

- **name**: lowercased, hyphenated, and prefixed with `locale-` (e.g. `locale-eu-fi`).
- **description**: explicitly says when to apply this locale and what makes it distinct.
- **locale**: the canonical ID like `EU`, `EU-FI`, `US-CA`, `APAC-JP`.
- **region**: human-readable region or country name.
- **language**: BCP 47 language codes where applicable (e.g. `en-GB`, `fi`, `sv`).
- **version**: start with `1.0.0` for new locales.
- **extends**: parent locale ID or empty if standalone (e.g. `extends: EU`).

When updating an existing locale, keep the same `locale` ID and adjust `version`
only if the change is substantial.

---

## Required sections

Every locale should include **all** of these sections, even if some are marked “N/A”:

- `## 🗓 Date & Time`
- `## 💰 Currency & Numbers`
- `## ⚖️ Legal & Compliance`
  - `### Privacy / Data Protection`
  - `### Consumer Protection`
  - `### Accessibility`
  - `### Other Key Regulation`
- `## 🌐 Language & Copy`
- `## 🏛 Cultural Norms`
- `## 📅 Public Holidays`
- `## 🧾 Address Format`
- `## 🔧 Technical Defaults`

Do **not** delete sections when details are unknown; instead write “N/A” and, ideally,
add a comment in the PR description noting that expert input is needed.

---

## Authoring workflow

Follow this workflow when creating or editing a locale:

1. **Determine scope and inheritance**
   - Decide whether this is:
     - A regional base locale (e.g. `EU`).
     - A country or sub-region that extends a base locale (e.g. `EU-FI`, `EU-DE`).
     - A standalone locale with no parent (e.g. `APAC-JP`, `LATAM-BR`).
   - If extending a parent, only document what *differs* from the parent and rely
     on the parent for shared defaults.

2. **Set up the directory and frontmatter**
   - Use the naming convention for the folder and file:
     - `locales/{LOCALE-ID}/LOCALE.md`
   - Fill in frontmatter fields carefully, following the template.

3. **Populate sections with concise, factual rules**
   - Prefer bullet points with concrete examples (e.g. date examples, currency formats).
   - Make rules machine- and human-readable (agents should be able to copy/paste).
   - Be explicit when laws or conventions differ from a parent locale.

4. **Apply research standards (from CONTRIBUTING.md)**
   - For **laws**:
     - Cite the official law name and year (e.g. “General Data Protection Regulation (GDPR) 2016/679”).
   - For **formats**:
     - Verify with official government or ISO sources when possible.
   - For **cultural notes**:
     - Use observational, respectful language; avoid stereotypes and value judgments.
   - For **public holidays**:
     - Note the year of accuracy, especially if dates shift annually.

5. **Run the quality checklist**
   - Ensure:
     - Frontmatter parses as valid YAML.
     - All required headings exist.
     - Sections that don’t apply explicitly say “N/A”.
     - Currency examples show symbol placement, decimal separator, and thousands separator.
     - Address example looks realistic for the locale.

6. **Keep the file compact**
   - Avoid long narrative paragraphs; prefer structured lists and short explanatory notes.
   - Aim for a file that can fit comfortably into an agent’s context window.

---

## Extending vs standalone locales

When deciding between extending a parent or writing a standalone locale:

- **Extending a parent** (`extends: EU`):
  - Good for countries or sub-regions that mostly share rules with a parent.
  - Only override or add sections where the locale truly differs.
  - Clearly state what inherits from the parent unchanged.

- **Standalone locale**:
  - Good when there is no clear parent region or when rules diverge significantly.
  - Document all sections in full.

Examples:

- `EU-FI` extends `EU` and focuses on Finnish-specific law, formatting, and norms.
- `APAC-JP` might be standalone, with its own privacy law and writing systems.

---

## Example: Country extending EU

When creating `locales/EU-DE/LOCALE.md`:

1. Frontmatter:
   - `name: locale-eu-de`
   - `locale: EU-DE`
   - `region: Germany`
   - `extends: EU`
2. Sections:
   - In `Date & Time`: specify `DD.MM.YYYY` and relevant timezones.
   - In `Legal & Compliance`:
     - Note that the Bundesdatenschutzgesetz (BDSG) supplements GDPR.
     - Mention the supervisory authority (e.g. BfDI).
   - In `Language & Copy`:
     - Mention formal “Sie” vs informal “du” conventions, etc.

Keep the file focused on what differs from the EU general locale, while relying
on `locales/EU/LOCALE.md` for shared rules.

---

## Review checklist (quick)

Before considering a locale file “ready”:

- [ ] Frontmatter: valid YAML, all required keys present.
- [ ] Locale ID and naming: matches `REGION-COUNTRY` pattern where appropriate.
- [ ] All standard sections are present.
- [ ] Legal claims reference real laws by name and year.
- [ ] Date, time, and currency examples are concrete and correctly formatted.
- [ ] Cultural notes are respectful and non-stereotyping.
- [ ] Public holidays and address formats look realistic.
- [ ] Differences from parent locale (if any) are clearly expressed.

