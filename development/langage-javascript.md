# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️
- les normes `ecmascript` ✔️
- l'utilisation de l'`asynchrone` ✔️
- les spécifités du mot-clef `this` ✔️

## 💻 Je code en Javascript

### Un exemple de code commenté ✔️

```javascript
const getServices = async () => {
  try {
    // Étape 1: Effectuer une requête HTTP GET à l'URL spécifiée
    const res = await fetch("http://localhost:4000/services", {
      headers: {
        "Content-Type": "application/json",
        Accept: "application/json",
      },
    });

    // Étape 2: Analyser la réponse en tant que JSON
    const data = await res.json();

    // Étape 3: Définir les services avec les données récupérées
    return setServices(data);
  } catch (err) {
    // Étape 4: Gérer les erreurs en cas d'échec de la requête
    return console.log(err);
  }
};
```

### Utilisation dans un projet ✔️

[lien github](...)

Description : https://github.com/AnkaPieka/swappy-test/blob/main/src/Components/Agenda/index.jsx

### J'ai utilisé ce langage en production ✔️

Impossible de mettre le lien car c'était pour un travail et je n'ai plus accès au repo

Description :

### J'ai utilisé ce langage en environement professionnel ✔️

Description : utilisé au quotidien dans mon entreprise (ReactJS)

## 🌐 J'utilise des ressources

### Titre

- [lien](https://developer.mozilla.org/fr/)
- mdn

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
