
## Informations 

- [Tutoriel CSS](#Tutoriel-CSS)
  
- [Sélecteurs CSS](#Sélecteurs-CSS)
  
- [Comment ajouter du CSS](#Comment-ajouter-du-CSS)
  
- [Couleurs CSS](#Couleurs-CSS)

- [Couleurs CSS HEX](#Couleurs-CSS-HEX)
  
- [Arrière-plans CSS](#Arrière-plans-CSS)

- [Image d’arrière-plan CSS](#Image-d’arrière-plan-CSS)

- [Répetition de l'image d'arrière-plan CSS ](#Répétition-de-l’image-d’arrière-plan-CSS)

- [Bordures CSS](#Bordures-CSS)

- [Largeur de la bordure CSS](#Largeur-de-la-bordure-CSS)

- [Couleur de la bordure CSS](#Couleur-de-la-bordure-CSS)

- [Marges CSS](#Marges-CSS)

- [Tableaux CSS](#Tableaux-CSS)

- [Taille du tableau CSS](#Taille-du-tableau-CSS)


-----------------------------------------------------------------------------------------------
# Tutoriel CSS



## Exemples dans chaque chapitre
Ce tutoriel CSS contient des centaines d’exemples CSS.

Avec notre éditeur en ligne, vous pouvez modifier le CSS et cliquer sur un bouton pour afficher le résultat.

    body {
      background-color: lightblue;
    }

    h1 {
      color: white;
      text-align: center;
    }

    p {
      font-family: verdana;
      font-size: 20px;
    }
![image](https://github.com/user-attachments/assets/15fa09e4-71d8-4781-980a-12ba070d1712)


-----------------------------------------------------------------------------------------------
# Sélecteurs CSS
Un sélecteur CSS sélectionne le ou les éléments HTML que vous envie de style.


## Le sélecteur d’élément CSS
Le sélecteur d’éléments sélectionne les éléments HTML en fonction du nom de l’élément.

Ici, tous les éléments `<p>` de la page seront aligné au centre, avec une couleur
de texte rouge :

    p {
      text-align: center;
      color: red;
    }
![image](https://github.com/user-attachments/assets/1e255dfa-8ed9-4e36-8f51-b3b743e4c4b2)


## Le sélecteur d’id CSS
Le sélecteur id utilise l’attribut id d’un élément HTML pour sélectionner un élément spécifique.

L’id d’un élément est unique au sein d’une page, donc le sélecteur d’id est habituel Sélectionnez un élément unique !

Pour sélectionner un élément avec un id spécifique, écrivez un caractère dièse `(#)`, suivi de ID de l’élément.

La règle CSS ci-dessous sera appliquée à l’élément HTML avec id="`para1` » :

    #para1 {
      text-align: center;
      color: red;
    }
![image](https://github.com/user-attachments/assets/80b88dc5-bcb4-4773-b70f-16bce6ff200b)



## Le sélecteur de classe CSS
Le sélecteur de classe sélectionne les éléments HTML avec un attribut de classe spécifique.

Pour sélectionner des éléments avec une classe spécifique, écrivez un point `(.)`, suivi de l’icône nom de la classe.

Dans cet exemple, tous les éléments HTML avec class="center » seront rouges et alignés au centre :

    .center {
      text-align: center;
      color: red;
    }
![image](https://github.com/user-attachments/assets/481ea148-40d3-4c08-baf6-1249d2762199)



Vous pouvez également spécifier que seuls des éléments HTML spécifiques doivent être affectés par une classe.

Dans cet exemple, seuls les éléments `<p>` avec class="`center` » seront rouge et aligné au centre :

    p.center {
      text-align: center;
      color: red;
    }
![image](https://github.com/user-attachments/assets/53b696c4-6dc3-4bae-b74a-aad5bfdbc122)


Éléments HTML peut également faire référence à plus d’une classe.

Dans cet exemple, l’élément `<p>` sera stylisé selon `class="center `» et à `class="large` » :

    <p class="center large">This paragraph refers to two classes.</p>
![image](https://github.com/user-attachments/assets/778c8652-bb01-4af0-86f2-62edeaac71fb)


## Le sélecteur universel CSS
Le sélecteur universel (*) sélectionne tous les fichiers HTML éléments sur la page.

La règle CSS ci-dessous affectera tous les éléments HTML de la page :

    * {
      text-align: center;
      color: blue;
    }
![image](https://github.com/user-attachments/assets/0fd1ab98-7697-42fd-b9d6-a06ae28d7395)


## Le sélecteur de regroupement CSS
Le sélecteur de regroupement sélectionne tous les éléments HTML avec le même style Définitions.

Regardez le code CSS suivant (les éléments h1, h2 et p ont les mêmes définitions de style) :

    h1 {
      text-align: center;
      color: red;
    }

    h2 {
      text-align: center;
      color: red;
    }

    p {
      text-align: center;
      color: red;
    }
    
![image](https://github.com/user-attachments/assets/171f2575-cdaa-45a1-a4e7-e301a5e54d8f)

Il sera préférable de regrouper les sélecteurs, pour minimiser le code.

Pour regrouper des sélecteurs, séparez chaque sélecteurs par une virgule.


Dans cet exemple, nous avons regroupé les sélecteurs du code ci-dessus :

    h1, h2, p {
      text-align: center;
      color: red;
    }
![image](https://github.com/user-attachments/assets/171f2575-cdaa-45a1-a4e7-e301a5e54d8f)
    
-----------------------------------------------------------------------------------------------

# Comment ajouter du CSS

Trois façons d’insérer du CSS :

- CSS externe
- CSS interne
- CSS en ligne

## CSS externe
Avec un feuille de style externe, vous pouvez changer l’apparence d’un site Web entier en modifiant Un seul fichier !

Chaque page HTML doit inclure une référence au fichier de feuille de style externe à l’intérieur l’élément <lien> à l’intérieur de la section de la tête.

Les styles externes sont définis dans l’élément `<link>` dans
la section `<head>` d’une page HTML :

    <!DOCTYPE html>
    <html>
    <head>
    <link rel="stylesheet" href="mystyle.css">
    </head>
    <body>

    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>

    </body>
    </html>



Une feuille de style externe peut être écrite dans n’importe quel éditeur de texte et doit être enregistrée avec une extension .css.

Le fichier .css externe ne doit pas contenir de balises HTML.
Voici à quoi ressemble le fichier `« mystyle.css »` :
`« mystyle.css »`

    body {
        background-color: lightblue;
    }

    h1 {
      color: navy;
      margin-left: 20px;
    }

## CSS interne
Une feuille de style interne peut être utilisée si une seule page HTML a un style unique.

Le style interne est défini à l’intérieur de l’élément  `<style>`, à l’intérieur de la tête section.
Les styles internes sont définis dans l’élément `<style>` dans la section <head> d’une page HTML :

    <!DOCTYPE html>
    <html>
    <head>
    <style>
    body {
      background-color: linen;
    }

    h1 {
      color: maroon;
      margin-left: 40px;
    }
    </style>
    </head>
    <body>

    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>

    </body>
    </html>

## CSS en ligne
Un style en ligne peut être utilisé pour appliquer un style unique à un seul élément.

Pour utiliser des styles en ligne, ajoutez l’attribut style à l’élément approprié. Le style peut contenir n’importe quelle propriété CSS.
Les styles en ligne sont définis dans l’attribut `« style »` de la élément:

    <!DOCTYPE html>
    <html>
    <body>

    <h1 style="color:blue;text-align:center;">This is a heading</h1>
    <p style="color:red;">This is a paragraph.</p>

    </body>
    </html>

## Plusieurs feuilles de style
Si certaines propriétés ont été définies pour le même sélecteur (élément) dans différentes feuilles de style, La valeur de la dernière feuille de style lue sera utilisée.
Supposons qu’une feuille de style externe ait le style suivant pour l’élément `<h1>`:


      h1 {
          color: navy;
        }



Ensuite, supposons qu’une feuille de style interne ait également le style suivant pour l’élément `<h1>` :


    h1 {
      color: orange;   
    }


Si le style interne est défini après le lien vers la feuille de style externe, les éléments `<h1>` seront « orange » :

    <head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    <style>
    h1 {
      color: orange;
    }
    </style>
    </head>

Cependant, si le style interne est défini avant le lien vers la feuille de style externe, les éléments `<h1>` seront « marine » :

    <head>
    <style>
    h1 {
      color: orange;
    }
    </style>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    </head>

----------------------------------------------------------------------------------------------


# Couleurs CSS

## Couleur d’arrière-plan CSS

Vous pouvez définir la couleur d’arrière-plan des éléments HTML :

    <h1 style="background-color:DodgerBlue;">Hello World</h1>
    <p style="background-color:Tomato;">Lorem ipsum...</p>


![image](https://github.com/user-attachments/assets/b5aa0e94-90f7-48fe-a1cd-e1d7fe5ebca1)


## Couleur du texte CSS

Vous pouvez définir la couleur du texte :

        <h1 style="color:Tomato;">Hello World</h1>
        <p style="color:DodgerBlue;">Lorem ipsum...</p>
        <p style="color:MediumSeaGreen;">Ut wisi enim...</p>


![image](https://github.com/user-attachments/assets/6f8cb308-aece-429a-894a-368edad10799)



## Couleur de la bordure

Vous pouvez définir la couleur des bordures :

    <h1 style="border:2px solid Tomato;">Hello World</h1>
    <h1 style="border:2px solid DodgerBlue;">Hello World</h1>
    <h1 style="border:2px solid Violet;">Hello World</h1>


![image](https://github.com/user-attachments/assets/6f91f68b-b4b5-4d98-a48f-b7ef556565d0)


## Valeurs de couleur

En HTML, les couleurs peuvent également être spécifiées à l’aide de `valeurs RVB`, de `valeurs HEX`, de `HSL valeurs`, `valeurs RGBA` et `valeurs HSLA`.

La couleur d’arrière-plan des trois éléments `<div>` suivants est définie avec `RVB` : Valeurs `HEX` et `HSL` :

    <h1 style="background-color:rgb(255, 99, 71);">...</h1>
    <h1 style="background-color:#ff6347;">...</h1>
    <h1 style="background-color:hsl(9, 100%, 64%);">...</h1>

    <h1 style="background-color:rgba(255, 99, 71, 0.5);">...</h1>
    <h1 style="background-color:hsla(9, 100%, 64%, 0.5);">...</h1>


![image](https://github.com/user-attachments/assets/d1cf1b2a-e06c-40d5-a891-72fd1ac328ac)

------------------------------------------------------------------------------------------------



# Couleurs CSS HEX

## Valeur HEX à 3 chiffres
Parfois, vous verrez un code hexadécimal à 3 chiffres dans la source CSS.

Le code hexadécimal à 3 chiffres est un raccourci pour certains codes hexadécimaux à 6 chiffres.

Le code hexadécimal à 3 chiffres se présente sous la forme suivante :

#RVB

où are, g et b représentent les composantes rouge, verte et bleue avec des valeurs comprises entre 0 et f.

Le code hexadécimal à 3 chiffres ne peut être utilisé que lorsque les deux valeurs (RR, GG et BB) sont identiques pour chaque composant. Donc, si nous avons #ff00cc, cela peut s’écrire comme suit : #f0c.

En voici un exemple :

        body {
          background-color: #fc9; /* same as #ffcc99 */
        }

        h1 {
          color: #f0f; /* same as #ff00ff */
        }

        p {
          color: #b58; /* same as #bb5588 */
        }

![image](https://github.com/user-attachments/assets/b18e8c8e-3d9e-467a-be06-0afc442ab5b1)



---------------------------------------------------------------------------------------------
# Arrière-plans CSS

Les propriétés d’arrière-plan CSS sont utilisées pour ajouter des effets d’arrière-plan pour les éléments.


les propriétés d’arrière-plan CSS suivantes :
- `background-color`
- `background-image`
- `background-repeat`
- `background-attachment`
- `background-position`
- `background` (propriété abrégée)


## Couleur d’arrière-plan CSS

La propriété spécifie la couleur d’arrière-plan d’un élément.`background-color`

La couleur d’arrière-plan d’une page est définie comme suit :

    body {
      background-color: lightblue;
    }
![image](https://github.com/user-attachments/assets/5343b8bf-cd01-4e7c-9f20-84c912385054)


Avec CSS, une couleur est le plus souvent spécifiée par :

un nom de couleur valide - comme « rouge »
`une valeur HEX` - comme « #ff0000 »
`une valeur RVB` - comme « rgb(255,0,0) »
Regardez les valeurs de couleur CSS pour une Liste des valeurs de couleur possibles.

## Autres éléments
Vous pouvez définir la couleur d’arrière-plan de n’importe quel élément HTML :

Ici, les éléments `<h1>`, `<p>` et `<div>` auront des couleurs d’arrière-plan différentes :

    h1 {
      background-color: green;
    }

    div {
      background-color: lightblue;
    }

    p {
      background-color: yellow;
    }
![image](https://github.com/user-attachments/assets/b49415e5-9d11-434c-8424-b24adf075ada)



# Opacité / Transparence
La propriété spécifie l’opacité/transparence d’un élément. Il peut prendre une valeur comprise entre 0,0 et 1,0. Plus la valeur est faible, plus la transparence est grande :opacity

    div {
      background-color: green;
      opacity: 0.3;
    }
![image](https://github.com/user-attachments/assets/970b5194-8737-4cad-8ce1-fcafaccfc0b6)




# Image d’arrière-plan CSS

## Image-arrière-plan CSS
La propriété spécifie une image à utiliser comme arrière-plan d’un élément.`background-image`

Par défaut, l’image est répétée de sorte qu’elle couvre l’ensemble de l’élément.

Définissez l’image d’arrière-plan d’une page :

    body {
    background-image: url("paper.gif");
    }
![image](https://github.com/user-attachments/assets/13e87d5b-7eed-4a3f-a4b3-385951e69a52)


Cet exemple montre une mauvaise combinaison de texte et d’image d’arrière-plan. Le texte est Difficilement lisible :

    body {
    background-image: url("bgdesert.jpg");
    }
![image](https://github.com/user-attachments/assets/32767551-1438-4719-9859-5475659c1dd5)



L’image d’arrière-plan peut également être définie pour des éléments spécifiques, comme l’élément <p> :

    p {
    background-image: url("paper.gif");
    }
![image](https://github.com/user-attachments/assets/f35b9d08-05ad-42ca-980f-be4ce3201d5f)




# Répétition de l’image d’arrière-plan CSS

## CSS background-repeat
Par défaut, la propriété répète une image à la fois horizontalement et verticalement.`background-image`

Certaines images ne doivent être répétées qu’horizontalement ou verticalement, sinon elles auront l’air étranges, comme ceci :

    body {
    background-image: url("gradient_bg.png");
    }
![image](https://github.com/user-attachments/assets/de3f1978-9d0e-4172-8270-004dcea9031c)


Si l’image ci-dessus n’est répétée qu’horizontalement (), l’arrière-plan aura l’air mieux: `background-repeat`: `repeat-x`;

    body {
    background-image: url("gradient_bg.png");
    background-repeat: repeat-x;
    }
![image](https://github.com/user-attachments/assets/02dd9f65-e497-4efa-9c66-5c842cd8cdbc)


## CSS background-repeat : pas de répétition
L’affichage de l’image d’arrière-plan une seule fois est également spécifié par la propriété :` background-repeat`

N’affichez l’image d’arrière-plan qu’une seule fois :

    body {
    background-image: url("img_tree.png");
    background-repeat: no-repeat;
    }
![image](https://github.com/user-attachments/assets/e17788f9-b8ae-4667-9ac3-fb6c641d92a1)


Dans l’exemple ci-dessus, l’image d’arrière-plan est placée au même endroit que le texte. Nous voulons changer la position de l’image, afin qu’elle ne dérangez trop le texte.

## CSS background-position
La propriété est utilisée pour Spécifiez la position de l’image d’arrière-plan.`background-position`

Positionnez l’image d’arrière-plan dans le coin supérieur droit :

    body {
    background-image: url("img_tree.png");
    background-repeat: no-repeat;
    background-position: right top;
    }

![image](https://github.com/user-attachments/assets/5323d36a-e5c3-4c34-9e69-42e8db416a8f)


  
# Bordures CSS
Les propriétés CSS border vous permettent de spécifier le style, largeur et couleur de la bordure d’un élément.

## Style de bordure CSS

La propriété spécifie le type de bordure à afficher.border-style

Les valeurs suivantes sont autorisées :

- `dotted` - Définit une bordure en pointillés
- `dashed` - Définit une bordure en pointillés
- `solid` - Définit une bordure unie
- `double` - Définit une double bordure
- `groove` - Définit une bordure rainurée en 3D. L’effet dépend de la valeur de la couleur de la bordure
- `ridge` - Définit une bordure striée 3D. L’effet dépend de la valeur de la couleur de la bordure
- `inset` - Définit une bordure en encart 3D. L’effet dépend de la valeur de la couleur de la bordure
- `outset` - Définit une bordure de départ 3D. L’effet dépend de la valeur de la couleur de la bordure
- `none` - Ne définit aucune bordure
- `hidden` - Définit une bordure cachée

La propriété peut avoir de une à quatre valeurs (pour la bordure supérieure, la bordure droite, la bordure inférieure et la bordure gauche).border-style.

Démonstration des différents styles de bordure :

p.dotted {`border-style: dotted;`}
p.dashed {`border-style: dashed;`}
p.solid {`border-style: solid;`}
p.double {`border-style: double;`}
p.groove {`border-style: groove;`}
p.ridge {`border-style: ridge;`}
p.inset {`border-style: inset;`}
p.outset {`border-style: outset;`}
p.none {`border-style: none;`}
p.hidden {`border-style: hidden;`}
p.mix {`border-style: dotted dashed solid double;`}


![image](https://github.com/user-attachments/assets/3056a3fb-97f8-4ea4-a936-60d324b7fedc)

# Largeur de la bordure CSS

## Largeur de la bordure CSS
La propriété spécifie la largeur des quatre bordures.`border-width`

La largeur peut être définie comme une taille spécifique (en px, pt, cm, em, etc.) ou en utilisant L’une des trois valeurs prédéfinies : Mince, Moyen ou Épais :


    p.one {
      border-style: solid;
      border-width: 5px;
    }

    p.two {
      border-style: solid;
      border-width: medium;
    }

    p.three {
      border-style: dotted;
      border-width: 2px;
    }

    p.four {
      border-style: dotted;
      border-width: thick;
    }



![image](https://github.com/user-attachments/assets/563fbdb5-1cd2-4d06-90a4-8bb16ee65f23)

 
## Largeurs latérales spécifiques
La propriété peut avoir de une à quatre valeurs (pour la bordure supérieure, la bordure droite, bordure inférieure et la bordure gauche) :`border-width`

    p.one {
      border-style: solid;
      border-width: 5px 20px; /* 5px top and bottom, 20px on the sides */
    }

    p.two {
      border-style: solid;
      border-width: 20px 5px; /* 20px top and bottom, 5px on the sides */
    }

    p.three {
      border-style: solid;
      border-width: 25px 10px 4px 35px; /* 25px top, 10px right, 4px bottom and 35px left */
    }


![image](https://github.com/user-attachments/assets/38a513ef-2b7b-4f05-9593-8f6c6e145888)


# Couleur de la bordure CSS
La propriété est utilisée pour définir la couleur des quatre `bordures.border-color`

La couleur peut être définie par :

- Nom - spécifiez un nom de couleur, comme « rouge »
- HEX - spécifiez une valeur HEX, comme « #ff0000 »
- RGB - spécifiez une valeur RVB, comme « rgb(255,0,0) »
- HSL : spécifiez une valeur HSL, comme « hsl(0, 100%, 50%) »
transparent

        p.one {
      border-style: solid;
      border-color: red;
        }

        p.two {
      border-style: solid;
      border-color: green;
        }

        p.three {
      border-style: dotted;
      border-color: blue;
        }
![image](https://github.com/user-attachments/assets/1465b9b5-172e-4d1b-9083-aec0b24c941c)

## Bordure CSS Propriété abrégée

Comme vous l’avez vu à la page précédente, il existe de nombreuses propriétés à prendre en compte lorsqu’il s’agit de frontières.

Pour raccourcir le code, il est également possible de spécifier toutes les propriétés de bordure individuelles dans une propriété.

La propriété est une propriété abrégée pour les propriétés de bordure individuelles suivantes :`border`

- `border-width`
- `border-style` (obligatoire)
- `border-color`

        p {
      border: 5px solid red;
        }
Résultat:
![image](https://github.com/user-attachments/assets/3fddbe6a-08ed-4d12-bcb2-d5dcd3ba60bd)

Vous pouvez également spécifier toutes les propriétés de bordure individuelles pour un seul côté :

    p {
      border-left: 6px solid red;
    }

Résultat:
![image](https://github.com/user-attachments/assets/221cc7ed-512c-4693-92aa-4d0b59cf35dc)

## Bordure inférieure

    p {
      border-bottom: 6px solid red;
    }
Résultat:
![image](https://github.com/user-attachments/assets/1ce202ad-d392-4372-a3a7-1c4948cfc1c6)

## Bordures arrondies CSS
La propriété est utilisée pour ajouter des bordures arrondies à un élément :`border-radius`

![image](https://github.com/user-attachments/assets/b389c960-70b5-410e-b8b2-ed52b5e02b28)

    p {
      border: 2px solid red;
      border-radius: 5px;
    }
# Marges CSS
Toutes les propriétés de marge CSS

![image](https://github.com/user-attachments/assets/5d04c1f7-c5d1-453f-85bb-d6be4956ddfc)

## Marges CSS
Les propriétés CSS sont utilisées pour créer de l’espace autour des éléments, en dehors de toute frontière définie.`margin`

Avec CSS, vous avez un contrôle total sur les marges. Il y a des propriétés pour définir la marge de chaque côté d’un élément (en haut, à droite, en bas et à gauche).

## Marge Côtés individuels
CSS a des propriétés pour spécifier la marge pour chaque côté d’un élément :

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

Toutes les propriétés de marge peuvent avoir les valeurs suivantes :

- auto - le navigateur calcule la marge
- Longueur - spécifie une marge en px, pt, cm, etc.
- % - spécifie une marge en % de la largeur de l’élément contenant
- inherit - spécifie que la marge doit être héritée de l’élément parent
  
Pourboire: Les valeurs négatives sont autorisées.

Définissez des marges différentes pour les quatre côtés d’un élément <p> :

    p {
      margin-top: 100px;
      margin-bottom: 100px;
      margin-right: 150px;
      margin-left: 80px;
    }

ou Si la propriété a quatre valeurs :margin

- marge : 25px 50px 75px 100px ;
    - La marge supérieure est de 25px
    - La marge de droite est de 50px
    - La marge inférieure est de 75px
    -  La marge de gauche est de 100px
 
Utilisez la propriété abrégée margin avec quatre valeurs :

    p {
      margin: 25px 50px 75px 100px;
    }

ou Si la propriété a trois valeurs :margin

- marge : 25px 50px 75px ;
    - La marge supérieure est de 25px
    - Les marges droite et gauche sont de 50px
    - La marge inférieure est de 75px

Utilisez la propriété abrégée margin avec trois valeurs :

    p {
      margin: 25px 50px 75px;
    }

## La valeur auto
Vous pouvez définir la propriété margin sur pour centrer horizontalement l’élément dans son conteneur.`auto`

L’élément occupera alors la largeur spécifiée et l’espace restant seront répartis à parts égales entre les marges gauche et droite.

    div {
    width: 300px;
    margin: auto;
    border: 1px solid red;
    }

## Réduction de la marge
Les marges supérieure et inférieure des éléments sont parfois réduites en une seule marge égale à la plus grande des deux marges.

Cela ne se produit pas sur les marges de gauche et de droite ! Uniquement des marges supérieures et inférieures !

    h1 {
    margin: 0 0 50px 0;
    }

    h2 {
    margin: 20px 0 0 0;
    }

## Remplissage CSS
Le remplissage est utilisé pour créer de l’espace autour du contenu d’un élément, à l’intérieur de toutes les bordures définies.

![image](https://github.com/user-attachments/assets/c65ad147-ee0a-4561-8ad2-4caef2aab437)

Les propriétés CSS sont utilisées pour générer de l’espace autour de le contenu d’un élément, à l’intérieur des bordures définies.`padding`

Avec CSS, vous avez un contrôle total sur le remplissage. Il y a des propriétés pour définir le remplissage de chaque côté d’un élément (haut, droite, bas et gauche).

## Rembourrage - Côtés individuels

CSS a des propriétés pour spécifier le remplissage pour chaque côté d’un élément :

- padding-top
- padding-right
- padding-bottom
- padding-left

Toutes les propriétés de remplissage peuvent avoir les valeurs suivantes :

- Longueur - spécifie un remplissage en px, pt, cm, etc.
- % - spécifie un remplissage en % de la largeur de l’élément conteneur
- inherit - spécifie que le remplissage doit être hérité de l’élément parent

Note: Les valeurs négatives ne sont pas autorisées.

Définissez un remplissage différent pour les quatre côtés d’un élément <div> :

    div {
    padding-top: 50px;
    padding-right: 30px;
    padding-bottom: 50px;
    padding-left: 80px;
    }
![image](https://github.com/user-attachments/assets/3d047e15-1428-4453-a125-a9592d36db20)


ou Si la propriété a quatre valeurs :`padding`

- rembourrage : 25px 50px 75px 100px ;
  - Le rembourrage supérieur est de 25 px
  - Le rembourrage droit est de 50px
  - Le rembourrage inférieur est de 75 px
  - Le rembourrage gauche est de 100px
 
        div {
        padding: 25px 50px 75px 100px;
        }
![image](https://github.com/user-attachments/assets/75090694-4967-411d-986a-f7cac893c899)


ou Si la propriété a trois valeurs :padding

- rembourrage : 25px 50px 75px ;
  - Le rembourrage supérieur est de 25 px
  - Les rembourrages droit et gauche sont de 50px
  - Le rembourrage inférieur est de 75 px

        div {
        padding: 25px 50px 75px;
        }

![image](https://github.com/user-attachments/assets/fed5fa34-f146-42d7-9d35-fca31493df7e)


## Remplissage et largeur de l’élément
La propriété CSS spécifie la largeur de la zone de contenu de l’élément. Le La zone de contenu est la partie à l’intérieur du remplissage, de la bordure et de la marge d’un élément.`width`

Ainsi, si un élément a une largeur spécifiée, le remplissage ajouté à cet élément à la largeur totale de l’élément. C’est souvent un résultat indésirable.

Ici, l’élément <div> reçoit une largeur de 300px. Cependant, la largeur réelle de l’élément <div> sera de 350px (300px + 25px de rembourrage gauche + 25px de rembourrage droit) :

    div {
    width: 300px;
    padding: 25px;
    }

![image](https://github.com/user-attachments/assets/32085ee6-8ada-4cde-84ff-755a0b8e012c)


Pour maintenir la largeur à 300px, quelle que soit la quantité de remplissage, vous pouvez utiliser la propriété. Cela permet à l’élément de conserver sa largeur réelle ; si Vous augmentez le remplissage, l’espace de contenu disponible diminuera. `box-sizing`

Utilisez la propriété box-sizing pour maintenir la largeur à 300px, quel que soit le Quantité de rembourrage :

    div {
    width: 300px;
    padding: 25px;
    box-sizing: border-box;
    }

![image](https://github.com/user-attachments/assets/9677134e-4b1e-4c33-addf-07fb20f96449)

# Tableaux CSS


## Bordures de tableau
Pour spécifier les bordures de tableau en CSS, utilisez la propriété.border

L’exemple ci-dessous spécifie une bordure solide pour les éléments `<table>`, `<th>` et `<td>` :

    table, th, td {
    border: 1px solid;
    }

![image](https://github.com/user-attachments/assets/e90f90d0-33fe-45d6-a513-f927e66213b8)

## Table pleine largeur
Le tableau ci-dessus peut sembler petit dans certains cas. Si vous avez besoin d’un tableau qui doit couvrir tout l’écran (pleine largeur), ajoutez à la page `<table>` élément :`width: 100%`


    table {
    width: 100%;
    }

![image](https://github.com/user-attachments/assets/261af420-4cbc-429a-8fa8-00cf409bd316)

## Réduire les bordures de table
La propriété définit si les bordures de la table doit être réduit en une seule bordure :`border-collapse`

    table {
    border-collapse: collapse;
    }

![image](https://github.com/user-attachments/assets/06ffac9b-592d-44d2-bb30-ff194fe0ace4)


Si vous souhaitez uniquement une bordure autour de la table, spécifiez uniquement la propriété pour `<table>` :`border`

    table {
    border: 1px solid;
    }

![image](https://github.com/user-attachments/assets/6f831d1e-988e-4092-a34d-db0efb165ad3)

# Taille du tableau CSS


## Largeur et hauteur de la table
La largeur et la hauteur d’une table sont définies par les propriétés et .`widthheight`

L’exemple ci-dessous définit la largeur de la table à 100 % et la hauteur de la <ème> éléments à 70px :

    table {
    width: 100%;
    }

    th {
    height: 70px;
    }

![image](https://github.com/user-attachments/assets/22672202-16f4-403c-ae8c-aa6893dd890f)


Pour créer un tableau qui ne doit couvrir que la moitié de la page, utilisez :width: 50%

    table {
    width: 50%;
    }

![image](https://github.com/user-attachments/assets/a8de3f3d-9b7e-4165-919c-4d685a37d699)
