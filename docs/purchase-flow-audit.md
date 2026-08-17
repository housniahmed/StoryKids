# StoryKids — audit du parcours d’achat actuel

Date : 17 août 2026

## Parcours actuellement visible

La landing page renvoie les visiteurs vers trois liens Stripe distincts depuis les cartes d’offres. Les offres publiques sont Mon histoire à 299 MAD, Mon histoire + narration à 449 MAD et StoryKids Premium à 699 MAD. Les autres CTA renvoient soit vers l’ancre des offres, soit vers l’ancre de contact WhatsApp.

Une page de confirmation existe déjà à l’adresse `/merci-votre-histoire-storykids-est-bien-commandee/`. Le site utilise également WhatsApp au numéro +212 664 740 015 pour le contact initial.

## Parcours manquant ou non démontré

Le parcours public ne démontre pas encore un formulaire de personnalisation relié à la commande, un upload sécurisé des photos après paiement, une confirmation automatique contenant une référence de commande, un tableau de suivi de production, un mécanisme d’aperçu avec validation explicite du parent, ni une livraison structurée par offre. Les liens Stripe existants doivent donc être conservés, mais complétés par une passerelle claire vers le formulaire de personnalisation et la collecte sécurisée des éléments de commande.

## Parcours cible demandé

Landing page → Choix de l’offre → Paiement → Formulaire de personnalisation → Upload des photos → Confirmation → Production → Aperçu → Validation → Livraison.

## Points à clarifier techniquement avant automatisation complète

Il faut confirmer si les liens Stripe peuvent rediriger vers une URL de succès contenant l’identifiant de session ou de paiement, si Stripe collecte déjà l’e-mail du client, où les photos doivent être stockées pendant la production, qui reçoit les notifications de nouvelle commande, comment l’aperçu est partagé, et quel canal est utilisé pour la validation finale et la livraison.

Les paiements par virement bancaire doivent suivre le même formulaire de personnalisation, mais leur passage en production ne doit intervenir qu’après vérification manuelle du virement. Les photos d’enfants doivent être collectées uniquement après consentement parental et conservées pendant la durée réelle du travail, avec suppression définitive 48 heures après la livraison, conformément aux informations déjà validées.

## 17 août 2026 — intégration MVP

Le constructeur WPForms étant inutilisable en raison d’une expiration persistante de session, le formulaire Contact Form 7 existant « StoryKids — Raconter son aventure » a été utilisé comme solution de secours stable. Il a été renommé « StoryKids — Créer votre histoire » et enregistré.

Le formulaire contient désormais le prénom et WhatsApp du parent, l’e-mail, le prénom et l’âge de l’enfant, les personnes à faire apparaître, le récit de l’aventure, l’offre choisie, le consentement parental et un champ d’upload de photos. Les photos sont attachées à la notification e-mail d’administration via le tag `[photos]`.

La page post-paiement « Bienvenue dans votre aventure StoryKids » contient maintenant le shortcode `[contact-form-7 id="12" title="StoryKids — Créer votre histoire"]`. Le rendu public confirme que le formulaire, le champ upload et les trois offres sont visibles.

Limites à valider avant utilisation commerciale : le canal de réception des pièces jointes doit être confirmé comme suffisamment sécurisé ; la conservation des e-mails et pièces jointes doit être maîtrisée ; un vrai test avec données non sensibles doit être réalisé ; les redirections Stripe doivent être vérifiées pour chaque offre ; aucune commande test réelle n’a été envoyée.

Les pages juridiques restent en brouillon et n’ont pas été publiées.

### Références de parcours

Landing page → choix de l’offre → paiement Stripe ou virement → page Bienvenue → formulaire de personnalisation et photos → notification manuelle → production → aperçu → validation → livraison numérique sous 2 à 4 jours.

Le suivi production, l’aperçu, la validation et la livraison restent manuels dans le MVP, sans automatisation inventée.

---


## Résultat du test fictif

Une soumission fictive sans photo et sans donnée personnelle a été envoyée depuis la page publique avec les valeurs « Test StoryKids », « Test » et `test@example.com`. Le formulaire a affiché « Thank you for your message. It has been sent. », confirmant l’acceptation côté navigateur et le message de succès Contact Form 7. Aucun achat Stripe ou virement n’a été effectué, et aucune photo n’a été transmise. La réception effective de l’e-mail doit encore être vérifiée dans la boîte d’administration.

---

