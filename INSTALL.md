<div align="center"><h1>Documentation administrateur</h1></div>
<details><summary>Prérecquis</summary>

Les prérecquis sont annoncés au début de chaque étape.

</details>

### *Installation des postes*
<details>
  <HR>
<summary><strong> Installation d'une VM client Ubuntu </strong></summary>
<HR>
  
  * Choisir l'OS et la version souhaitée.
 
![x](https://i.imgur.com/6WUTuYD.png)


![Y](https://i.imgur.com/IINxXgi.png)


 * Definition des ressources à allouer
   

![z](https://i.imgur.com/KR0v3Bd.png)


 * Determination de l'espace de stockage
   

   ![A](https://i.imgur.com/PSlvETM.png)


 * Configuration de la VM

   ![B](https://i.imgur.com/UHpwtwR.png)

 * Choisir l'image du disque (ISO)

   ![B](https://i.imgur.com/vbcgBsZ.png)

   ![C](https://i.imgur.com/oqviOma.png)

  * Installation de l'OS

    ![D](https://i.imgur.com/kzYhoKF.png) 

  * Prise en compte des preferences
    
   ![H](https://i.imgur.com/EujujhN.png)

  * Effacer tout contenu du disque pour installer l’OS

    ![G](https://i.imgur.com/0VnvBi9.png)

  *  Création de l’utilisateur (Le mot de passe servivra pour toute confirmation admin)

   ![G](https://i.imgur.com/HM5Zfup.png)

    
</details>

<details>
  <summary><strong>Configuration de la VM serveur Windows</strong></summary>
<HR>
  
### Configuration de l'IP

 - Clique droit sur *Ethernet* -> *Propriétés*
     
  ![Propriétéethe](https://i.imgur.com/LnzFb3R.png)

 - Sélectionner *Propriétés* de nouveau.
 
 ![Propriété](https://i.imgur.com/jOBHkY0.png)
 
 -  Cocher *Protocole internet version 4*
   
 ![ipv4](https://i.imgur.com/2hphSeT.png)
 
 - Renseigner l'adresse IPv4 du serveur (ici 172.16.10.10 avec masque de sous-réseau 255.255.255.0)

 ![tapeip](https://i.imgur.com/LumP4xV.png)


<HR>

### Création du serveur de fichier

- Dans le gestionaire de serveur, sélectionné le serveur et appuyer sur *Gérer* puis *Ajouter des rôles et fonctionnalités*

  
![servfich](https://cdn.discordapp.com/attachments/1293220511588810773/1295671480847175701/Capture_2.PNG?ex=6710d119&is=670f7f99&hm=9e11765d4c50add88350a4e07719291baa0892216937d6dd0ed62d7b7ed68041&)

- Suivre le guide d'installation jusqu'à la rubrique *Type d'installation* et choisir *Installation basée sur un rôle ou une fonctionalité*


![typeinsta](https://imgur.com/CvoYXct.png)

- Sélectionner le serveur sur lequel installer la fonctionnalité

![servdest](https://i.imgur.com/0L641Bk.png)

- Descendre dans la liste jusqu'à trouver *Services de fichiers et de stockage*, cocher *Services de fichiers et iSCSl*

![selecrole](https://i.imgur.com/bskgN8C.png)

- Descendre dans la liste jusqu'à trouver *Support de partage de fichiers SMB* puis le cocher

![fonctionnalité](https://cdn.discordapp.com/attachments/1293220511588810773/1295668123642626090/Capture.PNG?ex=6710cdf9&is=670f7c79&hm=10ffcc58a4617f5ce1cfc21276d994e82c6a111d099639315e203ae3f4b60a75&)

- Confirmer jusqu'au début de l'installation

![insta](https://i.imgur.com/mZjaiEn.png)

__Redémarrer la machine et c'est terminé !__

<HR> 
</details>

#### Connection du client au serveur

### *Chiffrer un fichier zippé*

### *Qu'est ce que Hashcat ?*

#### Installation d'HashCat

#### Utilisation d'HashCat pour tester la robustesse d'un mot de passe utilisateur
