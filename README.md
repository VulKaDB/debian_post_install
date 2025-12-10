# debian_post_install

# Script de Post-Installation Debian 13

Ce script Bash automatise la configuration initiale d'un serveur Debian 13 fraîchement installé. 

## Prérequis

* Une machine sous **Debian 13**.
* Être connecté en tant que **root** (ou avoir les droits sudo).
* Une connexion Internet active.
* Rendre le script executable avec chmod +x debian_post_install.sh

## Fonctionnalités

Le script effectue les actions suivantes de manière séquentielle :

1.  **Mise à jour du système** : `apt update` & `upgrade`.
2.  **Installation des outils indispensables** : 
    * Système : `sudo`, `ssh`, `git`, `screen`, `curl`.
    * Réseau/Diag : `nmap`, `net-tools`, `dnsutils`.
    * Utilitaire : `zip`, `unzip`, `ncdu`, `locate`.
3.  **Support Netbios/Samba** : Installation et configuration automatique du fichier `/etc/nsswitch.conf` (ajout de WINS).
4.  **Confort du terminal** : Activation des couleurs et alias dans le `.bashrc`.
5.  **Installation de Webmin** : Interface de gestion web du serveur (via le dépôt officiel).
6.  **Bonus** : Installation des jeux BSD (`bsdgames`).
