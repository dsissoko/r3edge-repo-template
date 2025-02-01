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

## 🚀 Build & Déploiement

### 📦 Build
Instructions pour compiler / packager le projet :
```bash
# Exemple (à adapter)
./build.sh
```

### ▶️ Exécution
Démarrer l’application :
```bash
# Exemple (à adapter)
./run.sh
```

### ⚙️ Déploiement
Déploiement sur un environnement cible :
```bash
# Exemple pour Kubernetes (à adapter)
kubectl apply -f k8s/deployment.yaml
```

---

## 🛠️ Configuration & Variables d’environnement

Le projet utilise plusieurs types d’emplacements pour gérer les configurations :

| Type | Description |
|------|------------|
| **Ligne de commande** | `./app --log-level=debug --cache-ttl=600` |
| **Variables d’environnement (EnvVar)** | `export DATABASE_URL=...` |
| **Fichier `.env`** | `.env`, `.env.dev`, `.env.prod` |
| **Fichier de configuration** | `config.yaml`, `application.properties` |
| **Gestionnaire de secrets** | Vault, AWS Secrets Manager, Kubernetes Secrets |
| **Secrets GitHub Actions** | Variables CI/CD définies dans `Settings > Secrets` |

### 📌 Exemples de variables clés

| Nom | Obligatoire ? | Valeur par défaut | Description | Emplacement source |
|---------|----------------|----------------|----------------|----------------|
| `DATABASE_URL` | ✅ Oui | `-` | URL de connexion DB | `1️⃣ EnvVar → 2️⃣ .env → 3️⃣ ConfigFile` |
| `GITHUB_TOKEN` | ✅ Oui | `-` | Token GitHub pour CI/CD | `1️⃣ GitHub Secrets → 2️⃣ EnvVar` |

📚 **Liste complète et instructions d’utilisation** : [config/README.md](config/README.md)

---

## 🤝 Contribution

Nous n’acceptons pas les contributions externes pour l’instant.  
Toute modification de cette documentation requiert une validation préalable.

---

## 📞 Support

Pour toute question ou suggestion, contactez-nous à [hello@r3edge.com](mailto:hello@r3edge.com).

---

## ⚖️ Licence

Ce projet est sous licence **Tous droits réservés**.  
Voir le fichier [LICENSE](LICENSE).

---

© 2024 r3edge. Tous droits réservés.

---

## 🏆 Badges

![Build](https://img.shields.io/github/actions/workflow/status/dsissoko/r3edge-repo-template/build.yml?branch=main)
![Coverage](https://img.shields.io/codecov/c/github/dsissoko/r3edge-repo-template)
![License](https://img.shields.io/badge/License-MIT-2f74c0?style=flat-square&logo=balance-scale)
