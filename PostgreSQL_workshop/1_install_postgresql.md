# 1.Installer postgreSQL pour Ubuntu
Vérifier la version :
```sbtshell
cat /etc/os-release
```
Dans notre cas, cette commande retourne :
```sbtshell
NAME="Ubuntu"
VERSION="20.04.4 LTS (Focal Fossa)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 20.04.4 LTS"
VERSION_ID="20.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=focal
UBUNTU_CODENAME=focal
```
Mettre à jour apt-get:
```sbtshell
sudo apt-get update 
```
Installer postgresql et postgresql-contrib (un package qui ajoute quelques utilités et fonctionnalités supplémentaires):
```sbtshell
sudo apt-get install postgresql postgresql-contrib
```
Vérifier la version de postgresql installée :
```sbtshell
ls /etc/postgresql/
```
Un dossier portant le numéro de version apparaît, dans notre cas c'est ```12```.
vérifier l'existence du fichier de configuration ```postgresql.conf```:
```sbtshell
ls /etc/postgresql/12/main/ 
```
Pour voir les commandes que nous pouvons utiliser avec le service postgresql:
```sbtshell
service postgresql
```
Vérifier l'état du service:
```sbtshell
service postgresql status
```
Par défaut, cette commande retourne ```online, port 5432```
```postgres``` est le username par défaut
```sbtshell
sudo su postgres 
```
Pour pouvoir commencer les commandes de bases de postgresql:
```sbtshell
psql
```
