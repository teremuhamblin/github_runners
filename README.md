# 📘 GitHub Runner
- – Organisation

Un runner GitHub Actions auto‑hébergé, exécuté dans un conteneur Docker, conçu pour fonctionner au niveau d’une organisation GitHub.  
- Ce pack inclut :
   - un Dockerfile, un docker‑compose.yml, un script d’entrée, et un dossier de travail persistant.

---

#### 🚀 Fonctionnalités
```text
- Runner GitHub Actions pour organisation  
- Déploiement simple via Docker Compose  
- Support Docker‑in‑Docker (build, run, push)  
- Redémarrage automatique  
- Configuration non‑interactive  
- Workdir persistant
```

---

#### 📂 Structure du projet
- Base initiale
```text
├── README.md
├── .github/
      └── .gitkeep
├── docs/
      └── .gitkeep
├── .gitignore
├── LICENSE
├── dockerfile
├── dck-compose.yml
├── entrypoint.sh
└── runner-workdir/
```

---

#### ⚙️ Prérequis
- Docker  
- Docker Compose  
- Un token GitHub Runner (organisation)
   - → GitHub → Settings → Actions → Runners → New Runner

---

#### 🔧 Configuration des variables
- Dans docker-compose.yml, renseigne :
```yaml
environment:
  - RUNNER_NAME=github-runner-organisasi
  - ORG_URL=https://github.com/<votre-organisation>
  - TOKEN=<token-github-runner>
```

---

▶️ Installation & Lancement

》》 1. Construire l’image
```bash
docker-compose build
```

》》 2. Démarrer le runner
```bash
docker-compose up -d
```

》》 3. Vérifier le conteneur
```bash
docker ps
```

》》 4. Vérifier le runner dans GitHub
   - GitHub → Organisation → Settings → Actions → Runners  
Tu devrais voir ton runner apparaître.

---

#### 🛠️ Arrêter le runner
```bash
docker-compose down
```

---

#### ♻️ Redémarrage automatique
- Le runner redémarre automatiquement grâce à :

```yaml
restart: always
```

---

#### 📜 Licence
```text
Ce projet utilise la TheMadDoG.tmdg Personal License (TPL) ou toute licence que tu souhaites ajouter.
```

---

### 🙌 Auteur
- **The MadDoG.tmdg**
- GitHub :
   - https://github.com/teremuhamblin
   - github.com in Bing

---
