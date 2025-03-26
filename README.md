# Serveur Rocket.Chat 
![logo de Rocket.Chat](Ressources/rocketchat.jpg)

Cette documentation a pour objectif de présenter le projet 1 réalisé au sein de la Wild Code School par Anthounes NEZI, Brendan BORNE et Lloyd MORLET.

Ce projet a pour but de mobiliser les compétences suivantes :
* Mise en place de serveur
* Installation et configuration de service
* Réalisation de projet en équipe
* Documentation des étapes
* Démonstration de réalisation finale

Les guides d'installation et d'utilisation sont disponibles respectivement dans les fichiers **INSTALL.md** et **USER_GUIDE.md**. 

---

## Sommaire 

- [🎯 Présentation générale du projet](#presentation-du-projet)
- [📜 Introduction](#introduction)
- [👥 Membres du groupe par sprint](#membres-du-groupe-par-sprint)
- [⚙️ Choix Techniques](#choix-techniques)
- [🧗Difficultés rencontrées](#difficultes-rencontrees)
- [💡 Solutions trouvées](#solutions-trouvees)
- [🚀 Améliorations possibles](#ameliorations-possibles)

---

## 🎯 Présentation générale du projet
<span id="presentation-du-projet"></span>

### Présentation

Le sujet qui a été choisi pour ce projet est le sujet numéro 8. Il s'agit pour ce projet d'implémenter un serveur de chat.

Pour cela, une machine serveur est créée, afin d’accueillir le service de messagerie Rocket.Chat. Deux machines clients pourront accéder au service de messagerie en s'y connectant grâce à un navigateur.

### Objectifs finaux

Ce projet est divisé en deux objectifs, un objectif principal et un objectif secondaire.

L'objectif principal est la mise en place du serveur de messagerie instantanée. Pour cela, il doit être effectivement utilisable entre 2 clients. Le serveur doit être installé et configuré sur une machine Debian 12. Les clients sont une machine sous Windows, et une machine sous Ubuntu. Les détails techniques concernant les machines sont donnés dans la partie **Choix techniques** de ce document.

La tâche secondaire est de personnaliser les emojis et les réactions disponibles en fonction des conversations du serveur de chat.

---

## 📜 Introduction
<span id="introduction"></span>

Cette partie de la documentation présente la gestion du projet jusqu'à réalisation, ainsi que les choix techniques effectués, les difficultés rencontrées, les solutions qui y ont été trouvées et les pistes d'améliorations possibles pour le serveur de chat.

## 👥 Membres du groupe par sprint
<span id="membres-du-groupe-par-sprint"></span>

Pour réaliser ce projet, nous avons implémenté la méthode de gestion de projet Scrum. Comme le projet dure 2 semaines, il est divisé en deux sprints. Les rôles de Product Owner et Scrum Master ont tourné à chaque sprint afin de permettre à tous (ou presque) d'endosser différents rôles au cours du projet.

Les tableaux suivants résument la répartition des rôles par sprint, ainsi que la répartition des tâches à effectuer.

### Sprint 1

| Membre         | Rôle          | Missions                                                                   |
| -------------- | ------------- | -------------------------------------------------------------------------- |
| Anthounes NEZI | Product Owner | Machine  client WIN01, structure USER_GUIDE.md                             |
| Brendan BORNE  | Scrum Master  | Machine client UBU02, structure README.md, renfort machine serveur SRVLX01 |
| Lloyd MORLET   | Technicien    | Machine serveur SRVLX01, structure INSTALL.md                              |

### Sprint 2

| Membre         | Rôle          | Missions                                                                        |
| -------------- | ------------- | ------------------------------------------------------------------------------- |
| Anthounes NEZI | Scrum Master  | Rédaction des questions de la FAQ                                               |
| Brendan BORNE  | Technicien    | Rédaction de README.md et USER_GUIDE.md, configuration du serveur et des emojis |
| Lloud MORLET   | Product Owner | Rédaction de INSTALL.md, configuration du serveur et des emojis                 |

## ⚙️ Choix techniques
<span id="choix-techniques"></span>

L'adresse du réseau configuré est **172.16.10**. Le masque de sous-réseau est **255.255.255.0**. 

Chacune des deux machines client a un système d'exploitation différent. Cela permet de vérifier la compatibilité du serveur de chat sur un plus grand ensemble de machines. Sur chacune de ces machines, il y a au moins un compte wilder. Pour la machine serveur, il existe également un compte root. 

Les caractéristiques de chaque machine sont résumées dans la section ci-dessous.

### Machines

#### Configuration de machine virtuelle serveur

* **Nom** : SRVLX01
* **Comptes utilisateurs** :
	* root
	* wilder
  * **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.5 avec le masque 255.255.255.0
* **Langue** : Anglais (US)

####  Configuration de machine virtuelle client 1

* **Système d'exploitation** : Windows 10
* **Nom** : WIN01 
* **Compte utilisateur** : wilder
	* **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.10 avec le masque 255.255.255.0 
* **Langue** : Français

#### Configuration de machine virtuelle client 2

* **Nom** : UBU02
* **Compte utilisateur** : wilder
  * **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.20 avec le masque 255.255.255.0
* **Langue** : Français

### Logiciel

Rocket.Chat est une plateforme de communication Open-Source permettant d'implémenter des canaux de messagerie instantanée textuelle, audio, vidéo, ainsi que le partage de fichiers. Cette plateforme est très personnalisable et configurable, permettant d'ajouter de nombreux modules liés à la sécurité des données, la modération des canaux de discussion et de services tiers (GitHub, Google Drive, etc...).

##  🧗 Difficultés rencontrées
<span id="difficultes-rencontrees"></span>

Quelques difficultés ont été rencontrées lors de la réalisation de ce projet.

### Installation de Rocket.Chat

L'installation de Rocket.Chat manuellement, en tenant compte de la bonne configuration et versions compatibles pour ses dépendances peut être ardue. Il faut avoir installé une version spécifique de _node.js_, _deno_ et _mongoDB_ pour que Rocket.Chat fonctionne correctement. De plus, la configuration à la main de _mongoDB_ peut s'avérer difficile. 

### Compatibilité des machines virtuelles

La compatibilité des machines virtuelles entre les différents membres de l'équipe n'est pas assurée. Certaines machines ont été créées sur un hôte Debian, les autres sur des hôtes Windows. Certains jeux d'instructions de processeurs (AVX et AVX2) sont nécessaires pour faire fonctionner Rocket.Chat. Cependant, les hôtes Windows peuvent bloquer l'utilisation de ces jeux d'instructions dans des machines virtuelles créées sur Virtualbox.

### Personnalisation du serveur

Par défaut, la personnalisation des canaux de discussion avec des emojis spécifiques n'est pas supportée par Rocket.Chat.

## 💡 Solutions trouvées
<span id="solutions-trouvees"></span>

### Installation de Rocket.Chat

Il a été choisi de passer par le gestionnaire de packages **snap**. Ce gestionnaire de package permet d'embarquer simplement l'intégralité des dépendances nécessaires, pré-configurées avec la bonne version.

### Compatibilité des machines virtuelles

Il a été choisi de refaire chacun de son côté les machines lorsque cela était possible, et un membre de l'équipe a tout simplement changé d'OS pour rendre les machines virtuelles créées compatibles.

### Personnalisation du serveur

Pour personnaliser des conversations spécifiques, il est peut-être possible d'installer un module en passant par le Marketplace de Rocket.Chat. 

>Ce module n'a pas été trouvé à ce jour.

## 🚀 Améliorations possibles
<span id="ameliorations-possibles"></span>

Bien que le serveur Rocket.Chat soit actuellement fonctionnel, des pistes d'amélioration sont possibles.

### Sécurité et maintien

Le passage par le gestionnaire de paquets **snap** n'est pas optimal en matière de sécurité et mise à jour. Même s'il permet d'installer rapidement et facilement le service de serveur Rocket.Chat, cette installation est surtout destinée à de petites implémentations et pour des tests de développement. Il serait possible d'améliorer l'installation de Rocket.Chat en passant par **Docker** ou **Kubernetes**. 

### Personnalisation du serveur

Il est possible d'ajouter de nombreux modules pour améliorer l'expérience proposée sur le serveur Rocket.Chat. Il est par exemple possible d'installer un antivirus (_clamAV_), des chatbots conversationnels, des bots de modération automatiques, une intégration de GitHub ou autres outils de travail...

> Nota Bene : Avec la version gratuite de Rocket.Chat (actuellement installée), on ne peut activer que 5 modules à la fois.
