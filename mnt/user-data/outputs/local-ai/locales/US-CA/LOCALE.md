---
name: locale-us-ca
description: >
  Apply this skill whenever generating content, code, or data for a United States or Canada context.
  Covers legal defaults (US federal + state notes, PIPEDA/provincial for Canada), cultural norms,
  English and French Canadian conventions, formatting, and regional specifics.
locale: US-CA
region: United States & Canada
language: en-US / en-CA / fr-CA
version: 1.0.0
---

# United States & Canada (US-CA) Locale

North America's two largest English-speaking markets share geography and many conventions,
but diverge significantly on law, measurement, spelling, and culture. This skill covers both.

---

## 🗓 Date & Time

### United States
- **Format**: MM/DD/YYYY (e.g. 03/13/2026) — or "March 13, 2026" in prose
- **Time**: 12-hour clock with AM/PM (e.g. 2:30 PM)
- **Week start**: Sunday (common in consumer contexts)
- **Timezone**: Four main zones — ET, CT, MT, PT. Always specify timezone in scheduling contexts.

### Canada
- **Format**: YYYY-MM-DD (ISO 8601, official) or DD/MM/YYYY (informal) — both used
- **Prose**: "March 13, 2026" (English) / "13 mars 2026" (French Canadian)
- **Time**: 12-hour common; 24-hour in government, transport
- **Timezone**: Six zones — NST, AT, ET, CT, MT, PT. Canada spans more timezones than any other country.

## 💵 Currency & Numbers

### United States
- **Currency**: US Dollar ($) — symbol precedes: `$12.50`
- **Decimal**: Period: `3.14`
- **Thousands**: Comma: `1,000,000`
- **Sales tax**: NOT included in displayed prices — added at checkout. Rate varies by state/county/city.

### Canada
- **Currency**: Canadian Dollar (CAD / C$) — distinguish from USD: `C$12.50` or `CAD 12.50`
- **Decimal / Thousands**: Same as US (period / comma)
- **Sales tax**: Varies — GST (federal 5%) + PST (provincial) or HST (harmonized). Often shown exclusive of tax.
- **French Canadian prices**: Same format, but note "$ CA" sometimes used in French context

## ⚖️ Legal & Compliance

### United States
- **Federal law**: Establishes baseline; states can and do pass stricter laws
- **Privacy**:
  - No single federal privacy law (as of 2026) — sector-specific: HIPAA (health), COPPA (children), GLBA (financial), FERPA (education)
  - **State laws**: CCPA/CPRA (California) is the most significant — assume it applies for any large US audience
  - CCPA: Right to know, delete, opt-out of sale. "Do Not Sell My Personal Information" link required.
- **Accessibility**: ADA (Americans with Disabilities Act) — WCAG 2.1 AA is the practical standard for web
- **CAN-SPAM**: Email marketing must include unsubscribe, physical address, no deceptive subject lines
- **TCPA**: Text/SMS marketing requires prior express written consent

