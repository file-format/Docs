{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language","file", "extension", "file format", "Maya 3D", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded Language File Format",
  "description":"Meer informatie over MEL-bestandsindelingen en API's die MEL-bestanden kunnen maken en openen.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Wat is een MEL-bestand?

Een bestand met de extensie .mel (Maya Embedded Language) is een scripttaal die door Autodesk Maya wordt gebruikt om grafische interfaces te maken. Hiermee kunt u het maken van grafische elementen automatiseren met behulp van uitvoerbare scripts naast de grafische interface van Maya. MEL stelt u in staat om grafische interfaces te maken zonder te leren programmeren. Dit wordt bereikt door macro's en aangepaste acties te maken die repetitieve taken versnellen. Met deze procedures en scripts kunt u aangepaste modellering, animaties, dynamiek en taakweergave maken. Autodesk Maya 2020 kan worden gebruikt om de inhoud van een EML-bestand te openen en te bekijken.

## MEL-bestandsindeling - Meer informatie

Een [referentiehandleiding](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) van een programmeur is beschikbaar voor ontwikkelaars in Maya's documentatiesectie. MEL is gebaseerd op shellscripting-commando's, vergelijkbaar met UINX, om dingen te bereiken. De op scripts gebaseerde commando's maken het irrelevant voor conventioneel en objectgeoriënteerd programmeren (OOP), wat resulteert in geen gebruik van datastructuren, aanroepen van functies of het gebruik van OOP zoals in andere talen.

Enkele belangrijke punten over MEL zijn als volgt.

`Opmerkingen` - Elke instructie in MEL moet eindigen met een puntkomma (;), zelfs aan het einde van een blok.

`Waarden retourneren` - Als u een uitdrukking opgeeft die een waarde retourneert, wordt de waarde niet automatisch in MEL afgedrukt. In plaats daarvan veroorzaakt het een fout.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Opdrachten voor maken, bewerken en verwijderen` - Dezelfde opdracht wordt gebruikt om dingen te maken, dingen te bewerken of informatie over bestaande dingen op te vragen. Een vlag bepaalt echter wat (maken, bewerken of opvragen) de opdracht doet.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - Functiesyntaxis retourneert automatisch een waarde. Om een retourwaarde te krijgen met behulp van de opdrachtsyntaxis, moet u de opdracht tussen aanhalingstekens plaatsen.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referenties

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

