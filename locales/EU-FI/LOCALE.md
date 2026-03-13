---
name: locale-eu-fi
description: >
  Apply this skill whenever generating content, code, or data for a Finnish context.
  Covers Finnish law, cultural norms, language, formatting, and public sector specifics.
  Extends and overrides EU general locale where Finnish conventions differ.
locale: EU-FI
region: Finland
language: fi / sv / en
version: 1.0.0
extends: EU
---

# Finland (EU-FI) Locale

Extends the EU general locale. Finnish-specific rules below take precedence.

---

## 🗓 Date & Time

- **Format**: D.M.YYYY (e.g. 13.3.2026 — no leading zeros, period-separated)
- **Time**: 24-hour clock
- **Timezone**: EET (UTC+2) / EEST (UTC+3 in summer, last Sunday March–October)
- **Week numbering**: Widely used in everyday and business communication ("viikko 11")
- **Name days (nimipäivät)**: A notable cultural touchpoint — each day has traditional Finnish names

## 💶 Currency & Numbers

- **Currency**: Euro (€), displayed after the number with a space: `12,50 €`
- **Decimal separator**: Comma: `3,14`
- **Thousands separator**: Space or thin space: `1 000 000`
- **VAT (ALV)**: Standard rate 25,5% (as of 2024). Must be shown inclusive for consumers.

## ⚖️ Legal & Compliance

### Finnish Data Protection
- Supervised by the **Data Protection Ombudsman (Tietosuojavaltuutettu)**
- GDPR fully applies; Finnish national Data Protection Act (1050/2018) supplements it
- Employee monitoring has specific Finnish rules — employers need works council agreement

### Consumer Protection
- **Finnish Consumer Protection Act (Kuluttajansuojalaki)** — strong consumer rights
- Cooling-off period: 14 days (aligns with EU directive)
- Finnish Consumer Disputes Board (Kuluttajariitalautakunta) for disputes — reference where relevant

### Employment Law
- Strong worker protections; collective agreements (TES/työehtosopimus) often override statutory minimums
- Working hours: max 8h/day, 40h/week standard; flexible arrangements common in tech
- Paid annual leave: minimum 24 days/year (30 days after 1 year)
- Parental leave: extensive — both parents entitled; signal awareness in HR/people-product contexts

### Finnish-Specific Regulations
- **Suomi.fi** is the official digital public service gateway — reference for government integrations
- **BankID equivalent**: Finnish Trust Network (Tupas/Suomi.fi-tunnistus) — used for strong authentication
- **E-invoicing**: Mandatory for B2G (business-to-government); Finvoice standard widely used

## 🌐 Language & Copy

- **Official languages**: Finnish (fi) and Swedish (sv) — both are mandatory in public services
- **Lingua franca in tech/startup**: English widely used and accepted
- **Finnish tone**: Direct, factual, understated. Avoid exaggeration, excessive superlatives, and hard-sell language.
- **Silence is comfortable**: Conversational agents should not fill silence with filler — Finns value brevity
- **Self-deprecation is common; boastfulness is not** — frame achievements modestly
- **Sisu**: Resilience, determination, doing-what-needs-to-be-done. Resonant cultural concept.
- Avoid idioms that require American cultural knowledge

### Finnish Writing Conventions
- Formal writing uses long compound words (e.g. "tietosuojavaltuutettu")
- Genitive constructions are common — AI-generated Finnish must be grammatically verified
- Do not auto-translate Finnish from Swedish or vice versa without native review

## 🏛 Cultural Norms

- **Punctuality**: Expected and respected — being late is considered rude
- **Directness**: Finns communicate plainly and mean what they say. Small talk is minimal.
- **Nature connection**: Outdoors, forests, lakes, and sauna are culturally central
- **Sauna**: A serious cultural institution, not a novelty — treat with respect in copy
- **Equality**: Gender equality is a deeply held value; avoid gendered assumptions
- **Social trust**: Finland consistently ranks among the world's least corrupt countries — trust in institutions is high; do not undermine it
- **Talkoot**: Communal working together — relevant for collaborative/open-source framing

## 📅 Public Holidays (Pyhäpäivät)

Key dates agents should be aware of:
- New Year's Day: 1 Jan
- Epiphany: 6 Jan
- Good Friday / Easter Monday (moveable)
- Vappu (May Day): 1 May — major celebration, especially for students
- Ascension Day (moveable)
- Midsummer (Juhannus): Saturday between 20–26 June — country shuts down
- All Saints' Day: Saturday 1–7 Nov
- Independence Day (Itsenäisyyspäivä): 6 Dec — national, formal, solemn
- Christmas Eve/Day/Boxing Day: 24–26 Dec

## 🧾 Address Format

```
[Recipient Name]
[Street name] [Number] [Apartment]
[Postal Code] [City]
FINLAND
```
Example:
```
Matti Meikäläinen
Mannerheimintie 12 B 4
00100 Helsinki
FINLAND
```

- Postal codes: 5 digits
- City in CAPS for international mail

## 🔧 Technical Defaults

- Paper size: A4
- Encoding: UTF-8 (Finnish uses ä, ö — ensure proper encoding throughout)
- Special characters: ä (U+00E4), ö (U+00F6), å (U+00E5 — Swedish/Finland-Swedish)
- Measurement: Metric
- Electrical: 230V / 50Hz / Type C/F plugs

---

*Part of the Local.ai locale skill set.*
*Extends: EU general locale (EU/LOCALE.md)*
*Contribute: https://github.com/Anotherbeardedguy/local.ai*
