# taille pour le caratère 
Pour créer un titre, ajoutez un à six symboles avant le texte de votre titre. Le nombre que vous utilisez déterminera le niveau hiérarchique et la taille de la police de caractères de l’en-tête.
```
# bonjour ( grand ) 
## bonjour ( moyen ) 
### bonjour (petit ) 

```



# Style de caratère 
<table>
  <tr>
    <th>Style</th>
    <th>Syntaxe</th>
    <th>Raccourci clavier</th>
    <th> Exemple </th>
  </tr>
  <tr>
    <td>Audacieux</td>
    <td> ** **ou  __ __ </td>
    <td> Commende + B (MAC ) ou Controle B (windows ou linux ) </td>
    <td> **This is bold text** </td>
  </tr>
  <tr>
    <td>Italique </td>
    <td>* * ou _ _ </td>
    <td>Command+I (Mac) ou (Windows/Linux)Ctrl I </td>
    <td> _This text is italicized_ </td>
</tr>
  <tr>
    <td>Barré </td>
    <td>	~~ ~~ </td>
    <td> Aucun </td>
    <td> ~~This was mistaken text~~ </td>
</tr>
  <tr>
    <td>Italique gras et imbriqué	 </td>
    <td>** ** et _ _ </td>
    <td>Aucun </td>
    <td> **This text is _extremely_ important**	</td>
  </tr>
  
  <tr>
     <td>Tout en gras et en italique		 </td>
    <td>*** ***	</td>
    <td>Aucun </td>
    <td> ***All this text is important*** </td>
  </tr>

   <tr>
     <td>Indice		 </td>
    <td> (<>)sub  et /sub	(<>) </td>
    <td>Aucun </td>
     <td> This is a <sub>subscript</sub> text	</td>
  </tr>

   <tr>
     <td>Superscript		 </td>
    <td> (<>)sub  et /sub	(<>) 	</td>
    <td> Aucun </td>
      <td> This is a <sup>superscript</sup> text </td>
  </tr>
</table>

# Citation du texte
Vous pouvez citer du texte avec un >

Par exemple:
>bonjour 

# Citation du code 
Vous pouvez appeler du code ou une commande dans une phrase avec des apostrophes inversées simples. Le texte à l’intérieur des apostrophes inversées ne sera pas formaté. Vous pouvez également appuyer sur le raccourci clavier + (Mac) ou + (Windows/Linux) pour insérer les apostrophes inversées d’un bloc de code dans une ligne de Markdown.CommandECtrlE ( ``)

Bonjour  `git status` efnjeznfezjnf.

Pour formater du code ou du texte dans son propre bloc distinct, utilisez des apostrophes inversées triples.
```
git status
git add
git commit
```

# Modèles de couleurs pris en charge

Dans les problèmes, les demandes de tirage et les discussions, vous pouvez appeler des couleurs dans une phrase à l’aide d’apostrophes inversées. Un modèle de couleur pris en charge dans les apostrophes inversées affichera une visualisation de la couleur. 
```
The background color is `#ffffff` for light mode and `#000000` for dark mode.
```

<table>
  <tr>
    <th>Couleur </th>
    <th>Syntaxe </th>
    <th> Exemple</th>

  </tr>

   <tr>
    <td> SORTILÈGE	 </td>
    <td> `#RRGGBB`	 </td>
    <td>`#0969DA`	 </td>
  </tr>

  <tr>
    <td> RVB </td>
    <td> `rgb(R,G,B)`	</td>
    <td> `rgb(9, 105, 218)`	</td>
  </tr>

  <tr>
    <td> HSL </td>
    <td> `hsl(H,S,L)`</td>
    <td>` hsl(212, 92%, 45%)`</td>
  </tr>
  </table>


# Lien 
Vous pouvez créer un lien en ligne en encapsulant le texte du lien entre crochets, puis en enveloppant l’URL entre parenthèses. Vous pouvez également utiliser le raccourci clavier + pour créer un lien. Lorsque du texte est sélectionné, vous pouvez coller une URL à partir de votre presse-papiers pour créer automatiquement un lien à partir de la sélection `.[ ]( )Command K `

