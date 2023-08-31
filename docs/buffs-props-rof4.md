# Fonctions spéciales

La fiche de personnage Chroniques Galactiques comporte de nombreuses fonctionnalités avancées détaillées ci-dessous.

## Buffs

De nombreuses capacités et traits permettent de donner des bonus (ou debuffs/malusà aux tests et jets de dés.

Certaines concernent les attaques du personnages et doivent être indiquées sur l'onglet _Caractéristiques_ dans les listes _Modificateurs d'attaque_ et _Modificateurs de dommages_.

D'autres concernent les divers caractéristiques et attributs du personnage et doivent être indiqués sur l'onglet _Capacités_ dans la liste _Buffs_.

Dans tous les cas :
- Si le buff est temporaire, une case à cocher permet de l'activer ou le désactiver selon les circonstances.
- Si le buff est permanent, il suffit de laisser la case cochée en permanence.
- Tous les buffs ont la même structure : 
  - le nom de la capacité ou du trait, qui apparaît dans les bulles d'aide associées aux jets dans le chat
  - la ou les attributs bénéficiant du modificateur ainsi que la valeur effective de celui-ci
  - si un buff modifie plusieurs attributs, ceux-ci doivent être indiqués à la suite les uns des autres, séparés entre eux par des points-virgules ';'

Les attributs modifiés peuvent être :
- Les six caractéristiques de base : FOR, DEX, CON, INT, PER, CHA
- L'attaque au contact que l'on peut indiquer via plusieurs alias : atc, atkcac, cac, contact
- L'attaque à distance que l'on peut indiquer via plusieurs alias : atd, atktir, cad, distance, tir
- L'attaque magique que l'on peut indiquer via plusieurs alias : mag, atkmag, magie
- Les attaques psy que l'on peut indiquer via plusieurs alias : psyinf, psyinflu, psyint,	psyintui
- L'Initiative que l'on peut indiquer via plusieurs alias : init, initiative
- Les défenses : def, dep
- Les points de vie : pv

La valeur du modificateur peut être spécifiée comme :
- Un nombre fixe
- La valeur d'un autre attribut, en l'indiquant entre [] (ex : [PER])
- Le rang dans une voie, en l'indiquant soit sous la forme [VOIE#] (où # est le numéro de la voie), soit sous la forme [rang {nom voie}]


## Propriétés d'équipement

Pour chaque élément de la liste d'équipement du personnage, il est possible de spécifier diverses propriétés influant sur les attributs.

### Cases à cocher

- La case "Equipement utilisé" est prise en compte par la fonctionnalité _**Règle des 4**_ (voir ci-dessous).

- La case "Equipement porté" est prise en compte dans la gestion de l'encombrement. De plus, si une propriété 'DEF' apparait dans la liste des propriétés de cet équipement, cocher ou décocher cette case coche ou décoche la case "Armure portée" dans la section DEFENSE de l'onglet _**Caractéristiques**_ de la fiche. Si le mot 'BOUCLIER' apparait dans le nom de l'équipement, c'est la case "Champ de force activé" qui sera cochée ou décochée.

- La case "A une attaque" crée une ligne d'attaque sur l'onglet _**Caractéristiques**_ de la fiche. La ligne d'attaque est créée en fonction des propriétés indiquées pour l'équipement.

### Propriétés d'équipement

Une liste de propriétés peut être fournie pour un équipement, sous la forme d'une liste de paires _nom:valeur_ séparées par des virgules (,). La liste des propriétés supportées est la suivante :

- **DEF** :	Valeur du bonus de DEF de l'armure.
- **DEF-** : Valeur du malus d'armure.
- **RD** : Valeur de réduction des dommages.
- **ATD** : Valeur de portée pour une arme à distance.
  - Si cette proprété est indiquée, la ligne d'attaque utilise l'ATD du personnage, sinon la ligne d'attaque créée utilise l'ATC.
- **DM** : Dés de dommages de arme.
- **MOD** : Valeur du bonus de matériel (pour la règle des 4, cf ci-dessous).


## Règle des 4

La **_règle des 4_** stipule que pour une action donnée, après avoir lancé le d20 et ajouté une caractéristique, on ne peut prendre en compte que 4 types de modificateurs dont la valeur va de -5 à +5 :
- un modificateur de compétence correspondant au rang dans une voie appropriée (si plusieurs voies peuvent servir, le meilleur rang s'applique)
- un modificateur de situation (si plusieurs circonstances influent sur l'action, le moins favorable s'applique)
- un modificateur de matériel (si plusieurs équipements peuvent être utilisés, le meilleur s'applique)
- un modificateur de chance

Cette règle peut être mise en oeuvre dans la fiche de la manière suivante :

- Sur l'onglet **_Capacités_**, cocher les cases de toutes les voies qui s'appliquent. La fiche utilise celle dont le rang possédé est le plus élevé.

- Sur l'onglet **_Capacités_**, une liste permet d'indiquer tous les modificateurs de situation dont le personnage peut bénéficier ou qu'il peut subir. Cette liste est proposée chaque fois qu'un jet de caractéristique est effectué. Le modificateur correspondant est appliqué au jet, à moins que le choix effectué dans la liste déroulante **_Situation_** de la fiche soit moins favorable.

- Sur l'onglet **_Equipement_**, dans la liste du matériel, cocher la case **_Utilisé_** de tous les objets pouvant servir au personnage dans la résolution de l'action. La fiche utilise celui dont la valeur de la propriété MOD est la plus élevée.

Une fois les différents modificateurs sélectionnés, il n'y a plus qu'à cliquer sur l'un des boutons de caractéristique pour effectuer le jet correspondant.