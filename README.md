# delivrary_api_opensources
# Delivery API (Gozem-as-a-Service)

## Description

Cette API est un service de gestion de livraisons, conçu pour permettre aux développeurs d'intégrer facilement un système de livraison dans leurs projets. Elle permet de suivre les colis en temps réel, gérer les livraisons, et s'intègre avec des systèmes CRM, tout en offrant une architecture modulaire et évolutive.

Elle est ouverte aux développeurs externes, avec un SDK facilement installable et configurable pour une intégration rapide.

## Fonctionnalités

1. **Gestion des Environnements**:
   - **Mode Sandbox** : Utilisé pour les tests. Les appels API renvoient des données simulées sans affecter le système en production.
   - **Mode Preview** : Pour tester les nouvelles versions avant de les déployer en production. Il permet de valider les fonctionnalités en condition réelle.
   - **Mode Production** : Mode final, stable, avec des données réelles pour l’utilisation en production.

2. **Tracking des Livraisons**:
   - Permet de suivre les livraisons en temps réel.
   - Offre une API de suivi qui retourne des informations comme le statut de la livraison, l'ETA, et la position du livreur.

3. **Gestion des Livraisons**:
   - Crée des livraisons en enregistrant les détails comme l'adresse, les coordonnées du client et le produit à livrer.
   - Suivi complet du statut de la commande, de la préparation à la livraison.

4. **API de Gestion des Commandes**:
   - Permet de créer des commandes, de les modifier et de les supprimer via des endpoints dédiés.
   - Gestion du statut de la commande (en attente, en préparation, en livraison, livrée).

5. **API d'Intégration CRM**:
   - Fournit des endpoints pour intégrer la solution de livraison dans des CRM ou d'autres outils externes.
   - Prise en charge de l'export des données de suivi pour la gestion des livraisons dans les systèmes externes.

6. **Sécurité**:
   - Authentification via JWT pour sécuriser les endpoints.
   - Contrôle d’accès basé sur des rôles (admin, utilisateur, etc.).

7. **Logging et Monitoring**:
   - Intégration avec des outils de monitoring (Sentry, Datadog, etc.) pour la gestion des erreurs en production.
   - Logs détaillés en mode Sandbox pour faciliter le débogage.

8. **SDK Installable**:
   - SDK pour intégrer facilement l'API dans des projets externes. Le SDK est prêt à être publié et utilisé par les développeurs pour connecter leurs projets à cette API de manière simple et rapide.

## Prérequis

- **Node.js** (version 16 ou supérieure)
- **NestJS** (framework backend)
- **TypeORM** (gestion des bases de données)
- **MySQL/PostgreSQL** (base de données relationnelle)
- **Docker** (facultatif, pour les environnements locaux)
- **JWT** (pour l’authentification)
- **Redis** (pour la gestion des sessions et de la mise en cache)

##Structure du Projet
├── src/
│   ├── modules/           # Modules principaux (Livraisons, Commandes, CRM, etc.)
│   ├── common/            # Fonctions utilitaires, services partagés
│   ├── config/            # Fichiers de configuration (base de données, JWT, etc.)
│   ├── middleware/        # Middleware (authentification, validation)
│   ├── services/          # Services métiers
│   ├── controllers/       # Gestion des requêtes HTTP
│   └── main.ts            # Point d'entrée de l'application NestJS
├── dist/                  # Code compilé après la build
├── .env                   # Fichier d'environnement
├── Dockerfile             # Dockerfile pour la production
├── docker-compose.yml     # Configuration Docker
├── package.json           # Dépendances et scripts
└── README.md              # Documentation du projet


## Installation


### 1. Clonez le dépôt
Clonez ce dépôt GitHub sur votre machine locale :
```bash
git clone https://github.com/ton-utilisateur/delivery-api.git
cd delivery-api


