# Signatures visuelles

Trois signatures, à utiliser systématiquement et exclusivement. Toute autre fioriture est hors charte.

## Signature 1 — L'italique éditorial

L'italique d'Instrument Serif sur des mots-clés du positionnement, dans les titres principaux. Apparition rare et stratégique.

> Product Manager *qui pense*, qui écrit, qui livre.

## Signature 2 — Le soulignement vermillon

Un trait `2px` en `--accent`, légèrement décollé du baseline (`text-underline-offset: 4px`), sur certains liens ou mots-clés inline. Inspiré du filet Hermès, transposé dans un contexte tech.

Cette signature s'applique comme un **text style** sur des mots ou portions de phrase à l'intérieur d'un bloc de texte — il ne s'agit pas d'un atom dédié. Elle cohabite avec deux autres mécanismes de liens du système : l'atom **Link** (lien autoportant, sans soulignement) et le **`variant=link` du Button** (CTA tertiaire). Les trois servent des intentions différentes :

- **Soulignement vermillon (text style)** : un ou plusieurs mots-clés à l'intérieur d'un paragraphe qui pointent vers une ressource éditoriale (« lire sur *Medium* », « publié dans la *Harvard Business Review* »).
- **Atom Link** : un lien autoportant sur sa propre ligne (« Back home », « LinkedIn », « GitHub »).
- **Button variant=link** : un CTA tertiaire, action faiblement marquée (« Voir tout », « Découvrir le projet »).

```css
.accent-underline {
  text-decoration: underline;
  text-decoration-color: var(--accent);
  text-decoration-thickness: 2px;
  text-underline-offset: 4px;
}
```

## Signature 3 — L'air

Les spacings entre sections sont volontairement généreux. Le ratio espace-vide / contenu doit toujours pencher du côté du vide. C'est un parti-pris assumé qui distingue le portfolio des grilles denses habituelles.

## Interdits visuels

Pour préserver la cohérence, **ne jamais utiliser** :

- Gradients (linéaires ou radiaux)
- Glassmorphism, neumorphism
- Ombres portées spectaculaires
- Motifs décoratifs (lignes, points, formes géométriques décoratives)
- Illustrations vectorielles génériques (style Storyset, unDraw, etc.)
- Plus d'une couleur d'accent
- Plus de deux familles typographiques
- Mélange de styles d'icônes
- Émojis dans les titres ou le contenu structurel
