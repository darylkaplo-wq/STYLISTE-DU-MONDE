# Styliste du Monde

Application web de stylisme et de découverte de mode multiculturelle : création de tenues, recommandations de la styliste, comptes utilisateurs, tenues sauvegardées, inspiration et catalogue marchand importable.

## État du dépôt

Ce dépôt accueille la version de livraison du 31 octobre 2026. Le projet source utilise Node.js 22.5+, SQLite (node:sqlite) et des fichiers locaux. Il ne doit pas être présenté comme déjà migré vers Cloudflare Workers/D1/R2.

## Démarrage local

    cp .env.example .env
    npm install
    npm run seed
    npm start

Puis ouvrir http://localhost:3000.

## Tests

    npm test

## Documentation

- docs/PLAN.md — périmètre et plan du projet
- docs/DEPLOIEMENT.md — lancement et déploiement
- docs/DECISION-HEBERGEMENT.md — choix d'hébergement et migration nécessaire
- docs/AVANT-OUVERTURE-PUBLIQUE.md — contrôles avant lancement public
- docs/FOURNISSEURS-CATALOGUE-ET-IMAGES.md — sources de catalogue et règles d'utilisation des images
- docs/AUDIT-LANCEMENT-2026-10-31.md — audit de livraison

## Avant une ouverture publique

Compléter les informations légales, vérifier les droits sur les images et flux marchands, configurer les secrets hors du dépôt, auditer l'authentification et effectuer la migration de la base et des médias vers un stockage persistant.

Ne jamais committer le fichier .env, des mots de passe, des clés API ou des jetons.