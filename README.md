# School Management System

![GitHub repo size](https://img.shields.io/github/repo-size/aachibane/school_dotnet_angular)
![GitHub language count](https://img.shields.io/github/languages/count/aachibane/school_dotnet_angular)
![GitHub top language](https://img.shields.io/github/languages/top/aachibane/school_dotnet_angular)

School Management System est une application full-stack développée avec Angular pour le frontend et ASP.NET (C#) pour le backend. Elle permet de gérer les entités principales d'une école (étudiants, classes, enseignants, etc.) via des API REST.

## Technologies

**Frontend**  
- Angular  
- TypeScript  
- HTML / CSS  
- Angular Router  
- HttpClient (services REST)

**Backend**  
- ASP.NET (C#)  
- API REST  
- Entity Framework  
- SQL Server ou base relationnelle

## Fonctionnalités

- Interface web Angular connectée au backend .NET  
- Opérations CRUD pour étudiants, classes et enseignants  
- Architecture séparée : Frontend (angularapp1.client) / Backend (AngularApp1.Server)  
- Communication via REST API

## Installation

### Backend (.NET)
```bash
cd AngularApp1.Server
dotnet restore
dotnet run
```

L'API sera disponible sur `http://localhost:5000`

### Frontend (Angular)
```bash
cd angularapp1.client
npm install
ng serve
```

L'application sera disponible sur `http://localhost:4200`

## Structure du projet
```
school_dotnet_angular
│
├── angularapp1.client   → Frontend Angular
├── AngularApp1.Server  → Backend ASP.NET
└── README.md
```

Le frontend Angular consomme les endpoints REST exposés par le backend .NET pour afficher et manipuler les données.

## Objectifs du projet

- Développer une application full-stack Angular + .NET
- Implémenter une communication REST frontend ↔ backend
- Gérer des opérations CRUD sécurisées
- Pratique des architectures full-stack et d'API REST

## Auteur

**Akram Achibane** - Ingénieur Logiciel

- GitHub : [github.com/aachibane](https://github.com/aachibane)
- LinkedIn : [linkedin.com/in/akram-achibane](https://linkedin.com/in/akram-achibane)
