# Documentation utilisateur
<details>
<summary><strong> Qu'est ce que John The Ripper ?</strong></summary>
  
- JohnTheRipper est un outil de "cracking" de mots de passe, prenant en charge de nombreux algorithmes de "hash". La version "-jumbo" est une amélioration de cet outil, et permet, entre autres, de récupérer le "hash" des fichiers .zip
  
-  Mode "simple" : L'outil effectue quelques modifications sur le nom d'utilisateur afin de trouver le mot passe (Par exemple, si l'utilisateur s'appelle Wilder, l'outil essaierait les mots de passe "Wilder", "wilder123", "WiLdeR123', etc ...). Ce mode étant le plus rapide à effectuer, le mot de passe qui serait trouvé avec cette méthode serait un mauvais mot de passe.
  

- Mode incrémental (Ou attaque "brute force"): Dans ce mode, l'outil va essayer toutes les combinaisons de caractères possibles jusqu'à trouver le bon mot de passe. Cette technique est techniquement infaillible, bien que la robustesse du mot de passe influe grandement sur le temps de calcul nécessaire à le trouver. Afin d'augmenter la pertincence de l'algorithme, l'outil va implémenter la recherche des caractères par fréquence d'utilisation, pour rechercher en priorité les caractères les plus utilisés statistiquement.
  

- Attaque par dictionnaire : L'outil essaiera un à un tous les mots contenus dans une liste préalablement chargée (Par défault, la liste password.lst fournie contiens plus de 3000 mots), en leur appliquant les mêmes modifications que dans le mode "simple".

### Fonctionnalités clés de John The Ripper

 John the Ripper possède plusieurs fonctionnalités qui le distinguent des autres outils de craquage de mots de passe 

* Prise en charge de nombreux formats de hachage de mots de passe.

* Capacité à fonctionner sur différentes plateformes (Unix, Windows, macOS).

* Modularité et extensibilité grâce à sa structure de plugins.

* Utilisation de divers modes de craquage, y compris le brute force et l’attaque par dictionnaire.
</details>
<HR>
<details>
  <summary><strong> Qu'est ce que Hashcat ?</strong></summary>
  
### Fonctionnalités Clés de Hashcat

Hashcat offre une gamme impressionnante de fonctionnalités qui en font un outil de choix pour les experts en sécurité 

* Compatibilité: Prise en charge de nombreux algorithmes de hachage, comme MD5, SHA-1, et WPA2.
  
* Performance: Utilisation optimisée des GPU pour une vitesse de craquage accrue.
  
* Flexibilité: Modes de fonctionnement variés, incluant attaque par force brute et attaque par dictionnaire.
  
* Personnalisation: Options avancées pour personnaliser les attaques en fonction des besoins spécifiques.

</details>
<HR>
<details>
<summary><strong> Utilisation de John the Ripper et Hashcat ensemble</strong></summary>

</details>
<HR>


## FAQ - Vos questions, nos réponses

__J'ai le message "AVX is recquired for this build" lorsque je veux utiliser John the Ripper, pourquoi ?__

- *Un problème connu est l'utilisation de John The Ripper sur un OS virtualisé avec Windows 11. Ce problème provient des processeurs INTEL avec la virtualisation. Aucune solution n'a été encore trouvée à ce sujet.*

__Pourquoi je ne peux pas lire mon fichier zip avec Hashcat ?__

- *Hashcat permet de lire le "hash" d'un fichier et non le fichier zip en lui même. Pour ce faire, il faut d'abord extraire le hash afin de le lire avec Hashcat. L'utilisation de John The Ripper est recomandé pour une extraction rapide et complète du "hash".*
