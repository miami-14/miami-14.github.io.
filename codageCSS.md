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

Ici, tous les éléments <p> de la page seront aligné au centre, avec une couleur
de texte rouge :

    p {
      text-align: center;
      color: red;
    }

## Le sélecteur d’id CSS
Le sélecteur id utilise l’attribut id d’un élément HTML pour sélectionner un élément spécifique.

L’id d’un élément est unique au sein d’une page, donc le sélecteur d’id est habituel Sélectionnez un élément unique !

Pour sélectionner un élément avec un id spécifique, écrivez un caractère dièse (#), suivi de ID de l’élément.

La règle CSS ci-dessous sera appliquée à l’élément HTML avec id="para1 » :

    #para1 {
      text-align: center;
      color: red;
    }

## Le sélecteur de classe CSS
Le sélecteur de classe sélectionne les éléments HTML avec un attribut de classe spécifique.

Pour sélectionner des éléments avec une classe spécifique, écrivez un point (.), suivi de l’icône nom de la classe.

Dans cet exemple, tous les éléments HTML avec class="center » seront rouges et alignés au centre :

    .center {
      text-align: center;
      color: red;
    }

Vous pouvez également spécifier que seuls des éléments HTML spécifiques doivent être affectés par une classe.

Dans cet exemple, seuls les éléments <p> avec class="center » seront rouge et aligné au centre :

    p.center {
      text-align: center;
      color: red;
    }

Éléments HTML peut également faire référence à plus d’une classe.

Dans cet exemple, l’élément <p> sera stylisé selon class="center » et à class="large » :

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

Les styles externes sont définis dans l’élément <link> dans
la section <head> d’une page HTML :

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
Voici à quoi ressemble le fichier « mystyle.css » :
« mystyle.css »

    body {
        background-color: lightblue;
    }

    h1 {
      color: navy;
      margin-left: 20px;
    }

## CSS interne
Une feuille de style interne peut être utilisée si une seule page HTML a un style unique.

Le style interne est défini à l’intérieur de l’élément <style>, à l’intérieur de la tête section.
Les styles internes sont définis dans l’élément <style> dans la section <head> d’une page HTML :

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
Les styles en ligne sont définis dans l’attribut « style » de la élément:

    <!DOCTYPE html>
    <html>
    <body>

    <h1 style="color:blue;text-align:center;">This is a heading</h1>
    <p style="color:red;">This is a paragraph.</p>

    </body>
    </html>

## Plusieurs feuilles de style
Si certaines propriétés ont été définies pour le même sélecteur (élément) dans différentes feuilles de style, La valeur de la dernière feuille de style lue sera utilisée.

Supposons qu’une feuille de style externe ait le style suivant pour l’élément <h1> :

    h1 {
      color: navy;
    }

Ensuite, supposons qu’une feuille de style interne ait également le style suivant pour l’élément <h1> :

    h1 {
      color: orange;   
    }

Si le style interne est défini après le lien vers la feuille de style externe, les éléments <h1> seront « orange » :

    <head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    <style>
    h1 {
      color: orange;
    }
    </style>
    </head>

Cependant, si le style interne est défini avant le lien vers la feuille de style externe, les éléments <h1> seront « marine » :

    <head>
    <style>
    h1 {
      color: orange;
    }
    </style>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    </head>
