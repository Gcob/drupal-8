[Retour à l'accueil](../README.md)

# La configuration du serveur - Développer avec Drupal 8

## Indexe

* [Introduction](#2)
* [Développer avec une machinne virtuelle](#3)
* [La machinne virtuelle de Drupal](#4)
* [Les étapes d'installation](#5)

## Introduction

 La configuration du serveur est une problématique courante pour tout projet web. Cepandant, Drupal 8 n'est pas très exigent pour la configuration du serveur. Par contre, il est important d'aborder [la configuration du serveur de développement Drupal](https://www.drupal.org/docs/develop/local-server-setup). Vous pouvez employer simplement [Acquia](https://www.acquia.com/fr), [Wamp](http://www.wampserver.com/) ou tout autre serveur [*AMP](https://fr.wikipedia.org/wiki/*AMP). Je crois que pour aider à développer en communauter ou simplement si vous développer sur plus d'une machine (au travail et à domicile par exemple), une [machine virtuel](https://fr.wikipedia.org/wiki/Machine_virtuelle) est l'option idéal. 
 
## Développer avec une machinne virtuelle
 
 Voici quelques avantages de développer avec une machinne virtuelle:
 
 * la configuration des serveurs se fait en quelques étapes minimalistes,
 
 * la configuration des serveurs se fait qu'une seule fois au début et est facilement maintenable par la suite,
 
 * la configuration des serveurs est uniforme pour tout les utilisateurs,
 
 * les logicielles de développements peuvent être inclus, donc plus besoins de réinstaller tout les outils nécessaire au développement (Ex.: Git, Composer et autres plugins CLI),
 
 * les tests sont 100% représentatifs et le déploiement ne laisse aucunnes mauvaises surprises,
 
 * le transport du projet est rapide et centralisé,
 
 * etc.
 
Apprendre à développer avec une machine virtuelle nécessite plus de compétences et de configurations, mais un coup maitrisser, des journées de travails peuvent être sauvés.
 
## La machinne virtuelle de Drupal
 
Étant très populaire, il existent déjà plusieurs outils formidable offerts par la communauté pour le développement avec Drupal 8. [Drupal VM](https://www.drupalvm.com/) fait parti d'entre-eux. Très bien documenté, maintenu, configuré et efficace, cette machine virtuelle est un puissant outil. Je ne parlerais pas en détailles de tout ses configurations et avantages, mais vous vous doutez surement que c'est un environnement Linux *AMP ;)

## Les étapes d'installation

DrupalVM en soit est asser simple à configurer. Par contre, pour aidez à votre installation, voici les étapes détaillées que je suis sous Windows:

> Pour voir les étapes officielles, visitez [le "quick-start-guide" sur Github](https://github.com/geerlingguy/drupal-vm#quick-start-guide)

* Téléchargement et installation de  [Vagrant](https://www.vagrantup.com/downloads.html) et [Virtual Box](https://www.virtualbox.org/wiki/Downloads);

* Téléchargement de [Drupal VM](https://api.github.com/repos/geerlingguy/drupal-vm/zipball/4.4.5);

> **Je recommande fortement de télécharger DrupalVM qu'une seule fois au début du projet et de l'inclure dans votre repo git pour vous assurer de toujours avoir les même configuration et la même version de DrupalVM.**

> Astuce: vous pouvez inclure différente configurations par branche, permettant d'installer un serveur optimisé pour développer ou faire fonctionner un élément en particulier.

* Pour une configuration personnalisé du serveur, dupliquez le fichier `default.config.yml` et nommez le `config.yml`. Normalement, la configuration se fait directement dans le fichier Vagrant, mais le créateur de DrupalVM a conformé la configuration de la machine semblablement à celle de Drupal 8 à l'aide d'un fichier Yaml, nous simplifiant énormément cette étape. Je vous encourage à prendre le temps de modifier ce fichier à votre guise le plus tôt possible et faire les ajustement nécessaire tout au long du projet, car il n'est pas compliqué de mettre a jour un serveur Vagrant ou de simplement le détruire et de le reconstuire. Certainne configuration est obligatoire ou à vérifier et potentiellement unique à chaque installation (locale, dev, prod, etc.):

	* Sous `vagrant_synced_folders`, ajoutez le dossier de partage avec la machinne virtuelle à `local_path`. Par exemple: `C:/webdev/projects/drupal-vm/sync-folder`
	
	* Installez les bons outils, dépendamment de l'environnement désiré, sous `installed_extras`. Par exemple, en mode développement (dev) je vous recommande fortement Drush et la console Drupal qui vous aiderons à développer vos projet.
	
	* N’hésitez pas à modifier la version de php (7 par défaut). Personnellement, je préfère la version 5.6
	
	* Je vous laisse découvrir le reste ;)
	
* L'étape la plus difficile: *vagrant up*! Par contre, avant de l'exécuter, je vous recommande d'installer au moins trois plugins vagrant:

	1. [hostsupdater plugin](https://github.com/cogitatio/vagrant-hostsupdater): `vagrant plugin install vagrant-hostsupdater`
	
	2. [vbguest plugin](https://github.com/dotless-de/vagrant-vbguest): `vagrant plugin install vagrant-vbguest`
	
	3. [auto_network plugin](https://github.com/oscar-stack/vagrant-auto_network): `vagrant plugin install vagrant-auto_network`
	
	> *Pour plus de renseignement sur la relation entre ces plugins et DrupalVM, [lisez la documentation officielle ici](https://github.com/geerlingguy/drupal-vm)*
	
	De plus, avant d'exécuter la commande *vagrant up*, je vous conseille d'exécuter votre CLI en mode administrateur pour laisser paisiblement vagrant faire sa magie.
	
	Alors voilà, vous pouvez enfin dire `vagrant up`
	
> Ayant mentionner dans les [exigence et recommandations](../README.md#5) d'être familier avec les machines virtuelles, il se peut que la commande Vagrant up ne s'exécute pas toujours comme on le voudrait. Par exemple, curl peut empêcher les connexions SSL qu'il ne trouve pas sécuritaire ou votre BIOS peut ne pas être préconfiguré pour autoriser les machines virtuelles. Ne vous découragez pas trop rapidement avec Les VM, je vous assure que si vous rencontrez un ou des problèmes, un coup surmontés, c'est un puissant outil de développement qui vous sauvera beaucoup plus de migraine et de temps que le temps et les migraines que Vagrant peut vous apporter ;)






