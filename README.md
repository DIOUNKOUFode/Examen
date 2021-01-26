

##Afficher sous forme de grille d’images, les tableaux qui dépeignent un lion.
...
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

