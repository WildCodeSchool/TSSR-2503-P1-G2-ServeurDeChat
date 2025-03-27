## Sommaire

1. [Prérequis technique](#prerequis-technique)
2. [Installation sur le serveur](#installation-sur-le-serveur)
3. [Création et configuration d'un compte administrateur](#creation-et-configuration-d'un-compte-administrateur)
4. [Installation sur le client](#installation-sur-le-client)
5. [FAQ](#faq)

# 1. Prérequis techniques
<span id="prerequis-techniques"></span>
- Une machine serveur baser sur Linux (Ubuntu, Debian, Fedora, etc ...)
- Un Processeur supportant AVX/AVX2 pour pouvoir lancer le service MongoDB qui est requis pour Rocket.Chat
- Le service Snap d'installé (il est préinstallé sur la plupart des distributions Linux modernes. Sinon, reportez-vous au [guide d'installation de Snaps](https://snapcraft.io/docs/installing-snapd))
# 2. Installation sur le serveur
<span id="installation-sur-le-serveur"></span>
## Déployer Rocket.Chat avec Snaps

Pour installer Rocket.Chat sur un serveur baser sur Linux on va utilise la commande snap :

Pour la dernière version de Rocket.Chat, utilisez la commande :
>`sudo snap install rocketchat-server`
	
Si vous souhaitez installer un version précise de Rocket.Chat, utilisez cette commande :
>`sudo snap install rocketchat-server --channel=x.x/stable`

Remplacer le premier *x* par le numéro de la version majeur désirer
Remplacer le deuxième *x* par le numéro de la version mineur désirer.

Une fois l’installation finir par snap, le service démarre automatique.

Il ne vous reste plus cas vous connecter avec une machine client par navigateur ou application en utilisent cette URL : http://172.16.10.5:3000/

# 3. Création et configuration d'un compte administrateur
<span id="creation-et-configuration-d'un-compte-administrateur"></span>
Lors de la 1er connexion sur le serveur par navigateur ou application
le serveur demande la création d'un compte administrateur et le paramétrage initial du serveur.

## 3a. 1er étape - création du compte administrateur

Renseigner les information du compte administrateur.

![admin_config](Ressources/install_imgs/Install_admin_config.png)

- Nom complet : indiquer ici votre nom complet d'administrateur
- Nom utilisateur : indiquer le nom qui sera afficher sur le serveur de chat
- E-mail : indique l'adresse e-mail qui sera lier au compte administrateur
- Mot de passe : indiquer ici le mot de passe pour le compte administrateur

## 3b. 2eme étape - Informations sur l'organisation

Renseigner les informations de votre organisation qui va utiliser le serveur Rocket.chat

![orga_config](Ressources/install_imgs/install_orga_config.png)

- Nom de l'organisation : indiquer le nom de votre organisation
- Secteur de l'organisation : indiquer le secteur lié a votre organisation 
- Taille de l'organisation : indiquer le nombre de personne  au sein de votre organisation
- Pays : indiquer le pays ou ce situe votre organisation

## 3c. 3eme étape - Confirmation

Un mail de confirmation viens d’être envoyer sur l'adresse mail renseigner à la 1ere etape.
Dans ce mail vous trouverez un code de sécurité à utiliser sur la page pour valider

![security_check](Ressources/install_imgs/install_security_check.png)

Vous voilà connectez sur votre serveur Rocket.chat en tant que Administrateur.

![admin_dashboard](Ressources/install_imgs/install_admin_dashboard.png)

Pour commencer a personnaliser votre espace de travail, ajouter des utilisateurs, créer de nouveaux canaux, et gérer l'ensemble de votre serveur, référez vous à la documentation [USER_GUIDE.md](https://github.com/WildCodeSchool/TSSR-2503-P1-G2-ServeurDeChat/blob/c5851948e9ee321d73bdbf4ff8a145df496df95e/USER_GUIDE.md)

# 4. Installation sur le client
<span id="installation-sur-le-client"></span>
Pour utiliser Rocket.chat sur une machine client, vous avez 2 options :

- Utiliser un navigateur web
- utiliser l'application Rocket.chat Desktop

## 4a. Navigateur web

Aucune installation n'est nécessaire. Ouvrez simplement votre navigateur internet et renseigner l'URL de votre serveur Rocket.chat, par exemple : `https://open.rocket.chat`

## 4b. Rocket.chat Desktop

Télécharger et installer Rocket.Chat pour votre système d'exploitation en suivant ce lien : 
https://www.rocket.chat/download-apps

Une fois l'application installer, lancer là et vous arrivez sur cette page :

![app_connect](Ressources/install_imgs/install_app_connect.png)

Il vous suffis de renseigner le lien de votre serveur dans le champs disponible et cliquer sur 'Connect'


# 5. FAQ
<span id="faq"></span>
