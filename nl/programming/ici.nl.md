{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "bestand", "extensie", "bestandsformaat", "ICI-implementatie", "Programmeergids", "ici-voorbeeld", "ICI-programmeertaal", "modules van ICI", "gegevensmodel van ICI ", "documentatie van ICI", "ICI-taal"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Programmeertaalbestand",
  "description":"Meer informatie over ICI-bestandsindelingen en API's die ICI-bestanden kunnen maken en openen.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Wat is een ICI-bestand?

Een programmeertaal voor algemene doeleinden die wordt geïnterpreteerd en verschillende functies bevat, zoals dynamisch typen samen met de flexibele gegevenstypen, staat bekend als ICI-programmeertaal (geen acroniem). Het wordt beschouwd als vergelijkbaar met de taal [Perl](/nl/programmering/pl/). Deze ICI-taal omvat constructies voor flow control en bevat ook enkele operators van de C-taal. Het is geen objectgeoriënteerde taal, maar sommige functies van OOP kunnen worden bereikt door een specifieke overervingsmethode die bekend staat als superstructuren. Net als [C](/nl/programming/c), heeft deze ICI-programmeertaal dezelfde systeeminterface en een standaardbibliotheek voor ingebouwde functies.


## Korte geschiedenis ##

In de late jaren 1980 werd het ontwikkeld door Tim Long als een algemeen geïnterpreteerde programmeertaal. De meeste functies van deze taal zijn vergelijkbaar met C en het kan ook enkele functies bereiken door enkele speciale methoden toe te passen. Deze taal is eigendom van het publieke domein en is beschikbaar als een verkoopbare taal en niemand is verplicht te vermelden waar hij de broncode vandaan heeft. De documentatie van ICI valt onder het copyright van Canon Information System Research Australia.

## Technische specificatie ##

Er worden in deze taal twee verschillende gegevenstypen gebruikt. Deze twee zijn primitieve en geaggregeerde gegevenstypen. Beide bevatten verschillende uitdrukkingen volgens hun vooraf gedefinieerde samenstelling in de taal. Verschillende modules zoals geneste en subroutines worden door deze taal ondersteund. Omdat sommige eigenschappen vergelijkbaar zijn met Perl, is het strikt geïntegreerd met de reguliere expressies.

Sets zijn beperkt tot heterogeen en genest. Deze sets bieden ondersteuning voor veelgebruikte setbewerkingen zoals Union en Intersection enz. Het wordt meestal gebruikt als een taal omwille van de kernimplementatie voor applicaties die eigendom zijn van multinationale organisaties.

Bijna alle soorten programma's kunnen in deze taal worden geschreven en meestal zijn de specifieke programma's die complexe datastructuren bevatten, geschreven in de ICI-programmeertaal. Applicaties kunnen de ICI-implementatie zodanig betrekken dat ze erin zouden moeten worden geschreven. Functionele delen van de applicatie kunnen worden geïmplementeerd door de modules van ICI. De taal van ICI lijkt enigszins op C-taal, maar het datamodel van ICI is van een hoger niveau en verschilt met typen zoals woordenboeken (struct), sets, dynamische arrays, reguliere expressies en (echte) strings.


## Voorbeeld van ICI-bestandsindeling ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referentie ##

* [ICI-programmeertaal](http://atrn.org/ici/doc/ici.html)



