# Spacing, radius & shadows

## Spacing

Échelle stricte basée sur 4px. Aucune valeur intermédiaire ne doit être utilisée — si un besoin n'entre pas dans l'échelle, c'est probablement un signe que la composition doit être repensée.

| Token | Valeur | Usage typique |
| --- | --- | --- |
| `--space-1` | 4px | Espacement intra-composant minimal |
| `--space-2` | 8px | Espacement intra-composant |
| `--space-3` | 12px | Espacement entre éléments liés |
| `--space-4` | 16px | Espacement standard |
| `--space-6` | 24px | Espacement entre éléments d'un même groupe |
| `--space-8` | 32px | Espacement entre groupes |
| `--space-12` | 48px | Espacement entre sections proches |
| `--space-16` | 64px | Espacement entre sections |
| `--space-24` | 96px | Espacement entre sections majeures |
| `--space-32` | 128px | Marges de respiration verticale (hero, fin de page) |

## Radius

Très peu de radius — l'esthétique est plutôt anguleuse pour renforcer le côté éditorial.

| Token | Valeur | Usage |
| --- | --- | --- |
| `--radius-none` | 0 | Cards, sections, dividers |
| `--radius-sm` | 4px | Inputs, tags, petits boutons |
| `--radius-md` | 8px | Boutons, composants interactifs |
| `--radius-lg` | 12px | Modales, cards mises en avant |
| `--radius-full` | 9999px | Avatars, pills |

## Shadows

Trois niveaux suffisent. Les ombres sont subtiles, jamais spectaculaires.

| Token | Valeur | Usage |
| --- | --- | --- |
| `--shadow-sm` | `0 1px 2px rgba(15, 14, 13, 0.04)` | Élévation très subtile |
| `--shadow-md` | `0 4px 12px rgba(15, 14, 13, 0.06)` | Cards interactives au hover |
| `--shadow-lg` | `0 12px 32px rgba(15, 14, 13, 0.08)` | Modales, popovers |

En mode sombre, les ombres sont remplacées par des bordures subtiles (`--border-subtle`) — les ombres ne sont pas perçues sur fond sombre.

> Tous ces tokens sont définis dans [`tokens/tokens.css`](../../tokens/tokens.css).
