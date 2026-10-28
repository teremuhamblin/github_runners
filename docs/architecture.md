# ARCHITECTURE DU RUNNER

Ce projet implémente un runner GitHub Actions auto‑hébergé basé sur une architecture simple, stable et entièrement conteneurisée.

## Vue d’ensemble

- **Dockerfile** construit l’environnement du runner.
- **entrypoint.sh** configure et démarre le runner.
- **docker-compose** orchestre le service.
- **runner-workdir** assure la persistance des tâches.

## Composants

### 1. Conteneur Runner
- OS : Ubuntu 22.04
- Dépendances minimales (curl, tar, git, libicu)
- Téléchargement du runner GitHub officiel
- Exécution en utilisateur non‑root (`runner`)

### 2. Script d’entrée
- Configuration automatique du runner
- Mode non‑interactif
- Enregistrement auprès de l’organisation GitHub
- Lancement du service

### 3. Docker Compose
- Déploiement du conteneur
- Redémarrage automatique
- Accès au socket Docker pour les workflows
- Variables d’environnement pour l’URL et le token

## Flux d’exécution

1. Build de l’image via Dockerfile  
2. Initialisation via entrypoint.sh  
3. Enregistrement du runner  
4. Exécution continue des workflows GitHub Actions  

## Objectif

Offrir une architecture fiable, reproductible et facile à maintenir pour un runner GitHub Actions d’organisation.
