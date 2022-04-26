Dictionnaire de données - ZeForme
===================

| Entité | Mnémonique | Sens | Type | Taille | Remarques
|---|---|---|---|---|---|
| activités     | id | Identifiant de l'activité | N | 11 | Identifiant auto incrémenté
|               | nom | Nom de l'activité (tennis de table, badminton...) | AN | 64 | Obligatoire
|               | nombre_places | Nombre de place maximal pour l'activité | N | 6 | Obligatoire
|               | horaire_debut | Heure de début (cyclique) de l'activité | T | hh:mm:ss | Obligatoire
|               | horaire_fin | Heure de fin (cyclique) de l'activité | T | hh:mm:ss | Obligatoire
|               | duree_jours | Nombre de jour de durée de l'activité | N | 3 | Obligatoire, défaut à 1
|               | frequence | Fréquence de l'activité (unique, quotidien, hebdomadaire, mensuel...) | N | 32 | Obligatoire
|               | date_début_frequence | Date de début pour la fréquence de l'activité | N | YYYY-MM-DD | Obligatoire, défaut à 1
| evenements    | id | Identifiant de l'événement | N | 11 | Identifiant auto incrémenté 
|               | date_debut | Date de début de l'événement | D | YYYY-MM-DD | Obligatoire
|               | date_fin | Date de fin de l'événement | D | YYYY-MM-DD | Obligatoire
|               | horaire_debut | Heure de début de l'événement | T | hh:mm:ss | Obligatoire
|               | horaire_fin | Heure de fin de l'événement | T | hh:mm:ss | Obligatoire
|               | nombre_places | Nombre de place maximal pour l'événement | N | 6 | Obligatoire
|               | status | Status de l'événement : Activé, désactivé...  | AN | 32 | Obligatoire
|               | status_inscription | Est ce que les inscriptions sont ouvertes  | Boolean | 32 | Obligatoire
| lieux         | nom | Nom du lieu | A | 32 | Identifiant
| utilisateurs  | id | Identifiant de l'utilisateur | A | 11 | Identifiant auto incrémenté
|               | nom | Nom de l'utilisateur | A | 64 | Obligatoire
|               | prénom | Prénom de l'utilisateur | A | 64 | Obligatoire
|               | département | Nom de là où est l'utilisateur (section, role dans l'entreprise...) | AN | 32 | Obligatoire
| roles         | nom | Nom du role (administrateur, moniteur, utilisateur, etc) | A | 16 | Identifiant
