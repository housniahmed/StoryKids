# Périmètre de l’export

## Inclus

L’export contient un instantané HTML public de la landing page StoryKids restaurée, ainsi que la documentation de versioning et de restauration. Ces fichiers servent de référence visuelle et éditoriale pour comparer les futurs changements.

## Exclus volontairement

Sont exclus les identifiants WordPress, les cookies de session, les tokens GitHub, les clés Stripe, les coordonnées bancaires, les données de formulaires, les photos d’enfants, les adresses e-mail privées et toute autre donnée personnelle. La sauvegarde XML WordPress complète reste conservée localement dans l’environnement de travail, mais n’est pas publiée dans le dépôt sans nettoyage et validation supplémentaires.

## Limite technique

Un instantané HTML ne contient pas à lui seul les réglages WordPress, le thème, les extensions, la base de données ou les médias originaux. Il garantit la traçabilité du rendu observé, mais une restauration complète nécessite une sauvegarde WordPress ou hébergeur distincte.

## Prochaine étape recommandée

Pour obtenir un historique réellement déployable, il faudra identifier le thème et le constructeur utilisés, exporter leurs fichiers ou modèles, puis mettre en place une procédure de publication séparant clairement les environnements de test et de production.
