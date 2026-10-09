# appforge   # AppForge

**Rebuild any product workflow, cleanly.**

AppForge est une suite de 11 skills Claude qui analysent les parcours, fonctionnalités et patterns d'interface d'un produit, puis conçoivent et développent une alternative originale.

Il ne reproduit pas le code source, les marques, logos, textes, visuels, données ou contenus protégés d'un service existant. Toute création est réalisée de manière indépendante, à partir d'une analyse de fonctionnalités et d'expérience utilisateur.

## Parcours

| Étape | Skill | Rôle |
|---|---|---|
| 1 | `/appforge-recon` | Cartographie : écrans, flows, composants, modèle de données, matrice de fonctionnalités |
| 2 | `/appforge-architect` | Stack, schéma SQL, API par flow, ordre de build en tranche verticale |
| 3 | `/appforge-design` | Design system : rôles de couleurs, typographie, espacements, tokens, contraste WCAG |
| 4 | `/appforge-build` | Construction écran par écran, états complets, matrice cochée au fil de l'eau |
| 5 | `/appforge-backend` | Auth, base et règles d'accès, paiements, emails, jobs, intégrations via API officielles |
| 6 | `/appforge-test` | Plan de test, tests Playwright end-to-end, rapports de bugs formatés |
| 7 | `/appforge-diff` | Score de parité avec la matrice, diff visuel ignorant la couleur |
| 8 | `/appforge-entrepreneur` | Lecture des avis publics (citations réelles et liées) : ce qui manque, ce qui gêne |
| 9 | `/appforge-brand` | Nom, palette, logo, voix, balayage des restes de l'original |
| 10 | `/appforge-launch` | Landing page, tarification, fiches App Store et Google Play |
| 11 | `/appforge-deploy` | Mise en production : preflight, base, DNS, Stripe live, TestFlight et Play |

## Installation

Dépôt : https://github.com/dvdlgustin-afk/appforge

Cloner le dépôt puis copier les skills dans le répertoire de Claude Code :

```bash
git clone https://github.com/dvdlgustin-afk/appforge
cp -r appforge/appforge-* ~/.claude/skills/
```

Vérifier avec `/appforge-recon` dans Claude Code.

## Prérequis

- Python 3 (scripts `contrast.py`, `parity.py`, `imgdiff.py`, `sweep.py`, `reviews.py` : bibliothèque standard uniquement)
- Node.js et Playwright pour les tests end-to-end (`appforge-test`)

## Règles de conduite

- Écrire chaque ligne de code à neuf : ni le code, ni les assets, ni les textes de l'original.
- Remplacer les logos, icônes, illustrations et polices sous licence par des éléments originaux.
- Ne pas utiliser de nom, marque ou domaine proche de l'original : `/appforge-brand` vérifie ces points.
- Passer par les API publiques et officielles uniquement. Pas d'API privée ni de scraping de données protégées.
- Les secrets restent dans les variables d'environnement, jamais dans le code client.

## Crédits et licence

AppForge est un rebrand de **Replica** par Jake Schincariol (opusjake.ai), publié sous licence MIT.

```text
Portions based on Replica by Jake Schincariol (opusjake.ai),
licensed under the MIT License.
Copyright (c) 2026 Jake Schincariol.
```

La licence MIT autorise l'utilisation, la modification et la redistribution, à condition de conserver l'avis de copyright et la permission dans les copies et œuvres dérivées. Voir `LICENSE`.
