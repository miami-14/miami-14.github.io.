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

''
![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)

''


