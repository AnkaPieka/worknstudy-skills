# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️
- les besoins auxquels répond GraphQL ✔️
- la définition d'un schéma ❌ / ✔️ (en cours)
- Query ❌ 
- Mutation ❌ 
- Subscription ❌

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

import { Field, ObjectType } from 'type-graphql';
import { Column, Entity, ManyToOne, PrimaryGeneratedColumn } from 'typeorm';
import { User } from './User';
import { Time } from './interfaces';

@ObjectType() // Décorateur pour définir cette classe comme un type GraphQL
@Entity() // Décorateur pour indiquer que cette classe est une entité dans TypeORM
export class Challenge {
  @Field() // Décorateur pour exposer ce champ comme un champ GraphQL
  @PrimaryGeneratedColumn() // Décorateur pour indiquer que c'est une clé primaire générée automatiquement
  id: number;

 ...
 
  @Field(() => User) // Décorateur avec le type User
  @ManyToOne(() => User, (user) => user.challenges, { // Décorateur pour indiquer une relation Many-to-One avec User
    onDelete: 'CASCADE', // Indique que lorsque l'utilisateur est supprimé, les challenges associés sont également supprimés
  })
  user: User;
}


### Utilisation dans un projet ❌ / ✔️

[lien du projet](https://github.com/AnkaPieka/wilder-book-TS/tree/main/server)

Description : 

### Utilisation en production si applicable❌

[lien github](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- [lien](https://graphql.org/)
- Doc graphQL

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
