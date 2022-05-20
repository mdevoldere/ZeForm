ZeForm - Régles de gestion
============

- Activités & événements :
    - Une activité génère 0 ou plusieurs événements.
    - Un événement est généré suite à 0 ou 1 activité.
- Utilisateurs & événements :
    - Un utilisateur s'inscrit à 0 ou plusieurs événements.
    - Un événement est inscrit par 0 ou plusieurs utilisateurs.
    - Un événement est géré par 1 et 1 seul utilisateur(role administrateur).
    - Un utilisateur gère 0 ou plusieurs événements.
- Lieux et événements :
    - Un événement est localisé à 1 et 1 seul lieu.
    - Un lieu localise 0 ou plusieurs événements.
- Lieux et activités :
    - Une activité est généralement réalisée à 1 et 1 seul lieu.
    - Un lieu réalise généralement 0 ou plusieurs activités.
- Utilisateurs & rôles :
    - Un utilisateur est caractérisé par 1 et 1 seul rôle.
    - Un rôle caractérise 1 ou plusieurs utilisateurs.

- **personne et événements**
    - une personne s'inscrit à 0 ou plusieurs événements.
    - un événement est inscrit par 0 ou plusieurs personnes.
    - (une personne monitore 0 ou plusieurs événements.)
    - (un événement est monitorer par 1 (0 ?) ou plusieurs personnes.)

- **personne et role**
    - une personne est regroupé dans 1 (ou plusieurs ?) role(s).
    - un role regroupe 0 ou plusieurs personnes.
    - (un role est descendant d'un ou de 0 roles)
    - (un role descent de 0 ou 1 role)

- **activité et événement**
    - un événements est spécialisé par une activité.
    - une activité spécialise 0 ou plusieurs événements.

- **événements et état**
    - un événement est caractérisé par un état.
    - un état caractérise 0 ou plusieurs événements.

- **activité et état**
    - une activité est défini par un état.
    - un état défini 0 ou plusieurs activités.

- **lieu et activité**
    - une activité est localisé dans un lieu.
    - un lieu localise 0 ou plusieurs activités.

- **lieu et événement**
    - un événement se situe dans 1 lieu.
    - un lieu localise 0 ou plusieurs événements.
