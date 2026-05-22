# Accessibilité & Do / Don't

## Contrastes (WCAG 2.2)

| Combinaison | Ratio | Niveau | Usage autorisé |
| --- | --- | --- | --- |
| `text-primary` sur `surface-primary` (clair) | 17.5:1 | AAA | Tout texte |
| `text-secondary` sur `surface-primary` (clair) | 7.4:1 | AAA | Tout texte |
| `text-tertiary` sur `surface-primary` (clair) | 3.5:1 | AA Large | **Texte ≥ 18px uniquement** |
| `--accent` (`#E8482A`) sur `surface-primary` (clair) | 3.7:1 | AA Large | **Texte ≥ 18px ou bold ≥ 14px / non-text UI** |
| `--accent` sur `--surface-inverse` (sombre) | 4.5:1 | AA | Tout texte |

**Règle critique** : la couleur primary `#E8482A` ne doit **jamais** être utilisée pour des paragraphes de corps de texte sur fond clair — son contraste est insuffisant. Elle est réservée aux titres, aux CTA, aux soulignements et aux éléments graphiques. Pour du texte de lien inline sur fond clair, utiliser `--color-primary-700` (`#9F2D17`).

## Tailles tactiles

Toute cible interactive doit mesurer au minimum **44 × 44 px** sur mobile.

## Focus

États focus visibles obligatoires sur tous les éléments interactifs :

```css
:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 2px;
}
```

## Réduction du mouvement

Respecter `prefers-reduced-motion` pour toutes les animations.

---

## Do / Don't

| ✅ Do | ❌ Don't |
| --- | --- |
| Utiliser le crème `#F5F0E8` comme surface principale en mode clair | Utiliser le blanc pur `#FFFFFF` comme fond généralisé |
| Mettre un ou deux mots-clés en italique serif par titre | Mettre des phrases entières en italique |
| Aérer généreusement les sections | Remplir l'espace par peur du vide |
| Utiliser l'accent vermillon avec parcimonie (CTA, soulignements, mots-clés) | Saturer la page d'accents colorés |
| Référencer les tokens sémantiques (`--text-primary`) | Hardcoder des valeurs hex dans le code |
| Adapter les tailles typo en mobile | Garder des tailles desktop sur petits écrans |
| Respecter l'échelle de spacing 4px | Utiliser des valeurs intermédiaires (15px, 22px…) |
| Tester systématiquement le mode sombre | Designer uniquement en mode clair |
