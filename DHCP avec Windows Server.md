
# _**DHCP avec Windows Server**_


  ## Deux machines seront utilisées pour la mise en œuvre cette quête serveur DHCP sous Windows Server :


Spécifications technique 

Réseau : 172.20.0.0/24


SRVWIN01-DHCP sous Windows Server 2025

    
  Il s'agit du serveur sur lequel nous allons monter le rôle DHCP
  Adresse IP : 172.20.0.1

CLIWIN01 sous Windows 10

  il s'agit d'un poste de travail client sous Windows 10 pro que nous utiliserons pour tester notre serveur DHCP

1) Paramétrage de l'adresse IP fixe du serveur

![Image](/Images/0-Configuration%20adresse%20IP%20fixe%20pour%20le%20serveur%20DHCP.png)

2) Paramétrage du nom du serveur


![Image](/Images/1-Changement%20nom%20du%20serveur.png)


3) Installation du role serveur DHCP

   ![Image](/Images/2-Gérer-Ajouter%20des%20roles%20et%20fonctionnalités.png)
   ![Image](/Images/3-Installation%20basé%20sur%20un%20role%20ou%20une%20fonctionnalité.png)


4) Selection du serveur de destination

   ![Image](/Images/4-Selection%20du%20serveur%20de%20destination.png)

5) Ajout des fonctionnalités requises pour le serveur WINSERV01-DHCP

  ![Image](/Images/5-Ajout_des_fonctionnalités_pour_requises_pour_serveur_WINSERV01-DHCP.png)

6) Confirmation des selections d'installations

![Image](/Images/6-Confirmation%20des%20selections%20d'installations.png)

7) 



