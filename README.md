# Exerice - Opendatasoft

## Liste des fromages Français

### Le jeu de données utilisé est disponible ci-dessous :

<iframe src="https://data.opendatasoft.com/explore/embed/dataset/fromagescsv-fromagescsv@public/table/?disjunctive.fromage&location=5,46.66619,2.91208&basemap=jawg.streets&dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6ImZyb21hZ2VzY3N2LWZyb21hZ2VzY3N2QHB1YmxpYyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuZnJvbWFnZSI6dHJ1ZX19LCJjaGFydHMiOlt7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiJyYW5nZS1BY2NlbnQifV0sInhBeGlzIjoiZGVwYXJ0ZW1lbnQiLCJtYXhwb2ludHMiOjUwLCJzb3J0IjoiIiwic2VyaWVzQnJlYWtkb3duIjoibGFpdCIsInNlcmllc0JyZWFrZG93blRpbWVzY2FsZSI6IiJ9XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>

### Quel type de lait est le plus utilisé en fonction du département ?

<iframe src="https://data.opendatasoft.com/explore/embed/dataset/fromagescsv-fromagescsv@public/analyze/?disjunctive.fromage&location=5,46.66619,2.91208&basemap=jawg.streets&dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6ImZyb21hZ2VzY3N2LWZyb21hZ2VzY3N2QHB1YmxpYyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuZnJvbWFnZSI6dHJ1ZX19LCJjaGFydHMiOlt7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiJyYW5nZS1BY2NlbnQifV0sInhBeGlzIjoiZGVwYXJ0ZW1lbnQiLCJtYXhwb2ludHMiOjUwLCJzb3J0IjoiIiwic2VyaWVzQnJlYWtkb3duIjoibGFpdCIsInNlcmllc0JyZWFrZG93blRpbWVzY2FsZSI6IiJ9XSwidGltZXNjYWxlIjoiIiwiZGlzcGxheUxlZ2VuZCI6dHJ1ZSwiYWxpZ25Nb250aCI6dHJ1ZX0%3D&static=false&datasetcard=false" width="800" height="600" frameborder="0"></iframe>

### Quelle est la région la plus diversifées en termes de fromages ?

<iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/varietes_de_fromages_par_departements/?&static=false&scrollWheelZoom=true"></iframe>



# SUITE DE L'EXERCICE

## Liste des fromages français
'''
<p color="red">Ce jeu de données réunit la liste de 338 spécialités de fromages françaises.Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public.com</p>

<p align="center"><iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)</p>
<iframe src="https://data.opendatasoft.com/chart/embed/camembert0/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>
<iframe src="https://data.opendatasoft.com/chart/embed/radar/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>

````sparql
## Requête permettant d'afficher la liste des identifiants des peintures de Monet et ses lieux de conservation

SELECT ?painting ?paintingLabel ?image WHERE {
  ?painting wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296;
    wdt:P18 ?image;
    wdt:P195 ?lieu.
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

## Requête permettant d'afficher la grille d’images des lions

SELECT ?item ?itemLabel ?image WHERE {
  ?item wdt:P31 wd:Q140.
  OPTIONAL { ?item wdt:P18 ?image. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}

## Par ordre descendant

SELECT ?painting ?paintingLabel ?image WHERE {
  ?painting wdt:P31 wd:Q3305213;
    wdt:P170 wd:Q296;
    wdt:P18 ?image;
    wdt:P195 ?lieu.
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
ORDER BY DESC(?sitelinks) 
````

