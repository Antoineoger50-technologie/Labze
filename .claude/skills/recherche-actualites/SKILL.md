---
name: recherche-actualites-contextualisees
description: Veille intelligente qui filtre les actualités selon le contexte personnel de l'utilisateur (objectifs, projets, activité). À activer quand l'utilisateur demande "fais-moi un point sur les actualités", "donne-moi les news du jour", "quoi de neuf", ou via la commande /morning. L'objectif est zéro bruit, seulement ce qui le concerne vraiment.
---

# Recherche d'actualités contextualisées

## But

Faire gagner du temps à l'utilisateur en lui présentant uniquement les actualités pertinentes vu sa situation, et pas un flux générique d'informations.

## Étapes

1. **Charger le contexte personnel**
   Lis `context/CONTEXT.md` pour récupérer :
   - L'activité principale de l'utilisateur
   - Ses objectifs court et long terme
   - Ses projets en cours
   - Son domaine d'aide prioritaire

   Ce sont les filtres qui déterminent ce qui est pertinent.

2. **Chercher les actualités**
   Utilise la recherche web pour trouver les actualités récentes (du jour ou des derniers jours) sur :
   - Le secteur d'activité de l'utilisateur
   - Les thématiques liées à ses projets et objectifs
   - Les outils ou plateformes qu'il utilise

   Privilégie des sources fiables et récentes. Recoupe quand c'est possible.

3. **Filtrer sans pitié**
   Écarte tout ce qui ne touche pas directement aux objectifs ou projets de l'utilisateur. Mieux vaut 3 actualités vraiment pertinentes que 10 génériques.

4. **Présenter le brief**
   Format court, lisible en 30 secondes :

   ```
   Veille du [date]

   1. [Titre de l'actualité]
      Pourquoi ça vous concerne : [une ligne reliée à un objectif ou projet précis]

   2. [Titre]
      Pourquoi ça vous concerne : [une ligne]

   3. [Titre]
      Pourquoi ça vous concerne : [une ligne]

   Focus suggéré aujourd'hui : [une action concrète alignée avec un objectif]
   ```

## Règles

- Communique en français, ton direct
- Pas de tirets longs (em dashes)
- Toujours relier chaque actualité à un élément concret du contexte de l'utilisateur
- Si aucune actualité pertinente n'est trouvée, le dire honnêtement plutôt que de remplir avec du bruit
- Si l'accès web n'est pas disponible, le signaler et proposer un focus basé uniquement sur les projets en cours
