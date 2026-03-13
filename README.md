# Local.ai

**Region-aware skills for AI agents.**

Local.ai is an open, community-maintained collection of locale skill files that teach AI agents how to behave correctly for a specific region — covering laws, cultural norms, date and number formats, language conventions, and more.

Drop a locale file into your agent's context and it knows the rules of the place.

---

## What's included

| Locale | Region | Extends |
|--------|--------|---------|
| `EU` | European Union (general) | — |
| `EU-FI` | Finland | EU |
| `EU-UK` | United Kingdom | — |
| `US-CA` | United States & Canada | — |
| *More coming* | [Contribute yours →](CONTRIBUTING.md) | |

---

## How to use

### Option 1: Copy into your agent's context

Paste the contents of the relevant `LOCALE.md` file into your system prompt or agent configuration.

```
You are a helpful assistant. Follow the rules in the locale skill below.

[paste LOCALE.md contents here]
```

### Option 2: Reference the file path (for agents with file access)

```
Read and apply the locale skill at: locales/EU-FI/LOCALE.md
```

### Option 3: Stack locales (general + specific)

For the best results, apply the regional parent first, then the country-specific locale:

```
Apply these locale skills in order:
1. locales/EU/LOCALE.md      ← EU general rules
2. locales/EU-FI/LOCALE.md   ← Finnish overrides
```

---

## Contributing

We welcome locale contributions for any country, region, or sub-region.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the template, quality checklist, and submission process.

---

## License

CC0 1.0 Universal — public domain. Use freely, no attribution required.
