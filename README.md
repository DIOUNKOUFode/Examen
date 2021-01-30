## Mémorial virtuel des morts pour la France :

<iframe src='https://flo.uri.sh/story/743592/embed' title='Interactive or visual content' frameborder='0' scrolling='no' style='width:100%;height:600px;' ></iframe><div style='width:100%!; margin-top:4px!important;text-align:right!important;' ><a class='flourish-credit' href='https://public.flourish.studio/story/743592/?utm_source=embed&utm_campaign=story/743592' target='_top' style='text-decoration:aucun!important'><img alt='Made With flourish' src='https://public.flourish.studio/resources/made_with_flourish.svg' style='width:105px!important;height:16px!important;border:none!important;margin:0!important;' > </a></div>

Dans la cadre de notre projet de fin d'étude du [Cours d'analyse de données et de dataVisualisation], nous nous sommes intéressés au jeu de données issue d'un service public certifié et dont la mise à disposition a été rendu possible par l'excellent travail mené par la ville de Nancy: il s'agit du Mémorial virtuel des morts pour la France de Nancy lors des différents conflits militaires.
Le choix de ce jeu, tant cher aux yeux de ses initiateurs ne se justifie point par la richesse des données qu'elle contient mais par l'immense valeur que réprésentent ces hommes. En effet, ce Mémorial donne vie à ces vaillant.e.s Hommes/Femmes qui ont "garanti" la vie à la génération future : celle-là même qui tente aujourd'hui de les immortaliser. Cette histoire est blindée de sens, d'émotion, de leçon mais surtout, reflète d'énormes sacrifices pour une cause commune. 

Initié à l'occasion des commémorations du Centenaire de la Grance Guerre, le mémorial sera éditié après la Première Guerre mondiale dans le cimetière du Sud, à proximité d'un carré militaire. A l'origine de ce recensement des morts pour la France, une volonté de la ville de Nancy pour "honorer la mémoire de ces milliers de soldats et transmettre aux générations futures la grandeur de leur sacrifice. Un site Internet a d'ailleur été créé en ce sens : http://memorial.nancy.fr. L'idée étant d'élever ces héros à leur mérite. Aujourd'hui encore, elle compte poursuivre cette démarche jusqu'aux conflits les plus récents afin d'apporter à cette démarche mémorielle l'unité qui lui donnera tout son sens".

"Des fiches individuelles ont été réalisées afin d'illustrer le parcours de ces hommes. Sur chacune de ces fiches, figure l'état-civil des victimes, leur grade, l'unité à laquelle elles appartenaient, leur lieu de naissance, de dernière résidence (si celle-ci est connue) et selon les cas, leur portrait photographique. Leur contenu dépend néanmoins des sources parvenues jusqu'à ce jour".

Par ailleurs, "l'application de la loi du 28 février 2012, demandant l’inscription des noms des morts pour la France sur les monuments aux morts communaux, les morts, militaires ou civils, figurant dans cette liste doivent être natifs de Nancy ou y avoir résidé avant leur décès. Ils doivent également avoir reçu la mention « Mort pour la France », créée par la loi du 2 juillet 1915, qui honore la mémoire des victimes de guerre".

Par conséquent, "les données proposées ci-dessous présentent pour chaque soldat le nom du conflit, le nom du soldat, les prénoms, le grade, le corps, le numéro de matricule et le bureau lié, la date de naissance, le département de naissance, la commune de naissance, la date de décès, la pays de décès, le département de décès, la commune de décès et la mention en tant que mort pour la France".

