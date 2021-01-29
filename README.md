## Mémorial virtuel des morts pour la France :

<iframe src="story/743592"><script src="https://public.flourish.studio/resources/embed.js"></iframe>
                                                                                                               
Dans la cadre de notre projet de fin d'étude du [Cours d'analyse de données et de dataVisualisation], nous nous sommes intéressés au jeu de données issue d'un service public certifié et dont la mise à disposition a été rendu possible par l'excellent travail mené par la ville de Nancy: il s'agit du Mémorial virtuel des morts pour la France de Nancy lors des différents conflits militaires.
Le choix de ce jeu, tant cher, aux yeux de ses initiateurs ne se justifie point par la richesse des données qu'elle contient mais par l'immense valeur que réprésentent ces hommes.
En ce sens, ce Mémorial virtuel des morts pour la France de Nancy donne vie à ces vaillant.e.s hommes qui ont garanti des vies à une époque, pour la génération future [celle-là même qui tente aujourd'hui de les immortaliser].
Cette histoire est blindée de sens, d'émotion, de leçon mais surtout d'énormes sacrifices pour une cause commune. 

Ainsi, raporte-t-on : "c'est pour honorer la mémoire de ces milliers de soldats et transmettre aux générations futures la grandeur de leur sacrifice, que la Ville de Nancy a souhaité initier le recensement de ses Morts pour la France".
Un site Internet a d'ailleur été créé : http://memorial.nancy.fr. L'idée étant d'élever ces héros à leur valeur : "Des fiches individuelles ont été réalisées afin d'illustrer le parcours de ces hommes. Sur chacune de ces fiches, figure l'état-civil des victimes, leur grade, l'unité à laquelle elles appartenaient, leur lieu de naissance, de dernière résidence (si celle-ci est connue) et selon les cas, leur portrait photographique. Leur contenu dépend néanmoins des sources parvenues jusqu'à ce jour".

Initié à l'occasion des commémorations du Centenaire de la Grance Guerre et edifié après la Première Guerre mondiale dans le cimetière du Sud, à proximité d'un carré militaire, les noms des Nancéiens morts pour la France n'ont cependant jamais été inscrits.
Pour ces initiateurs, "cette démarche [...], sera poursuivie jusqu'aux conflits les plus récents, afin d'apporter à cette démarche mémorielle l'unité qui lui donnera tout son sens".

Par ailleurs, "l'application de la loi du 28 février 2012, demandant l’inscription des noms des morts pour la France sur les monuments aux morts communaux, les morts, militaires ou civils, figurant dans cette liste doivent être natifs de Nancy ou y avoir résidé avant leur décès. Ils doivent également avoir reçu la mention « Mort pour la France », créée par la loi du 2 juillet 1915, qui honore la mémoire des victimes de guerre".

Par conséquent, "les données proposées ci-dessous présentent pour chaque soldat le nom du conflit, le nom du soldat, les prénoms, le grade, le corps, le numéro de matricule et le bureau lié, la date de naissance, le département de naissance, la commune de naissance, la date de décès, la pays de décès, le département de décès, la commune de décès et la mention en tant que mort pour la France".
Nous n'exploiteront pas dans le cadre de ce projet les données la table des sigles explicative qui accompagnes les données.  

Source: Data.gouv.fr [https://www.data.gouv.fr/fr/datasets/memorial-virtuel-des-morts-pour-la-france-de-nancy-lors-des-differents-conflits-militaires/]></text>



Après avoir nettoyer nos données dans OpenRefine, nous les avons importées dans Flourish pour les visualiser. Nous avons dans un premier temps cherché à savoir le corps armés qui est le plus représentatif dans ce mémorial. :

<iframe style="width: 50vw; height: 50vh; border: none;" data-src="visualisation/5122962"><script src="https://public.flourish.studio/resources/embed.js"></iframe>
                                                                                                                                                
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
