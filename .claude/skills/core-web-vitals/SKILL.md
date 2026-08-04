---
name: core-web-vitals
description: Utiliser pour tout ce qui touche à la vitesse de chargement d'aldesagn — LCP, INP, CLS, poids des images/polices, optimisation performance. Se déclenche sur "le site est lent", "optimise les performances", "vérifie les Core Web Vitals", ou lors de l'ajout d'images/scripts/polices dans index.html.
---

# Core Web Vitals — Performance

Adapté de [addyosmani/web-quality-skills](https://github.com/addyosmani/web-quality-skills) (2,6k★, MIT — Addy Osmani, équipe performance Chrome), scopé à la stack statique d'aldesagn.

## Seuils cibles (Google)

| Métrique | Bon | À surveiller sur ce projet |
|---|---|---|
| **LCP** (Largest Contentful Paint) | ≤ 2.5s | L'élément du hero est probablement le plus lourd — revérifier après tout ajout d'image |
| **INP** (Interaction to Next Paint) | ≤ 200ms | Le générateur de démo interactif (`#demo`) est le point le plus sensible — JS déclenché au clic |
| **CLS** (Cumulative Layout Shift) | ≤ 0.1 | Vérifier que les polices Google Fonts ne provoquent pas de saut de mise en page |

## Points spécifiques à ce projet

- **Fichier unique** : `index.html` fait ~193 Ko — surveiller que cette taille ne grimpe pas significativement à chaque ajout de section
- **`og-image.png`** : 196 Ko — raisonnable pour une image Open Graph, mais compresser si elle grossit
- **Polices externes** (Plus Jakarta Sans + Fraunces via Google Fonts) : `preconnect` déjà présent sur `fonts.googleapis.com`/`fonts.gstatic.com` — bon réflexe, à garder si de nouvelles polices sont ajoutées
- **Formulaire EmailJS** : script tiers chargé — vérifier qu'il est en `async`/`defer` et ne bloque pas le rendu initial
- **Démo interactive** (`#demo`) : générateur pas-à-pas en JS — surveiller le temps de réponse au clic (INP), éviter les manipulations DOM lourdes synchrones

## Format de rapport

Tableau des 3 métriques (estimé/mesuré), causes probables identifiées dans le code, correctifs classés par effort (rapide / modéré / structurel).
