# 2.Créer un utilsateur de base de données
```sbtshell
sudo su postgres
psql
```
Voir les bases de données présentes par défaut:
```sbtshell
\l
```
Lister tous les utilisateurs: par défaut, postgres est le seul utilisateur, c'est un superuser, il peut créer les rôles, créer les bases de données et effectuer les réplications
```sbtshell
\du
```
Changer le mot de passe de l'utilisateur par défaut:
```sbtshell
ALTER USER postgres WITH PASSWORD 'test123';
```
La commande retourne ```ALTER ROLE```.
Créer un nouvel utilisateur user_1 (ou votre prénom):
```sbtshell
CREATE USER user_prenom WITH PASSWORD 'votremdp';
```
La commande retourne ```CREATE ROLE```.
Lister les utilisateurs:
```
\du
```
Fournir certains privilèges à l'utilisateur user_prenom:
```sbtshell
ALTER USER user_prenom WITH SUPERUSER;
```
Créer un autre utilisateur:
```sbtshell
CREATE user_2 WITH PASSWORD 'user2mdp';
```
Le supprimer:
```sbtshell
DROP USER user_2;
```
