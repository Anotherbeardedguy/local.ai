---
name: locale-eu-uk
description: >
  Apply this skill whenever generating content, code, or data for a United Kingdom context.
  Covers UK law (post-Brexit), cultural norms, British English conventions, formatting,
  and regulatory specifics. Note: UK is no longer an EU member — this skill reflects UK-specific rules.
locale: EU-UK
region: United Kingdom
language: en-GB
version: 1.0.0
note: Post-Brexit — UK GDPR and UK law applies, not EU law directly
---

# United Kingdom (EU-UK) Locale

> ⚠️ Post-Brexit note: The UK left the EU on 31 January 2020. UK law diverges from EU law in several areas. This skill reflects current UK-specific rules, not EU rules.

---

## 🗓 Date & Time

- **Format**: DD/MM/YYYY (e.g. 13/03/2026)
- **Spoken/written**: "13 March 2026" or "13th March 2026" — never "March 13th" (American style)
- **Time**: 12-hour clock common in everyday use (2:30 pm); 24-hour in transport, military, formal
- **Timezone**: GMT (UTC+0) / BST (UTC+1, last Sunday March–October)
- **Week start**: Monday

## 💷 Currency & Numbers

- **Currency**: British Pound Sterling (£) — symbol precedes the number: `£12.50`
- **Decimal separator**: Period: `3.14`
- **Thousands separator**: Comma: `1,000,000`
- **VAT**: Standard rate 20%. Consumer prices typically shown inclusive of VAT.

## ⚖️ Legal & Compliance

### UK GDPR & Data Protection
- **UK GDPR** + **Data Protection Act 2018** — retained from EU GDPR post-Brexit but independently maintained
- Supervisory authority: **Information Commissioner's Office (ICO)**
- Principles broadly similar to EU GDPR: lawful basis, data minimisation, rights of data subjects
- UK and EU GDPR are currently deemed "adequate" for data transfers — monitor for changes
- Cookie consent: same principles as EU — clear accept/reject, no pre-ticked boxes

### Consumer Protection
- **Consumer Rights Act 2015** — goods must be satisfactory quality, fit for purpose, as described
- **Consumer Contracts Regulations 2013** — 14-day cooling-off for distance/online purchases
- **FCA regulation** applies to any financial products or services — flag prominently
- **ASA** (Advertising Standards Authority) governs advertising — no misleading claims

### Accessibility
- **Public Sector Bodies Accessibility Regulations 2018** — WCAG 2.1 AA for public sector
- **Equality Act 2010** — reasonable adjustments required for disabled users

### Other Key Regulation
- **Companies House**: UK business registration; company number required on formal correspondence
- **HMRC**: Tax authority — use correct terminology (National Insurance, PAYE, VAT, not "social security")

## 🌐 Language & Copy

- **British English**: Always use en-GB spellings, not en-US
  - colour, not color
  - centre, not center
  - organise, not organize
  - licence (noun) / license (verb)
  - programme, not program (except software)
  - autumn, not fall
  - maths, not math
- **Tone**: Measured, understated, often dry. Avoid American enthusiasm and hyperbole.
- **Humour**: Dry wit is appreciated; directness is valued but politeness is expected
- **Avoid**: "Quite literally", excessive exclamation marks, American-isms ("reach out", "touch base")
- **Preferred**: Clear, precise, unshowy prose. The reader's time is respected.

### Regional Nuance
- England, Scotland, Wales, Northern Ireland have distinct identities — avoid conflating "British" and "English"
- Scottish law differs significantly (separate legal system); flag when relevant
- Northern Ireland has specific post-Brexit trade rules (Windsor Framework)

## 🏛 Cultural Norms

- **Understatement**: "Not bad" often means excellent. "Interesting" can be polite dismissal.
- **Queueing**: Deeply held social norm — never skip the queue (metaphorically or literally)
- **Class awareness**: Subtle but real — avoid copy that reads as condescending or elitist
- **Weather**: A genuine conversational staple, not a cliché — it's fine to reference it
- **NHS**: The National Health Service is a cultural institution — treat with appropriate gravity
- **Monarchy**: Constitutional monarchy — relevant for formal/legal contexts (e.g. "His Majesty's Government")
- **Sport**: Football (soccer), cricket, rugby, tennis (Wimbledon) are culturally significant

## 📅 Public Holidays (Bank Holidays)

England & Wales (Scotland and Northern Ireland differ):
- New Year's Day: 1 Jan
- Good Friday (moveable)
- Easter Monday (moveable)
- Early May Bank Holiday: First Monday in May
- Spring Bank Holiday: Last Monday in May
- Summer Bank Holiday: Last Monday in August
- Christmas Day: 25 Dec
- Boxing Day: 26 Dec

## 🧾 Address Format

```
[Recipient Name]
[Organisation]
[Building number] [Street Name]
[Town/City]
[County] (optional)
[Postcode]
```
Example:
```
Jane Smith
Acme Ltd
42 Baker Street
London
NW1 6XE
```

- Postcode: Always on its own line, in CAPS
- No "UK" needed for domestic mail; add "UNITED KINGDOM" for international

## 🔧 Technical Defaults

- Paper size: A4
- Encoding: UTF-8
- Measurement: Mixed — metric officially, but imperial widely used (miles, pints, feet/inches for height)
  - Road distances: miles
  - Draught beer: pints
  - Body height: often feet/inches colloquially
  - Weight: often stone + pounds colloquially (not just kg)
- Electrical: 230V / 50Hz / Type G (3-pin) plugs — different from continental Europe

---

*Part of the Local.ai locale skill set.*
*Note: UK diverges from EU post-Brexit — do not assume EU directives apply.*
*Contribute: https://github.com/Anotherbeardedguy/local.ai*
