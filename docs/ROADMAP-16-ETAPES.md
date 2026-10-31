# Roadmap de livraison — 16 étapes

Mis à jour le 31 octobre 2026. Une étape n'est cochée que si une preuve vérifiable existe.

## Validé dans cette session

- [x] 1. Retrouver et inspecter l'archive source de livraison (51 entrées).
- [x] 2. Vérifier le runtime source : Node.js 22.16.0.
- [x] 3. Installer/lancer les tests de l'archive : 29 réussis, 0 échec.
- [x] 4. Démarrer le serveur en environnement local isolé.
- [x] 5. Vérifier `GET /` : HTTP 200.
- [x] 6. Vérifier `GET /api/products?limit=2` : HTTP 200 et 97 fiches initiales.
- [x] 7. Vérifier `GET /api/facets` : HTTP 200.
- [x] 8. Vérifier la présence des pages de confidentialité et conditions dans l'archive.
- [x] 9. Vérifier les règles d'exclusion des secrets et données locales dans `.gitignore` source.
- [x] 10. Créer le dépôt GitHub et vérifier l'accès d'administration/écriture.
- [x] 11. Ajouter au dépôt le README d'état, le modèle d'environnement, le `.gitignore`, la stratégie d'hébergement et une CI de contrôle du dépôt.

## Non validé — travaux encore nécessaires

- [ ] 12. Importer les 51 éléments source dans le dépôt et exécuter les tests depuis GitHub Actions. Le dépôt contient actuellement le dossier de préparation, pas encore l'application complète.
- [ ] 13. Porter l'API et le stockage de `node:sqlite`/fichiers vers Cloudflare Workers + D1 + R2, ou choisir explicitement un hébergeur compatible Node + disque persistant.
- [ ] 14. Exécuter les tests d'intégration, sécurité, sauvegarde/restauration et parcours mobile sur l'environnement cible.
- [ ] 15. Configurer les secrets, le domaine, le DNS et HTTPS dans les comptes fournisseurs du propriétaire ; aucun accès fournisseur ou changement DNS n'est confirmé ici.
- [ ] 16. Charger des flux marchands réellement autorisés, valider les licences et mentions légales, puis effectuer une mise en production et un contrôle public.

## Preuves et limites

- Les tests ont été exécutés dans l'environnement local de cette session, pas dans GitHub Actions.
- Le catalogue de 97 fiches est un catalogue de démonstration sans prix, stock, images commerciales ni URL d'achat vérifiés.
- Les clés Unsplash, Awin, Rakuten et IA ne sont pas configurées/testées avec des comptes réels.
- Le domaine et les DNS ne sont pas confirmés ; aucune modification DNS n'a été effectuée.
- Le statut « prêt pour le public » est refusé tant que les étapes 12 à 16 ne sont pas validées.