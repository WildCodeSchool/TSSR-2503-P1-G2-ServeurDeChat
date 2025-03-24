![logo de Rocket.Chat](Ressources/rocketchat.jpg)

Cette documentation a pour objectif de présenter le projet 1 réalisé au sein de la Wild Code School par Anthounes NEZI, Brendan BORNE et Lloyd MORLET.

Ce projet a pour but de mettre en place un réseau constitué de 1 machine virtuelle serveur et 2 machines virtuelles client. 

## Sommaire 

- [🎯 Présentation du projet](#presentation-du-projet)
- [📜 Introduction](#introduction)
- [👥 Membres du groupe par sprint](#membres-du-groupe-par-sprint)
- [⚙️ Choix Techniques](#choix-techniques)
- [🧗Difficultés rencontrées](#difficultes-rencontrees)
- [💡 Solutions trouvées](#solutions-trouvees)
- [🚀 Améliorations possibles](#ameliorations-possibles)

# 🎯 Présentation du projet
<span id="presentation-du-projet"></span>

### Présentation

**Sujet choisi :** Sujet numéro 8 serveur de chat

Tâche principale :
1. Mise en place d’un serveur de messagerie instantanée (chat)
2. Utilisable entre 2 clients
3. Utilisation de **Rocket.Chat**
- **Serveur** : Debian 12
- **Clients** : Windows 10/11 Pro ou Ubuntu 24.04 LTS



### Objectifs finaux

Tâche principale 

Tâche secondaire : 
 - Personnalisation des emojis et des réactions selon les conversations



# 📜 Introduction
<span id="introduction"></span>

# 👥 Membres du groupe par sprint
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

# ⚙️ Choix techniques
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

Présentation de Rocket.Chat


# 🧗 Difficultés rencontrées
<span id="difficultes-rencontrees"></span>

1. Installation de Rocket.Chat sur Debian
  * Procédure longue et difficile
  * Installation des dépendances à la main
  * Configuration à la main   

# 💡 Solutions trouvées
<span id="solutions-trouvees"></span>

1. Passer par le gestionnaire de package snap

# 🚀 Améliorations possibles
<span id="ameliorations-possibles"></span>

1. Utiliser un autre système d'installation pour le serveur (Docker par exemple)