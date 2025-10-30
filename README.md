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

  **sudo apt install openssh-server -y** pour installer le paquet
   ![Installation OpenSSH](Captures/installation_OpenSSH.png)
  </p>
 
  <p>
  
  Puis **systemctl status ssh** pour vérifier que le service était bien actif. 
  Après vérification on a constaté que le service n’était pas activé, il a donc fallu démarrer et activer SSH à l’aide des commandes
suivantes :
**sudo systemctl start ssh**
**sudo systemctl enable ssh**
![Activation service](Captures/vrf_service.png)
</p>

<p>

L’adresse IP de la machine virtuelle a ensuite été identifiée avec **ip a**.  
Au départ, la configuration réseau était en mode NAT (exemple : 10.0.2.x), ce qui ne permettait pas une connexion directe depuis Windows.  
Pour résoudre ce problème, l’adaptateur réseau a été configuré en mode « Pont », ce qui a permis à Ubuntu et Windows d’être sur le même réseau local avec une adresse du type 192.168.x.x.  
![Adresse IP](Captures/IP-a.png)
</p>

