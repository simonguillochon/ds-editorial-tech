# Typographie

## Familles

| Rôle | Famille | Source |
| --- | --- | --- |
| **Titres** | Instrument Serif | [Google Fonts](https://fonts.google.com/specimen/Instrument+Serif) |
| **Corps & UI** | Inter | [Google Fonts](https://fonts.google.com/specimen/Inter) |
| **Mono** | Geist Mono | [Vercel](https://vercel.com/font) |

Le contraste serif éditorial / grotesque tech est la **deuxième signature visuelle** du système, après la couleur. Il doit être préservé partout.

## Échelle typographique

Base 16px. Mobile-first — les tailles indiquées sont les tailles desktop, à réduire d'environ 20-30 % sur mobile pour les niveaux Display et H1.

| Niveau | Taille (desktop) | Taille (mobile) | Famille | Graisse | Line-height | Letter-spacing |
| --- | --- | --- | --- | --- | --- | --- |
| Display | 96px | 56px | Instrument Serif | Regular | 1.05 | -0.02em |
| H1 | 64px | 40px | Instrument Serif | Regular | 1.1 | -0.02em |
| H2 | 40px | 32px | Instrument Serif | Regular | 1.15 | -0.01em |
| H3 | 28px | 24px | Instrument Serif | Regular | 1.25 | -0.01em |
| H4 | 20px | 18px | Inter | Medium (500) | 1.4 | -0.005em |
| Body L | 18px | 17px | Inter | Regular (400) | 1.6 | 0 |
| Body | 16px | 16px | Inter | Regular (400) | 1.6 | 0 |
| Body S | 14px | 14px | Inter | Regular (400) | 1.5 | 0 |
| Caption | 13px | 13px | Inter | Medium (500) | 1.4 | 0.01em |
| Overline | 12px | 12px | Inter | Semibold (600) | 1.3 | 0.08em (uppercase) |
| Mono | 14px | 14px | Geist Mono | Regular | 1.5 | 0 |

## Italiques

L'italique d'Instrument Serif est particulièrement expressif. Utilise-le pour souligner les **mots-clés du positionnement** dans les titres : *empathie*, *recul*, *humain*, *innovation*. Maximum un ou deux mots en italique par titre — l'effet doit rester rare pour ne pas se diluer.

```html
<!-- Exemple -->
<h1>Product Manager <em>qui pense,</em> qui écrit, qui livre.</h1>
```

## Tokens CSS

Les tokens typographiques (`--font-serif`, `--font-sans`, `--font-mono` et l'échelle `--text-*`) sont définis dans [`tokens/tokens.css`](../../tokens/tokens.css).
