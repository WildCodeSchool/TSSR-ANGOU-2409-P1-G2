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

<HR>
<details>
  
<summary><strong><front size="+5">Présentation du projet et objectifs</front></strong></summary>

- Monter un serveur
  
- Connecter un ou plusieurs client(s)

- Récupérer un fichier zippé chiffré sur le serveur
  
- Tester la robustesse du mot de passe à l'aide d'une attaque par dictionnaire

- Documenter les actions réalisées, les problèmes rencontrés et les solutions apportées le cas échéant.
 

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

- Les objectifs de cette semaine sont d'avoir un serveur fonctionnel et de connecter le client dessus ainsi que de documenter ces actions réalisées.

| Tâches | Réalisation | Description |
| :-: | :-: | :-: |
| Création du serveur de fichier | Fait | Serveur fonctionnel |
| Squelette de la documentation utilisateur | Fait | Squelette établi |
| Connection du client au serveur | Fait | Partage de fichier entre les deux VM |
| Continuité des documentations | Fait | Documentation à jour des avancées techniques |


<HR>

- Semaine 3

| Tâches | Réalisation | Description |
| :-: | :-: | :-: |
| Installation JTR et Hashcat | Fait | Logiciels fonctionnels |
| Création du Fichier zippé sur le serveur | Fait | Fichier protégé |
| Récupération du mot de passe du fichier zippé | Fait | Mort de passe récupéré |
| Finalisation de la doc | |


</details>


<HR>

## *__Choix techniques__*

Nous avons utilisé un serveur windows 2022 avec des clients Linux Ubuntu 24.04 LTS

Nous utiliserons le logiciel John the Ripper et Hashcat pour le craquage de mot de passe.

## *__Tests réalisés__*

Nous avons tenté de se connecter par SSH sur le serveur windows avec un client Ubuntu sans succès. La communication était possible mais la connection refusée par les ports de Windows malgré la désactivation du Pare-Feu. 

Lors du choix de notre logiciel, nous avons essayé d'utiliser les 2 afin d'avoir une vue d'ensemble des fonctionnalités de l'un comme de l'autre. Malheureusement, il nous est impossible d'utiliser John the Ripper pour l'instant. L'addition du processeur AVX512 n'est pas supporter via la VM.

Concernant Hashcat, nous n'arrivons pas encore à lancer une attaque par dictionnaire car le character set n'est pas supporter pour ce type d'attaque (notre base de données de mots).
Ce problème était dû au fait que nous tentions sur un fichier autre qu'un "hash". Désormais, nous combinons JTR avec HashCat afin de récupérer le fichier "hash" d'un zip avec le premier puis récupérer le mot de passe chiffrer dans ce hash avec le second.

| Problèmes rencontrés | Solutions apportées |
| :-: |:-:   |
| - CRTL+ALT+SUPPR sur une VM windows serveur | - Menu "Entrée" puis "Executer CTRL+ALT+SUPPR" | 
| - Connection par SSH sur serveur windows avec client Ubuntu impossible | - Connection en partage de fichiers SAMBA|
| - Craquage de mot de passe avec JTR ou Hashcat | Utilisation des 2 outils en même temps |


## *__Suggestions d'amélioratons__*

- Précisez que l'utilisation d'un logiciel sans l'autre est très complexe et comporte encore des bugs non corrigés, connu depuis longtemps.

- Le nom du sujet n'est pas en adéquation avec son contenu, il ne s'agit pas de sécuriser un mot de passe mais de le craquer.



