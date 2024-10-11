<div align="center"><h1>Projet 1 - Groupe 2 TSSR 2024</h1></div>
<div align="center"><h1>Sécurisation de Mot de passe</h1></div>

<HR>

### Membres
Théophile Tristan Bastien

| Rôle | Semaine 1 | Semaine 2 | Semaine 3 |
| :-: |:-: |:-: |:-: |
| __Product Owner__ | *Tristan* | | |
| __Scrum Master__ | *Théophile* | | |
| __Techos__ | *Bastien* | | |

<details>
  
<summary><strong><front size="+5">Présentation du projet et objectifs</front></strong></summary>

- Monter un serveur
  
- Connecter un ou plusieurs client(s)

- Récupérer un fichier zippé chiffré sur le serveur
  
- Tester la robustesse du mot de passe à l'aide d'une attaque par dictionnaire
 


</details>

<details>
  <summary><strong> Introduction </summary>
> La sécurité des données est une chose essentielle dans la société moderne. Le mot de passe est la première couche de sécurité et elle se doit d'être robuste afin d'empêcher toute intrusion.
    De plus, l'accessibilité aux outils de piratage de mot de passe est ouvert à tous aujourd'hui et est devenu relativement simple pour une personne aguéri.
> C'est un enjeu majeur qui touche particuliers comme professionels et la sensibilisation sur ce sujet est primordiale.
  
  </details>




<HR>

## *__Choix techniques__*
Nous avons utilisé un serveur windows 2022 avec des clients Linux Ubuntu 24.04 LTS

## *__Tests réalisés__*
Nous avons tenté de se connecter par SSH sur le serveur windows avec un client Ubuntu sans succès. La communication était possible mais la connection refusée par les ports de Windows malgré la désactivation du Pare-Feu. 

| Problèmes rencontrés | Solutions apportées |
| :-: |:-:   |
| - CRTL+ALT+SUPPR sur une VM windows serveur | - Menu "Entrée" puis "Executer CTRL+ALT+SUPPR" |
| - Installation de Hashcat | - Installer John-The-Ripper | 
| - Connection par SSH sur serveur windows avec client Ubuntu impossible | - Création d'un serveur de fichier pour s'y connecter|


## *__Suggestions d'amélioratons__*






