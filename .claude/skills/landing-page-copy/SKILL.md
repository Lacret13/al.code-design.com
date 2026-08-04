---
name: landing-page-copy
description: Utiliser pour écrire ou retravailler le texte de vente d'aldesagn — hero, accroche, preuve sociale, gestion des objections, appels à l'action. Se déclenche sur "améliore le texte", "réécris l'accroche", "ajoute une section", "ça ne convertit pas assez", ou lors de l'édition du contenu textuel de index.html.
---

# Copywriting page de vente (framework conversion)

Adapté de [rampstackco/claude-skills](https://github.com/rampstackco/claude-skills/blob/main/skills/landing-page-copy/SKILL.md) (515★), calé sur la structure réelle d'aldesagn.

## Structure actuelle de la page (respecter cet ordre, ne pas réinventer)

1. **Hero** (`#hero-title`) — "Votre site web qui..." + CTA
2. **Secteurs** (`#secteurs`) — "Je connais [les métiers ciblés]"
3. **Différenciation** (`#cmp-title`) — "La différence, [aldesagn vs agences classiques]"
4. **Comment ça marche**
5. **FAQ** — "Les vraies questions"
6. **Tarifs** (`#tarifs`) — "Prix transparents" + options de personnalisation
7. **Maintenance** (`#maintenance`) — "Votre site toujours [à jour]", "Sans maintenance, [risque]"
8. **Comparaison agences** — "Ce que les grandes agences [ne font pas]"
9. **Démo interactive** (`#demo`) — générateur pas-à-pas (activité → offre → style → aperçu)
10. **Contact** (`#contact`) — formulaire EmailJS, confirmation "Demande reçue !"

## Règles à appliquer à chaque section

- **Hero** : bénéfice concret en premier (pas "nous créons des sites", mais ce que le client obtient), CTA unique et visible
- **Langage métier-spécifique** : parler le vocabulaire du secteur ciblé (boulanger ≠ garagiste) plutôt que du jargon web générique
- **Fonctionnalités → bénéfices** : ne jamais lister une feature brute sans dire ce qu'elle change pour le commerçant (ex: pas "responsive", mais "vos clients vous trouvent aussi bien depuis leur téléphone")
- **Objections courantes à couvrir** : prix ("pourquoi pas gratuit avec Wix"), délai (36h), engagement (sans engagement), maintenance (peur de la panne)
- **Une seule action principale par section** — ne pas diluer le CTA
- **Mobile-first** : la majorité des commerçants consulteront depuis leur téléphone, prévisualiser en mobile avant de valider une accroche

## Ce que ce skill ne doit pas faire

Ne pas casser la structure existante (ordre des 10 sections) sans demande explicite — proposer des améliorations de texte à l'intérieur de chaque section, pas une refonte de l'architecture.
