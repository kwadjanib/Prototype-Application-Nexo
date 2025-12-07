# Application de Gestion de Restaurant

## Présentation
Prototype destiné à digitaliser la gestion des repas d’entreprise.  
Trois acteurs : **Employés**, **Restaurant**, **RH**.

Fonctionnalités principales :
- Employés : consulter les repas, passer une commande.
- Restaurant : consulter les commandes du jour.
- RH : recharger le compte d’un employé.

## Installation

### Backend
```bash
cd backend
npm install
npx prisma migrate dev
npm run start:dev
