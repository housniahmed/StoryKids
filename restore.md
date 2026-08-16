# Procédure de restauration et de traçabilité

## Avant toute modification

Créer une sauvegarde complète depuis WordPress ou l’hébergeur, puis exporter la page d’accueil et les médias réellement utilisés. Vérifier que la sauvegarde ne contient pas de mots de passe, cookies, clés API, informations bancaires ou données de clients avant toute publication dans GitHub.

## Version Git

Créer un commit distinct pour chaque état publiable. Pour revenir à un état antérieur, consulter l’historique du dépôt, identifier le commit voulu et le restaurer dans une nouvelle branche ou un nouveau commit. Éviter de réécrire l’historique partagé avec `git push --force`.

## Restauration WordPress

La restauration fonctionnelle du site doit être effectuée depuis l’administration WordPress, l’hébergeur ou une sauvegarde complète. Pour une page individuelle, ouvrir la page dans WordPress, consulter les révisions, sélectionner la version souhaitée, vérifier le contenu puis utiliser **Restaurer cette révision**. Après restauration, contrôler la page publique, les boutons, les images, la version mobile et le parcours de commande.

## État de référence actuel

L’état de référence exporté est celui de la landing page après restauration de la révision WordPress datée du 15 août 2026 à 21 h 06. L’instantané public associé est `site-snapshot/homepage-restored.html`.

## Limite importante

Le fichier HTML du dépôt est un instantané de référence et non un thème WordPress directement déployable. Pour une restauration complète et automatisable, il faudra ensuite versionner le thème ou les fichiers source du constructeur WordPress, ainsi qu’établir une procédure de déploiement contrôlée.
