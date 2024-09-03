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

