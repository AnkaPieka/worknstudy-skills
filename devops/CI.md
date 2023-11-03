# Integration continue

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les enjeux de l'integration continue ✔️
- la mise en place d'une github action ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

name: client-tests-workflow

# Déclenche le workflow à chaque demande d'extraction (pull request)
on: pull_request

jobs:
  # Job pour les tests backend
  test-backend:
    # Environnement d'exécution (dans ce cas, une machine Ubuntu)
    runs-on: ubuntu-latest

    # Étapes à suivre dans ce job
    steps:
      # Étape 1 : Vérification du code
      - name: Check out code
        uses: actions/checkout@v2
        # Cette étape utilise l'action "actions/checkout@v2" pour cloner le code source dans l'environnement d'exécution.

      - name: Goto back and run tests
        # Se déplacer dans le dossier "back",installer les dépendances npm puis exécuter un test en utilisant la commande "npm test ./tests/userresolver.test.ts".
        run: cd back && npm i && npm test ./tests/userresolver.test.ts


### Utilisation dans un projet ✔️

[lien github] https://github.com/AnkaPieka/ecogeste/tree/US-16_CI

Description : la branche US16 dédiée à la CI

### Utilisation en production si applicable❌ 

[lien du projet](...)

Description :

### Utilisation en environnement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

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
