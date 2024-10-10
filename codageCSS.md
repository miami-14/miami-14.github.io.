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

Ici, tous les éléments <p> de la page seront aligné au centre, avec une couleur de texte rouge :

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







