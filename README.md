# 🛍️ VendreFacile — Backend Microservices Architecture

**VendreFacile** est une plateforme de petites annonces moderne, conçue avec une architecture en microservices pour une meilleure scalabilité, maintenabilité et robustesse. Ce backend est conteneurisé avec Docker et orchestré via Docker Compose.

---

## 📦 Structure du projet

```bash
vendrefacile-backend/
├── gateway/                # API Gateway pour le routage global
│   ├── Dockerfile
│   └── ...
├── users-service/          # Authentification & profils utilisateurs
│   ├── Dockerfile
│   └── ...
├── annonces-service/       # CRUD des annonces, modération, recherche
│   ├── Dockerfile
│   └── ...
├── favoris-service/        # Gestion des annonces suivies
│   ├── Dockerfile
│   └── ...
├── messaging-service/      # Messagerie temps réel (WebSocket ou MQTT)
│   ├── Dockerfile
│   └── ...
├── notifications-service/  # Notifications email & SMS
│   ├── Dockerfile
│   └── ...
├── docker-compose.yml
└── README.md
```

---

## 🚀 Principes clés

- **Microservices indépendants** : chaque domaine métier est isolé pour faciliter l’évolution et la maintenance.
- **Scalabilité** : chaque service peut être répliqué ou déployé indépendamment.
- **Conteneurisation** : tous les services sont prêts à être déployés via Docker.
- **Orchestration** : gestion centralisée des services avec Docker Compose.

---

## 📚 Services principaux

- **gateway/** : Point d’entrée unique, gestion du routage et de la sécurité.
- **users-service/** : Authentification, gestion des profils et rôles utilisateurs.
- **annonces-service/** : Création, modification, suppression, recherche et modération des annonces.
- **favoris-service/** : Gestion des annonces favorites/suivies par les utilisateurs.
- **messaging-service/** : Messagerie temps réel entre utilisateurs (WebSocket/MQTT).
- **notifications-service/** : Envoi d’emails et SMS pour les notifications système.

---

## 🐳 Lancement rapide

1. Cloner le repo
2. Adapter les variables d’environnement si besoin
3. Lancer :
   ```sh
   docker-compose up --build
   ```
4. Accéder à l’API via le gateway (par défaut : http://localhost:8080)

---

## 📖 Documentation

Chaque service possède son propre README pour la documentation technique et fonctionnelle.

---

## 🛠️ Contribution

Les PR sont les bienvenues ! Merci de documenter vos changements et de respecter la structure microservices.
