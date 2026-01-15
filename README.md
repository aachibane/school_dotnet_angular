# School Management System

![GitHub repo size](https://img.shields.io/github/repo-size/aachibane/school_dotnet_angular)
![GitHub language count](https://img.shields.io/github/languages/count/aachibane/school_dotnet_angular)
![GitHub top language](https://img.shields.io/github/languages/top/aachibane/school_dotnet_angular)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Angular](https://img.shields.io/badge/Angular-17+-red.svg)
![.NET](https://img.shields.io/badge/.NET-8.0-purple.svg)

> Application full-stack de gestion scolaire développée avec Angular et ASP.NET Core, démontrant l'intégration frontend-backend via API REST.

## 📋 À propos du projet

School Management System est une application web moderne qui permet de gérer efficacement les entités principales d'un établissement scolaire. Ce projet démontre la maîtrise des technologies Angular et .NET dans un contexte d'architecture full-stack professionnelle.

### Cas d'usage

- Gestion complète des étudiants (ajout, modification, suppression, consultation)
- Administration des classes et groupes
- Gestion du personnel enseignant
- Interface utilisateur responsive et intuitive
- Communication sécurisée entre frontend et backend via API REST

## 🚀 Technologies utilisées

### Frontend
- **Angular 17+** - Framework JavaScript moderne
- **TypeScript** - Typage statique pour JavaScript
- **HTML5 / CSS3** - Structure et style
- **Angular Router** - Navigation SPA
- **HttpClient** - Communication HTTP avec le backend
- **RxJS** - Programmation réactive

### Backend
- **ASP.NET Core 8.0** - Framework backend Microsoft
- **C#** - Langage de programmation
- **Entity Framework Core** - ORM pour la base de données
- **API REST** - Architecture d'API
- **SQL Server** - Base de données relationnelle

### Outils et méthodologies
- **Architecture MVC** - Pattern de conception
- **Dependency Injection** - Inversion de contrôle
- **CORS** - Gestion des requêtes cross-origin
- **Git** - Contrôle de version

## ✨ Fonctionnalités principales

- ✅ **Interface Angular moderne** connectée au backend .NET via HTTP
- ✅ **Opérations CRUD complètes** pour toutes les entités (Create, Read, Update, Delete)
- ✅ **Architecture séparée** avec frontend et backend indépendants
- ✅ **Communication REST API** avec gestion des erreurs
- ✅ **Routing Angular** pour navigation fluide
- ✅ **Services réutilisables** pour la logique métier
- ✅ **Composants modulaires** Angular suivant les best practices

## 📦 Installation et lancement

### Prérequis

```bash
Node.js (v18+)
npm (v9+)
.NET SDK 8.0+
SQL Server ou SQL Server Express
```

### 1. Backend (.NET)

```bash
# Naviguer vers le dossier backend
cd AngularApp1.Server

# Restaurer les dépendances NuGet
dotnet restore

# Appliquer les migrations de base de données (si configuré)
dotnet ef database update

# Lancer l'API
dotnet run
```

L'API REST sera disponible sur `http://localhost:5000` ou `https://localhost:5001`

### 2. Frontend (Angular)

```bash
# Naviguer vers le dossier frontend
cd angularapp1.client

# Installer les dépendances npm
npm install

# Lancer le serveur de développement
ng serve
```

L'application web sera accessible sur `http://localhost:4200`

### 3. Accès à l'application

Une fois les deux serveurs démarrés :
- Frontend : `http://localhost:4200`
- Backend API : `http://localhost:5000`
- Swagger (si activé) : `http://localhost:5000/swagger`

## 📁 Structure du projet

```
school_dotnet_angular/
│
├── angularapp1.client/          # Application Angular (Frontend)
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/      # Composants Angular
│   │   │   ├── services/        # Services pour API calls
│   │   │   ├── models/          # Interfaces TypeScript
│   │   │   └── app.module.ts    # Module principal
│   │   ├── assets/              # Ressources statiques
│   │   └── environments/        # Configuration environnements
│   ├── package.json
│   └── angular.json
│
├── AngularApp1.Server/          # API ASP.NET Core (Backend)
│   ├── Controllers/             # Contrôleurs API REST
│   ├── Models/                  # Modèles de données
│   ├── Data/                    # DbContext et migrations
│   ├── Services/                # Logique métier
│   ├── Program.cs               # Point d'entrée
│   └── appsettings.json         # Configuration
│
├── AngularApp1.sln              # Solution Visual Studio
└── README.md                    # Documentation
```

## 🔄 Architecture et flux de données

```
┌─────────────────┐         HTTP REST API          ┌──────────────────┐
│                 │         (JSON)                  │                  │
│  Angular App    │ ◄──────────────────────────► │   ASP.NET API    │
│  (Frontend)     │         CORS enabled            │   (Backend)      │
│                 │                                 │                  │
└─────────────────┘                                 └──────────────────┘
        │                                                    │
        │                                                    │
   Components                                         Entity Framework
   Services                                                  │
   Routing                                                   │
        │                                                    ▼
        └──────────────► User Interface         ┌──────────────────┐
                                                 │   SQL Server     │
                                                 │   Database       │
                                                 └──────────────────┘
```

Le frontend Angular communique avec le backend via des appels HTTP. Les services Angular encapsulent la logique de communication avec l'API REST, et les composants affichent les données reçues.

## 🎯 Objectifs du projet

Ce projet a été développé pour démontrer les compétences suivantes :

1. **Développement full-stack** : Maîtrise complète de la stack Angular + .NET
2. **Architecture REST** : Conception et implémentation d'API RESTful
3. **Intégration frontend-backend** : Communication HTTP, gestion des états
4. **Opérations CRUD** : Création, lecture, mise à jour et suppression de données
5. **Best practices** : Architecture modulaire, séparation des responsabilités
6. **Gestion de projet** : Utilisation de Git, organisation du code

## 🛠️ Configuration

### Configuration du Backend

Modifier `appsettings.json` pour la connexion à la base de données :

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=SchoolManagement;Trusted_Connection=True;"
  },
  "AllowedOrigins": ["http://localhost:4200"]
}
```

### Configuration du Frontend

Modifier `src/environments/environment.ts` :

```typescript
export const environment = {
  production: false,
  apiUrl: 'http://localhost:5000/api'
};
```

## 📸 Aperçu de l'application

> *Note : Des captures d'écran de l'interface seront ajoutées prochainement pour illustrer les fonctionnalités.*

**Fonctionnalités à venir dans les captures** :
- Dashboard principal avec statistiques
- Liste des étudiants avec pagination
- Formulaire d'ajout/modification d'étudiant
- Interface de gestion des classes
- Vue détaillée d'un enseignant

## 🧪 Tests

```bash
# Tests unitaires Angular
cd angularapp1.client
ng test

# Tests backend .NET
cd AngularApp1.Server
dotnet test
```

## 🚧 Améliorations futures

- [ ] Authentification et autorisation (JWT)
- [ ] Gestion des rôles utilisateurs (Admin, Enseignant, Étudiant)
- [ ] Export de données (PDF, Excel)
- [ ] Système de notifications en temps réel
- [ ] Dashboard avec graphiques et statistiques
- [ ] Internationalisation (i18n)
- [ ] Mode sombre

## 📝 Utilisation pour le CV

Ce projet démontre :
- ✅ Compétences Angular avancées (services, routing, HTTP, reactive forms)
- ✅ Développement backend avec ASP.NET Core et C#
- ✅ Conception d'API REST professionnelle
- ✅ Intégration full-stack complète
- ✅ Utilisation d'Entity Framework Core
- ✅ Architecture moderne et scalable

## 🤝 Contribution

Ce projet est principalement à des fins de démonstration de compétences. Les suggestions d'amélioration sont bienvenues via les issues GitHub.

## 📄 License

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 👨‍💻 Auteur

**Akram Achibane**  
Ingénieur Logiciel Full-Stack

- 💼 LinkedIn : [linkedin.com/in/akram-achibane](https://linkedin.com/in/akram-achibane)
- 🐱 GitHub : [github.com/aachibane](https://github.com/aachibane)
- 📧 Email : [Disponible sur demande]

---

## 🌟 Projets connexes

Ce projet fait partie de mon portfolio technique qui inclut également :
- Applications microservices avec .NET
- Intégrations API REST sécurisées
- Solutions full-stack Angular/.NET en environnement professionnel
