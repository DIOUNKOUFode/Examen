
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

## Le résultat1 de ma requête
<iframe frameborder="0" width="600" height="600"; src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fpeinture%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe></p>

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
## Le résultat2 de ma requête
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
## Le résultat3 de ma requête

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fpeinture%20%3FpeintureLabel%20%3Fimage%20%3Fcollection%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%20%20OPTIONAL%20%7B%0A%20%20%20%20%3Fpeinture%20wdt%3AP18%20%3Fimage%3B%0A%20%20%20%20%20%20%28wdt%3AP195%2F%28wdt%3AP361%2a%29%29%20%3Fcollection.%0A%20%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%7D%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Requête permettant de compter le nombre de Monet dans chaque collection/lieux de conservation et les afficher par ordre décroissant 

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
## Le résultat4 de ma requête

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%0A%23defaultView%3ABarChart%0ASELECT%20DISTINCT%20%3FcollectionLabel%20%28COUNT%28%3Fpeinture%29%20AS%20%3Fcount%29%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%20%20OPTIONAL%20%7B%20%3Fpeinture%20%28wdt%3AP195%2F%28wdt%3AP361%2a%29%29%20%3Fcollection.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22.%20%7D%0A%7D%0AGROUP%20BY%20%3FcollectionLabel%0AORDER%20BY%20DESC%20%28%3Fcollection%29" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

## Requête permettant d'afficher la grille d’images des lions

```sparql

SELECT ?item ?itemLabel ?image WHERE {
  ?item wdt:P31 wd:Q140.
  OPTIONAL { ?item wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

```
## Le résultat5 de ma requête

<iframe style="width: 50vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#SELECT%20%3Fitem%20%3FitemLabel%20%3Fimage%20WHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ140.%0A%20%20OPTIONAL%20%7B%20%3Fitem%20wdt%3AP18%20%3Fimage.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0A" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>
