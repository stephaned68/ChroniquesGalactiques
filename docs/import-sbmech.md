# Import de statblock de mécha

La fiche de personnage Chroniques Galactiques comporte une fonction d'import de statblock (bloc d'attributs abrégé résumant les données techniques de jeu) pour les fiches de mécha. Cette fonction essaye d'extraire les données du statblock et les insère dans la fiche de PNJ.

## Mode d'emploi

Pour importer un statblock et récupérer ses données dans une fiche de mécha :

1. Copier le texte du statblock depuis le document PDF de COG
2. Sur l'onglet _Configuration_ d'une fiche de _Mécha_, cliquer sur la flèche _Importer statblock_ pour afficher le champ d'import
3. Coller le texte précédemment copié dans le champ approprié
4. Cliquer sur _Import_

Si l'import se déroule sans encombres, le champ contenant le statblock est effacé.

Si un problème se pose au cours de l'import et que la fonction n'est capable d'extraire qu'une partie des données du mécha, un ou plusieurs messages explicitant l'origine du problème sont affichés sous le bouton d'import.

Si le champ contenant le statblock n'est pas effacé, il s'agit d'une erreur d'analyse ayant entraîné l'arrêt de l'import.

## Format du statblock

_**Profil**_  
_Notes_  
**CARACTERISTIQUES**  
_**TAILLE** x (xxxxx) **NIVEAU** x_  
_**DV** dx **PV** xx_  
_**FOR** xx **INT** xx_  
_**DEX** xx **PER** xx_  
_**CON** xx **CHA** xx_  
**OPTIONS (xx OPT)**  
_Option, Option, Option_  

Toutes les données n'ont pas obligatoirement à être présentes. La fonction d'import extrait celles qu'elle trouve et les insère dans les champs appropriés de la fiche de mécha, les autres seront à remplir manuellement.

## Trucs & astuces

- Le module d'import sait reconnaitre dans la liste des options ce qui correspond à une arme ou pas, et il crée une ligne d'attaque pour chacune d'entre elles.
