
# _**DHCP avec Windows Server**_


  ## Deux machines seront utilisées pour la mise en œuvre cette quête serveur DHCP sous Windows Server :


Spécifications technique 

Réseau : 172.20.0.0/24


SRVWIN01-DHCP sous Windows Server 2022

    
  Il s'agit du serveur sur lequel nous allons monter le rôle DHCP avec l'adresse IP : 172.20.0.1

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

7) 7-Configuration post déploiement

   Selectionner : Terminer la configuration DHCP
   
   ![Image](/Images/7-Configuration%20post%20déploiement.png)

   

   
8) Asssistant configuration Post Installation DHCP

   ![Image](/Images/8-Asssistant_configuration_Post_Installation_DHCP.png)
   
9) Fin Asssistant configuration Post Installation DHCP

  ![Image](/Images/9-Fin_Asssistant_configuration_Post_Installation_DHCP.png)


10) Gestionnaire DHCP

    Clic droit sur le serveur dans la liste
    
    Selectionner : Gestionnaire DHCP

  ![Image](/Images/10-Gestionnaire%20DHCP.png)

Le gestionnaire DHCP s'ouvre
  
  ![Image](/Images/11-Gestionnaire%20DHCP.png)

11) Nouvelle étendue IPv4

    Clic droit sur IPV4

    Selectionner : Nouvelle étendue...
    

   ![Image](/Images/12-Nouvelle%20etendue%20IPv4.png)

l'assistant nouvelle étendue se lance
    
  ![Image](/Images/13-Configuration%20nouvelle%20étendue.png)

12) Paramètrage de la plage d'adresses IP

    Renseigner la plage d'adresses IP

   ![Image](/Images/14-Paramètres%20de%20la%20plage%20d'adresses%20IP.png)

  puis au besoin la passerelle par défaut et si existant le nom de domaine, le serveur DNS

  ![Image](/Images/16-Passerelle%20par%20défaut.png)
  ![Image](/Images/17-Nom%20de%20domaine%20et%20seveur%20DNS.png)

  Ne rien renseigner pour Serveur WINS

  ![Image](/Images/18-Serveur%20Wins.png)

   
13) Activation de l'étendue

    Pour finire cette configuration, il faut activer l'étendue

      
  ![Image](/Images/19-Activer%20l'étendue.png)

  Il est ensuite possible de visualiser, dans le gestionnaire DHCP,l'étendue qui vient d'être activée

  ![Image](/Images/20-activation%20de%20l'étendue.png)     


    
14) Vérification de la configuration de l'adresse IP du client Windows CLIWIN01

    Choisir le mode "Obtenir une adresse IP automatiquement" afin que le serveur DHCP fournisse une adresse au client

    ![Image](/Images/21-Configuration%20adresse%20IP%20du%20client%20Windows.png)


15) Vérification du bon fonctionnement de la configuration

    La commande ipconfig /all permet de vérifier le bon fonctionnement

    Nous pouvons voir que le serveur DHCP est activé et que l'adresse du poste client donné par le serveur DHCP est la première adresse disponible de l'étendue

    ![Image](/Images/22-IPCONFIG.png)

16) Reservation d'une adresse IP

Pour reserver une adresse pour, par exemple un serveur d'impression avec une adresse IP fixe, il faut aller dans le gestionnaire DHCP puis selectionner "Reservation"

  ![Image](/Images/Reservation%20adresse.png)

Il faut alors spécifier l'adresse MAC de l'équipement et l'adresse IP à lui reserver

![Image](/Images/22-Reservation%20IP.png)

En rentrant l'adresse MAC de la machine CLIWIN01 puis en rentrant la commande ipconfig /all, il est possible de vérifier le bon fonctionnement de la reservation.



17) Conclusion

En suivant ce tutoriel pas à pas, il est possible de mettre en fonction un serveur DHCP sur un poste sous Windows Server avec une étandue d'adresses et une reservation d'adresse IP.


