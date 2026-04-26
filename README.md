# LeadelMarché - Système de gestion de magasin

## Description
Ce projet est une application Java Swing de gestion de magasin pour le magasin LeadelMarché.
Le système couvre :
- Inventaire des produits
- Management du personnel
- Management des clients
- Points de vente et encaissement
- Statistiques et alertes simples
- Sauvegarde dans des fichiers texte

## Structure du projet
- `src/com/leadelmarche/Main.java` : point d'entrée principal
- `src/com/leadelmarche/model/` : classes métiers (`Product`, `Client`, `Employee`, `Sale`, `SaleItem`, `Promotion`)
- `src/com/leadelmarche/service/` : services applicatifs et persistance
- `src/com/leadelmarche/view/` : interface graphique MVC
- `data/` : emplacement de stockage des fichiers texte (créé à l'exécution)

## Diagramme de classes (logique)
- `Main` initialise le `DataStore` et les services.
- `DataStore` charge et sauvegarde les entités métiers.
- `InventoryService`, `ClientService`, `PersonnelService`, `PromotionService`, `SalesService`, `StatisticsService` gèrent les règles métier.
- `MainWindow` agrège les panneaux GUI : `InventoryPanel`, `ClientPanel`, `PersonnelPanel`, `SalesPanel`, `StatisticsPanel`.

## Diagramme de communication (logique)
1. L'utilisateur ouvre l'application.
2. Le système charge les données textes via `DataStore`.
3. L'utilisateur sélectionne un module via l'interface.
4. Le module exécute une action CRUD via le service correspondant.
5. Les services mettent à jour les entités et sauvegardent dans les fichiers texte.
6. Une vente génère un ticket texte dans `data/invoices/`.

## Fonctionnalités clés implémentées
- CRUD produit / client / employé
- Recherche partielle insensible aux accents et à la casse
- Gestion de stock avec alerte basse quantité
- Vente avec sélection manuelle ou code-barres
- Ticket de caisse sauvegardé en texte
- Promotion simple appliquée automatiquement
- Gestion du personnel avec contraintes horaires
- Statistiques avec comparaison de périodes
- Données d'exemple déjà présentes pour tester l'application

## Instructions de compilation et d'exécution
1. Ouvrir un terminal dans le dossier `C:\Users\Oussama\LeadelMarche`.
2. Compiler :

```bash
javac -d out src/com/leadelmarche/*.java src/com/leadelmarche/model/*.java src/com/leadelmarche/service/*.java src/com/leadelmarche/view/*.java
```

3. Exécuter :

```bash
java -cp out com.leadelmarche.Main
```

## Améliorations possibles
- Interface plus riche avec icônes et aide intégrée
- Optimisation automatique des plannings du personnel
- Export PDF des tickets et statistiques graphiques
- Envoi par email des tickets/statistiques
- Gestion multi-points de vente avec collaboration entre magasins
