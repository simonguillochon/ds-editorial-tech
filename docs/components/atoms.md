# Atomes

Les composants sont organisés en trois niveaux (atomes · patterns portfolio · layout). Cette organisation doit être reflétée dans le fichier Figma (page Components, sous-sections).

| Composant | Variantes / propriétés | États | Total |
| --- | --- | --- | --- |
| Button | `variant` : primary / secondary / ghost / link · `size` : sm / md / lg | default / hover / pressed / disabled | 48 |
| Icon Button | `variant` : default / ghost · `size` : md / lg | default / hover / pressed / disabled | 16 |
| Input | `type` : text / email / password | default / focus / filled / error / disabled | 15 |
| Password Input | `visible` : false / true · composition Input + Icon Button ghost md | default / focus / filled / error / disabled | 10 |
| Textarea | — | default / focus / filled / error / disabled | 5 |
| Field label | — | static | 1 |
| Checkbox | `checked` : false / true | default / hover / focus / disabled | 8 |
| Choice Group | composition de Buttons sm secondary | none / selected / disabled | 3 |
| Message | `variant` : success / warning / error | static | 3 |
| Tag | `variant` : neutral / accent · `style` : solid / outline · `size` : sm / md | static | 8 |
| Avatar | `size` : xs (24) / s (32) / m (40) / l (64) | static | 4 |
| Link | — | default / hover | 2 |
| Icon | une variante par icône Phosphor (cf. ci-dessous) | static | — |
| Divider | `orientation` : horizontal / vertical · `style` : subtle / default | — | 4 |

## Notes de spécification

- **Icon Button** — la propriété `size` (md/lg) a été ajoutée par rapport à la spec initiale pour couvrir les usages portfolio (theme toggle en md, actions de nav en lg). Pas de `sm` : aucun cas d'usage identifié.
- **Divider** — la propriété `style` (subtle / default) a été ajoutée pour distinguer les séparations internes discrètes (`border/subtle`) des séparations de section plus marquées (`border/default`).
- **Input vs Textarea** — séparés en deux composants distincts plutôt qu'un seul atom à 3 types, pour garder des dimensions par défaut et des comportements de redimensionnement spécifiques.
- **Loading state du Button** — non implémenté dans la première version. À ajouter quand un cas d'usage portfolio le justifiera (formulaire de contact en soumission, par exemple).
- **Link** — atom de lien, en Inter Regular 18px (Body L) sur `text/primary`, sans soulignement vermillon. Pensé pour les liens de navigation et de footer (retour à l'accueil, réseaux sociaux). Au hover, une icône Phosphor (24px) apparaît avant le texte via une transition d'opacité ; l'icône par défaut est `arrow-right`, remplaçable selon l'usage (par exemple `arrow-left` pour un retour). Coexiste avec deux autres mécanismes : (1) `variant=link` du Button pour les CTA tertiaires, (2) le text style soulignement vermillon pour les liens éditoriaux inline (cf. [Signature 2](../signatures.md)).
- **Input — propriété `type`** — la valeur `password` s'ajoute à text et email. Le type devient une propriété de variant (3 types × 5 états = 15 variants) : seul le contenu du champ change (placeholder, valeur saisie masquée par des puces pour `password`).
- **Password Input** — ajouté pour la saisie de secrets (Readme Capture, US-01). Input suivi d'un Icon Button ghost md, espacés de 8px (`--space-2`). Propriété `visible` : à `false`, le champ utilise l'Input `type=password` et l'icône `eye` (action « Afficher ») ; à `true`, l'Input `type=text` et l'icône `eye-slash` (action « Masquer »). L'Icon Button suit l'état `disabled` de l'Input. En code : libellé accessible « Afficher » / « Masquer » et `aria-pressed` reflétant l'état visible.
- **Field label** — ajouté pour les formulaires (Readme Capture, US-01). Text style Caption sur `text/secondary`, 8px (`--space-2`) au-dessus du champ. En code : élément `label` relié au champ.
- **Checkbox** — ajouté pour les sélections multiples (Readme Capture, US-02). Case de 20px, rayon `sm`, libellé Body sur `text/primary` à droite (8px). `checked` est une propriété distincte de l'état, pour que chaque état (hover, focus, disabled) existe coché et non coché. Non cochée : fond `surface/elevated`, bordure `border/default` (`border/accent` au hover). Cochée : fond `accent/default` (`accent/hover` au hover), coche `check` sur `text/inverse`. Focus : anneau 2px `accent`, décalé de 2px, identique aux autres atomes. En code : `input type="checkbox"` relié à son libellé, navigation par Tab, cochage par Espace, cible tactile 44 × 44px sur mobile.
- **Choice Group** — ajouté pour les choix exclusifs sans valeur par défaut (Readme Capture, US-02). Rangée de Buttons `size=sm` `variant=secondary`, espacés de 8px. L'option choisie garde le style secondary et reçoit une bordure 2px `border/accent` — plutôt qu'un Button primary, pour ne pas multiplier les aplats vermillon quand plusieurs groupes cohabitent (cf. principe « une seule couleur signature, avec parcimonie »). En code : `role="radiogroup"` sur le conteneur, `role="radio"` et `aria-checked` sur chaque bouton, flèches pour passer d'une option à l'autre.
- **Message** — ajouté pour les retours d'action (Readme Capture, US-01). Bloc de 320px, padding 12px (`--space-3`), rayon `sm`, fond `surface/elevated`, bordure 1px et texte Body S de la même couleur, `feedback/success`, `feedback/warning` ou `feedback/error`. Contraste du texte vérifié en Body S (≥ 4,5:1) sur `surface/elevated` : success 6,4:1 en clair et 6,8:1 en sombre, warning 5,3:1 en clair et 4,6:1 en sombre, error 7,4:1 en clair et 5,0:1 en sombre. Le texte porte seul le sens du message : la couleur de bordure ne doit jamais être l'unique indice. En code : `role="status"` pour success et warning, `role="alert"` pour error.

## Icônes

Librairie [Phosphor Icons](https://phosphoricons.com/), style **Light** retenu pour la première version — son trait fin renforce la dimension éditoriale tout en restant lisible à 24px. Ne jamais mélanger plusieurs styles dans un même écran.

Le composant `Icons` du fichier Figma expose une icône par variante de la propriété `Icon`. La collection est désormais **complète** : 1512 icônes Phosphor Light, de `acorn-light 1` à `youtube-logo-light 1`. Toute spec peut référencer librement une icône Phosphor Light.

**Couleur** : le composant Icons est bindé à `text/primary` et s'inverse en mode sombre. Une icône posée sur un fond coloré (coche de la Checkbox, par exemple) surcharge sa couleur avec `text/inverse`.
