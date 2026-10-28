# Changelog

Évolutions notables du design system Editorial Tech.

| Version | Date | Changements |
| --- | --- | --- |
| 1.0 | 2026-05-06 | Version initiale — direction Editorial Tech, palette vermillon, duo Instrument Serif + Inter, icônes Phosphor |
| 1.1 | 2026-05-09 | Ajustements suite à la construction des atoms : ajout des propriétés `size` sur Icon Button et `style` sur Divider · Input et Textarea séparés en deux composants · Phosphor Light retenu (au lieu de Regular) avec couverture H–Y · suppression de l'atom Link au profit du `variant=link` du Button et d'un text style pour les liens inline éditoriaux · note dark mode sur le binding des Icons |
| 1.2 | 2026-05-13 | Collection Icons complétée : passage de 751 à 1512 variants, couverture intégrale de Phosphor Light (A–Y) |
| 1.3 | 2026-05-15 | Réintroduction d'un atom **Link** (4 variants `has icon × state`) pour les liens autoportants type navigation et footer. La Signature 2 (soulignement vermillon) reste un text style inline, distinct de l'atom Link. Trois mécanismes de liens coexistent désormais : soulignement vermillon (mots-clés inline), atom Link (lien autoportant), Button `variant=link` (CTA tertiaire). |
| 1.4 | 2026-10-28 | Atoms issus de Readme Capture : ajout de **Password Input** (10 variants `visible × state`), **Field label**, **Message** (success / error, texte et bordure en `feedback/*`), **Checkbox** (8 variants `checked × state`) et **Choice Group** (option choisie en secondary bordé `border/accent`) · propriété `type` sur Input avec la valeur `password` (15 variants) · tokens `--feedback-*` documentés, avec variantes sombres `success-dark` et `error-dark` pour tenir 3:1 en mode sombre · Icons rebindés à `text/primary` pour le mode sombre · `arrow-right` comme icône par défaut du Link au hover · correction du total de l'atom Link (2 variants) et retrait de la note obsolète « Pas d'atom Link dédié » |
| 1.5 | 2026-10-28 | Variante **warning** du Message (texte et bordure en `feedback/warning`) · primitive `--color-warning-light` (#8A6508) pour tenir 4,5:1 en mode clair, `--feedback-warning` rebranché dessus en mode clair |
