# StoryKids — Export versionné du site WordPress

Ce dépôt conserve des instantanés publics et une documentation de traçabilité du site [story-kidz.com](https://www.story-kidz.com/). Il ne remplace pas une sauvegarde complète de l’hébergement WordPress et ne contient volontairement aucun mot de passe, cookie, token, clé de paiement, donnée client ou identifiant privé.

## État exporté

L’instantané `site-snapshot/homepage-restored.html` correspond à la landing page restaurée depuis l’historique WordPress, après l’annulation de la refonte non souhaitée. Il a été récupéré le 16 août 2026 après vérification publique du site.

## Fichiers

| Chemin | Description |
| --- | --- |
| `site-snapshot/homepage-restored.html` | Instantané HTML public de la page d’accueil restaurée. |
| `docs/restore.md` | Procédure de traçabilité et de restauration future. |
| `docs/export-scope.md` | Périmètre, limites et exclusions de cet export. |

## Versioning recommandé

Chaque modification future doit être précédée d’un instantané daté, d’une description claire et d’un commit séparé. Les messages de commit doivent indiquer la zone modifiée et l’objectif, par exemple `landing: update hero copy` ou `landing: restore pre-change snapshot`.

> Important : modifier un fichier dans GitHub ne modifie pas automatiquement le site WordPress. La publication vers WordPress doit rester une opération distincte et vérifiée.
