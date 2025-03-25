# Serveur Rocket.Chat 
![logo de Rocket.Chat](Ressources/rocketchat.jpg)

Cette documentation a pour objectif de présenter le projet 1 réalisé au sein de la Wild Code School par Anthounes NEZI, Brendan BORNE et Lloyd MORLET.

Ce projet a pour but de mobiliser les compétences suivantes :
* Mise en place de serveur
* Installation et configuration de service
* Réalisation de projet en équipe
* Documentation des étapes
* Démonstration de réalisation finale

---

## Sommaire 

- [🎯 Présentation du projet](#presentation-du-projet)
- [📜 Introduction](#introduction)
- [👥 Membres du groupe par sprint](#membres-du-groupe-par-sprint)
- [⚙️ Choix Techniques](#choix-techniques)
- [🧗Difficultés rencontrées](#difficultes-rencontrees)
- [💡 Solutions trouvées](#solutions-trouvees)
- [🚀 Améliorations possibles](#ameliorations-possibles)

---

## 🎯 Présentation du projet
<span id="presentation-du-projet"></span>

### Présentation

Le sujet qui a été choisir pour ce projet est le sujet numéro 8. Il s'agit pour ce projet d'implémenter un serveur de chat.

Pour cela, une machine serveur est créée, afin d’accueillir le service de messagerie Rocket.Chat. Deux machines clients pourront accéder au service de messagerie en s'y connectant grâce à un navigateur.

### Objectifs finaux

Ce projet est divisé en deux objectifs, un objectif principal et un objectif secondaire.

L'objectif principal est la mise en place du serveur de messagerie instantanée. Pour cela, il doit être effectivement utilisable entre 2 clients. Le serveur doit être installé et configuré sur une machine Debian 12. Les clients sont une machine sous Windows, et une machine sous Ubuntu. Les détails techniques concernant les machines sont donnés dans la partie _Choix techniques_ de ce document.

La tâche secondaire est de personnaliser les emojis et les réactions disponibles en fonction des conversations du serveur de chat.

---

## 📜 Introduction
<span id="introduction"></span>

* Utilisation de la méthodologie Scrum
* Rôles tournant
* Répartition des tâches

## 👥 Membres du groupe par sprint
<span id="membres-du-groupe-par-sprint"></span>

### Sprint 1

| Membre   | Rôle       | Missions |
| -------- | ---------- | -------- |
| Anthounes NEZI| PO    | Machine  client WIN01, structure USER_GUIDE.md |
| Brendan BORNE | SM    | Machine client UBU02, structure README.md, renfort machine serveur SRVLX01 |
| Lloyd MORLET  | Sbire | Machine serveur SRVLX01, structure INSTALL.md |

### Sprint 2

| Membre   | Rôle         | Missions |
| -------- | ----------   | -------- |
| Anthounes NEZI  | SM    | Rédaction de USERGUIDE.md, configuration du serveur et des emojis |
| Brendan BORNE   | Sbire | Rédaction de README.md, configuration du serveur et des emojis |
| Lloud MORLET    | PO    | Rédaction de INSTALL.md, configuration du serveur et des emojis |

## ⚙️ Choix techniques
<span id="choix-techniques"></span>

### Machines

Configuration de machine virtuelle client 1
* **Système d'exploitation** : Windows 10
* **Nom** : WIN01 
* **Compte utilisateur** : wilder
	* **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.10 avec le masque 255.255.255.0 
* **Langue** : Fr


Configuration de machine virtuelle client 2:
* **Nom** : UBU02
* **Compte utilisateur** :
  * wilder
  * **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.20 avec le masque 255.255.255.0
* **Langue** : Fr

Configuration de machine virtuelle serveur:
* **Nom** : SRVLX01
* **Comptes utilisateur** :
	* root
  * wilder
  * **Mot de passe** : Azerty1*
* **Adresse IP** : 172.16.10.5 avec le masque 255.255.255.0
* **Langue** : US

### Logiciel

Rocket.Chat est une plateforme de communication Open-Source permettant d'implémenter des canaux de messagerie instantanée textuelle, audio, vidéo, ainsi que le partage de fichiers. Cette plateforme est très personnalisable et configurable, permettant d'ajouter de nombreux modules liés à la sécurité des données, la modération des canaux de discussion et de services tiers (GitHub, Google Drive, etc...).


# 🧗 Difficultés rencontrées
<span id="difficultes-rencontrees"></span>

1. Installation de Rocket.Chat sur Debian
  * Procédure longue et difficile
  * Installation des dépendances à la main
  * Configuration à la main   

1. Personnalisation des canaux de discussion non supportée nativement

# 💡 Solutions trouvées
<span id="solutions-trouvees"></span>

1. Passer par le gestionnaire de package snap

2. Installer un module ?
	1. -> pas encore trouvé

# 🚀 Améliorations possibles
<span id="ameliorations-possibles"></span>

1. Utiliser un autre système d'installation pour le serveur (Docker par exemple)