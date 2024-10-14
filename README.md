<div align="center"><h1>Projet 1 - Groupe 2 TSSR 2024</h1></div>
<div align="center"><h1>Sécurisation de Mot de passe</h1></div>

<HR>

### Membres
- Théophile
- Tristan
- Bastien

| Rôle | Semaine 1 | Semaine 2 | Semaine 3 |
| :-: |:-: |:-: |:-: |
| __Product Owner__ | *Tristan* | *Théophile* | *Bastien* |
| __Scrum Master__ | *Théophile* | *Bastien* | *Tristan* |
| __Techos__ | *Bastien* | *Tristan* | *Théophile* |

<details>
  
<summary><strong><front size="+5">Présentation du projet et objectifs</front></strong></summary>

- Monter un serveur
  
- Connecter un ou plusieurs client(s)

- Récupérer un fichier zippé chiffré sur le serveur
  
- Tester la robustesse du mot de passe à l'aide d'une attaque par dictionnaire
 


</details>

<HR>

<details>
  <summary><strong> Introduction </summary>
    
> La sécurité des données est une chose essentielle dans la société moderne. Le mot de passe est la première couche de sécurité et elle se doit d'être robuste afin d'empêcher toute intrusion.
    De plus, l'accessibilité aux outils de piratage de mot de passe est ouvert à tous aujourd'hui et est devenu relativement simple pour une personne aguéri.

> C'est un enjeu majeur qui touche particuliers comme professionels et la sensibilisation sur ce sujet est primordiale.
  
  </details>

<HR>

<details><summary>Tâches réalisées<strong></strong></summary>
<HR>

- Semaine 1
  
| Tâches | Réalisation | Description |
| :-: | :-: | :-: |
| Installer le client Ubuntu | Fait | Client fonctionnel |
| Squelette de la documentation générale | Fait | Plan établi |
| Squelette de la documention administrateur | Fait | Plan établi |
| Création du serveur de fichier | Non fait | Report S2 cause documentation |

<HR>

- Semaine 2 

| Tâches | Réalisation | Description |
| :-: | :-: | :-: |
| Création du serveur de fichier | | 
| Squelette de la documentation utilisateur | |
| Connection de la VM au serveur | |
| Continuité des documentations | | 


<HR>

- Semaine 3

| Tâches | Réalisation | Description |
| :-: | :-: | :-: |


</details>


<HR>

## *__Choix techniques__*

Nous avons utilisé un serveur windows 2022 avec des clients Linux Ubuntu 24.04 LTS

Nous utiliserons le logiciel John the Ripper pour le craquage de mot de passe.

<details><summary><strong>John The ripper c'est quoi ?</strong></summary>
  
- JohnTheRipper est un outil de "cracking" de mots de passe, prenant en charge de nombreux algorithmes de "hash". La version "-jumbo" est une amélioration de cet outil, et permet, entre autres, de récupérer le "hash" des fichiers .zip
  
-  Mode "simple" : L'outil effectue quelques modifications sur le nom d'utilisateur afin de trouver le mot passe (Par exemple, si l'utilisateur s'appelle toto, l'outil essaierait les mots de passe "Wilder", "wilder123", "WiLdeR123', etc ...). Ce mode étant le plus rapide à effectuer, le mot de passe qui serait trouvé avec cette méthode serait un mauvais mot de passe.
  

- Mode incrémental (Ou attaque "brute force"): Dans ce mode, l'outil va essayer toutes les combinaisons de caractères possibles jusqu'à trouver le bon mot de passe. Cette technique est techniquement infaillible, bien que la robustesse du mot de passe influe grandement sur le temps de calcul nécessaire à le trouver. Afin d'augmenter la pertincence de l'algorithme, l'outil va implémenter la recherche des caractères par fréquence d'utilisation, pour rechercher en priorité les caractères les plus utilisés statistiquement.
  

- Attaque par dictionnaire : L'outil essaiera un à un tous les mots contenus dans une liste préalablement chargée (Par défault, la liste password.lst fournie contiens plus de 3000 mots), en leur appliquant les mêmes modifications que dans le mode "simple".
</details>

## *__Tests réalisés__*
Nous avons tenté de se connecter par SSH sur le serveur windows avec un client Ubuntu sans succès. La communication était possible mais la connection refusée par les ports de Windows malgré la désactivation du Pare-Feu. 

| Problèmes rencontrés | Solutions apportées |
| :-: |:-:   |
| - CRTL+ALT+SUPPR sur une VM windows serveur | - Menu "Entrée" puis "Executer CTRL+ALT+SUPPR" |
| - Installation de Hashcat | - Installer John-The-Ripper | 
| - Connection par SSH sur serveur windows avec client Ubuntu impossible | - Création d'un serveur de fichier pour s'y connecter|


## *__Suggestions d'amélioratons__*






