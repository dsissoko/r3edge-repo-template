# r3edge-repo-template

Ce dépôt **r3edge-repo-template** sert de modèle pour structurer les projets de l'écosystème **r3edge**. Il peut être utilisé via la fonctionnalité **"Use this template"** de GitHub.

## 📌 Usage

1. **Cloner le dépôt** :  
   ```bash
   git clone https://github.com/dsissoko/r3edge-repo-template.git
   cd r3edge-repo-template
   ```
2. **Ou utiliser le template** :  
   Cliquez sur **"Use this template"** pour créer un nouveau projet basé sur cette structure.

---

## 🔧 Prérequis

Avant d'utiliser ce projet, assurez-vous que votre environnement répond aux exigences suivantes :

### 📂 Système d'exploitation
- Linux (Ubuntu/Debian, CentOS, etc.)
- macOS
- Windows avec WSL2 recommandé

### 📦 Dépendances système
- **Docker** (si le projet utilise Docker Compose)
- **Docker Compose** (version 2.x recommandée)
- **Kubernetes** (si le projet cible un cluster Kubernetes)
- **Helm** (si l'application est déployée avec Helm Charts)
- **Git** (gestion des versions)
- **Python 3.x / Node.js / Java** (selon le stack du projet)

### 🌐 Prérequis réseau
- Ouverture des ports entrants/sortants nécessaires
- Accès Internet pour récupérer les dépendances et images Docker
- Configuration d’un proxy si nécessaire

---

## 🚀 Build & Déploiement

### 📦 Build
```bash
./build.sh  # Exemple, à adapter
```

### ▶️ Exécution
```bash
./run.sh  # Exemple, à adapter
```

### ⚙️ Déploiement
```bash
kubectl apply -f k8s/deployment.yaml  # Exemple pour Kubernetes
```

---

## 🛠️ Configuration

### 🔹 Variables externalisées

#### 📌 Issues des dépendances
Ces variables sont définies par les librairies utilisées et doivent être configurées selon leur documentation officielle.

| Dépendance | Documentation |
|------------|--------------|
| Spring Boot | [Spring Docs](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html) |
| Kafka | [Kafka Docs](https://kafka.apache.org/documentation/) |
| PostgreSQL | [PostgreSQL Docs](https://www.postgresql.org/docs/) |

#### 📌 Spécifiques à l'application
Ces variables sont définies au niveau de l'application.

| Nom | Valeur par défaut | Description | Source |
|-----|------------------|-------------|--------|
| `APP_ENV` | `dev` | Environnement d'exécution | `.env`, Spring Profile |
| `LOG_LEVEL` | `INFO` | Niveau de logs (`DEBUG`, `INFO`, `WARN`, `ERROR`) | `.env`, CLI |
| `DATABASE_URL` | `-` | URL de connexion à la base de données | `.env`, Kubernetes Secret |

---

### 🔹 Paramètres de démarrage

#### 📌 Issues des dépendances

| Dépendance | Exemples de paramètres | Documentation |
|------------|-----------------------|--------------|
| Spring Boot | `--spring.profiles.active=prod` | [Spring Docs](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html) |
| Kafka | `--bootstrap-server=localhost:9092` | [Kafka Docs](https://kafka.apache.org/documentation/) |

#### 📌 Spécifiques à l'application

| Nom | Valeur par défaut | Description |
|-----|------------------|-------------|
| `--debug` | `false` | Active le mode debug |
| `--cache-ttl` | `600` | Durée de mise en cache en secondes |
| `--max-workers` | `4` | Nombre de workers utilisés |

📚 **Liste complète et instructions d’utilisation** : [config/README.md](config/README.md)

---

## 🤝 Contribution
Nous n’acceptons pas les contributions externes pour l’instant.

---

## 📞 Support
Pour toute question, contactez-nous à [hello@r3edge.com](mailto:hello@r3edge.com).

---

## ⚖️ Licence
Ce projet est sous licence **Tous droits réservés**.

---

© 2024 r3edge. Tous droits réservés.

---

## 🏆 Badges

![Build](https://img.shields.io/github/actions/workflow/status/dsissoko/r3edge-repo-template/build.yml?branch=main)
![Coverage](https://img.shields.io/codecov/c/github/dsissoko/r3edge-repo-template)
![License](https://img.shields.io/badge/License-MIT-2f74c0?style=flat-square&logo=balance-scale)
