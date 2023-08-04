# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les verbes HTTP ✔️
- les statuts HTTP ✔️
- les endpoints ✔️
- CORS ✔️
- la nomenclature recommandée pour les routes ✔️

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

// Importation du module "express" pour créer des routes
const express = require("express");
// Création d'un routeur pour gérer les différentes routes
const router = express.Router();

// Importation du contrôleur "ArgonauteCtrl" qui contient les fonctions pour gérer les actions relatives aux Argonautes
const ArgonauteCtrl = require("../controllers/argonautes");

// Définition d'une route HTTP POST pour créer un nouvel Argonaute
// Lorsque cette route est appelée avec une requête POST sur "/argonautes",
// le contrôleur "createArgonaute" sera exécuté pour traiter la demande
router.post("/argonautes", ArgonauteCtrl.createArgonaute);

// Définition d'une route HTTP GET pour récupérer la liste de tous les Argonautes
// Lorsque cette route est appelée avec une requête GET sur "/argonautes",
// le contrôleur "getAllArgonautes" sera exécuté pour traiter la demande
router.get("/argonautes", ArgonauteCtrl.getAllArgonautes);

// Exportation du routeur contenant les routes définies
// Cela permettra d'utiliser ces routes dans d'autres parties de l'application
module.exports = router;


### Utilisation dans un projet ✔️

[lien github](https://github.com/AnkaPieka/wild-code-test/tree/main)

Description :

Test d'entrée à la Wild Code School

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ✔️

Description : Dans mon poste précédent, l'app était sous React / API REST

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
