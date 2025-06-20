Partie 1 : Gestion des utilisateurs

Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_11_09_04](https://github.com/user-attachments/assets/41507465-1df2-4e48-9d4f-47f614ac8628)

Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?

Avoir un mot de passe fort est les bons permitions dans le bon groupe.

Partie 2 : Configuration de SSH

Un serveur SSH est lancé sur le port par défaut.
Il est possible de s'y connecter avec n'importe quel compte, y compris le compte root.

Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.

"nano /etc/ssh/sshd_config"
"PermitRootLogin no"

Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.

Il faut ajouter dans le fichier conf "AllowUsers ...."

Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe

Dans le fichier conf nous allons autoriser les clé valide est desactivée l'authentification par mot de passe.

Partie 3 : Analyse du stockage

Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?

![VirtualBox_Checkpoint3-SRVLX01_20_06_2025_11_29_48](https://github.com/user-attachments/assets/92dbed37-d995-4391-8ecd-f260627c4b2e)

Q.2.3.2 Quel type de système de stockage ils utilisent ?

RAID

Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?
Partie 4 : Sauvegardes

Le logiciel bareos est installé sur le serveur.
Les composants bareos-dir, bareos-sd et bareos-fd sont installés avec une configuration par défaut.

Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.

bareos-dir : Sauvegarde,restauration et vérification il gére tous les composants est lit les fichier.
bareos-sd :  Gestionnaire de stockage recoit les données 
bareos-fd : Envoin les fichier selon bareos-dir

Partie 5 : Filtrage et analyse réseau

Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?

Q.2.5.2 Quels types de communications sont autorisées ?
SSH, ping 

Q.2.5.3 Quels types sont interdit ?

les port qui sont pas acceptée connexion non autorisée

Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.

Rappel : Bareos utilise les ports TCP 9101 à 9103 pour la communication entre ses différents composants.

Partie 6 : Analyse de logs

Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :

    La date et l'heure de la tentative
    L'adresse IP de la machine ayant fait la tentative

