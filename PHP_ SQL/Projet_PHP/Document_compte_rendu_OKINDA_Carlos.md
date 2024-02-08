
# **Présentation du projet**

Mon projet s'intitule sobrement : **Global Fighting Cup**, il fonctionne le manière suivante.

Dans un premier temps vous créer un compte à l'aide de vos informations personnelles .

Quand vous vous connecter pour la première fois, il y'a un tableau avec les personnage valide par les admins et classé par ordre décroissant par rapport à leurs stats. juste en bas il y'a un autre tableau avec les 10 derniers combats réalisée avec les gagnants et ceux les ont réalisés.

En haut de cette page il y'a la barre de navigation, dans celle-ci il y'a le logo du projet (qui renvoie vers la page d'acceuil) et toutes les autres fonctionnalités de mon site de la création de type, d'équipements,  de type ect...

Lorsque l'on crée un élément il n'est pas encore disponible, il doit être validé et ou modifié par les admins. (Et je vous assure qu'ils seront réactifs parce que je les payent bien).

Une fois vos personnages validés ils ont des fiches dans lesquelles il y'a leurs stats, leurs types etc..., et vous pouvez donc les faire combattre.

Pourquoi ce concept vous me direz? Parce que j'aime bien la bagarre et je veux savoir qui gagne une baston entre Batman et Eric Zemmour.


# **L' Installation**

Si vous lisez ce document c'est que vous avez déjà télécharger les fichiers importants de mon site c'est-à-dire la structure du site et la Base de données sinon faites le (svp).

Ensuite aller dans votre fichier "www" de votre Laragon et mettez le dossier du site à l'interieur.

Puis lancez votre "PhpmyAdmin" et importez le .sql dans une nouvelle base de données, nommez là "gfc_test1".

Une fois ça fait tout est bon. Lancez votre Laragon et tapez le nom du fichier qui est dans votre repertoire "www", "site_ceo" si vous n'avez pas changer et rajoutez un .test à la fin.

La vous pouvez soit vous creer un  compte utilisateur, et lui donner les droits administrateur via la BDD ou utiliser les comptes suivants :

Utilisateur Lambda: 
**d2**
Mdp:
**d2**

Utilisateur Admin:
**admin**
Mdp:
**admin**


Utilisateur Banni: 
**dd**
Mdp:
**dd**


# **Avancement du projet**

Pour mon projet, j'ai commencé par créer mon MCD et mon MLD, puis j'y ai ajouter des certaine données test . Puis je me suis mis à la programmation en php du site. En commençant par l'ajout d'utilisateur (inscriptions +connexion et cryptage de mots de passe), puis par celle de personnage et d'équipement. A partir de ce moment j'avais réalisé une grande partie du site. J'ai donc ensuite créer l'interface de combat, et j'ai programmé les retours par rapport au stats des combattants (Qui gagne et quels stats ect...). Puis j'ai ajouter tous les codes liés à la création, la modification et l'affiche des types, des personnages et des équipements.

J'ai ensuite mis en place l'interface des admins qui ont accès à plus de fonctionnalités que les utilisateurs, notamment la validation des créations des utilisateurs ainsi que le bannissement des utilisateurs ou leurs promotions en administrateurs. J'ai ensuite ajouter des vérifications de connections et de ban.

Pour finir j'ai ajouté un menu de navigation et un peu de Bootstrap pour rendre un peu plus stylé mon site mais très légèrement.

# **Bilan**

Pour finir, je suis assez content de ce que j'ai produis même si j'ai souvent rencontrer plusieurs problèmes dont les plus importants étaient :

- Lors des combats j'ai voulu créer une vérification permettant de savoir si l'utilisateur a déjà fait un combat (que vous pouvez retrouver dans mon code) 

- Le problème le plus récurant était l'erreur suivante :
	
```php
Warning: Cannot modify header information - headers already sent by (output started at C:\laragon\www\Site_ceo\menu.php:10) in C:\laragon\www\Site_ceo\function.php on line 6
```

Elle était liés à la présence de fonction dans mon code et j'ai réussis à "régler" ce problème grâce aux fonction :

```php
ob_start();
et 
ob_flush_end();
```

Comme bilan, mon site est loin d'être parfait et il y'a une ribambelles de fonctionnalités que j'aurais voulus implémenter et ajouter comme l'usage de de terrain et une mise à jour du fond lors des combats et plein d'autres. Mais pour l'instant je suis satisfait de ce que j'ai produit.


# **RGPD**

- Il s'agit du Règlement Générale sur la protection des données, elle est créer par l'union Européenne et mis en vigueur en mai 2018 et son but est de renforcer la protection des données personnelles de chaque individus. Son objectif principale est d'assurer un niveau élevé de protection des données personnelles de chaque individus et de réguler leur traitement par les organisations.

- Comme données personnelles on a par exemple les mots de passe, le nom , les coordonnées bancaires. Il est portant de protéger ce genre de données sensibles afin de respecter leurs vie privée, éviter les abus et garantir la confiance.

- Le consentement dans le RGPD signifie une autorisation claire et explicite donnée par l'individu sur le traitement de ses données personnelles.

   Il est nécessaire pour s'assurer  que l'individu a pris connaissances du fait que l'on accès à ses données et ainsi lui montrer qu'il a le contrôle sur la manière dont nous les traitons.

- Ils ont le droit d'accéder à leurs données personnelles détenus par une organisation.
   Il est essentiel de respecter ces droits  afin de se conformer à la législation et établir une relation de confiance avec ses clients en évitants des sanctions.

- La responsabilités des entreprises en matière de protections de données incluent la mise en place de mesure de sécurité, la transparence dans les traitements des données  et la notification en cas de violation de données. 
- L'AIPD est une évaluation des risques et des impacts potentiels sur la vie privée effectuée par une entreprise avant la mise en œuvre de certains traitements de données. Elle est importante pour anticiper et atténuer les risques liés au traitement des données.



