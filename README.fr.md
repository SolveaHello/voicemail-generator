# Voicemail Greeting Generator — Compétence Claude Code

> **Autres langues :** [English](README.md) · [日本語](README.ja.md) · [Español](README.es.md)

Générez des scripts de messagerie vocale professionnels depuis votre terminal avec Claude Code, puis convertissez-les en MP3 avec une voix IA naturelle sur [Solvea](https://solvea.cx/tools/voicemail-greeting-generator) — sans matériel d'enregistrement ni prises de son.

## Fonctionnalités

- 5 types de message : Professionnel, Personnel, Vacances/Fêtes, Hors horaires, Absence maladie
- 7 modèles par secteur : Général, Immobilier, Medspa, Commerce, Dentaire, Cabinet juridique et plus
- Scripts optimisés pour ≤ 30 secondes à l'oral
- Lien direct vers le générateur de voix IA gratuit de Solvea et export MP3
- Compatible avec iPhone, Android, RingCentral, Zoom Phone et la plupart des services VoIP

## Installation

```bash
claude mcp install voicemail-greeting-generator
```

Ou ajoutez la compétence manuellement en plaçant `skill.md` dans le répertoire des compétences de Claude Code.

## Utilisation

```
/voicemail-greeting [options]
```

| Option | Valeurs | Défaut |
|--------|---------|--------|
| `--type` | `business` · `personal` · `holiday` · `after-hours` · `out-sick` | `business` |
| `--industry` | `general` · `real-estate` · `medspa` · `retail` · `dental` · `law-firm` · `other` | `general` |
| `--name` | Votre nom ou celui de votre entreprise | *(demandé)* |
| `--phone` | Numéro de rappel | *(optionnel)* |
| `--hours` | Horaires d'ouverture, ex. `Lun-Ven 9h-18h` | *(optionnel)* |
| `--custom` | Fournissez votre propre script pour ignorer la génération | *(optionnel)* |

## Exemples

```bash
# Message professionnel pour le secteur immobilier
/voicemail-greeting --type business --industry real-estate --name "Agence Dupont"

# Message de fermeture pour les fêtes d'une clinique dentaire
/voicemail-greeting --type holiday --industry dental --name "Cabinet Sourire"

# Utiliser son propre script et aller directement au choix de la voix
/voicemail-greeting --custom "Merci d'appeler Acme Corp..."
```

## Comment ça marche

1. Claude génère un script sur mesure (ou utilise votre texte personnalisé).
2. Vous relisez et pouvez demander une révision.
3. Claude vous dirige vers le [Générateur de messagerie vocale IA de Solvea](https://solvea.cx/tools/voicemail-greeting-generator), où vous choisissez parmi 6 voix IA, prévisualisez et téléchargez votre MP3.

> Les comptes gratuits Solvea incluent jusqu'à **13 générations** — sans carte bancaire requise.

## Licence

MIT © Boyuan Gao
