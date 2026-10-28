📁 STRUCTURE DU PROJET

Ce dépôt contient un runner GitHub Actions auto‑hébergé, packagé en Docker et prêt pour une utilisation au niveau d’une organisation.

Arborescence

```text
├── README.md
├── .github/
│     └── .gitkeep
├── docs/
│     └── .gitkeep
├── .gitignore
├── LICENSE
├── dockerfile
├── dck-compose.yml
├── entrypoint.sh
└── runner-workdir/
````

Description des éléments

- **README.md** — Guide d’utilisation du runner.
- **.github/**
   - — Métadonnées GitHub, workflows ou templates (placeholder).
- **docs/**
   - — Documentation additionnelle (placeholder).
- **.gitignore**
   - — Fichiers ignorés par Git.
- **LICENSE** — Licence du projet.
- dockerfile — Image du runner GitHub Actions.
- **dck-compose.yml** — Déploiement du runner via Docker Compose.
- **entrypoint.sh** — Script d’initialisation du runner.
- **runner-workdir/** — Dossier de travail persistant pour les jobs.

Objectif

Fournir une structure claire, légère et extensible pour déployer un runner GitHub Actions d’organisation.

---
