# SmartStock - Gestion de Stock Intelligente 

Bienvenue dans le projet **SmartStock**, une application mobile complète développée avec Flutter pour faciliter la gestion de stock des Petites et Moyennes Entreprises et Industries (PME/PMI).

##  Description du Projet

SmartStock est conçue pour fonctionner **100% Hors-Ligne (Offline)** grâce à une base de données locale robuste. Elle permet aux gestionnaires de suivre en temps réel l'état de leur inventaire, de gérer leurs relations fournisseurs et de tracer chaque mouvement de stock.

L'objectif est d'éliminer les erreurs manuelles, d'optimiser les niveaux de stock et de simplifier la facturation et les commandes.

##  Fonctionnalités Détaillées

### 1.  Tableau de Bord (Dashboard)
- Vue synthétique de l'activité.
- Indicateurs clés : Valeur totale du stock, produits en rupture, ventes de la semaine.
- Graphiques interactifs pour l'analyse des tendances.

### 2.  Gestion des Produits (Inventaire)
- **Catalogue complet** : Liste détaillée de tous les articles avec images, prix d'achat/vente, et quantités.
- **Ajout rapide** : Formulaire intuitif pour ajouter/modifier des produits.
- **Catégorisation** : Organisation par familles (Électronique, Mobilier, etc.) pour une recherche rapide.
- **Alertes de stock** : Notification visuelle lorsque le stock atteint le seuil minimum (`minStockLevel`).

### 3.  Gestion des Fournisseurs (Suppliers)
- **Annuaire centralisé** : Fiches détaillées avec coordonnées (Email, Téléphone, Adresse).
- **Historique** : Suivi des interactions et notes par fournisseur.

### 4. Commandes & Mouvements
- **Traçabilité** : Chaque entrée ou sortie est enregistrée dans un journal d'activité.
- **Audit** : Savoir qui a fait quoi et quand (Table `activities`).

### 5.  Administration & Paramètres
- **Profil Utilisateur** : Gestion des informations personnelles.
- **Sécurité** : Authentification et protection des données sensibles.
- **Personnalisation** :
    - Mode Sombre (Dark Mode) / Mode Clair.
    - Support Multi-langues (Français 🇫🇷, Anglais 🇺🇸, Arabe 🇲🇦).

##  Modèle de Données (Base de Données Locale)

L'application utilise **SQLite** pour un stockage performant et fiable. Voici les principales tables :
*   `products` : Stocke les informations produits (SKU, Prix, Stock, Seuil d'alerte...).
*   `suppliers` : Base de données des partenaires (Nom, Contact, Notes...).
*   `categories` : Nomenclature des familles de produits.
*   `activities` : Journal d'audit pour la sécurité et la traçabilité.

## Stack Technique

*   **Langage** : Dart (3.0+)
*   **Framework** : Flutter (Stable)
*   **Architecture** : MVVM (Model-View-ViewModel) avec `Provider`.
*   **Base de Données** : `sqflite` (SQL natif sur Android/iOS).
*   **Interface UI** : Material Design 3 avec une touche personnalisée moderne.
*   **Navigation** : `go_router` pour une gestion fluide des écrans.
*   **Utilitaires** :
    - `intl` : Formatage dates et devises.
    - `fl_chart` : Visualisation de données.
    - `shared_preferences` : Stockage des paramètres utilisateur.

##  Guide de Démarrage

### Prérequis
- [Flutter SDK](https://docs.flutter.dev/get-started/install) installé et configuré.
- Un émulateur Android/iOS ou un appareil physique connecté.

### Installation

1.  **Cloner le dépôt** :
    ```bash
    git clone https://github.com/votre-user/smart_stock.git
    cd Projet_F
    ```

2.  **Récupérer les librairies** :
    ```bash
    flutter pub get
    ```

3.  **Lancer l'application** :
    ```bash
    flutter run
    ```
    *(Astuce : Appuyez sur 'r' dans le terminal pour recharger à chaud après une modification)*

## Organisation du Code Source

```
lib/
├── core/                   # Cœur de l'application
│   ├── models/             # Classes de données (Product, Supplier...)
│   ├── providers/          # Logique métier (State Management)
│   ├── services/           # Services externes (Database, API...)
│   └── theme/              # Configuration du design (Couleurs, Polices)
├── features/               # Modules fonctionnels
│   ├── auth/               # Écrans de connexion
│   ├── dashboard/          # Accueil
│   ├── stock/              # Gestion inventaire
│   ├── suppliers/          # Gestion fournisseurs
│   └── ...
└── main.dart               # Point d'entrée
```

##  Contribuer

1.  Forker le projet
2.  Créer une branche (`git checkout -b feature/AmazingFeature`)
3.  Commit vos changements (`git commit -m 'Add some AmazingFeature'`)
4.  Push vers la branche (`git push origin feature/AmazingFeature`)
5.  Ouvrir une Pull Request

---
**SmartStock** - La solution simple pour une gestion complexe.
