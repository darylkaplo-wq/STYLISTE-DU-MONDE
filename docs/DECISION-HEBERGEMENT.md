# Hébergement et migration

## État actuel du code source

La version de livraison identifiée utilise Node.js 22.5+, `node:sqlite` et un stockage de fichiers local. Elle ne peut pas être publiée telle quelle comme un site statique Cloudflare Pages ni être considérée comme déjà compatible Workers/D1/R2.

## Architecture cible proposée

- Cloudflare Workers : API HTTP et logique serveur adaptée au runtime Workers.
- Cloudflare D1 : données relationnelles, après adaptation de la couche d'accès SQL.
- Cloudflare R2 : images et médias téléversés, avec contrôle des droits d'utilisation.
- GitHub Actions : tests et contrôles automatiques.

## Travaux nécessaires avant déploiement

1. Migrer les routes Node HTTP vers le runtime Workers (ou un framework compatible).
2. Remplacer `node:sqlite` par les bindings D1 et adapter les requêtes au driver D1.
3. Remplacer les accès au système de fichiers par R2 pour les médias persistants.
4. Ajouter les migrations D1 et vérifier l'initialisation des données.
5. Adapter les tests au runtime cible et exécuter une suite complète.
6. Configurer les secrets uniquement dans Cloudflare, jamais dans Git.
7. Vérifier les politiques légales, les flux marchands et les droits des images avant ouverture publique.

Ne pas déployer en production tant que ces étapes et les tests de sécurité ne sont pas terminés.