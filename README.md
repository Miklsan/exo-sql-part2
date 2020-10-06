#Exercices database partie 2
Le rendu de ces exercices se fera dans un repository accessible depuis github qui contiendra un unique fichier README.md. Ce fichier contiendra toutes les commandes et les outputs(si demandés dans l'énoncé) de ces commandes classées par exercices, comme demandé dans les énoncés.

##LE FICHIER README.md devra être lisible, un chapitre par exercice, les commandes SQL devront être mises en valeur dans un bloc de code, ainsi que les outputs.

**Ne mettez les outputs des commandes que si ils sont demandés dans l'énoncé**

**1**
[Télécharger la base de donnée](https://sp.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip)
Dézipper le fichier dvdrental.zip et installer la base de donnée dvdrental.tar avec les commandes suivantes:

```sql
% psql -d postgres -U db_user
```

```sql
postgres=> CREATE DATABASE dvdrental;
postgres=> \quit
```
```sql
% pg_restore -U db_user -d dvdrental ./dvdrental.tar
% psql -d dvbrental -U db_user
```
Vous êtes maintenant connectés à la base de donnée dvdrental

Vous pouvez récupérer un modele visuel de cette base de donnée sur: (https://www.postgresqltutorial.com/postgresql-sample-database/)
C'est très utile si vous voulez comprendre que représente cette base de données.

la commande \dt+ NOM_DE_LA_TABLE vous donne la liste des tables.
la commande \dt+ NOM_DE_LA_TABLE vous donne le nom des colonnes de d'une table. la commande \d NOM_DE_LA_TABLE vous affiche le nom des colonnes ainsi que les types associés à chaque colonnes.

**2**
Ecrivez une requête SQL qui affiche tous les titres et descriptions des films dont la description contient le mot Amazing.