Description du projet
Ce projet est une application Java développée pour illustrer la gestion d'un système de commerce avec interface graphique. L'application "LeadelMarche" permet de gérer les clients, le personnel, l'inventaire, les ventes et les statistiques d'une entreprise commerciale à travers une interface utilisateur conviviale basée sur Swing.

Le programme principal se trouve dans la classe Main du package com.leadelmarche.

Prérequis
Java Development Kit (JDK) : Version 8 ou supérieure doit être installé sur le système
Compilation préalable : Tous les fichiers source .java doivent être compilés pour générer les fichiers .class correspondants

Étapes d'exécution
1.Ouvrir un terminal (invite de commandes ou PowerShell sous Windows)

2.Naviguer vers le dossier racine du projet :
cd chemin/vers/le/dossier/du/projet
Remplacez chemin/vers/le/dossier/du/projet par le chemin absolu vers le dossier contenant les packages Java

3.Lancer l'application :
java -cp . com.leadelmarche.Main

Remarques importantes
Compilation obligatoire : Avant toute exécution, assurez-vous que tous les fichiers .java ont été compilés avec succès en utilisant javac. Les fichiers .class générés doivent être présents dans la structure de dossiers correspondante aux packages.
Structure des packages : L'application utilise une architecture modulaire avec les packages suivants :
com.leadelmarche : Point d'entrée principal
com.leadelmarche.model : Classes de données (Client, Employee, Product, etc.)
com.leadelmarche.service : Logique métier et services
com.leadelmarche.view : Interface utilisateur graphique
Interface graphique : L'application s'ouvre dans une fenêtre avec onglets pour naviguer entre les différentes fonctionnalités de gestion.
