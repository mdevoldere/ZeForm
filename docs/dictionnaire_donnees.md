ZeForm - Dictionnaire de données
===================

| Entité | Mnémonique | Sens | Type | Taille | Remarques
|---|---|---|---|---|---|
| activites     | id | Identifiant de l'activité | N | 11 | Identifiant auto incrémenté
|               | nom | Nom de l'activité (tennis de table, badminton...) | AN | 64 | Obligatoire
|               |description | description de l'activité | AN | 255 | Obligatoire
|               | nombre_places | Nombre de place maximal pour l'activité | N | 6 | Obligatoire
|               | horaire_debut | Heure de début (cyclique) de l'activité | T | hh:mm:ss | Obligatoire
|               | horaire_fin | Heure de fin (cyclique) de l'activité | T | hh:mm:ss | Obligatoire
|               | duree_jours | Nombre de jour de durée de l'activité | N | 3 | Obligatoire, défaut à 1
|               | frequence | Fréquence de l'activité (unique, quotidien, hebdomadaire, mensuel...) | N | 32 | Obligatoire
|               | date_debut_frequence | Date de début pour la fréquence de l'activité | N | YYYY-MM-DD | Obligatoire, défaut à 1
| evenements    | id | Identifiant de l'événement | N | 11 | Identifiant auto incrémenté 
|               | date_debut | Date de début de l'événement | D | YYYY-MM-DD | Obligatoire
|               | date_fin | Date de fin de l'événement | D | YYYY-MM-DD | Obligatoire
|               | horaire_début | Heure de début de l'événement | T | hh:mm:ss | Obligatoire
|               | horaire_fin | Heure de fin de l'événement | T | hh:mm:ss | Obligatoire
|               | nombre_places | Nombre de place maximal pour l'événement | N | 6 | Obligatoire
|               | status | Status de l'événement : Activé, désactivé...  | AN | 32 | Obligatoire
|               | status_inscription | Est ce que les inscriptions sont ouvertes  | Boolean | 1 | Obligatoire
| lieux         | nom | Nom du lieu | A | 32 | Identifiant
| utilisateurs  | id | Identifiant de l'utilisateur | A | 11 | Identifiant auto incrémenté
|               | nom | Nom de l'utilisateur | A | 64 | Obligatoire
|               | prenom | Prénom de l'utilisateur | A | 64 | Obligatoire
|               | departement | Nom de là où est l'utilisateur (section, role dans l'entreprise...) | AN | 32 | Obligatoire
| roles         | nom | Nom du role (administrateur, moniteur, utilisateur, etc) | A | 16 | Identifiant

| Entité | Mnémonique | Sens | Type | Taille | Remarques
|---|---|---|---|---|---
| personne  | personne_id       | Identifiant du stagiaire  | N | |
| personne  | personne_nom      | Nom du stagiaire          | A | |
| personne  | personne_prenom   | Prénom du stagiaire       | A | |
| personne  | personne_section  | Section du stagiaire (cda 2111, abc dev, etc...) | AN | |
| personne  | personne_etat     | Status d'une personne : présent, absent, etc | A ||
| activite  | activite_id                       | Identifiant d'une activité    | N | |
| activite  | activite_recurrence_time_debut    | Heure de début de l'activité  | T | |
| activite  | activite_recurrence_time_fin      | Heure de fin de l'activité    | T | |
| activite  | activite_recurrence_date          | Date de début de l'activité (jour de la semaine, numéro du jour du mois, etc) | AN | |
| activite  | activite_recurrence_type          | Type de récurrence (tous les jours, toutes les semaines, tous les mois...) | A | |
| activite  | activité_date_fin                 | Date de fin de l'activité | D | | Optionnelle
| activite  | activite_nombre_max_place         | Nombre maximal de place autorisé | N | |
| activite  | activite_nombre_min_place         | Nombre minimal de place autorisé | N | |
| activite  | activite_jours_avant_ouverture    | Nombre de jours avant l'ouverture des inscriptions | N | |
| evenement | evenement_id                      | Identifiant de l'événement | N | |
| evenement | evenement_nom                     | Nom de l'événement | AN | |
| evenement | evenement_etat_inscription        | Etat de l'inscription de l'événement : ouvert, fermé | A | |
| evenement | evenement_jours_avant_ouverture   | Nombre de jours avant l'ouverture des inscriptions | N | |
| evenement | evenement_place_max               | Nombre maximal de places | N | |
| evenement | evenement_place_min               | Nombre minimal de places | N | |
| evenement | evenement_datetime_debut          | Date et heure de l'événement | DT | |
| evenement | evenement_datetime_fin            | Date et heure de l'événement | DT | |
| evenement | evenement_presence_genere         | Est ce que la feuille de présence a été généré ? | B | |
| etat      | etat_id     | Identifiant d'un état                                         |
| etat      | etat_nom    | Nom de l'état (inscription ouverte ou fermé, annulé, etc.)    | A | |
| lieu      | lieu_id   | Identifiant du lieu           | N | |
| lieu      | lieu_nom  | Nom du lieu                   | A(N) | |
| role      | role_id   | Identifiant du role           | N | |
| role      | role_nom  | Nom du role : administrateur, moniteur, stagiaire, etc. | N | |
|           | personne_evenement_inscription
|           | personne_evenement_inscription_status


Entité section ?
Comment gérer plusieurs types de récurrences (tous les jours, toutes les semaines, tous les mois, toutes les 2 semaines, tous les ans...)
