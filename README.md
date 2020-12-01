# Comment déployer un projet Django sur Digital Ocean

Dans cet article, nous allons voir comment vous pouvez facilement déployer votre projet Django sur un serveur Linux (Virtual Private Server aka vps). Dans ce tutoriel, j'utiliserai DigitalOcean , un fournisseur de cloud bien connu qui vous offre un contrôle total sur votre serveur, je choisis également DigitalOcean car ils ont une application en 1 clic Dokku droplet pour vous permettre de démarrer rapidement.

## QU'EST-CE QUE DOKKU ?

Dokku est une plate-forme en tant que service extensible et open source qui s'exécute sur un serveur unique de votre choix.

Pour commencer à utiliser Dokku, vous aurez besoin d'un système qui répond aux exigences minimales suivantes :
- Une nouvelle installation d' Ubuntu 16.04 / 18.04 x64 , Debian 9+ x64 ou CentOS 7 x64 (expérimental) avec l'ensemble FQDN
- Au moins 1 Go de mémoire système

## Conditions préalables
1. Créer un compte **[DigitalOcean](https://cloud.digitalocean.com/)** 
2. S'identifier sur digitalocean puis créer un Droplet
Les étapes à suivre : Create Dokku Droplet > Choisir Marketplace > Basic > $5/mo > London > Password > Create root password:motdepasse > Create Droplet

## Configurez votre VPS

ssh root@your_ip_address

Lorsque vous avez configuré votre droplet, vous avez ajouté un mot de passe root, vous en avez besoin ici pour exécuter les commandes sudo.

'''sudo apt update'''
'''sudo apt upgrade'''

**ajouter un utilisateur limité**

'adduser votre_nom_utilisateur'
'adduser votre_nom_utilisateur sudo'

Vous pouvez maintenant fermer votre session avec la commande '\q' et vous reconnecter avec

'ssh votre_nom_utilisateur @ votre_adresse_ip'
