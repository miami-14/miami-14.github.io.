
## Informations 

- [Exemples dans chaque chapitre](#Exemples-dans-chaque-chapitre)
- [Le sélecteur d’élément CSS ](#Le-sélecteur-d’élément-CSS)
- [Le sélecteur d’id CSS](#Le-sélecteur-d’id-CSS)
- [Le sélecteur de classe CSS](#Le-sélecteur-de-classe-CSS)
- [Le sélecteur universel CSS](#Le-sélecteur-universel-CSS)
- [Le sélecteur de regroupement CSS](#Le-sélecteur-de-regroupement-CSS)
- [Comment ajouter du CSS](#Comment-ajouter-du-CSS)
- [CSS externe](#CSS-externe)
- [CSS interne](#CSS-interne)
- [CSS en ligne](#CSS-en-ligne)
- [Plusieurs feuilles de style](#Plusieurs-feuilles-de-style)
  
- [Couleurs CSS](#Couleurs-CSS)
- [Couleur d’arrière-plan CSS](#Couleur-d’arrière-plan-CSS)
- [Couleur du texte CSS](#Couleur-du-texte-CSS)
- [Couleur de la bordure](#Couleur-de-la-bordure)
- [Valeurs de couleur](#Valeurs-de-couleur)
- [Valeur HEX à 3 chiffres](#Valeur-HEX-à-3-chiffres)
- [Arrière-plans CSS](#Arrière-plans-CSS)
- [Couleur d’arrière-plan CSS](#Couleur-d’arrière-plan-CSS)
- [Autres éléments](#Autres-éléments)
- [Opacité / Transparence](#Opacité-/-Transparence)
  
- [Bordures CSS](#Bordures-CSS)
- [Style de bordure CSS](#Style-de-bordure-CSS )
- [Largeur de la bordure CSS](#Largeur-de-la-bordure-CSS)
- [Largeurs latérales spécifiques](#Largeurs-latérales-spécifiques)
- [Couleur de la bordure CSS](#Couleur-de-la-bordure-CSS)
- [Bordure CSS - Propriété abrégée](#Bordure-CSS-Propriété-abrégée)
- [Bordure CSS - Propriété abrégée](#Bordure-CSS-Propriété-abrégée)
- [Bordure CSS - Propriété abrégée](#Bordure-CSS-Propriété-abrégée)
- [Bordure inférieure](#Bordure-inférieure)
- [Bordures arrondies CSS](#Bordures-arrondies-CSS)
- [Marges CSS](#Marges-CSS)
- [Marge - Côtés individuels](#Marge-Côtés-individuels)




# codage CSS


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

## Le sélecteur d’élément CSS
Le sélecteur d’éléments sélectionne les éléments HTML en fonction du nom de l’élément.

Ici, tous les éléments `<p>` de la page seront aligné au centre, avec une couleur
de texte rouge :

    p {
      text-align: center;
      color: red;
    }

## Le sélecteur d’id CSS
Le sélecteur id utilise l’attribut id d’un élément HTML pour sélectionner un élément spécifique.

L’id d’un élément est unique au sein d’une page, donc le sélecteur d’id est habituel Sélectionnez un élément unique !

Pour sélectionner un élément avec un id spécifique, écrivez un caractère dièse `(#)`, suivi de ID de l’élément.

La règle CSS ci-dessous sera appliquée à l’élément HTML avec id="`para1` » :

    #para1 {
      text-align: center;
      color: red;
    }

## Le sélecteur de classe CSS
Le sélecteur de classe sélectionne les éléments HTML avec un attribut de classe spécifique.

Pour sélectionner des éléments avec une classe spécifique, écrivez un point `(.)`, suivi de l’icône nom de la classe.

Dans cet exemple, tous les éléments HTML avec class="center » seront rouges et alignés au centre :

    .center {
      text-align: center;
      color: red;
    }

Vous pouvez également spécifier que seuls des éléments HTML spécifiques doivent être affectés par une classe.

Dans cet exemple, seuls les éléments `<p>` avec class="`center` » seront rouge et aligné au centre :

    p.center {
      text-align: center;
      color: red;
    }

Éléments HTML peut également faire référence à plus d’une classe.

Dans cet exemple, l’élément `<p>` sera stylisé selon `class="center `» et à `class="large` » :

    <p class="center large">This paragraph refers to two classes.</p>

## Le sélecteur universel CSS
Le sélecteur universel (*) sélectionne tous les fichiers HTML éléments sur la page.

La règle CSS ci-dessous affectera tous les éléments HTML de la page :

    * {
      text-align: center;
      color: blue;
    }

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

Il sera préférable de regrouper les sélecteurs, pour minimiser le code.

Pour regrouper des sélecteurs, séparez chaque sélecteurs par une virgule.


Dans cet exemple, nous avons regroupé les sélecteurs du code ci-dessus :

    h1, h2, p {
      text-align: center;
      color: red;
    }
    
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

# Arrière-plans CSS

Les propriétés d’arrière-plan CSS sont utilisées pour ajouter des effets d’arrière-plan pour les éléments.


les propriétés d’arrière-plan CSS suivantes :
- background-color
- background-image
- background-repeat
- background-attachment
- background-position
- background (propriété abrégée)


## Couleur d’arrière-plan CSS

La propriété spécifie la couleur d’arrière-plan d’un élément.`background-color`

La couleur d’arrière-plan d’une page est définie comme suit :

    body {
      background-color: lightblue;
    }

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

# Opacité / Transparence
La propriété spécifie l’opacité/transparence d’un élément. Il peut prendre une valeur comprise entre 0,0 et 1,0. Plus la valeur est faible, plus la transparence est grande :opacity

    div {
      background-color: green;
      opacity: 0.3;
    }

# Bordures CSS
Les propriétés CSS border vous permettent de spécifier le style, largeur et couleur de la bordure d’un élément.

## Style de bordure CSS

La propriété spécifie le type de bordure à afficher.border-style

Les valeurs suivantes sont autorisées :

- dotted - Définit une bordure en pointillés
- dashed - Définit une bordure en pointillés
- solid - Définit une bordure unie
- double - Définit une double bordure
- groove - Définit une bordure rainurée en 3D. L’effet dépend de la valeur de la couleur de la bordure
- ridge - Définit une bordure striée 3D. L’effet dépend de la valeur de la couleur de la bordure
- inset - Définit une bordure en encart 3D. L’effet dépend de la valeur de la couleur de la bordure
- outset - Définit une bordure de départ 3D. L’effet dépend de la valeur de la couleur de la bordure
- none - Ne définit aucune bordure
- hidden - Définit une bordure cachée

La propriété peut avoir de une à quatre valeurs (pour la bordure supérieure, la bordure droite, la bordure inférieure et la bordure gauche).border-style.

Démonstration des différents styles de bordure :

p.dotted {border-style: dotted;}
p.dashed {border-style: dashed;}
p.solid {border-style: solid;}
p.double {border-style: double;}
p.groove {border-style: groove;}
p.ridge {border-style: ridge;}
p.inset {border-style: inset;}
p.outset {border-style: outset;}
p.none {border-style: none;}
p.hidden {border-style: hidden;}
p.mix {border-style: dotted dashed solid double;}


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
La propriété peut avoir de une à quatre valeurs (pour la bordure supérieure, la bordure droite, bordure inférieure et la bordure gauche) :border-width

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
La propriété est utilisée pour définir la couleur des quatre bordures.border-color

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

## Bordure CSS - Propriété abrégée

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


## Marges CSS
Les propriétés CSS sont utilisées pour créer de l’espace autour des éléments, en dehors de toute frontière définie.`margin`

Avec CSS, vous avez un contrôle total sur les marges. Il y a des propriétés pour définir la marge de chaque côté d’un élément (en haut, à droite, en bas et à gauche).

## Marge - Côtés individuels
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
