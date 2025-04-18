# 🚚 Delivery API - Gozem-as-a-Service (Open Source)

> Une API modulaire, extensible et indépendante, prête à être intégrée dans tout système CRM, e-commerce ou app mobile.

---

## 🧭 Description

Cette API de livraison open source vous permet de créer, suivre et gérer des livraisons en temps réel. Elle est conçue pour s’intégrer facilement dans n’importe quel projet, dans n’importe quel langage (JS, PHP, Python, etc.), avec un SDK installable, des endpoints RESTful, et un système modulaire.

---

## 🚀 Fonctionnalités

- 🔁 **Multi-modes** : Sandbox, Preview, Production
- 📦 **Tracking en temps réel** des colis et livreurs
- 🛍️ **Création et gestion complète des livraisons**
- 🔒 **Authentification sécurisée (JWT)**
- 🧑‍💼 **Rôles et permissions (Admin, livreur, client)**
- 📡 **WebSocket-ready** (notifications de suivi)
- 📥 **SDK Node/JS installable**
- 🧠 **Intégrable avec IA pour suggestion d’itinéraires**
- 📊 **Statistiques et monitoring**
- 🔌 **Connexion facile avec CRM, ERP, etc.**

---

## ⚙️ Prérequis

- **Node.js** v16+
- **NestJS**
- **Redis** (cache, sessions)
- **JWT** (authentification)
- **Base de données** : libre au développeur d’utiliser **TypeORM**, **Prisma**, ou tout autre ORM avec MySQL/PostgreSQL *(vous choisissez l’ORM que vous préférez, l’API s’adapte)*
- (Optionnel) **Docker** pour déploiement local

---

## 📁 Structure du projet

```bash
delivery-api/
│
├── src/
│   ├── app.module.ts
│   ├── main.ts
│   ├── common/
│   ├── config/
│   ├── delivery/
│   ├── tracking/
│   ├── auth/
│   ├── users/
│   ├── websockets/
│   ├── sdk/
│   └── utils/
├── prisma/ ou typeorm/
├── test/
├── .env.example
├── docker-compose.yml
├── package.json
├── README.md
└── docs/
