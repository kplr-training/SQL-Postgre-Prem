# 2.0. Installer pgAdmin
Si vous disposer de Ubuntu Software Center, y aller, chercher 'pgadmin', installer directement. Sinon:
Dans un nouveau terminal: 
Installer la clé publique  du repository:
```sbtshell
curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
```
Créer le fichier de configuration du repository :
```sbtshell
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
```
Installer pgAdmin pour les modes Desktop et Web:
```sbtshell
sudo apt install pgadmin4
```
