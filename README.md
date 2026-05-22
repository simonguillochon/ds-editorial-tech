# Design System — Editorial Tech

Documentation de la direction artistique du portfolio **Editorial Tech**.
Ce dépôt fait foi pour toute décision de design ou d'implémentation. Toute déviation doit être discutée et tracée.

> **Source de vérité** — Figma est canonique pour le design. Les tokens de [`tokens/tokens.css`](tokens/tokens.css) en sont un **miroir exporté** : ne jamais éditer les valeurs à deux endroits. Quand la copie manuelle deviendra pénible, ce sera le signal d'ajouter un vrai pipeline (Style Dictionary / Tokens Studio).

## Navigation

**Principes**
- [Philosophie & positionnement de marque](docs/principles.md)

**Foundations**
- [Couleurs](docs/foundations/color.md)
- [Typographie](docs/foundations/typography.md)
- [Spacing, radius & shadows](docs/foundations/space.md)
- [Grille responsive](docs/foundations/layout.md)

**Composants**
- [Atomes](docs/components/atoms.md)
- [Patterns portfolio](docs/components/patterns.md)
- [Layout](docs/components/layout.md)

**Transverse**
- [Signatures visuelles](docs/signatures.md)
- [Accessibilité & Do / Don't](docs/accessibility.md)
- [Ressources](docs/resources.md)

**Artefacts**
- [Tokens CSS](tokens/tokens.css)
- [Changelog](CHANGELOG.md)

## État du système

| Domaine | État |
| --- | --- |
| Principes & positionnement | ✅ Documenté |
| Foundations (couleurs, typo, spacing, radius, shadows, grille) | ✅ Documenté |
| Tokens CSS (mode clair + sombre) | ✅ Exportés |
| Specs composants | 🟡 En cours (atoms construits dans Figma) |
| Code des composants | ⬜ À venir |
| Pipeline de tokens automatisé | ⬜ À venir (copie manuelle pour l'instant) |

## Organisation du dépôt

- `docs/` — le « pourquoi » et les specs ; miroir des décisions Figma.
- `tokens/` — artefacts machine-readable, exportés depuis Figma.
- `assets/` — captures, exports Figma, images de référence.
- Le **code** des composants arrivera dans un dossier dédié (`components/` ou `src/`) quand la première implémentation démarrera — pas avant.
