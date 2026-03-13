# Contributing a Locale to Local.ai

Thank you for helping make AI agents more locally aware! This guide explains how to add a new locale or improve an existing one.

---

## 📂 File Structure

Each locale lives in its own folder under `/locales/`:

```
locales/
├── EU/           ← EU general (base for European locales)
│   └── LOCALE.md
├── EU-FI/        ← Finland (extends EU)
│   └── LOCALE.md
├── EU-UK/        ← United Kingdom (extends EU conventions)
│   └── LOCALE.md
├── US-CA/        ← United States & Canada
│   └── LOCALE.md
└── YOUR-LOCALE/  ← Your new locale
    └── LOCALE.md
```

### Locale Naming Convention

Use the pattern `REGION-COUNTRY` or just `REGION` for regional groupings:

| Scope | Example ID | Example |
|---|---|---|
| Continent/region | `EU` | European Union general |
| Country in region | `EU-DE` | Germany |
| Subregion/state | `US-CA-NYC` | New York City specifics |
| Non-EU European | `EUR-NO` | Norway |

Use ISO 3166-1 alpha-2 country codes where applicable.

---

## 📝 LOCALE.md Template

Copy this template when creating a new locale:

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

# {Region Name} ({LOCALE-ID}) Locale

{One paragraph overview. What makes this locale distinct? What should agents know upfront?}

---

## 🗓 Date & Time

- **Format**: 
- **Time**: 
- **Timezone**: 
- **Week start**: 
- **Other**: 

## 💰 Currency & Numbers

- **Currency**: 
- **Decimal separator**: 
- **Thousands separator**: 
- **Tax/VAT**: 

## ⚖️ Legal & Compliance

### Privacy / Data Protection
- Governing law: 
- Supervisory authority: 
- Key requirements: 

### Consumer Protection
- 

### Accessibility
- 

### Other Key Regulation
- 

## 🌐 Language & Copy

- **Language(s)**: 
- **Tone**: 
- **Spelling conventions**: 
- **Avoid**: 
- **Prefer**: 

## 🏛 Cultural Norms

- 

## 📅 Public Holidays

- 

## 🧾 Address Format

```
[Address format example]
```

## 🔧 Technical Defaults

- **Measurement**: 
- **Paper size**: 
- **Encoding**: 
- **Electrical**: 

---

*Part of the Local.ai locale skill set.*
*Extends: {parent locale if applicable}*
*Contribute: https://github.com/Anotherbeardedguy/local.ai*
```

---

## ✅ Quality Checklist

Before submitting a pull request, verify:

- [ ] Frontmatter is complete and valid YAML
- [ ] All section headings from the template are present (fill in "N/A" if not applicable — don't delete sections)
- [ ] Legal information is accurate and cites the specific law name and year
- [ ] Date/time format is verified with a real example
- [ ] Currency format shows symbol placement, decimal, and thousands separator
- [ ] Cultural notes are observational and respectful — not stereotyping
- [ ] Public holidays are current and accurate (note the year if they change annually)
- [ ] Address format includes a real-looking example
- [ ] If extending a parent locale, only include items that differ from the parent
- [ ] No personal opinions or editorializing in legal/compliance sections

---

## 🔍 Research Standards

Locale files must be factually accurate. When researching:

1. **Laws**: Cite the official law name (e.g. "General Data Protection Regulation (GDPR) 2016/679") — not just a summary site
2. **Formats**: Verify with official government or ISO sources, not just Wikipedia
3. **Cultural observations**: Draw from multiple perspectives — avoid single-source cultural characterizations
4. **Dates**: Public holidays can change — note the year of accuracy and link official source where possible

---

## 🌿 Extending vs. Standalone

**Extending a parent locale** (`extends: EU`):
- Only document what *differs* from the parent
- Always note which sections inherit from the parent unchanged
- Good for country-specific locales within a region

**Standalone locale**:
- Document everything from scratch
- Good for regions with no clear parent (e.g. Japan, Brazil, South Korea)

---

## 🤝 What We Welcome

- New country locales (any country!)
- Sub-regional locales (states, provinces, cities with distinct rules)
- Corrections to existing locales (laws change — PRs welcome)
- Industry-specific locale supplements (healthcare, finance, education)
- Non-English locale metadata (descriptions in the locale's own language)

## ❌ What We Don't Accept

- Political opinions or advocacy
- Disparaging characterizations of any culture or people
- Unverified legal claims
- Locale files without sources for legal claims
- Duplicate locales without clear differentiation

---

## 🚀 Submitting

1. Fork the repository
2. Create a branch: `git checkout -b locale/EU-DE` (use locale ID)
3. Add your locale folder and `LOCALE.md`
4. Run the checklist above
5. Open a pull request with:
   - Title: `Add locale: {LOCALE-ID} ({Full Name})`
   - Brief description of sources used for legal/compliance sections
   - Note any sections that need expert review

---

*Questions? Open an issue tagged `locale-question`.*
*Local.ai — https://github.com/Anotherbeardedguy/local.ai*
