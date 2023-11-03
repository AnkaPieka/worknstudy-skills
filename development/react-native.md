# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les différences et points communs entre du code react et du code react native ✔️
- ce que devient et comment est interprêté le code javascript dans une application react native ❌
- les avantages et inconvénients de react native ✔️
- la différence entre react native et expo ❌
- les principales briques qui composent react native (core components) ✔️
- comment écrire du style en react native ✔️
- comment est géré le layout en react native ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️


import { StyleSheet, Text, View, Pressable, TextInput, Image } from "react-native";
import { global } from "../Styles/global";
export default function LoginScreen({navigation}) {
  return(
    <View style={global.container}>
      <Image source ={require("../../././assets/logoEcoChallenge.png")}/>
      <Text style={global.colorWhite}>Email</Text>
      <TextInput style={global.input} value="" />
      <View style={{ marginBottom: 20 }}></View>
      <Text style={global.colorWhite}>Password</Text>
      <TextInput style={global.input} value="" />
      <View style={loginScreenStyles.btncontainer}>
      <Pressable style={global.button} onPress={() => navigation.navigate("")}>
        <Text style={global.colorGreen}>LOG IN</Text>
      </Pressable>
      <View style={{ marginRight: 150 }}></View>
      <Pressable style={loginScreenStyles.btnSignUp} onPress={() => navigation.navigate("SignUp")}>
        <Text style={global.colorWhite}>SIGN UP</Text>
      </Pressable>
      </View>
    </View>
  );;
const loginScreenStyles = StyleSheet.create({
  btncontainer: {
    margin:50,
    flexDirection: "row",
  },
  btnSignUp: {
    backgroundColor: 'transparent',
    display: "flex",
    alignItems: "center",
    borderRadius: 4,
    margin: 5,
    paddingLeft: 10,
    paddingRight: 10,
    paddingTop: 5,
    paddingBottom: 5,
    borderWidth: 1,
    borderColor: "#fff",
  }
});

### Utilisation dans un projet ✔️

[lien github] https://github.com/AnkaPieka/ecogeste-mobile

Description : projet de groupe Wild dédié à React Native

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

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
