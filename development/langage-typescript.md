# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ✔️
- les classes et les decorators ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

import { gql, useMutation } from "@apollo/client";
import blank_profile from "../assets/profile.png";
import Skill, { ISkillProps } from "./Skill";
import { GET_WILDERS_AND_SKILLS } from "../components/HomePage";

// Interface décrivant les propriétés d'un Wilder
export interface IWilderProps {
  name: string;
  id: number;
  skills: ISkillProps[];
}

// Définition de la requête de mutation DELETE_WILDER en utilisant gql pour le langage de requête GraphQL
const DELETE_WILDER = gql`
  mutation Mutation($deleteWilderId: String!) {
    deleteWilder(id: $deleteWilderId)
  }
`;

// Composant fonctionnel Wilder qui affiche les détails d'un Wilder
const Wilder = ({ name, id, skills }: IWilderProps) => {
  // Utilisation du hook useMutation pour effectuer la mutation DELETE_WILDER
  const [deleteWilder, { data, loading, error }] = useMutation(DELETE_WILDER, {
    refetchQueries: [GET_WILDERS_AND_SKILLS], // Liste des requêtes à recharger après la mutation
  });

  // Gestion des états de chargement et d'erreur
  if (loading) {
    return <p>Loading</p>; // Affiche un message de chargement si la requête est en cours
  }
  if (error) {
    console.log(error); // Affiche l'erreur dans la console en cas d'échec de la requête
    return <p>Error</p>; // Affiche un message d'erreur si la requête a échoué
  }
  
  console.log(data); // Affiche les données renvoyées par la mutation dans la console

  // Rendu du composant Wilder avec les détails du Wilder
  return (
    <>
     ...
    </>
  );
};

export default Wilder; // Exportation du composant Wilder par défaut

### Utilisation dans un projet ✔️

[lien github] : https://github.com/AnkaPieka/wilders-book-v2

Description : Premier projet TS + GraphQL avec la Wild

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description : projet d'entreprise en JS

## 🌐 J'utilise des ressources

### Titre

- [lien](https://www.typescriptlang.org/docs/)
- Documentation TS officielle

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
