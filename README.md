# Styliste du Monde

Projet d'application web de stylisme, création de tenues et découverte de mode multiculturelle.

## État vérifié au 31 octobre 2026

Le dépôt GitHub est créé et contient le dossier de préparation, les consignes de déploiement et la stratégie de migration. **Le code applicatif complet n'a pas encore été importé dans ce dépôt** : il se trouve dans l'archive de livraison conservée dans la bibliothèque du projet.

Le code source de cette archive a été exécuté séparément sous Node.js 22.16.0 : 29 tests sur 29 réussis. Un test local de démarrage a également renvoyé HTTP 200 pour `/`, `/api/products?limit=2` et `/api/facets`. Ces résultats ne sont pas encore un résultat CI de ce dépôt.

## Architecture source actuelle

- Node.js 22.5+ et `node:sqlite`.
- Base SQLite et médias stockés sur disque persistant.
- Catalogue de démonstration : 97 fiches sans prix, stock, images ni liens marchands validés.

## Architecture cible

Cloudflare Workers pour l'API, D1 pour les données relationnelles et R2 pour les médias. Cette migration nécessite un portage réel : le code source actuel dépend de modules Node (`node:sqlite`, `node:http`, `node:fs`) et ne peut pas être déployé tel quel comme Worker.

## Prochaines étapes

Consulter `docs/ROADMAP-16-ETAPES.md` et `docs/DECISION-HEBERGEMENT.md`. Ne pas considérer le produit comme lancé publiquement avant l'import du code, la migration ou le choix d'un hébergeur Node persistant, les tests de production, la configuration des secrets, du domaine et les validations légales.

Ne jamais committer `.env`, des mots de passe, des clés API ou des jetons.