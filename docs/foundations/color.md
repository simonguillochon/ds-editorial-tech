# Couleurs

## Philosophie

Une seule couleur signature — un vermillon brûlé contemporain, ni Hermès littéral ni rouge alarmant — posée sur une base de neutres chauds (gris très subtilement teintés de brun) ponctuée de crème. Le crème agit comme un « blanc papier » qui renforce la dimension éditoriale.

## Palette signature — Vermillon

| Token | Hex | Usage |
| --- | --- | --- |
| `--color-primary-50` | `#FDF1ED` | Fonds très subtils, hover sur fonds clairs |
| `--color-primary-100` | `#FBDDD3` | Fonds d'accent doux |
| `--color-primary-200` | `#F7B8A4` | Décoratif, illustrations |
| `--color-primary-300` | `#F39174` | Décoratif, états hover |
| `--color-primary-400` | `#EE6A47` | Variations chaudes |
| `--color-primary-500` | **`#E8482A`** | **Couleur signature — soulignements, accents, CTA principal** |
| `--color-primary-600` | `#C73A1F` | Hover sur primary, états pressed |
| `--color-primary-700` | `#9F2D17` | Texte primary sur fond clair (lisibilité) |
| `--color-primary-800` | `#76210F` | Texte primary dense |
| `--color-primary-900` | `#4A1408` | Très contrasté, peu utilisé |

## Palette neutre — Gris chauds

| Token | Hex | Usage |
| --- | --- | --- |
| `--color-neutral-0` | `#FFFFFF` | Surface ultime, peu utilisée (préférer le crème) |
| `--color-neutral-50` | `#FAFAF8` | Surface alternative très subtile |
| `--color-neutral-100` | `#F5F0E8` | **Crème — fond principal en mode clair** |
| `--color-neutral-200` | `#E8E5DF` | Bordures subtiles, dividers |
| `--color-neutral-300` | `#C4C2BD` | Bordures, états disabled |
| `--color-neutral-400` | `#8A8783` | Texte secondaire, captions |
| `--color-neutral-500` | `#6B6864` | Texte tertiaire |
| `--color-neutral-600` | `#52504C` | Texte body alternatif |
| `--color-neutral-700` | `#3A3835` | Texte de corps en mode clair |
| `--color-neutral-800` | `#2A2724` | Surfaces dark (cards en mode sombre) |
| `--color-neutral-900` | `#1A1816` | **Surface principale en mode sombre** |
| `--color-neutral-950` | `#0F0E0D` | **Texte principal en mode clair / fond ultime mode sombre** |

## Couleurs sémantiques

Toutes désaturées pour ne pas concurrencer la couleur signature.

| Token | Hex | Usage |
| --- | --- | --- |
| `--color-success` | `#2D6A4F` | Confirmations, validations |
| `--color-warning` | `#B8860B` | Avertissements, états intermédiaires |
| `--color-error` | `#A52121` | Erreurs (distinct du primary) |
| `--color-info` | `#3A6EA5` | Informations contextuelles |
| `--color-success-dark` | `#6FBF95` | Variante éclaircie de success pour le mode sombre |
| `--color-error-dark` | `#E57373` | Variante éclaircie de error pour le mode sombre |
| `--color-warning-light` | `#8A6508` | Variante assombrie de warning pour le mode clair |

Les variantes `-dark` existent parce que `success` et `error` tombent sous 3:1 sur `--surface-elevated` en mode sombre (#2A2724) : 2,3:1 et 2,0:1. Éclaircies, elles y atteignent 6,8:1 et 5,0:1. Le rouge sombre reste distinct du vermillon `--accent` du mode sombre (#EE6A47).

Pour `warning`, le problème est inverse : #B8860B ne tient que 3,25:1 sur `--surface-elevated` en mode clair (#FFFFFF), sous les 4,5:1 requis pour un texte Body S. La variante `-light` (#8A6508) y atteint 5,3:1 ; en mode sombre, la valeur d'origine tient 4,6:1 et reste en place.

## Tokens sémantiques (à utiliser dans le code)

Toujours référencer les tokens sémantiques plutôt que les valeurs littérales — ils s'adaptent automatiquement au mode clair/sombre.

> Les valeurs canoniques (primitives + tokens sémantiques clair/sombre) vivent dans [`tokens/tokens.css`](../../tokens/tokens.css). Ne pas redéfinir de hex ici.

| Token sémantique | Mode clair | Mode sombre |
| --- | --- | --- |
| `--surface-primary` | `neutral-100` (#F5F0E8) | `neutral-950` (#0F0E0D) |
| `--surface-secondary` | `neutral-50` (#FAFAF8) | `neutral-900` (#1A1816) |
| `--surface-elevated` | `neutral-0` (#FFFFFF) | `neutral-800` (#2A2724) |
| `--surface-inverse` | `neutral-950` (#0F0E0D) | `neutral-100` (#F5F0E8) |
| `--text-primary` | `neutral-950` (#0F0E0D) | `neutral-100` (#F5F0E8) |
| `--text-secondary` | `neutral-600` (#52504C) | `neutral-300` (#C4C2BD) |
| `--text-tertiary` | `neutral-400` (#8A8783) | `neutral-400` (#8A8783) |
| `--text-inverse` | `neutral-100` (#F5F0E8) | `neutral-950` (#0F0E0D) |
| `--text-accent` | `primary-500` (#E8482A) | `primary-400` (#EE6A47) |
| `--border-subtle` | `neutral-200` (#E8E5DF) | `neutral-800` (#2A2724) |
| `--border-default` | `neutral-300` (#C4C2BD) | `neutral-700` (#3A3835) |
| `--border-accent` | `primary-500` (#E8482A) | `primary-400` (#EE6A47) |
| `--accent` | `primary-500` (#E8482A) | `primary-400` (#EE6A47) |
| `--accent-hover` | `primary-600` (#C73A1F) | `primary-300` (#F39174) |
| `--accent-subtle` | `primary-50` (#FDF1ED) | `primary-900` (#4A1408) |
| `--feedback-success` | `success` (#2D6A4F) | `success-dark` (#6FBF95) |
| `--feedback-warning` | `warning-light` (#8A6508) | `warning` (#B8860B) |
| `--feedback-error` | `error` (#A52121) | `error-dark` (#E57373) |
| `--feedback-info` | `info` (#3A6EA5) | `info` (#3A6EA5) |

En mode sombre, `--text-accent` et `--accent` passent à `primary-400` (#EE6A47), légèrement éclairci pour préserver le contraste.

Les tokens `--feedback-*` servent aux retours d'état (bordure du Message, par exemple). `info` n'a pas encore été vérifié en contraste : à traiter quand un composant l'utilisera.
