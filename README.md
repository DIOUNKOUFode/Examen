
## Liste des fromages français
<p align="center">Ce jeu de données réunit la liste de 338 spécialités de fromages françaises.Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public.com</p>

<p align="center"><iframe frameborder="0" width="400" height="300" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)</p>
<p align="center"><iframe src="https://data.opendatasoft.com/chart/embed/camembert0/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe></p>
<p align="center"><iframe src="https://data.opendatasoft.com/chart/embed/radar/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe></p>


## Requête permettant d'afficher la liste des identifiants des peintures de Monet et ses lieux de conservation
```sparql
SELECT DISTINCT ?peinture WHERE {
  ?peinture wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296.
}
```

## Le résultat de ma requête
<p align="center">https://query.wikidata.org/sparql?query=SELECT%20DISTINCT%20%3Fpeinture%20WHERE%20%7B%0A%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%3B%0A%20%20%20%20wdt%3AP170%20wd%3AQ296.%0A%7D</p>


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

## Requête permettant d'afficher la grille d’images des lions

```sparql

SELECT ?item ?itemLabel ?image WHERE {
  ?item wdt:P31 wd:Q140.
  OPTIONAL { ?item wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

```
