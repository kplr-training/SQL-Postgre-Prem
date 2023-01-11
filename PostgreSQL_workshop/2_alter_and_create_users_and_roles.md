# 2.Créer un utilisateur de base de données
Dans votre machine Ubuntu, ouvrir le terminal :
![open_ubuntu_terminal](https://user-images.githubusercontent.com/73080397/211827531-6ab9276e-5f33-4e7c-b6d7-dc92621f53b5.png)

Entrer la commande suivante:

```sbtshell
sudo su postgres
```
Entrer le mot de passe su.

Accéder à la ligne des commande de postgresql par :
```sbtshell
psql
```
![image](https://user-images.githubusercontent.com/73080397/211828753-f4fc28b1-433f-4d4a-ba75-26a2b6e01c82.png)

Vous êtes maintenant en ligne de commandes, pour voir les bases de données existantes par défaut:
```sbtshell
\l
```
Pour quitter ce résultat et revenir à la ligne de commande, cliquer sur ```q```

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
Pour quitter la ligne de commande et revenir à votre utilisateur de base de données : ```CTRL``` + ```D```

Pour revenir à Ubuntu user : ```CTRL``` + ```D```