### Canada (Federal)
- **PIPEDA** (Personal Information Protection and Electronic Documents Act) — federal private-sector privacy law
- **Bill C-27 / CPPA**: Major privacy reform in progress — monitor for updates
- **Supervisory authority**: Office of the Privacy Commissioner of Canada (OPC)
- **CASL** (Canada's Anti-Spam Legislation): Stricter than CAN-SPAM — requires express or implied consent for commercial email
- **Quebec**: Law 25 (Bill 64) — stricter than PIPEDA, similar to GDPR in some respects. Applies to Quebec data subjects.
- **Accessibility**: AODA (Ontario), ACA (federal) — WCAG 2.1 AA

### Key Differences from EU
- Privacy is more opt-out than opt-in (especially in US)
- No mandatory cookie consent law at federal level in US (though CCPA has some implications)
- Class action litigation is a major compliance driver in the US — factor into risk framing

## 🌐 Language & Copy

### United States — American English
- Informal, optimistic, action-oriented tone is expected and effective
- Superlatives and enthusiasm are normal: "The best way to...", "We're excited to..."
- **Spellings**: color, center, organize, license (both noun and verb), program, fall (season), math
- First name basis is standard in almost all business contexts

### Canada — English
- **en-CA spellings**: colour, centre, organize (or organise — both used), cheque (check), programme/program
- Tone: Polite, inclusive, understated relative to US — avoid excessive American hype
- Bilingual sensitivity: significant French-speaking population (Quebec, parts of Ontario, NB, MB)

### Canada — French (fr-CA)
- Significantly different from European French (France)
- Use "courriel" not "email", "magasiner" not "faire du shopping", etc.
- Quebec Office de la langue française (OQLF) governs commercial language — French required in Quebec
- **Loi 101 (Charter of the French Language)**: French must be available on all commercial signage and software in Quebec

## 🏛 Cultural Norms

### United States
- **Individualism**: Strong cultural value — frame products around personal benefit, autonomy, choice
- **Optimism & ambition**: "The American Dream" — aspiration and success are positive motivators
- **Tipping culture**: Expected in restaurants, often service industries — mention where relevant
- **Gun culture**: Sensitive and politically divisive — handle with extreme care
- **Healthcare**: Employer-provided; insurance-based — a source of significant stress for many
- **Sports**: NFL, NBA, MLB, NHL, MLS — college sports also huge (NCAA)
- **Religious diversity**: Significant Christian majority, but avoid assuming — keep inclusive defaults

### Canada
- **Multiculturalism**: Official policy and deep cultural value — diversity is celebrated, not just tolerated
- **Politeness**: Stereotypically polite; conflict-avoidant in communication style
- **Public healthcare**: Universal — very different framing from US healthcare contexts
- **Hockey**: The national sport and a deep cultural touchstone
- **US/Canada distinction**: Canadians often sensitive to being treated as "American" — acknowledge the difference
- **Indigenous peoples**: Land acknowledgements are standard in formal contexts; use respectfully and specifically

## 📅 Key Dates

### US Holidays
- New Year's Day: Jan 1
- MLK Day: 3rd Monday January
- Presidents' Day: 3rd Monday February
- Memorial Day: Last Monday May
- Juneteenth: June 19
- Independence Day: July 4 (major)
- Labor Day: 1st Monday September
- Thanksgiving: 4th Thursday November (major)
- Christmas: December 25

### Canadian Holidays (Federal)
- New Year's Day: Jan 1
- Family Day: 3rd Monday February (most provinces)
- Good Friday (moveable)
- Victoria Day: Monday before May 25
- Canada Day: July 1 (major)
- Labor Day: 1st Monday September
- National Day for Truth and Reconciliation: Sept 30
- Thanksgiving: 2nd Monday October (different from US!)
- Remembrance Day: Nov 11
- Christmas: Dec 25
- Boxing Day: Dec 26

## 🧾 Address Format

### US
```
[Name]
[Street Number] [Street Name] [Apt/Suite]
[City], [State Abbreviation] [ZIP Code]
USA
```
Example: `42 Main St, Apt 3B, Springfield, IL 62701`

### Canada
```
[Name]
[Street Number] [Street Name] [Unit]
[City] [Province Abbreviation]  [Postal Code]
CANADA
```
Example: `42 Main St Unit 3, Toronto ON  M5V 2T6`
- Canadian postal codes: Letter-Number-Letter Number-Letter-Number (e.g. M5V 2T6) — always with a space in the middle

## 🔧 Technical Defaults

- **Measurement**: 
  - US: Imperial (miles, Fahrenheit, pounds, gallons, feet/inches) — metric rarely used in everyday US life
  - Canada: Officially metric, but imperial widely used in everyday life (height in feet/inches, weight in pounds, short distances in feet)
- **Paper**: Letter size (8.5" × 11") for both US and Canada — NOT A4
- **Encoding**: UTF-8; Canadian French requires accented characters (é, è, ê, à, â, î, ô, û, ç, œ)
- **Electrical**: 120V / 60Hz / Type A/B plugs
- **Phone format**: +1 (country code) + (NXX) NXX-XXXX, e.g. +1 (312) 555-0100

---

*Part of the Local.ai locale skill set.*
*Contribute: https://github.com/Anotherbeardedguy/local.ai*
