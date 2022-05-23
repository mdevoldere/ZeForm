ZeForm - Dictionnaire de données
===================

# Tableau

| Entité | Mnémonique | Sens | Type | Taille | Remarques
|---|---|---|---|---|---
| personne  | personne_id           | Identifiant de la personne  | N | 11 | Identifiant auto incrémenté
| personne  | personne_nom          | Nom de la personne          | A | 64 | Obligatoire
| personne  | personne_prenom       | Prénom de la personne       | A | 64 | Obligatoire
| personne  | personne_departement  | Nom du role dans l'entreprise de la personne (nom de section, nom dans l'entreprise...) | AN | 32 | Obligatoire
| activite  | activite_id                       | Identifiant d'une activité    | N | 11 | Identifiant auto incrémenté
| activite  | activite_nom                      | Nom de l'activité (tennis de table, badminton...)    | N | 64 | Obligatoire
| activite  | activite_frequence_heure_debut    | Heure "classique" du début de l'activité, de manière réccurente, qui servira à la génération automatique | T | hh:mm:ss | Obligatoire
| activite  | activite_frequence_heure_fin      | Heure "classique" de la fin de l'activité, de manière réccurente, qui servira à la génération automatique  | T | hh:mm:ss | Obligatoire
| activite  | activite_frequence_date       | Date de début de l'activité (jour de la semaine, numéro du jour du mois, etc) | AN | 64 | Obligatoire
| activite  | activite_frequence_type       | Fréquence de l'activité (unique, quotidien, hebdomadaire, mensuel...) | A | 32 | Obligatoire
| activite  | activité_date_début           | Date de début de l'activité | D | YYYY-MM-DD | Obligatoire
| activite  | activité_date_fin             | Date de fin de l'activité | D | YYYY-MM-DD | Optionnelle
| activite  | activite_place_max            | Nombre maximal de place autorisée | N | 6 | Obligatoire
| activite  | activite_place_min            | Nombre minimal de place autorisée | N | 6 | Obligatoire, défaut à 0
| activite  | activite_jours_inscriptions   | Nombre de jours avant l'ouverture des inscriptions pour les événements | N | 6 | Obligatoire, defaut à 0 (correspond à aucune attente)
| evenement | evenement_id                  | Identifiant de l'événement | N | 11 | Identifiant auto incrémenté
| evenement | evenement_nom                 | Nom de l'événement | AN | 64 | Obligatoire
| evenement | evenement_jours_inscriptions  | Nombre de jours avant l'ouverture des inscriptions | N | 6 | Obligatoire, defaut à 0 (correspond à aucune attente)
| evenement | evenement_place_max           | Nombre maximal de places | N | 6 | Obligatoire
| evenement | evenement_place_min           | Nombre minimal de places | N | 6 | Obligatoire, défaut à 0
| evenement | evenement_horaire_debut       | Date et heure de début de l'événement | DT | YYYY-MM-DD hh:mm:ss | Obligatoire, défaut à la date d'aujourd'hui
| evenement | evenement_horaire_fin         | Date et heure de fin de l'événement | DT | YYYY-MM-DD hh:mm:ss | Obligatoire
| etat      | etat_id     | Identifiant d'un état                                         | N | 11 | Identifiant auto incrémenté
| etat      | etat_nom    | Nom de l'état (inscription ouverte ou fermé, annulé, etc.)    | A | 32 | Obligatoire, unique
| lieu      | lieu_id     | Identifiant du lieu           | N | 11 | Identifiant auto incrémenté
| lieu      | lieu_nom    | Nom du lieu                   | A(N) | 32 | Obligatoire, unique
| role      | role_id     | Identifiant du role           | N | 11 | Identifiant auto incrémenté
| role      | role_nom    | Nom du role (administrateur, moniteur, stagiaire, etc.) | A | 16 | Obligatoire, unique


# Reflexions
- Devons nous créer une entité "section" ?
- Comment devons nous gérer les types de récurrences (tous les jours, toutes les semaines, tous les mois, toutes les 2 semaines, tous les ans...) .
