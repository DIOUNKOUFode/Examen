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
Source: Plateforme open data nationale [https://www.data.gouv.fr/fr/datasets/memorial-virtuel-des-morts-pour-la-france-de-nancy-lors-des-differents-conflits-militaires/]></text>

-----------------
<p style='color:blue' align='center'>
QUI SONT CES HEROS QUI FIGURENT CE MEMORIAL ?
</p>

-----------------

Pour réaliser ce graphique, nous avons été contraints d'aller au préalable dans « Openrefine » pour nettoyer les données et les rendre compréhensible.
Rappelons déjà que notre fichier csv issue de la plateforme Open Data nationale est accompagné d'une table de sigle explicative. Celle-ci contient des définitions des différents grades. Ainsi, pour nous éviter une alternance entre les deux fichiers, nous avons estimé plus simple de remplacer tous les sigles par leurs définitions contenues dans le second fichier complémentaire. Ce qui nous a permis de voir un peu plus clair dans cette base de données remplie d’abréviations militaires. 
Ce processus d'édition, bien qu'il ait pris du temps, a surtout été très facile à réaliser dans « Openrefine ». Il arrive cependant que certaines victimes soient dépourvues d'annotations, ils sont alors classés dans les facettes "blanc". Nous les avons alors attribués le "Grade inconnue" au lieu de les supprimer.

<iframe src='https://flo.uri.sh/visualisation/5137249/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'></div>

Le graphique ci-dessus est donc une représentation sous forme de cercles emballés qui permet d'avoir une vue d'ensemble des héros nancéiens morts au combat, tant au niveau de leur nombre, que de leur hiérarchie. Il y apparait naturellement que les Soldats sont plus nombreux, suivi des Sergents, les Caporaux et ceux dits "Inconnus". 


-----------------
<p style='color:blue' align='center'>
D'OU VIENNENT-ILS ?
</p>


-----------------
Ce graphique est une représentation cartographique des états-civils de ces Hommes et Femmes ont disparu au combat. Les différents points animés indiquent le premier endroit où chacun a vu le jour. La densité des points indique également qu'ils en majorité nés dans le Grand Est, le Hauts-de-France et en l'Ile-de-France.

<iframe src='https://flo.uri.sh/visualisation/5137434/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div>

Les coordonnées géographiques ayant permis la réalisation de ce graphique ont été obtenues à partir de Openrefine. Nous disposions déjà dans le fichier originel de la commune de naissance et il a seulement  fallu qu'on procède à la réconciliation.

-----------------
<p style='color:blue' align='center'>
Leurs lieux de décès (dernière adresse connue) ?
</p>


-----------------
Enfin nous avons ici une représentation cartographique de leurs lieux de décès. A l'instar de la première, cette deuxième carte indique aussi une forte concentration  des victimes dans le Hauts-de-France, Bourgogne-Franche-Comté, l'Île-de-France et le Grand Est surtout. Les Nancéiens restent logiquement les plus représenté.   

<iframe src='https://flo.uri.sh/visualisation/5137319/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div>

Si la cartographie des lieux de naissances se rapproche trop de celle des lieux de décès, cela ne remet pas en cause la pertinence des données. Au contraire cela fait montre de concordance et de fiabilité quant aux données recueillies et de celles générées lors de la réconciliation. En effet, les lieux de naissances de ces victimes ont été établis à partir de leur état-civil. Parallèlement, le recensement des lieux de décès, n'a tenu compte que de la dernière résidence connue (si celle-ci est connue), donc de cette même adresse, pour la plupart, qui figure déjà sur les états-civils. Il n’est donc pas étonnant que certains soldats par exemple aient les mêmes coordonnées comme étant leur lieu de naissance en plus de leur lieu de décès.L'explication la plus plausible, c'est que la plus part n'aient pas changé de résidence au moment de leur mort.

<iframe src='https://flo.uri.sh/story/743592/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ></div>

-----------------
-----------------
<p style='color:red' align='left'>
DIOUNKOU Fodé</p>
<p style='color:red' align='left'>M2 Info-com, DEFI
<p style='color:red' align='left'>39016761@parisnanterre.fr
</p>
-----------------




