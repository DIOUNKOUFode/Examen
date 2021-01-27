## Exo sur Monet (Wikidata Query)

* Afficher juste les peintures de Monet 

```sparql

SELECT DISTINCT ?peinture WHERE {
    ?peinture wdt:P31 wd:Q3305213 ; # C'est une peinture
          wdt:P170 wd:Q296; # de Monet
}
```
### Résultat
<iframe style="width: 80vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fpeinture%20WHERE%20%7B%0A%20%20%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%20%3B%20%23%20C%27est%20une%20peinture%0A%20%20%20%20%20%20%20%20%20%20wdt%3AP170%20wd%3AQ296%3B%20%23%20de%20Monet%0A%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>


* Afficher en plus les labels et les images associées 

```sparql
#defaultView:ImageGrid
SELECT DISTINCT ?peinture ?peintureLabel ?image WHERE {
    ?peinture wdt:P31 wd:Q3305213 ; # C'est une peinture
          wdt:P170 wd:Q296; # de Monet
    OPTIONAL { ?peinture wdt:P18 ?image } # avec une image si possible
    SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]" }
                           }
```
### Résultat
<iframe style="width: 80vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3AImageGrid%0ASELECT%20DISTINCT%20%3Fpeinture%20%3FpeintureLabel%20%3Fimage%20WHERE%20%7B%0A%20%20%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%20%3B%20%23%20C%27est%20une%20peinture%0A%20%20%20%20%20%20%20%20%20%20wdt%3AP170%20wd%3AQ296%3B%20%23%20de%20Monet%0A%20%20%20%20OPTIONAL%20%7B%20%3Fpeinture%20wdt%3AP18%20%3Fimage%20%7D%20%23%20avec%20une%20image%20si%20possible%0A%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22%20%7D%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>

* Affichr les collections/lieux de conservation
```sparql
SELECT DISTINCT ?peinture ?peintureLabel ?image ?collection WHERE {
    ?peinture wdt:P31 wd:Q3305213 ; # C'est une peinture
          wdt:P170 wd:Q296; # de Monet
    OPTIONAL { ?peinture wdt:P18 ?image .
             ?peinture wdt:P195/wdt:P361* ?collection } # avec une image (si possible) et qui fait partie d'une collection si possible 
    SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]" }
                            }
```

Comment préciser que les lieux de conservation nous intéressent aussi?

### Résultat



* Compter le nombre de Monet dans chaque collection/lieux de conservation et les afficher par ordre décroissant 

```sparql
#defaultView:BarChart
SELECT DISTINCT ?collectionLabel (COUNT(?peinture) AS ?count) 

WHERE {
    ?peinture wdt:P31 wd:Q3305213 ; # C'est une peinture
          wdt:P170 wd:Q296; # de Monet
    OPTIONAL {?peinture wdt:P195/wdt:P361* ?collection } # fait partie d'une collection si possible 
    SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE]" }
                            }
GROUP BY ?collectionLabel                            
ORDER BY DESC(?collection)
```

### Résultat

<iframe style="width: 80vw; height: 50vh; border: none;" src="https://query.wikidata.org/embed.html#%23defaultView%3ABarChart%0ASELECT%20DISTINCT%20%3FcollectionLabel%20%28COUNT%28%3Fpeinture%29%20AS%20%3Fcount%29%20%0A%0AWHERE%20%7B%0A%20%20%20%20%3Fpeinture%20wdt%3AP31%20wd%3AQ3305213%20%3B%20%23%20C%27est%20une%20peinture%0A%20%20%20%20%20%20%20%20%20%20wdt%3AP170%20wd%3AQ296%3B%20%23%20de%20Monet%0A%20%20%20%20OPTIONAL%20%7B%3Fpeinture%20wdt%3AP195%2Fwdt%3AP361%2a%20%3Fcollection%20%7D%20%23%20fait%20partie%20d%27une%20collection%20si%20possible%20%0A%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%22%20%7D%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D%0AGROUP%20BY%20%3FcollectionLabel%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%0AORDER%20BY%20DESC%28%3Fcollection%29" referrerpolicy="origin" sandbox="allow-scripts allow-same-origin allow-popups" ></iframe>










## Datavisualisation des fromages français (OpenDataSoft)

Visualisation des données:

<iframe src="https://data.opendatasoft.com/explore/embed/dataset/fromagescsv-fromagescsv@public/table/?disjunctive.fromage&static=false&datasetcard=false" width="800" height="600" frameborder="0"></iframe>


Carte des fromages selon le département (cluster et choroplèthe)
<iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/carte_des_fromages_francais/?&static=false&scrollWheelZoom=false"></iframe>

Datavisualisation des fromages selon le type de lait
<iframe src="https://data.opendatasoft.com/chart/embed/?dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6ImZyb21hZ2VzY3N2LWZyb21hZ2VzY3N2QHB1YmxpYyIsIm9wdGlvbnMiOnsiZGlzanVuY3RpdmUuZnJvbWFnZSI6dHJ1ZSwidGltZXpvbmUiOiJFdXJvcGUvQmVybGluIn19LCJjaGFydHMiOlt7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJjb2x1bW4iLCJmdW5jIjoiQ09VTlQiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiIjNTY1NjU2In1dLCJ4QXhpcyI6ImxhaXQiLCJtYXhwb2ludHMiOjUwLCJzb3J0IjoiIiwic2VyaWVzQnJlYWtkb3duIjoiIiwic2VyaWVzQnJlYWtkb3duVGltZXNjYWxlIjoiIiwiY2F0ZWdvcnlDb2xvcnMiOnsiVmFjaGUiOiIjRTUzNTJEIiwiQ2hcdTAwRTh2cmUiOiIjRjdBRDg0IiwiQnJlYmlzIjoiI0ZCRTZDNiJ9fV0sInRpbWVzY2FsZSI6IiIsImRpc3BsYXlMZWdlbmQiOnRydWUsImFsaWduTW9udGgiOnRydWV9&static=false&datasetcard=false" width="800" height="600" frameborder="0"></iframe>



