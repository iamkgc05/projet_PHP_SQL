
# **Description du projet**

Je suis un fan d'un jeu mobile qui se nomme *Dokkan Battle*, j'ai donc décidé de réaliser un système de comparaison des personnages de ce jeux mais avec des personnages d'autres animés voire de la vrai vie.

# **Avancement du projet**

## *27/10/2023 : Jour 1*

Lors de la création de mon projet j'ai eu beaucoup de premières idée; j'ai commencé avec un jeu comparant la puissance des personnages d'animé en générale. Puis je me suis retrouvé à obtenir des comparaisons absurde.  
Je vais m'inspirer du site Dokkan Essentiels, et je vais récupérer des données  d'autres jeux que dokkan battle. Comme One piece Treasure Cruise ect... 

Pour éviter que les utilisateurs mettent des personnages fumée juste parce que ils les aiment je vais créer un rôle administrateur qui va pouvoir régir et éditer la plupart des catégorie du site.

### **Utilisateur**
- [?] Un utilisateur est déterminé par quoi:
	- Un id
	- Un rôle -> Si il est admin il peut créer, modifier des cartes, ajouter des catégories, ajouter des catégorie à des personnnages + les avantages utilisateurs -> Si il est utilisateur il peut regarder les cartes, comparer deux cartes.
	- Son nom
	- Son mot de passe
	- Son adresse mail
	

### **Un personnage**
- [?] Un personnage est déterminé par quoi :
	-Un id (unique)
	- Son nom (il peut y avoir plusieurs formes d'un personnage)
	- Si il est réel ou fictif( Mon idée de Macron vs Batman)
	- Des stats (inspiré de jeux pour les fictifs, ou bien WTF pour les réels)
	-  + des liens de catégorie selon les personnages sous la forme d'une liste.
	- Le nombre de combat qu'il a gagné

### **Un table Combat**
- [?] Un Combat est défini par:
	- Un id perso A + un equipement
	- un id perso B + un equipement
	- l'id du gagnant

### **Equipement**
- [?] Un equipement est défini par : 
	-Un id
	-Une stat (Augmentation de stats)

### **Combattant**
- [?] Un Combattant correspond à l'association personnage + équipement.


## *06/11/2023 Jour 2*

J'ai eu l'idée de rajouter des terrains des lieux.
Je cherche un moyen d'inserer des images qui définissent les lieux en 2D style art comme dans les jeux pokemon.

j'imagine ajouter des effets spécifique aux perso mais ça me paraît un peu plus compliquer.
j'envisage

je reflechis un moyen afin que même les petits perso puissent battre les perso plus forts. Une sorte de stats de chance qui affecte ses stats ou debuff l'adversaire sur un lancés de dé par exemple.
Dans ce dé qui ne seras pas équilibré. Il y'aurais des bonus des malus allant de -1,5% des stats à  + 20% des stats par exemples.

Il va de soit que je dois également penser à creer une fiche d'édit, que ce soit supprimer ou ajouter un personnage.

une page de combat 
avec des messages genre 
- ["] "Le combat commence..."
- ["] "le personnage 1 calcule ses stats"
- ["] "le personnage 2 calcule ses stats"
- ["] "Le combat est terminer"
- ["] "Le Vainqueur est ..."

### *Commande du Jour*

```sql
CREATE TABLE Users ( id_user INT(11) NOT NULL AUTO_INCREMENT, nom VARCHAR(255), pseudonyme VARCHAR(100),mots_de_passe VARCHAR(255), adresse_mail VARCHAR(100), PRIMARY KEY(id_user));

CREATE TABLE Type (id_type INT(11) NOT NULL AUTO_INCREMENT PRIMARY KEY, nom VARCHAR(255));

CREATE TABLE Equipement( id_equipement INT(11) NOT NULL AUTO_INCREMENT PRIMARY KEY, nom_equipement VARCHAR(30), bonus INT (11), id_type_equipement INT(11), FOREIGN KEY(type_equipement) REFERENCES type(id_type) ON DELETE RESTRICT ON UPDATE CASCADE);

CREATE TABLE Terrain( id_terrain INT(11) NOT NULL AUTO_INCREMENT PRIMARY KEY, nom_terrain VARCHAR(30), bonus INT (11), couleur VARCHAR(255),id_type_terrain INT(11), FOREIGN KEY(id_type_terrain) REFERENCES type(id_type) ON DELETE RESTRICT ON UPDATE CASCADE);

CREATE TABLE Personnage( id_personnage INT(11) NOT NULL AUTO_INCREMENT PRIMARY KEY, nom_personnage VARCHAR(255), stats INT (11), id_type_personnage INT (11), FOREIGN KEY(id_type_personnage) REFERENCES type(id_type) ON DELETE RESTRICT ON UPDATE CASCADE);

CREATE TABLE combattant ( id_combattant INT(11) NOT NULL AUTO_INCREMENT, id_personnage_combattant INT(11), id_equipement_combattant INT(11), id_terrain_combattant INT(11), stats_calcule INT(11), FOREIGN KEY(id_personnage_combattant) REFERENCES personnage(id_personnage) ON DELETE RESTRICT ON UPDATE CASCADE, FOREIGN KEY(id_equipement_combattant) REFERENCES equipement(id_equipement) ON DELETE RESTRICT ON UPDATE CASCADE, FOREIGN KEY(id_terrain_combattant) REFERENCES terrain(id_terrain) ON DELETE RESTRICT ON UPDATE CASCADE);

CREATE TABLE Combat (id_combat INT(11) NOT NULL AUTO_INCREMENT PRIMARY KEY, id_combattant_combat_1 INT(11), id_combattant_combat_2 INT(11), id_user_combattant INT(11), FOREIGN KEY(id_combattant_combat_1) REFERENCES combattant(id_combattant) ON DELETE RESTRICT ON UPDATE CASCADE, FOREIGN KEY(id_combattant_combat_2) REFERENCES combattant(id_combattant) ON DELETE RESTRICT ON UPDATE CASCADE, FOREIGN KEY(id_user_combattant) REFERENCES users(id_user) ON DELETE RESTRICT ON UPDATE CASCADE);
```




```
## Basic
- [ ] to-do
- [/] incomplete
- [x] done
- [-] canceled
- [>] forwarded
- [<] scheduling

## Extras
- [?] question
- [!] important
- [*] star
- ["] quote
- [l] location
- [b] bookmark
- [i] information
- [S] savings
- [I] idea
- [p] pros
- [c] cons
- [f] fire
- [k] key
- [w] win
- [u] up
- [d] down
- [D] draft pull request
- [P] open pull request
- [M] merged pull request
```