Source: Data.gouv.fr [https://www.data.gouv.fr/fr/datasets/memorial-virtuel-des-morts-pour-la-france-de-nancy-lors-des-differents-conflits-militaires/]></text>

## *Nous aimerions raconté leur histoire!!!

Après avoir nettoyer nos données dans OpenRefine, nous les avons importées dans Flourish pour les visualiser. Nous avons dans un premier temps cherché à savoir le corps armés qui est le plus important (en terme de quantité) et voici le résultat :

<iframe style="width: 50vw; height: 50vh; border: none;" src="visualisation/5122962"><script src="https://public.flourish.studio/resources/embed.js"></iframe>

Voici leurs commune de naissance:

<iframe title="Lieu de naissance" aria-label="Carte" id="datawrapper-chart-LjZFl" src="https://datawrapper.dwcdn.net/LjZFl/1/" scrolling="no" frameborder="0" style="border: none;" width="600" height="620"></iframe>

## Liste des fromages français

<p align="default">Ce jeu de données réunit la liste de 338 spécialités de fromages françaises.Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public.com</p>

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)
<iframe style="width: 50vw; height: 50vh; border: none;" src="https://data.opendatasoft.com/chart/embed/camembert0/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>
<iframe style="width: 50vw; height: 50vh; border: none;"src="https://data.opendatasoft.com/chart/embed/radar/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>


## Requête permettant d'afficher la liste des identifiants des peintures de Monet et ses lieux de conservation
```sparql
SELECT DISTINCT ?peinture WHERE {
  ?peinture wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296.
}
```

## Résultat

<iframe style="width: 50vw; height: 50vh; border: none;"  src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fpeinture%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Requête permettant d'afficher les lables et les images associés

```sparql

#defaultView:ImageGrid
SELECT DISTINCT ?peinture ?peintureLabel ?image WHERE {
  ?peinture wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296.
  OPTIONAL { ?peinture wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]". }
}

```
## Résultat
<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Fpeinture%20%3FpeintureLabel%20%3Fimage%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%20%20OPTIONAL%20%7B%20%3Fpeinture%20wdt%3AP18%20%3Fimage.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Requête permettant d'afficher les collections/lieux de conservation

```sparql

SELECT DISTINCT ?peinture ?peintureLabel ?image ?collection WHERE {
  ?peinture wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296.
  OPTIONAL {
    ?peinture wdt:P18 ?image;
      (wdt:P195/(wdt:P361*)) ?collection.
  }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]". }
}

```
## Résultat

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fpeinture%20%3FpeintureLabel%20%3Fimage%20%3Fcollection%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%20%20OPTIONAL%20%7B%0A%20%20%20%20%3Fpeinture%20wdt%3AP18%20%3Fimage%3B%0A%20%20%20%20%20%20%28wdt%3AP195%2F%28wdt%3AP361%2a%29%29%20%3Fcollection.%0A%20%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%7D%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Le nombre de Monet dans chaque collection/lieux de conservation et les afficher par ordre décroissant 

```sparql

#defaultView:BarChart
SELECT DISTINCT ?collectionLabel (COUNT(?peinture) AS ?count) WHERE {
  ?peinture wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296.
  OPTIONAL { ?peinture (wdt:P195/(wdt:P361*)) ?collection. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]". }
}
GROUP BY ?collectionLabel
ORDER BY DESC (?collection)

```
## Résultat

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%0A%23defaultView%3ABarChart%0ASELECT%20DISTINCT%20%3FcollectionLabel%20%28COUNT%28%3Fpeinture%29%20AS%20%3Fcount%29%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%20%20OPTIONAL%20%7B%20%3Fpeinture%20%28wdt%3AP195%2F%28wdt%3AP361%2a%29%29%20%3Fcollection.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%7D%0AGROUP%20BY%20%3FcollectionLabel%0AORDER%20BY%20DESC%20%28%3Fcollection%29" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Requête permettant d'afficher la grille d’images des lions

```sparql

SELECT ?item ?itemLabel ?image WHERE {
  ?item wdt:P31 wd:Q140.
  OPTIONAL { ?item wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

```
## Résultat

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#SELECT%20%3Fitem%20%3FitemLabel%20%3Fimage%20WHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ140.%0A%20%20OPTIONAL%20%7B%20%3Fitem%20wdt%3AP18%20%3Fimage.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>
