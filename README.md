## Welcome to Fodé's Page

Ce jeu de données réunit la liste de 338 spécialités fromagères françaises. 
Il comprend : le nom du fromage, le département de fabrication, l'URL de la page Wikipédia française, l'URL de la page Wikipédia anglaise quand elle existait, la photographie quand elle existait, les coordonnées géographiques du département de fabrication, Identifiant du jeu de données: fromagescsv-fromagescsv@public

<iframe frameborder="0" width="800" height="600" src="https://data.opendatasoft.com/map/embed/filtre_en_polygone/?&static=false&scrollWheelZoom=false"></iframe>)
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
