-----------------
<p style='color:blue' align='center' size="gras"> De quoi s'agit-il ? </p>


-----------------

<background color="red">
Dans la cadre de notre projet de fin d'étude du cours d'analyse de données et de datavisualisation, nous nous sommes intéressés au jeu de données issue de la plateforme open data nationale qui a été réalisé par la ville de Nancy: le Mémorial virtuel des morts pour la France lors des différents conflits militaires.  
Il a été initié à l'occasion des commémorations du Centenaire de la Grande Guerre et édifié après la Première Guerre mondiale dans le cimetière du Sud, à proximité d'un carré militaire.
A l'origine de ce recensement, une volonté de la ville de Nancy qui cherche à "honorer la mémoire de ces milliers de soldats et transmettre aux générations futures la grandeur du sacrifice de ses héros. 
En ce sens, un site Internet a été créé : http://memorial.nancy.fr. L'idée étant d'élever ces vaillants hommes à leur mérite.
C’est ainsi que "des fiches individuelles ont été réalisées afin d'illustrer le parcours de ces hommes. Sur chacune d’elles, figurent l'état-civil des victimes, leur grade, l'unité à laquelle elles appartenaient, leur lieu de naissance, de dernière résidence (si celle-ci est connue) et selon les cas, leur portrait photographique. Leur contenu dépend néanmoins des sources parvenues jusqu'à ce jour".           
Aujourd'hui encore, la Ville compte poursuivre cette démarche jusqu'aux conflits les plus récents afin d’y apporter toute l'unité qui lui donnera tout son sens".

Source: Data.gouv.fr [https://www.data.gouv.fr/fr/datasets/memorial-virtuel-des-morts-pour-la-france-de-nancy-lors-des-differents-conflits-militaires/]></text>
</background> 

-----------------
<p style='color:blue' align='center'>
Qui sont les héros qui figurent dans ce Mémorial ?
</p>

-----------------

Le graphique ci-dessous est une représentation en cercles emballés qui permet d'avoir une vue d'ensemble des héros morts, tant au niveau nombre, que de leur composition (grade). Il apparait naturellement dans ces cercles imbriqués que les	Soldats sont plus nombreux, suivi des Sergents, les Caporals et ceux dits "Inconnus". Ils sont nombreux à être dépourvu de grade dans cette base de données mais s'ils y figurent, c'est parce qu'ils l'ont mérité, d'où toute la logique de les représenter. 

<iframe src='https://flo.uri.sh/visualisation/5137249/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;'></iframe><div style='width:100%!;margin-top:4px!important;text-align:right!important;'></div>

Pour réaliser ce graphique, nous avons été contraint d'aller au préalable dans [OpenRefine] pour nettoyer les données et les rendre compréhensible.
Rappellons déja que notre fichier csv issue de la plateforme Open Data nationale est accompagné d'une table de sigle explicative. Celle-ci contient des définitions de sigles des différents corps armés. Ainsi, pour nous éviter une alternance entre les deux fichiers, nous avons estimé plus simple de remplacer tous les sigles par les définitions qui nous ont été fournées dans le second fichier complémentaire. Ce qui nous permis de voir un peu plus clair dans cette base de données remplie d'expression militaire. 
Ce processus d'édition, bien qu'il ait pris du temps, a surtout été très facile à réaliser dans OpenRefine. Il arrive que certains corps armés soient dépourvus d'annotation, ils sont alors classés dans les facettes "blanc", nous les avons alors attribué l'appelleation "Grade inconnu" au lieu des les supprimer. 


-----------------
<p style='color:blue' align='center'>
D'où viennent-ils ?
</p>



-----------------
Ce graphique est une représentation cartographique du lieu de naissance de ces Hommes et Femmes disparus au combat. Les différents points animés indiquent le premier endroit où chacun à vu le jour en précisant son identité. La densité des points indiques qu'ils sont pour la plus part nés dans le Grand Est, le Hauts-de-France et en l'ïle-de-France. 

<iframe src='https://flo.uri.sh/visualisation/5137434/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ><a class='flourish-credit' href='https://public.flourish.studio/visualisation/5137434/?utm_source=embed&utm_campaign=visualisation/5137434' target='_top' style='text-decoration:none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;' > </a></div>

Les coordonnées géographique qui permis la réalisation de ce graphique ont été obtenu à partir de OpenRefine. Nous disposions déja de la commune de naissance et il a seulement  fallu qu'on procéde à la reconcilation pour obtenir les "coordonées géographiques".


-----------------
<p style='color:blue' align='center'>
Leurs lieux de décés (dernière adresse connue) ?
</p>


-----------------
Enfin nous avons une représentation cartographique des les lieux de décés. A l'instar de la première, cette deuxième carte indique une forte présences des victimes dans le Hauts-de-France, Bourgogne-Franche-Comté, l'Île-de-France et le Grand Est surtout. Les Nancéiens restent logiquement les plus représenté.   

<iframe src='https://flo.uri.sh/visualisation/5137319/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ><a class='flourish-credit' href='https://public.flourish.studio/visualisation/5137319/?utm_source=embed&utm_campaign=visualisation/5137319' target='_top' style='text-decoration :none!important'><img alt='Made with Flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;' > </a></div>

*Ps: Si la cartographie des lieux de naissances se rapproche trop de celle des lieux de décés, cela ne remet pas en cause la pertinence des données mais au contraire cela montre que nos données géographiques générées lors de la reconciliation, concordent avec celles fournies dans la base de données. En effet, les lieux de naissances de ces victimes ont été établis à partir de leur état-civil. Parallèlement, le recensement des lieux de décés, n'a tenu compte que de la dernière résidence connue (si celle-ci est connue).
L'explication la plus plausible, c'est que la plus part n'aient pas changé de résidence au moment de leur mort. .


<iframe src='https://flo.uri.sh/story/743592/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ><a class='flourish-credit' href='https://public.flourish.studio/story/743592/?utm_source=embed&utm_campaign=story/743592' target='_top' style='text-decoration:aucun!important'><img alt='Made With flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;' > </a></div>



