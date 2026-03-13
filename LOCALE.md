---
name: locale-eu
description: >
  Apply this skill whenever generating content, code, or data for a European Union context.
  Covers legal defaults (GDPR, DSA, consumer rights), formatting conventions, cultural tone,
  and language considerations that apply across EU member states.
locale: EU
region: European Union
version: 1.0.0
---

# EU General Locale

This skill governs agent behavior for the European Union as a whole. For country-specific
overrides, combine this skill with a country-level locale (e.g. EU-FI for Finland).

---

## 🗓 Date & Time

- **Format**: DD/MM/YYYY (e.g. 13/03/2026)
- **Time**: 24-hour clock (e.g. 14:30, not 2:30 PM)
- **Week start**: Monday
- **Timezone**: Always clarify — EU spans CET/CEST, EET/EEST, WET/WEST, etc.
- **Calendar week**: ISO 8601 week numbering is standard in business contexts

## 💶 Numbers & Currency

- **Decimal separator**: Comma (e.g. 1,5 not 1.5) — varies by member state, default to comma
- **Thousands separator**: Period or space (e.g. 1.000 or 1 000)
- **Currency**: Euro (€) for eurozone members. Symbol precedes or follows number depending on language — follow locale convention
- **VAT**: Always display prices inclusive of VAT for consumer-facing content (EU Consumer Rights Directive)

## ⚖️ Legal & Compliance

### GDPR (General Data Protection Regulation)
- Any feature collecting personal data MUST:
  - Identify a lawful basis (consent, contract, legitimate interest, etc.)
  - Provide a clear privacy notice
  - Support data subject rights: access, rectification, erasure, portability, objection
- Consent must be freely given, specific, informed, and unambiguous — no pre-ticked boxes
- Cookie banners: reject option must be as easy to access as accept
- Data minimization: collect only what is strictly necessary
- Retention limits: define and document data retention periods

### DSA (Digital Services Act)
- Platforms must be transparent about algorithmic recommendation systems
- Users must be able to opt out of profiling-based recommendations
- Illegal content removal obligations apply to relevant platform types

### Consumer Rights
- Mandatory 14-day right of withdrawal for online purchases
- Clear pre-contractual information required (price, identity of trader, etc.)
- Prohibited: dark patterns that trick users into purchases or subscriptions

### Accessibility
- Public sector: WCAG 2.1 AA minimum (EU Web Accessibility Directive)
- Private sector: increasingly required under European Accessibility Act (EAA) from 2025

## 🌐 Language & Copy

- Default language for EU-general content: English (unless context specifies otherwise)
- Tone: Formal but clear. Avoid overly casual or American-English idioms
- Legal/official content should be precise and unambiguous
- Avoid humor that doesn't translate across cultures
- Content may need localization into multiple official EU languages for broad reach

## 🏛 Cultural Norms

- Privacy is considered a fundamental right, not a product feature — treat it accordingly
- Sustainability and environmental impact are high-salience topics across the EU
- Work-life balance: avoid implying 24/7 availability expectations
- Public holidays vary significantly by country — never assume a single EU holiday calendar
- Trust is built through transparency, credentials, and institutional affiliation

## 🧾 Address & Contact Formats

- Address order: Street → Postal code + City → Country
- Phone: Use E.164 international format (+countrycode number) in data fields
- VAT numbers follow country-specific formats (e.g. DE123456789, FI12345678)

## 🔧 Technical Defaults

- Character encoding: UTF-8 always
- Paper size: A4 (210 × 297 mm)
- Measurement system: Metric (SI units)
- Electrical: 230V / 50Hz
- Keyboard: Varies by country — do not hardcode shortcuts that assume US QWERTY

---

*Part of the Local.ai locale skill set. Combine with country-level skills for full coverage.*
*Contribute: https://github.com/Anotherbeardedguy/local.ai*
