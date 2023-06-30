# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ✔️
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

// Importation du module Mongoose
const mongoose = require('mongoose');

// Connexion à la base de données MongoDB en utilisant l'URL stockée dans la variable d'environnement MONGODB_URI
mongoose
  .connect(process.env.MONGODB_URI, { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => console.log("Connexion à MongoDB réussie !")) // La connexion à MongoDB est réussie, affiche un message de succès
  .catch((err) => console.log("Connexion à MongoDB échouée :", err.message)); // La connexion à MongoDB a échoué, affiche l'erreur rencontrée

//////////////////////
// Définition de la fonction asynchrone "start" qui sera appelée pour démarrer le serveur
const start = async (): Promise<void> => {
  // Initialisation de la source de données
  await dataSource.initialize();
  // Construction du schéma GraphQL en utilisant la fonction "buildSchema" avec le resolver "WilderResolver"
  const schema = await buildSchema({ resolvers: [WilderResolver] });
  // Création d'une instance du serveur ApolloServer avec le schéma GraphQL
  const server = new ApolloServer({ schema });
  try {
    // Démarrage du serveur en écoutant sur le port spécifié
    const { url }: { url: string } = await server.listen({ port });
    console.log(`Server ready at ${url}`);
  } catch (err) {
    console.log("Error starting the server");
  }
};

// Appel de la fonction "start" en utilisant "void" pour ignorer la promesse retournée
void start();


### Utilisation dans un projet ✔️

[[lien du projet](...)](https://github.com/AnkaPieka/wilders-book-v2/tree/main)

Description : Projet de début d'alternance Wild

### Utilisation en production si applicable ❌

[[lien du projet](...)]

Description : 

### Utilisation en environement professionnel ❌ 

Description : pas de back en contexte pro

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
