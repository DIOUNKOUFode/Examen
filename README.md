##

We're so excited that you've decided to create a new project! Now that you're here, let's make sure you know how to get the most out of GitHub Projects.
- [x] <iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)
- [x] Give your project a name
- [ ] Press the <kbd>?</kbd> key to see available keyboard shortcuts
- [ ] Add a new column
- [ ] Drag and drop this card to the new column
- [ ] Search for and add issues or PRs to your project
- [ ] Manage automation on columns
- [ ] [Archive a card](https://docs.github.com/articles/archiving-cards-on-a-project-board/) or archive all cards in a column


Ce jeu de données réunit la liste de 338 spécialités fromagères françaises. 
Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public


<iframe src="https://data.opendatasoft.com/chart/embed/camembert0/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>
<iframe src="https://data.opendatasoft.com/chart/embed/nuage_de_point/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>
<iframe src="https://data.opendatasoft.com/chart/embed/radar/?&static=false&datasetcard=false" width="400" height="300" frameborder="0"></iframe>

#Afficher sous forme de grille d’images, les tableaux qui dépeignent un lion.

SELECT ?item ?itemLabel ?image
     #defaultView:ImageGrid #-->Vue par défaut 
WHERE
{
	?item wdt:P31 wd:Q140. 
	OPTIONAL {
		?item wdt:P18 ?image
	} 
	SERVICE wikibase:label { bd:serviceParam wikibase:language "en" }
}                       

