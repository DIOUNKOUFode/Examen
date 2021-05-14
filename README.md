-----------------------------------------------------------------------------
<p style='color:blue' align='center'>
DE QUOI S'AGIT-IL ?
</p>

-----------------------------------------------------------------------------

Dans la cadre de notre projet de fin d'étude en cours d'analyse de données et de datavisualisation, nous nous sommes intéressés au jeu de données issue de la plateforme open data nationale qui a été réalisé par la ville de Nancy: le Mémorial virtuel des morts pour la France lors des différents conflits militaires.  
Il a été initié à l'occasion des commémorations du Centenaire de la Grande Guerre et édifié après la Première Guerre mondiale dans le cimetière du Sud, à proximité d'un carré militaire.
A l'origine de ce recensement, une volonté de la ville de Nancy qui cherche à "honorer la mémoire de ces milliers de soldats et transmettre aux générations futures la grandeur du sacrifice de ses héros. 
En ce sens, un site Internet a été créé (http://memorial.nancy.fr) dans le but d'élever ces vaillants hommes au rang de leur mérite.
C’est ainsi que "des fiches individuelles ont été réalisées afin d'illustrer le parcours de ces hommes. Sur chacune d’elles, figurent l'état-civil des victimes, leur grade, l'unité à laquelle elles appartenaient, leur lieu de naissance, de dernière résidence (si celle-ci est connue) et selon les cas, leur portrait photographique. Leur contenu dépend néanmoins des sources parvenues jusqu'à ce jour".           
Aujourd'hui encore, la Ville compte poursuivre cette démarche jusqu'aux conflits les plus récents afin d’y apporter toute l'unité qui lui donnera tout son sens". Nous partons à la découverte de ces valeureux guerriers.
Source: Plateforme open data nationale [lien des données exploitées: https://www.data.gouv.fr/fr/datasets/memorial-virtuel-des-morts-pour-la-france-de-nancy-lors-des-differents-conflits-militaires/]></text>

-----------------
<p style='color:blue' align='center'>
QUI SONT CES HEROS QUI FIGURENT CE MEMORIAL ?
</p>

-----------------

Pour réaliser ce graphique, nous avons été contraints d'aller au préalable dans « Openrefine » pour nettoyer les données plus perceptibles.
Rappelons déjà que notre fichier csv issue de la plateforme Open Data nationale est accompagné d'une table de sigle explicative. Celle-ci contient les significations des différents grades. Ainsi, pour nous éviter une alternance entre les deux fichiers tout au long de ce travail, nous avons considéré qu'il serait plus simple de remplacer tous les sigles par leurs significations contenues dans le second fichier complémentaire. Ce qui nous a permis de voir un peu plus clair dans cette base de données remplie d’abréviations militaires. 
Ce processus de croisement entre de la table de la colonne des grades abrégée à celle des sigles, bien qu'il exige beaucoup de temps, a été d'un apport considérable. Il arrive cependant que certaines victimes dans la base de données soient dépourvues d'annotations, ils sont alors classés dans les facettes "blanc" par openrefine. Nous les avons alors attribués le "Grade inconnue" au lieu de les supprimer. 

![1](https://user-images.githubusercontent.com/77511932/118308659-84e7d700-b4ec-11eb-88ba-260e7f7a2e33.jpeg)

Le graphique ci-dessus est donc une représentation sous forme de cercles emballés qui permet d'avoir une vue d'ensemble des héros nancéiens morts au combat, tant au niveau de leur nombre, que de leur hiérarchie. Il y apparait naturellement que les Soldats sont plus nombreux, suivi des Sergents, les Caporaux et ceux dits "Inconnus". 


-----------------
<p style='color:blue' align='center'>
D'OU VIENNENT-ILS ?
</p>


-----------------
Ce graphique est une représentation cartographique des lieux de naissance de ces Hommes et Femmes qui ont disparu au combat. Les différents points animés indiquent le premier endroit où chacun a vu le jour. La densité des points indique également qu'ils sont en majorité nés dans le Grand Est, le Hauts-de-France et en l'Ile-de-France.

<iframe src='https://flo.uri.sh/visualisation/5137434/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div>

Les coordonnées géographiques ayant permis la réalisation de ce graphique ont été obtenues à partir de Openrefine. Nous disposions déjà dans le fichier originel des communes de naissance et il a seulement fallu qu'on procède à la réconciliation pour les géolocaliser. 

-----------------
<p style='color:blue' align='center'>
LEURS DERNIERES ADRESSES CONNUES ?
</p>

-----------------
Enfin nous avons ici une représentation cartographique de leurs lieux de décès. A l'instar de la première, cette deuxième carte indique aussi une forte concentration  des victimes dans le Hauts-de-France, Bourgogne-Franche-Comté, l'Île-de-France et le Grand Est surtout. Les Nancéiens restent logiquement les plus représenté.    

<iframe src='https://flo.uri.sh/visualisation/5137319/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div>

Si la cartographie des lieux de naissances se rapproche trop de celle des lieux de décès, cela ne doit pas néanmoins remettre en cause la pertinence des données. Au contraire cela fait montre de concordance et de fiabilité des données recueillies et de celles générées lors de la réconciliation. 

En effet, les lieux de naissances de ces victimes ont été établis à partir de leur état-civil. Parallèlement, le recensement des lieux de décès, n'a tenu compte que de leur dernière résidence connue (si celle-ci est connue). Et donc, pour la plupart, c'est la même adresse que celle qui figure déjà sur leurs états-civils. Il n’est donc pas étonnant que la localisationn de certains soldats par exemple reste inchangée. 

----------------
<p style='color:blue' align='center'>
+Hommage <iframe src='https://flo.uri.sh/story/743592/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div></p>

-----------------
En somme, comme vous pourrez le constater dans notre historique de parcours dans openrefine, il nous arrive de déplacé certaine colonne lors de la réalisation des cartes, d'imposer une séparation en deux colonnes pour les latitudes et longitudes pour répondre à la nomenclature du graphique que nous voulons réaliser.
Par ailleurs, nous avons toujours exporté nos fichiers dans openrefine uniquement au format csv. 
Il est important de préciser que notre historique peut ne pas contenir toutes les modifications faites durant le tout le long du projet, pour cause, il nous arrive de créer un nouveau projet sur un fichier qu'on a téléchargé à partir des modifications faites la veille sur open refine. Ce qui fait que nous avons plus d'un historique de parcours sur openrefine. Nous avons mis en bas de pages deux notre historique la plus pertinente.

------------------
<p style='color:red' align='center'>
Notre historique dans Openrefine 
</p>

```
[
  {
    "op": "core/column-removal",
    "columnName": "Nom",
    "description": "Remove column Nom"
  },
  {
    "op": "core/column-removal",
    "columnName": "Departement de naissance",
    "description": "Remove column Departement de naissance"
  },
  {
    "op": "core/column-removal",
    "columnName": "Carte CcommuneDeNaissance",
    "description": "Remove column Carte CcommuneDeNaissance"
  },
  {
    "op": "core/column-move",
    "columnName": "Latitude commune de naissance",
    "index": 0,
    "description": "Move column Latitude commune de naissance to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Longitude commune de naissance",
    "index": 0,
    "description": "Move column Longitude commune de naissance to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Longitude commune de naissance",
    "index": 1,
    "description": "Move column Longitude commune de naissance to position 1"
  },
  {
    "op": "core/column-move",
    "columnName": "Nom conflit",
    "index": 0,
    "description": "Move column Nom conflit to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Latitude Commune de deces",
    "index": 0,
    "description": "Move column Latitude Commune de deces to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Longitude Commune de deces",
    "index": 0,
    "description": "Move column Longitude Commune de deces to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Prenoms",
    "index": 0,
    "description": "Move column Prenoms to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Grade",
    "index": 0,
    "description": "Move column Grade to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Corps",
    "index": 0,
    "description": "Move column Corps to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Numero matricule",
    "index": 0,
    "description": "Move column Numero matricule to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Nom conflit",
    "index": 0,
    "description": "Move column Nom conflit to position 0"
  },
  {
    "op": "core/column-move",
    "columnName": "Grade",
    "index": 2,
    "description": "Move column Grade to position 2"
  }
]
```
----
|Outils_De_Viz_utilisés: 
  - Openrefine
  - Flourish
  - Datawrapper
  
|Auteur:
  - Nom: DIOUNNKOU
  - Prénom: Fodé
  - M2 Info-com, DEFI
  - 39016761@parisnanterre.fr
  
-----------------
Date: 02-02-2021
 
