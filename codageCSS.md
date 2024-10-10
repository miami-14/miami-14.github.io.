# Comment créer un fichier CSS 

## Aller dans Visual studio code

Puis cliqué sur en haut a gauche 

Cliqué sur `File`





# Codage CSS 

### Exemples dans chaque chapitre
Ce tutoriel CSS contient des centaines d’exemples CSS.

Avec notre éditeur en ligne, vous pouvez modifier le CSS et cliquer sur un bouton pour afficher le résultat.

-Par exemple :

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


### Le sélecteur d’élément CSS
Le sélecteur d’éléments sélectionne les éléments HTML en fonction du nom de l’élément.

Par Exemple :  

    p {
      text-align: center;
      color: red;
    }

### Le sélecteur d’id CSS
Le sélecteur id utilise l’attribut id d’un élément HTML pour sélectionner un élément spécifique.

L’id d’un élément est unique au sein d’une page, donc le sélecteur d’id est habituel Sélectionnez un élément unique !

Pour sélectionner un élément avec un id spécifique, écrivez un caractère dièse (#), suivi de ID de l’élément.

-Par Exemple :

    #para1 {
        text-align: center;
        color: red;
    }

### Le sélecteur de classe CSS

Le sélecteur de classe sélectionne les éléments HTML avec un attribut de classe spécifique.

Pour sélectionner des éléments avec une classe spécifique, écrivez un point (.), suivi de l’icône nom de la classe.

Par Exemple :

    .center {
        text-align: center;
        color: red;
    }

Vous pouvez également spécifier que seuls des éléments HTML spécifiques doivent être affectés par une classe.

Par Exemple : 

    p.center {
        text-align: center;
        color: red;
    }


Éléments HTML peut également faire référence à plus d’une classe.

    <p class="center large">This paragraph refers to two classes.</p>


### Le sélecteur universel CSS
Le sélecteur universel (*) sélectionne tous les fichiers HTML éléments sur la page.

Par Exemple : 

    * {
      text-align: center;
      color: blue;
    }

### Le sélecteur de regroupement CSS
Le sélecteur de regroupement sélectionne tous les éléments HTML avec le même style Définitions.

Regardez le code CSS suivant (les éléments h1, h2 et p ont les mêmes définitions de style) :

Par Exemple : 

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


Par Exemple : 

    h1, h2, p {
      text-align: center;
      color: red;
    }

