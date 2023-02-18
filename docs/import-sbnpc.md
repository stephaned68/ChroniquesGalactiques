# Import de statblock de PNJ

La fiche de personnage Chroniques Galactiques comporte une fonction d'import de statblock (bloc d'attributs abrégé résumant les données techniques de jeu) pour les fiches de PNJ. Cette fonction essaye d'extraire les données du statblock et les insère dans la fiche de PNJ.

## Mode d'emploi

Pour importer un statblock et récupérer ses données dans une fiche de PNJ :

1. Copier le texte du statblock depuis le document PDF de COG
2. Sur l'onglet _Configuration_ d'une fiche de _PNJ_, cliquer sur la flèche _Importer statblock_ pour afficher le champ d'import
3. Coller le texte précédemment copié dans le champ approprié
4. Cliquer sur _Import_

Si l'import se déroule sans encombres, le champ contenant le statblock est effacé.

Si un problème se pose au cours de l'import et que la fonction n'est capable d'extraire qu'une partie des données du PNJ, un ou plusieurs messages explicitant l'origine du problème sont affichés sous le bouton d'import.

Si le champ contenant le statblock n'est pas effacé, il s'agit d'une erreur d'analyse ayant entraîné l'arrêt de l'import.

## Format du statblock

_Profil_ _**NC** xx (...)_  
_Bio_  
**CARACTERISTIQUES**  
_**FOR** xx **INT** xx_  
_**DEX** xx **PER** xx_  
_**CON** xx **CHA** xx_  
_**DEF** xx **DEP** xx_  
_**PV** xx (xxx) **Init** xx_  
**ATTAQUES**  
_**Attaque/Arme** +Bonus **DM** Dommages_  
**CAPACITES**  
_**Nom.** Description de la capacité_  

Avant de cliquer sur le bouton d'import, il est nécessaire de préfixer le nom de chaque capacité d'un tiret (-).

Toutes les données n'ont pas obligatoirement à être présentes. La fonction d'import extrait celles qu'elle trouve et les insère dans les champs appropriés de la fiche de PNJ, les autres seront à remplir manuellement.

## Trucs & astuces

- Une ligne d'attaque est reconnue comme telle si elle apparait après le mot 'attaque' sur une ligne et qu'elle comporte le mot 'DM'.
- Le bonus d'attaque est le premier chiffre précédé d'un signe + présent sur la ligne d'attaque
- Les dommages sont le premier mot de la ligne d'attaque après le mot DM
- La fonction d'import regroupe les autres informations de la ligne d'attaque dans un champ _Spécial_ et si elle y détecte la mention d'un jet de dés, elle remet celui-ci en forme de manière à effectuer un _"inline roll"_ lorsque l'attaque est utilisée.
- Les descriptions de capacités sont également traitées pour transformer toute mention d´un jet de dés en _"inline roll"_
- Les données extraites du statblock qui ne correspondent pas à un champ sur la fiche de PNJ sont regroupées dans le champ texte _Divers_
