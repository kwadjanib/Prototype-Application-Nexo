# 🍽️ NEXO - Application de Gestion de Restaurant d'Entreprise

## 📋 À propos du projet

**NEXO** est une application interne de digitalisation dédiée à la gestion du service de restauration du personnel. Cette solution permet aux différents acteurs de l'entreprise (employés, équipe de restauration, ressources humaines) de gérer efficacement les repas, commandes et interactions autour du service de restauration d'entreprise.

## 🎯 Objectifs

L'application vise à :
- **Simplifier** le processus de commande et de gestion des repas
- **Optimiser** la planification et la préparation des repas par le restaurant
- **Améliorer** la communication entre les employés et le service de restauration
- **Faciliter** le suivi administratif pour les ressources humaines
- **Réduire** le gaspillage alimentaire grâce à une meilleure anticipation

## 👥 Acteurs et Fonctionnalités

### 👤 Employés
- Consultation du menu du jour et de la semaine
- Commande de repas en ligne
- Gestion de leurs préférences alimentaires et allergies
- Historique de leurs commandes
- Annulation de commandes (selon les délais définis)
- Système de notation et commentaires sur les repas
- Notifications de rappel pour les commandes

### 🍳 Équipe de Restauration
- Gestion du menu quotidien et hebdomadaire
- Visualisation des commandes en temps réel
- Planification de la production selon les commandes
- Gestion des stocks et ingrédients
- Statistiques sur les préférences alimentaires
- Gestion des alertes allergènes
- Suivi de la satisfaction client

### 👔 Ressources Humaines
- Tableau de bord global des statistiques
- Gestion des utilisateurs et des accès
- Suivi budgétaire du service de restauration
- Rapports d'utilisation et de fréquentation
- Gestion des subventions repas
- Export de données pour la comptabilité
- Configuration des paramètres de l'application

## 🚀 Fonctionnalités Clés

### Gestion des Commandes
- Système de commande intuitive avec aperçu visuel
- Délais de commande configurables
- Confirmation automatique par email/notification
- Modifications possibles jusqu'à la limite définie

### Gestion des Menus
- Création et publication de menus attractifs
- Catégorisation des plats (entrées, plats, desserts)
- Étiquetage nutritionnel et allergènes
- Photos des plats
- Menus spéciaux (végétarien, sans gluten, etc.)

### Système de Paiement
- Intégration avec le système de tickets restaurant
- Gestion des subventions employeurs
- Historique des transactions
- Facturation automatique

### Statistiques et Rapports
- Nombre de commandes par période
- Plats les plus populaires
- Taux de satisfaction
- Prévisions de fréquentation
- Analyse du gaspillage alimentaire

## 🛠️ Technologies Utilisées

> **Note**: Ce projet est actuellement en phase de prototype. Les technologies suivantes sont recommandées pour le développement.

### Frontend
- **Framework**: React.js / Vue.js / Angular
- **UI Library**: Material-UI / Bootstrap / Tailwind CSS
- **État**: Redux / Vuex / NgRx
- **Communication**: Axios / Fetch API

### Backend
- **Serveur**: Node.js (Express) / Python (Django/Flask) / Java (Spring Boot)
- **Base de données**: PostgreSQL / MySQL / MongoDB
- **Authentification**: JWT / OAuth 2.0
- **API**: RESTful / GraphQL

### Infrastructure
- **Hébergement**: Cloud (AWS / Azure / GCP) / On-premise
- **Conteneurisation**: Docker
- **CI/CD**: Jenkins / GitLab CI / GitHub Actions

## 📦 Installation

### Prérequis
```bash
# À définir selon la stack technique choisie
# Exemple pour une stack Node.js/React:
- Node.js (v16+)
- npm ou yarn
- Base de données (PostgreSQL/MySQL)
```

### Étapes d'installation
```bash
# 1. Cloner le repository
git clone https://github.com/kwadjanib/Prototype-Application-Nexo.git
cd Prototype-Application-Nexo

# 2. Installer les dépendances backend
cd backend
npm install

# 3. Configurer les variables d'environnement
cp .env.example .env
# Éditer le fichier .env avec vos configurations

# 4. Initialiser la base de données
npm run db:migrate
npm run db:seed

# 5. Démarrer le serveur backend
npm run dev

# 6. Dans un nouveau terminal, installer les dépendances frontend
cd ../frontend
npm install

# 7. Démarrer l'application frontend
npm start
```

## 🔧 Configuration

### Variables d'environnement
```env
# Base de données
DB_HOST=localhost
DB_PORT=5432
DB_NAME=nexo_restaurant
DB_USER=postgres
DB_PASSWORD=votre_mot_de_passe

# Serveur
PORT=3000
NODE_ENV=development

# JWT
JWT_SECRET=votre_secret_jwt
JWT_EXPIRATION=24h

# Email (pour notifications)
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=noreply@entreprise.com
SMTP_PASSWORD=mot_de_passe_smtp

# Autres configurations
UPLOAD_DIR=./uploads
MAX_FILE_SIZE=5MB
```

