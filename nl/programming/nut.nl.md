{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "bestand", "extensie", "bestandsindeling", "NUT-programmeertaal", "Programmeergids", "NUT-voorbeeld", "NUT-bestandsindeling", "eekhoorntaal", ".nut-extensiebestand ", "NUT-bestanden" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Eekhoorn Taalbestand",
  "description":"Meer informatie over de NUT-bestandsindeling en API's die NUT-bestanden kunnen maken en openen.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Wat is een NUT-bestand?

De NUT verwijst naar het NUT Open Container Format-bestand. Dit NUT-bestandsformaat behoort tot de programmeertaal die bekend staat als Squirrel. Het is een objectgeoriënteerde programmeertaal van hoog niveau en imperatief die voornamelijk wordt gebruikt in embedded systemen en videogames.

De eekhoorntaal wordt beschouwd als een lichtgewicht scripttaal die eenvoudig kan worden aangepast aan de grootte en bandbreedte. Het heeft het voordeel van automatisch tellen van referenties en het beheer van afval in het geheugen.

De syntaxis van de eekhoorntaal trekt de ontwikkelaars aan omdat deze C-achtig is en de functie van scripttaal omvat. Maar toch heeft het voor dit doel veel minder voordelen in vergelijking met andere, meer populaire programmeertalen.



## Korte geschiedenis ##

Het werd ontworpen door Alberto Demichelis in 2003. Een stabiele versie van deze taal werd echter uitgebracht in 2016. Het werd ontworpen onder de licentie van zlib/libpng. In 2010 is de licentie gewijzigd en overgedragen aan MIT. Deze taal wordt beschouwd als een geïnspireerde versie van [LUA](/nl/programming/lua/) (programmeertaal). Er is een lijst met suggesties voor de voormalige taal op de website die door Alberto is ontworpen om het voordeliger te maken.


## Technische specificatie ##

De functie en specificaties van de eekhoorntaal zijn veelvoudig. Het biedt de mogelijkheid van dynamisch typen, eigendom van delegatie, verschillende toepassingen van klassen en interfaces. De syntaxis van deze taal heeft een overeenkomst met de syntaxis van de C-taal. Toepassingen zoals Enduro/X (een clustertoepassingsserver) gebruiken deze taal. Omdat Squirrel ook voor videogames wordt gebruikt, zijn sommige daarvan OpenTTD, GTA IV, enz.

De stabiele versie van de taal is 3.0.7. Een toolkit die bekend staat als MirthKit gebruikt de programmeertaal Squirrel om een open-source en platformonafhankelijk platform te bieden voor tweedimensionale games. De aard van deze taal is dynamisch en de meeste functies zijn vergelijkbaar met [Python](/nl/programming/py/), LUA, enz. Het omvat ook de implementatie van op registers gebaseerde VM. De prestaties van Squirrel zijn langzamer in vergelijking met LUA.

Er is ook een ander bestandstype met de extensie ".nut". Daarom moet u naar de grootte van het bestand kijken om te zien welk NUT-bestand u heeft. NUT-bestanden met eekhoornscript zijn meestal kleiner dan 1 MB, terwijl NUT-videobestanden meestal groter zijn dan 1 MB.


## Voorbeeld van NUT-bestandsindeling ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Referentie ##

* [NUT - door Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



