# Voicemail Greeting Generator — Claude Code Skill

> **Translations:** [日本語](README.ja.md) · [Español](README.es.md) · [Français](README.fr.md)

Generate polished, professional voicemail greeting scripts from your terminal using Claude Code, then convert them to MP3 with a natural-sounding AI voice at [Solvea](https://solvea.cx/tools/voicemail-greeting-generator) — no recording equipment or retakes needed.

## Features

- 5 greeting types: Business, Personal, Holiday, After Hours, Out Sick
- 7 industry templates: General, Real Estate, Medspa, Retail, Dental, Law Firm, and more
- Scripts optimised for ≤ 30 seconds spoken aloud
- Direct link to Solvea's free AI voice generator and MP3 export
- Compatible with iPhone, Android, RingCentral, Zoom Phone, and most VoIP services

## Installation

```bash
claude mcp install voicemail-greeting-generator
```

Or add the skill manually by placing `skill.md` in your Claude Code skills directory.

## Usage

```
/voicemail-greeting [flags]
```

| Flag | Options | Default |
|------|---------|---------|
| `--type` | `business` · `personal` · `holiday` · `after-hours` · `out-sick` | `business` |
| `--industry` | `general` · `real-estate` · `medspa` · `retail` · `dental` · `law-firm` · `other` | `general` |
| `--name` | Your name or business name | *(prompted)* |
| `--phone` | Callback phone number | *(optional)* |
| `--hours` | Business hours, e.g. `Mon-Fri 9am-5pm` | *(optional)* |
| `--custom` | Provide your own script to skip generation | *(optional)* |

## Examples

```bash
# Professional real-estate greeting
/voicemail-greeting --type business --industry real-estate --name "Jane Doe Realty"

# Holiday closure message for a dental clinic
/voicemail-greeting --type holiday --industry dental --name "Bright Smile Dental"

# Use your own script and head straight to voice selection
/voicemail-greeting --custom "Thank you for calling Acme Corp..."
```

## How it works

1. Claude generates a tailored script (or uses your custom text).
2. You review and optionally request one round of revisions.
3. Claude links you to [Solvea's AI Voicemail Greeting Generator](https://solvea.cx/tools/voicemail-greeting-generator), where you choose from 6 natural AI voices, preview, and download your MP3.

> Free accounts on Solvea include up to **13 generations** — no credit card required.

## License

MIT © Boyuan Gao
