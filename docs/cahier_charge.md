Cahier des charges – ZeForm
===============

Le CRM utilise un formulaire en ligne pour gérer les inscriptions des stagiaires de la formation professionnelle (OFP) aux différentes activités sportives.

# Fonctionnement actuel 

Actuellement, les inscriptions sont gérées en plusieurs étapes :

1. Les stagiaires s'inscrivent à travers un formulaire accessible depuis une URL (avec Microsoft Form) en remplissant différentes informations.
2. L’administrateur récupère un fichier Excel auto-généré par Microsoft Form, avec l'ensemble des données des stagiaires. Il copie ces données dans un second fichier Excel pour établir la « liste de présence » pour les différentes activités sportives.
3. La liste de présence est ensuite envoyée, au format PDF, aux différents moniteurs sportifs, qui l'impriment.

Cette liste de présence permet aux moniteurs de vérifier la présence des différents stagiaires. Elle permet également aux stagiaires de valider leur présence en émargeant la feuille, à coté de leurs nom et prénom.

Une grosse partie des actions sont réalisées « manuellement », notamment :

- La copie des informations des stagiaires du fichier généré par le formulaire à la feuille de présence.
- La gestion du nombre d'inscrits aux activités sportives.
- La génération du formulaire, réalisé pour chaque date d’inscription.
- La notification des stagiaires en cas de problème d’inscription : trop d'inscrits, moniteur absent, annulation d'activités sportives... La notification est actuellement réalisée à travers un mail envoyé par l’administratrice.
- L'exportation de la feuille de présence au format PDF, ainsi que l’envoi aux moniteurs.

Nous avons également quelques données à prendre en compte : 

- Il y a actuellement 4 activités sportives avec un certain nombre de places par activités
  - Le tennis de table, 12 places
  - La salle de cardio et de muscu, 12 places
  - Le badminton, 16 places
  - L'accès à la piscine, 15 places

Les activités sportives se déroulent toutes les semaines, le mardi et le jeudi, de 16h à 17h. Il se pourrait que de nouveaux horaires se libèrent, sûrement de 17h à 18h (informations supplémentaires à demander).

- Le formulaire d’inscription des stagiaires enregistre les données suivantes :
  - Le nom du stagiaire
  - Le prénom du stagiaire
  - La section du stagiaire
  - L'activité sportive voulue pour la prochaine date

Le client a également 2 contraintes :

- Il ne peut y avoir une section complète inscrite aux activités sportives.
- Un même stagiaire ne peut s’inscrire plusieurs fois de suites aux même activités sportives.
  Un système de roulement s’est peu à peu mis en place entre les stagiaires, mais il faudrait imaginer un algorithme de système de roulement.

Le client a également formulé une demande concernant un autre projet d'automatisation de formulaire :  
Il est utilisé pour connaitre le nombre de stagiaires mangeant au self tous les midis au CRM.  
C’est un projet similaire à celui-ci, une attention particulière pourra être accordée à ce second projet pour peut-être étendre la future application.

# Informations complémentaires

Adresse du formulaire actuel : https://forms.office.com/pages/responsepage.aspx?id=pVEI9DKpJEiARBgjJDQA6UtjuvWfWt9Mohl3oEgDQThUNUZOOTA4MjBFNkExNkQ0RE42M0ZTRVJDTi4u

# Propositions pour le projet

Le but de ce projet est d’aider l'administrateur dans la gestion des inscriptions, en automatisant le processus. 

Cette automatisation peut être mise en place à plusieurs niveaux :

1. Générer automatiquement la feuille de présence à partir des données du formulaires.
2. Mettre à jour le formulaire en fonction de la date, du nombre d’inscrits ou d’événements souhaités par l'administrateur.
3. Récupérer les informations du stagiaire, comme son nom, son prénom et sa section.
4. Gérer la priorité entre les stagiaires, notamment entre ceux qui ne s’inscrivent que rarement et ceux qui s’inscrivent régulièrement.

Il faudra proposer 2 interfaces graphiques :
- Une interface pour les stagiaires, pour gérer leurs inscriptions aux activités.
- Une interface administrateur, pour gérer les inscriptions, notamment :
  - L’activation ou la désactivation de dates, d’activités sportives, ou la désinscription de stagiaires
  - L’affichage des stagiaires inscrits. Peut-être voir dans le temps les différentes inscriptions ? Peut-être voir toutes les dates pour un stagiaire ?
  - Peut-être l’ajout de nouvelles activités sportives (récemment, il y a eu l’ajout de l’activité piscine). Peut être également gérer les dates possibles pour les activités ?

On va devoir gérer l’authentification grâce au compte du CRM, liée à Microsoft et à Active Directory.

D’autres demandes ont étés formulées suite à la première rencontre :

- Il faudrait que certaines inscriptions puissent être désactivées par l’administrateur (moniteur absent, ou autre événement).
- Il faudrait pouvoir gérer l’annulation d’événements ayant déjà des inscriptions.
- Il faudrait pouvoir informer les stagiaires que les inscriptions sont complètes.
- Il faudrait pouvoir soit laisser à l'administrateur, soit définir dans l’application, l’ouverture des futures sessions d’inscriptions. Actuellement, les sessions sont ouvertes une fois que la réalisation de la feuille de présence de la journée précédente est finalisée.

**Idées pour le système de roulement des stagiaires :**

- A chaque inscription : vérifier si le stagiaire s’est inscrit au même sport la session d’avant et si oui => le mettre sur une file d’attente et ne l’inscrire au sport que s'il reste des places à la fermeture des inscriptions.

# Questionnement et autres demandes

- Comment gérer l’annulation ? (Actuellement l'administrateur envoie un email)
- Faut-il générer uniquement un fichier PDF pour les moniteurs, ou également leur réaliser une interface ?
Sachant que la feuille de présence est utilisée pour réaliser les signatures, il faudra certainement une version imprimable dans tous les cas.
- Demander le fonctionnement du processus du coté moniteur de sport et du coté payeur.

# Idées à trancher

- Gérer l’envoi de mails, notamment en cas d’annulation