Vous pouvez également créer un lien hypertexte Markdown en mettant le texte en surbrillance et en utilisant le raccourci clavier +. Si vous souhaitez remplacer le texte par le lien, utilisez le raccourci clavier ++. `CommandVCommand Shift V `

```
This site was built using [GitHub Pages](https://pages.github.com/).
```
# Liens de section 
Vous pouvez créer un lien direct vers une section d’un fichier rendu en survolant le titre de section à exposer .

![image](https://github.com/user-attachments/assets/b693ba35-1b83-4443-a5e8-3606d7420439)

# Liens relatifs

Vous pouvez définir des liens relatifs et des chemins d’accès aux images dans vos fichiers rendus pour aider les lecteurs à accéder à d’autres fichiers de votre référentiel.

Un lien relatif est un lien relatif au fichier actif. Par exemple, si vous avez un fichier README à la racine de votre dépôt et que vous avez un autre fichier dans docs/CONTRIBUTING.md, le lien relatif à CONTRIBUTING.md dans votre README peut ressembler à ceci :

```
[Contribution guidelines for this project](docs/CONTRIBUTING.md)
```

GitHub transformera automatiquement le chemin d’accès de votre lien ou de votre image en fonction de la branche sur laquelle vous vous trouvez, afin que le lien ou le chemin d’accès fonctionne toujours. Le chemin d’accès du lien sera relatif au fichier actuel. Les liens commençant par seront relatifs à la racine du dépôt. Vous pouvez utiliser tous les opérandes de lien relatifs, tels que et `././../ `

Le texte de votre lien doit être sur une seule ligne. L’exemple ci-dessous ne fonctionnera pas.

```
[Contribution 
guidelines for this project](docs/CONTRIBUTING.md)
```

Les liens relatifs sont plus faciles pour les utilisateurs qui clonent votre dépôt. Les liens absolus peuvent ne pas fonctionner dans les clones de votre dépôt - nous vous recommandons d’utiliser des liens relatifs pour faire référence à d’autres fichiers de votre dépôt.

# Images
Vous pouvez afficher une image en ajoutant et en enveloppant le texte alternatif dans . Le texte alternatif est un texte court équivalent aux informations de l’image. Ensuite, enveloppez le lien de l’image entre parenthèses.`![ ]() `


![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)



# Listes

Vous pouvez créer une liste non ordonnée en faisant précéder une ou plusieurs lignes de texte de `, , ou .-*+ `

```
- George Washington
* John Adams
+ Thomas Jefferson
```
- george
* John
+ Thomas

Pour ordonner votre liste, faites précéder chaque ligne d’un numéro.

```
1. James Madison
2. James Monroe
3. John Quincy Adams
```

1. James Madison
2. James Monroe
3. John Quincy Adams

# Listes de tâches 

Pour créer une liste de tâches, faites précéder les éléments de la liste d’un trait d’union et d’un espace suivis de . Pour marquer une tâche comme terminée, utilisez .`[ ][x]`

```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:

Si la description d’un élément de la liste des tâches commence par une parenthèse, vous devrez l’échapper avec: `\`

```
- [ ] \(Optional) Open a followup issue
 
```
Pour plus d’informations, consultez « À propos des listes de tâches ».

# Paragraphes
Vous pouvez créer un nouveau paragraphe en laissant une ligne vide entre les lignes de texte.


# Notes
Vous pouvez ajouter des notes de bas de page à votre contenu à l’aide de la syntaxe de crochet suivante :

```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.

```

La note de bas de page s’affichera comme suit :

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.

# Alertes

Les alertes sont une extension Markdown basée sur la syntaxe blockquote que vous pouvez utiliser pour mettre l’accent sur les informations critiques. Sur GitHub, ils sont affichés avec des couleurs et des icônes distinctives pour indiquer l’importance du contenu.

N’utilisez les alertes que lorsqu’elles sont cruciales pour le succès de l’utilisateur et limitez-les à une ou deux par article pour éviter de surcharger le lecteur. De plus, vous devez éviter de placer des alertes consécutives. Les alertes ne peuvent pas être imbriquées dans d’autres éléments.

Pour ajouter une alerte, utilisez une ligne de citation spéciale spécifiant le type d’alerte, suivie des informations d’alerte dans une citation standard. Cinq types d’alertes sont disponibles :

```
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```
Voici les alertes affichées :

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

