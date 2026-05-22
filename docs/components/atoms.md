# Atomes

Les composants sont organisés en trois niveaux (atomes · patterns portfolio · layout). Cette organisation doit être reflétée dans le fichier Figma (page Components, sous-sections).

| Composant | Variantes / propriétés | États | Total |
| --- | --- | --- | --- |
| Button | `variant` : primary / secondary / ghost / link · `size` : sm / md / lg | default / hover / pressed / disabled | 48 |
| Icon Button | `variant` : default / ghost · `size` : md / lg | default / hover / pressed / disabled | 16 |
| Input | text / email | default / focus / filled / error / disabled | 5 |
| Textarea | — | default / focus / filled / error / disabled | 5 |
| Tag | `variant` : neutral / accent · `style` : solid / outline · `size` : sm / md | static | 8 |
| Avatar | `size` : xs (24) / s (32) / m (40) / l (64) | static | 4 |
| Link | — | default / hover | 4 |
| Icon | une variante par icône Phosphor (cf. ci-dessous) | static | — |
| Divider | `orientation` : horizontal / vertical · `style` : subtle / default | — | 4 |

## Notes de spécification

- **Icon Button** — la propriété `size` (md/lg) a été ajoutée par rapport à la spec initiale pour couvrir les usages portfolio (theme toggle en md, actions de nav en lg). Pas de `sm` : aucun cas d'usage identifié.
- **Divider** — la propriété `style` (subtle / default) a été ajoutée pour distinguer les séparations internes discrètes (`border/subtle`) des séparations de section plus marquées (`border/default`).
- **Input vs Textarea** — séparés en deux composants distincts plutôt qu'un seul atom à 3 types, pour garder des dimensions par défaut et des comportements de redimensionnement spécifiques.
- **Loading state du Button** — non implémenté dans la première version. À ajouter quand un cas d'usage portfolio le justifiera (formulaire de contact en soumission, par exemple).
- **Pas d'atom Link dédié** — les liens du système se répartissent en deux usages couverts ailleurs : (1) les CTA tertiaires utilisent le `variant=link` du Button, (2) les liens éditoriaux inline sont traités comme un *text style* avec soulignement vermillon (cf. [Signature 2](../signatures.md)).
- **Link** — atom de lien, en Inter Regular 18px (Body L) sur `text/primary`, sans soulignement vermillon. Pensé pour les liens de navigation et de footer (retour à l'accueil, réseaux sociaux). Un espace pour une icône Phosphor (24px) avant le texte apparaît au hover via une transition d'opacité. Coexiste avec deux autres mécanismes : (1) `variant=link` du Button pour les CTA tertiaires, (2) le text style soulignement vermillon pour les liens éditoriaux inline (cf. [Signature 2](../signatures.md)).

## Icônes

Librairie [Phosphor Icons](https://phosphoricons.com/), style **Light** retenu pour la première version — son trait fin renforce la dimension éditoriale tout en restant lisible à 24px. Ne jamais mélanger plusieurs styles dans un même écran.

Le composant `Icons` du fichier Figma expose une icône par variante de la propriété `Icon`. La collection est désormais **complète** : 1512 icônes Phosphor Light, de `acorn-light 1` à `youtube-logo-light 1`. Toute spec peut référencer librement une icône Phosphor Light.

**À retenir** : la couleur du composant Icons est bindée à `color/neutral/950` (token primitif). Cela signifie que les icônes restent sombres en mode sombre — il faudra rebinder à `text/primary` (token sémantique) au moment du chantier dark mode.
