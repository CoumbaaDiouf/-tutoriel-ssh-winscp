# Projet 5 - Tutoriel SSH + WinSCP
## Introduction
<p>
L’objectif de ce projet est de mettre en place une communication sécurisée entre une machine virtuelle Ubuntu et un poste Windows en utilisant le protocole SSH et l’outil WinSCP.
Cette configuration permet de se connecter à distance à la machine Ubuntu et de transférer des fichiers entre les deux systèmes sans support physique (clé USB, disque dur externe). Le projet vise également à se familiariser avec l’utilisation d’un serveur SSH, la configuration réseau de VirtualBox ainsi que la gestion des transferts de fichiers via une interface graphique.
</p>

## 1. Installation d'OpenSSH Server sur Ubuntu
<p>La première étape a consisté à installer et activer le serveur OpenSSH sur Ubuntu.  
Les commandes utilisées ont été : </p>
  <p>
  
  **sudo apt install openssh-server -y** pour installer le serveur OpenSSH</p>
 , puis `systemctl status ssh` pour vérifier que le service était bien actif. 


![Installation OpenSSH](Captures/installation_OpenSSH.png)