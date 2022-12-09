# TIPS avant de commencer:

Lors d'un merge eviter d'etre sur sass et scss... choissisez l'un ou l'autre pour eviter tout type de conflit.

--------------------------------------------------
# reminder_sass
Pour le téléchargement de bootstrap: 
```
-npm init

-npm install bootstrap
```


Pour le téléchargement de Fontawesome:
```
-npm install --save @fortawesome/fontawesome-free
```


---------------------------------------------------

```Dans votre fichier app.scss```
```
// Les imports classiques

@import "./fonts";

@import "./variables";

//Import de fontawesome

$fa-font-path : "../../node_modules/@fortawesome/fontawesome-free/webfonts";

@import "../../node_modules/@fortawesome/fontawesome-free/scss/fontawesome.scss";

@import "../../node_modules/@fortawesome/fontawesome-free/scss/solid.scss";

@import "../../node_modules/@fortawesome/fontawesome-free/scss/brands.scss";

@import "../../node_modules/@fortawesome/fontawesome-free/scss/regular.scss";

//import de Bootstrap

@import "../../node_modules/bootstrap/scss/bootstrap.scss";
```
---------------------------------------------------


```Dans votre fichier "_variables.scss```
```

//import

@import "../../node_modules/bootstrap/scss/functions";

@import "../../node_modules/bootstrap/scss/variables";

//* Création de variable SASS

$couleurRouge : #f71b09;

//* Création de Spacer 

$spacer : 5px;

$spacers : map-merge($spacers, (
    0 : 0px ,
    1 : $spacer*1 ,
    2 : $spacer*2 ,
    3 : $spacer*3 ,
    4 : $spacer*4 ,
    5 : $spacer*5 ,
));

$couleur-perso : (
    "orange" : rgb(207, 130, 22),
    "rose"   : #df46c8,
);

$theme-colors : map-merge($theme-colors , $couleur-perso);
```
----------------------------------------------------

```On oublie pas dans son index.html le script js de bootstrap```

```
<script src="./node_modules/bootstrap/dist/js/bootstrap.bundle.js"></script>
```
