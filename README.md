# DAO avec Injection de Dépendances et Couplage Faible en Java

## Introduction

Ce projet a pour but de démontrer l'application des principes d’**Injection de Dépendances (DI)** et de **Couplage Faible** en Java, à l'aide du patron **DAO (Data Access Object)** pour gérer l'accès aux données.

Le projet permet de **basculer entre deux méthodes d'accès aux données** :  
- Une implémentation DAO traditionnelle (basée sur une base de données locale)  
- Une implémentation DAO via un **Web Service**

L'objectif principal est de montrer comment **injecter les dépendances de manière flexible**, tout en maintenant un **faible couplage** entre les différentes couches de l'application.

---

## Objectifs du TP

- Appliquer les principes de l’**injection de dépendances** et du **couplage faible**
- Mettre en place une solution qui permet de basculer entre :
  - un DAO Base de Données (BD)
  - un DAO Web Service
- Utiliser des **interfaces** pour assurer une abstraction entre les différentes couches de l'application

---

## Injection de Dépendances & Couplage Faible

- L’injection de dépendances est **réalisée manuellement** en Java.
- Le projet repose sur des **interfaces** (ex : `IDao`) pour définir les contrats d'accès aux données.
- Deux implémentations possibles :
  - `DaoImpl` (DAO classique)
  - `DaoImplV2` (DAO Web Service)

L’implémentation est **injectée dans la couche métier** selon la configuration choisie.

---

## Basculement entre DAO classique et Web Service

Le **basculement** entre les deux implémentations se fait grâce à une **configuration dans la classe `AppConfig.java`**.

En fonction du paramètre défini, l'application utilise :
- Soit `DaoImpl`
- Soit `DaoImplV2`

---

## Fichiers clés du projet

- `IDAO.java`  
- `DAOimpl.java`  
- `DAOimplV2.java`  
- `IMetier.java`  
- `MetierImpl.java`  
- `Presentation1.java`  
- `Presentation2.java`  
- `config.txt`

---

## Exécution

Lancer la classe principale correspondant à votre configuration :  

![Capture d’écran (27)](https://github.com/user-attachments/assets/80ee5ff4-d326-4e16-8d1e-88a8ee616983)

