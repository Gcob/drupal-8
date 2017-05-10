# Développer avec Drupal 8

## Indexe

### [Accueil](#1)
* [Introduction](#introduction)
* [Problématiques courantes du web](#problématiques-courantes-du-web)
* [Qu'est-ce qu'on voit dans ce repo](#quest-ce-quon-voit-dans-ce-repo)
* [Exigence et recommandations](#exigence-et-recommandations)

### [La configuration du serveur](./documentation/config-serveur.md)
* [Introduction](./documentation/config-serveur.md#introduction)
* [Développer avec une machinne virtuelle](./documentation/config-serveur.md#développer-avec-une-machinne-virtuelle)
* [La machinne virtuelle de Drupal](./documentation/config-serveur.md#la-machinne-virtuelle-de-drupal)
* [Les étapes d'installation](./documentation/config-serveur.md#les-étapes-dinstallation)

### [Exporter et importer Drupal 8](./documentation/export-import.md)

## Introduction

Bonjour à tous, j'ai créé ce repo git car je crois que la documentation pour développer avec Drupal 8 est présente et vaste, mais pas centralisé. Ne connaissant pas du tout Drupal avant, j'ai dû faire beaucoup de recherche et d'essai-erreur avant de pouvoir finalement trouver ce qui me convenait le plus pour développer un projet.

## Problématiques courantes du web

En programmation web, plusieurs problématiques sont récurrentes, tel que:

* La configuration du serveur *(serveur locale, de développement, de production, etc.)*;

* La configuration du framework utilisé *(configuration relative au serveur, modules complémentaire et leurs configurations, présence d'UUID, etc.)*;

* L'environnement de travail *(Logicielles Windows ou Mac, IDE, etc.)*;

* Le développement de groupe d'un même projet *(Git devrait être une excellente solution pour résoudre ce problème)*

* Compatibilité, Responsive et autres pratiques courantes du web;

* Etc.


## Qu'est-ce qu'on voit dans ce repo

L'objectif de ce repo est de centraliser les informations nécessaires pour développer un projet complexe Drupal 8. Les concepts expliqués ciblent un développement rapide et efficace. Concernant les problématiques du web mentionné plus haut, ce repo couvre les trois premières.

> Par complexe, je sous-entends le développement de thèmes, modules, bloques personnalisés, contenus personnalisés ou tout ce que Drupal 8 permet de réaliser pouvant sortir du cadre de l'interface utilisateur de base.

## Exigence et recommandations

Avant d'aller plus loin, assurez-vous d'être familier avec:

* l'interface utilisateur Drupal 8 et ses fonctionnalités,

* les CLI (interpréteur de commandes tel que GitBash),

* Git

* Php

* Composer (gestionnaire de dépendances php)

* Yaml (très simple à apprendre)

* les machines virtuelles (Vagrant et Virtual Box)

Je sais que cela peut sembler exhaustif, mais je ne demande pas de maitriser les éléments précédents. Je demande d'être familier avec, car aucun de ces concepts ne sera exploité en profondeur dans cette documentation, mais ils seront précent.
	
### Bonne lecture!