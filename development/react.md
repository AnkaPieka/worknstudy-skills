# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ✔️
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

// Importation des icônes ArrowBackIosNewIcon et ArrowForwardIosIcon depuis le module "@mui/icons-material"
import ArrowBackIosNewIcon from "@mui/icons-material/ArrowBackIosNew";
import ArrowForwardIosIcon from "@mui/icons-material/ArrowForwardIos";
// Importation des composants Button et IconButton depuis le module "@mui/material"
import { Button, IconButton } from "@mui/material";
// Importation des fonctions addWeeks, getWeek, getYear et subWeeks depuis le module "date-fns"
import { addWeeks, getWeek, getYear, subWeeks } from "date-fns";
// Importation des modules React et useState depuis la bibliothèque "react"
import React, { useMemo, useState } from "react";
// Importation de la fonction generateWeek depuis le fichier "../../helpers"
import { generateWeek } from "../../helpers";
// Importation du composant Week depuis le fichier "../Week"
import Week from "../Week";

import "./styles.scss";

function Agenda() {
  // Déclaration de l'état currentDate avec la fonction useState, initialisée avec la date courante
  let [currentDate, setCurrentDate] = useState(new Date());

  // Utilisation du hook useMemo pour générer la semaine courante basée sur la currentDate
  let currentWeek = useMemo(() => generateWeek(currentDate)(), [currentDate]);

  // Fonction pour changer la semaine affichée en avant ou en arrière avec une animation de glissement
  const changeWeek = (backOrForth, classForSliderAnimation) => {
    // Sélection de l'élément à faire glisser
    let elementToSlide = document.querySelector(`.${classForSliderAnimation}`);

    // Ajout des classes pour l'animation de glissement
    elementToSlide.classList.add("slide-out-bck-center");

    // Mise à jour de la currentDate en fonction de la direction (en avant ou en arrière)
    if (backOrForth === "forth") {
      setCurrentDate(addWeeks(currentDate, 1));
    } else {
      setCurrentDate(subWeeks(currentDate, 1));
    }

    elementToSlide.classList.add("slide-in-fwd-center");

    // Suppression des classes d'animation après un délai
    setTimeout(() => {
      elementToSlide.classList.remove("slide-out-bck-center");
      elementToSlide.classList.remove("slide-in-fwd-center");
    }, 2000);
  };

  // Fonction pour revenir à la date du jour
  const goBackToToday = () => {
    setCurrentDate(new Date());
  };

  // Rendu du composant Agenda
  return (
  return (
        <div id="agenda-container">
            <section id="week-topbar">
                <div className="week-changer">
                    <IconButton
                        onClick={() => changeWeek("back", "slider-animation")}
                        style={{ cursor: "pointer" }}
                    >
                        <ArrowBackIosNewIcon fontSize="small" />
                    </IconButton>

                    <div>
                        Semaine {getWeek(currentDate)} - {getYear(currentDate)}
                    </div>

                    <IconButton
                        onClick={() => changeWeek("forth", "slider-animation")}
                        style={{ cursor: "pointer" }}
                    >
                        <ArrowForwardIosIcon fontSize="small" />
                    </IconButton>
                </div>

                <Button onClick={() => goBackToToday()} variant="contained">
                    Date du jour
                </Button>
            </section>

            <div className="slider-animation">
            //utilisation du composant week avec passage de currentWeek en prop
                <Week currentWeek={currentWeek} />
            </div>
        </div>
    );
}
//////////////////////////

### Utilisation dans un projet ✔️

[lien github] https://github.com/AnkaPieka/swappy-test/tree/main

Description : test technique pour le poste en alternance

### Utilisation en production si applicable ✔️

[lien du projet] NC

Description : ancien projet professionnel, je ne peux pas partager le repo

### Utilisation en environement professionnel ✔️ 

Description: deux app en React, l'une en React Ts pur et l'autre sous React TS avec NextTS

## 🌐 J'utilise des ressources

### Titre

- [lien](https://react.dev/)
- Doc officielle react

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
