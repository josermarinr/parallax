[mar1n]: https://mar1n.com/parallax/
![mar1n](https://i.postimg.cc/X7S6L6G1/parallax.gif)

### **pour voir l'implementation final [mar1n]**

# *la recette*
[x] trouver / faire l'illustration sur la quelle vous voudrais faire parallax
> *note: il faut reflechir de surposer les elements, pour cette example on va utiliser des planetes un background statique aussi le personage, et des textes. pour reflechir bien il faut savoir que chaque elemente doit etre continue du style final.* nous utilison l'illustration du freepik https://www.freepik.com/free-vector/hand-drawn-colorful-space-background_4792337.htm#page=1&query=astronaut&position=27

[x] déchiqueter chaque element et enregistrer chaq'un comme une image different.
>dans ce cas il y a 14 element plus le Bg
>1.![p1](https://i.postimg.cc/4dkKvNt4/planetP1.png) 2.![p2](https://i.postimg.cc/SKz2zznt/planetP2.png) 3.![p3](https://i.postimg.cc/4NB9CGCw/planetP3.png) 4.![p4](https://i.postimg.cc/hjTdN7g7/planetP4.png) 5.![p5](https://i.postimg.cc/j2y46FCm/planetP5.png) 6.![p6](https://i.postimg.cc/wvZwQN2y/planetP6.png) 7.![pb1](https://i.postimg.cc/Px26pcp4/planteB1.png) 8.![pb2](https://i.postimg.cc/1X3jvPh2/planteB2.png) 9.![pb3](https://i.postimg.cc/3w2VRnFS/planteB3.png) 10.![pb4](https://i.postimg.cc/KvY6N7mj/planteB4.png) 11.![pb6](https://i.postimg.cc/jScJbrGZ/planteB6.png) 12.![pb7](https://i.postimg.cc/qv4CS7ZN/planteB7.png) 13.![pb8](https://i.postimg.cc/3Nkkj4Rq/planteB8.png) 14.![personage](https://i.postimg.cc/8cc6yXyt/astronaut.png)

[x] implementer sur le site.
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
   <!--votre style -->

    <link rel="stylesheet" href="style.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/parallax/3.1.0/parallax.min.js"></script>
    <!--le script parallax.js -->
    <title>title</title>
</head>
<body>
    <div class="container">
        <ul data-relative-input="true" id="scene" class="scene">

        </ul>
    </div>
</body>
```
>dans notre html il faut faire ** div ** avec la classe * conteneur * et un ** ul ** avec la classe * scène * et une id * scène * et ajuter data-relative-input = "true"
```javascript
var scene = document.getElementById('scene');
var parallaxInstance = new Parallax(scene, {
    relativeInput: true});

parallaxInstance.friction(0.2, 0.2);
```
>tout en bas faire une etiquete script. Dans ce script on va  faire deux variables une qui s'appelle scene, ou comme vous voudrais, qui va identifier le id scene, et autre qui s'appelle parallaxInstance où on va creer un nouveau Parallax avec les instance scene et le relativeInput true, dans ce variable on peut editer la friction qui va avoir chaque element avec 0.2 et 0.2
```html
<!-- text -->
<li class="layer" id="subtitle" data-depth="-0.10">
    <h3 class="subtitle">prochainement sera disponible mon portfolio</h3>
</li>
<!-- end -->
<!-- little planet -->
<li class="layer" id="planetp1" data-depth="0.20">
    <img src="https://i.postimg.cc/4dkKvNt4/planetP1.png" class="planetp1" alt="" srcset="">
</li>
```
>ici on fait les element de la liste, avec chaque element on l'identifie avec la classe "layer", et le id qui peut differencier une des autres, le "data-depth" est la quantite de deplacement que l'element va avoir quand le mouse ou le doigt passent pour le scran, on va faire parait avec tous les elements suivantes.. c'est votre devoir :smile: :smile:
```css
@import url("https://fonts.googleapis.com/css?family=Fredoka+One&display=swap" );
@import url("https://fonts.googleapis.com/css?family=Russo+One&display=swap" );
@import url("https://fonts.googleapis.com/css?family=Notable&display=swap");

body{
    margin: 0;
   padding: 0;
    font-size: 16px;
}
.container{
    width: 100%;
    height: 100vh;
    overflow: hidden;
    background: url(https://i.postimg.cc/t4s7LVNC/bg.png) no-repeat;
    background-size: cover;
    background-attachment: fixed;
}
.mixBlnd
{
       background-blend-mode: screen;
}

.scene,
.layer {
  display: block;
  height: 100%;
  width: 100%;
  padding: 0;
  margin: 0; }

.scene {
  min-height: 460px;
  position: relative;
  overflow: hidden; }

.layer {
  position: absolute; }

.astronaut{
  width: 50%;
  position: absolute;
  top: 30%;
  left: 20%;
}
#title{
  color: #ffffff;
  text-align: center;
  align-content: center;
  align-items: center;
  font-size: 20px;
  z-index: -7;

}
```
>alors, pour le style on doit mettre 0 margin et padding 0; le type de police que vous utilisez sera ce que vous convient :simple_smile:. pour le "container" on le utilise pour positioner le "Bg" sans repetition et avec un hauteur de 100vh et le 100% du longeur du scran. la classe "scene" et "layer" on le donne le heuteur de 100% du container et 100% de longeur; pour les "layer" on le donne position absolute et on commence a positioner chaque elemente dans le endroit de notre choix, pour le astronaut on utilise le milieux avec le 50% de dimention, le title on le donne position derrier au astronaut et aussi pour  autres elements.

resultat [mar1n]. c'est le moment de faire rouler votre imagination :smile: :smile: :smile: :smile:
