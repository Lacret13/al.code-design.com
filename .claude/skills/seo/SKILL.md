---
name: seo
description: Utiliser pour tout audit ou optimisation SEO du site aldesagn — meta tags, Open Graph, JSON-LD, sitemap.xml, robots.txt, ET référencement local (fiche Google Business Profile, avis, citations, cohérence NAP). Se déclenche sur "vérifie le SEO", "optimise le référencement", "audit SEO local", ou lors de modifications des balises meta / de la section secteurs.
---

# SEO — Audit technique on-page + référencement local

Fusionne deux sources : l'audit technique on-page de [aevans-eng/seo-skill](https://github.com/aevans-eng/seo-skill) et le framework de référencement local de [AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo/blob/main/skills/seo-local/SKILL.md) (13,3k★ — le plus complet des deux, retenu comme base), adapté à aldesagn (site vitrine pour commerces locaux : boulangeries, garages, salons, restaurants).

## Partie A — Audit technique on-page (déjà en place, à revalider à chaque changement)

- **Meta tags** : `<title>` unique et descriptif, `meta description` (déjà optimisée : "Sites web professionnels pour... Devis fixe en 36h...") — à revoir si l'offre change (prix, délai)
- **Open Graph / Twitter Card** : déjà complets (`og:title`, `og:description`, `og:image` 1200×630, `twitter:card`) — vérifier la cohérence si le texte de l'offre change ailleurs sur la page
- **JSON-LD** : 2 blocs déjà présents dans `index.html` — vérifier qu'ils restent valides (schema.org) après toute modification de structure
- **`robots.txt` / `sitemap.xml`** : déjà présents et cohérents (le sitemap liste les ancres `#secteurs`, `#tarifs`, `#maintenance`, `#demo`, `#contact`) — mettre à jour `lastmod` et ajouter toute nouvelle ancre/section créée
- **Images** : `alt` descriptif sur toute image ajoutée ; `og-image.png` (196 Ko) — garder un poids raisonnable si remplacée
- **Canonical** : `https://aldesagn.fr/` — s'assurer qu'il reste correct si le domaine change
- **HTTPS / liens cassés** : vérifier après tout ajout de lien externe

## Partie B — SEO local (le plus impactant business-wise pour ce site)

Le site cible explicitement des commerces locaux avec du contenu "SEO local" en meta keywords — ce volet compte plus que le volet technique pour la conversion des clients d'aldesagn.

1. **Signaux GBP (Google Business Profile)** — prioritaire : quand un client d'aldesagn est onboardé, rappeler l'importance d'une fiche complète (catégorie exacte, photos, posts réguliers, statut vérifié)
2. **Avis & réputation** — la "règle des 18 jours" : la vélocité d'avis récents pèse plus que le total cumulé ; encourager une demande d'avis systématique après chaque livraison de site
3. **SEO local on-page** — titres/H1 localisés (ex: "Création site web [métier] à [ville]"), NAP (Nom/Adresse/Téléphone) visible en pied de page pour chaque client livré
4. **Cohérence NAP & citations** — Google, annuaires locaux (PagesJaunes, etc.), cohérence stricte entre toutes les sources
5. **Schema local par secteur** — utiliser le bon sous-type schema.org selon le métier du client (`Restaurant`, `AutoRepair`, `HairSalon`, `Bakery`, etc.)
6. **Autorité locale** — CCI, labels "meilleur de [ville]", mentions presse locale

## Format de rapport

Deux sections distinctes : **Technique** (pass/fail par point de la Partie A) et **Local** (score pondéré par dimension de la Partie B, priorisation Quick Wins → Effort moyen → Impact fort).