## 📱 Utilisation

### Pour les Employés
1. **Se connecter** avec vos identifiants d'entreprise
2. **Consulter** le menu du jour ou de la semaine
3. **Commander** votre repas en sélectionnant vos choix
4. **Confirmer** votre commande avant la limite horaire
5. **Récupérer** votre repas au restaurant à l'heure indiquée

### Pour l'Équipe de Restauration
1. **Publier** le menu quotidien avec photos et descriptions
2. **Consulter** les commandes du jour en temps réel
3. **Préparer** les repas selon les quantités commandées
4. **Marquer** les commandes comme prêtes ou servies
5. **Analyser** les retours et statistiques

### Pour les RH
1. **Accéder** au tableau de bord administrateur
2. **Gérer** les comptes utilisateurs
3. **Configurer** les paramètres de l'application
4. **Consulter** les rapports et statistiques
5. **Exporter** les données pour la comptabilité

## 🗂️ Structure du Projet

```
Prototype-Application-Nexo/
│
├── backend/                 # Code du serveur backend
│   ├── controllers/         # Contrôleurs de l'API
│   ├── models/              # Modèles de données
│   ├── routes/              # Routes API
│   ├── middleware/          # Middleware (auth, validation)
│   ├── services/            # Logique métier
│   ├── config/              # Configuration
│   └── tests/               # Tests unitaires et d'intégration
│
├── frontend/                # Application frontend
│   ├── src/
│   │   ├── components/      # Composants réutilisables
│   │   ├── pages/           # Pages de l'application
│   │   ├── services/        # Services API
│   │   ├── store/           # Gestion d'état
│   │   ├── assets/          # Images, styles
│   │   └── utils/           # Utilitaires
│   └── public/              # Fichiers statiques
│
├── database/                # Scripts de base de données
│   ├── migrations/          # Migrations
│   └── seeds/               # Données de test
│
├── docs/                    # Documentation
│   ├── api/                 # Documentation API
│   ├── user-guide/          # Guide utilisateur
│   └── architecture/        # Documentation technique
│
└── README.md                # Ce fichier

```

## 🔐 Sécurité

- **Authentification** : Système JWT avec refresh tokens
- **Autorisation** : Contrôle d'accès basé sur les rôles (RBAC)
- **Données sensibles** : Chiffrement des données personnelles
- **HTTPS** : Communication sécurisée obligatoire en production
- **Validation** : Validation stricte des entrées utilisateur
- **Protection CSRF** : Tokens CSRF pour les formulaires
- **Rate Limiting** : Protection contre les abus

## 🧪 Tests

```bash
# Tests backend
cd backend
npm test                    # Tests unitaires
npm run test:integration    # Tests d'intégration
npm run test:coverage       # Couverture de code

# Tests frontend
cd frontend
npm test                    # Tests unitaires
npm run test:e2e            # Tests end-to-end
```

## 📈 Roadmap

### Phase 1 - MVP (En cours)
- [x] Définition des besoins
- [ ] Conception de l'architecture
- [ ] Développement de l'interface employé
- [ ] Système de commande basique
- [ ] Gestion des menus

### Phase 2 - Fonctionnalités avancées
- [ ] Interface équipe de restauration
- [ ] Dashboard RH
- [ ] Système de paiement
- [ ] Notifications push
- [ ] Application mobile

### Phase 3 - Optimisation
- [ ] Système de recommandations IA
- [ ] Analyses prédictives
- [ ] Intégration avec systèmes RH existants
- [ ] Module de feedback avancé
- [ ] Gamification

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le projet
2. **Créer** une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. **Commit** vos changements (`git commit -m 'Add some AmazingFeature'`)
4. **Push** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrir** une Pull Request

### Standards de code
- Suivre les conventions de nommage du projet
- Écrire des tests pour les nouvelles fonctionnalités
- Documenter le code avec des commentaires clairs
- Respecter les guidelines de style (ESLint, Prettier)

## 📝 Licence

Ce projet est un développement interne pour [Nom de l'Entreprise]. Tous droits réservés.

## 👨‍💻 Équipe de Développement

**Stagiaire Développeur Full-Stack**
- Développement et maintenance de l'application
- Documentation technique
- Support utilisateur

**Équipe Projet**
- Product Owner : [À définir]
- Scrum Master : [À définir]
- Équipe de développement : [À définir]

## 📞 Contact et Support

- **Email** : support-nexo@entreprise.com
- **Documentation** : [URL de la documentation]
- **Issues** : [GitHub Issues](https://github.com/kwadjanib/Prototype-Application-Nexo/issues)

## 🙏 Remerciements

- Équipe des Ressources Humaines pour les spécifications
- Équipe de restauration pour leur collaboration
- Tous les employés testeurs pour leurs retours

---

**Note**: Ce projet est actuellement en phase de prototype. Cette documentation sera mise à jour au fur et à mesure de l'avancement du développement.
