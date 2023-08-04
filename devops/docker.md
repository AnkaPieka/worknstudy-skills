# Docker

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la création d'une image docker ❌
- l'éxécution d'un container ❌
- l'orchestration de containers avec docker-compose ❌ 


## 💻 J'utilise

### Un exemple personnel commenté ✔️

// Utilisation de l'image "node:lts-alpine" comme image de base
FROM node:lts-alpine

// Installation des dépendances nécessaires pour certains modules NPM (node-pre-gyp)
RUN apk add make g++ python3 git
RUN npm i -g node-pre-gyp

// Définition du répertoire de travail à "/app" dans l'image
WORKDIR /app

// Copie du fichier package.json et package-lock.json dans le répertoire de travail
COPY package.json package.json
COPY package-lock.json package-lock.json

// Installation des dépendances spécifiées dans le fichier package.json
RUN npm install

// Copie du fichier tsconfig.json dans le répertoire de travail
COPY tsconfig.json tsconfig.json

// Copie du répertoire "src" (contenant le code source de l'application) dans le répertoire de travail
COPY src src

// Commande "npm start" pour lancer l'application
CMD npm start


### Utilisation dans un projet ✔️

[lien github] (https://github.com/AnkaPieka/ecogeste)

Description : Projet de groupe de la Wild, en cours

### Utilisation en production si applicable❌ 

[lien du projet](...)

Description :

### Utilisation en environement professionnel ✔️

Description : J'utilise Docker en milieu professionnel, principalement vie Docker Desktop, pour lancer l'application et travailler, car nous utilisons tous des set up différents.

## 🌐 J'utilise des ressources

### Titre

- [lien](https://docs.docker.com/get-started/)
- Documentation officielle de Docker

- https://docs.google.com/presentation/d/11fKYh_sZMNqwE0o44mWv5nA4nUOPJ93n-TAbNkBTamc/edit#slide=id.p
- Slides résumé sur Docker Compose

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
