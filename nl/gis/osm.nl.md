{
  "date" : "2019-10-11",
  "keywords" :[ "osm-bestand", "wat is een osm-bestand", "bestand", "osm-voorbeeld", "osm-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap-bestandsindeling",
  "description":"Meer informatie over de bestandsindeling van OSM en API's die OSM-bestanden kunnen maken en openen.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een OSM-bestand?

OpenStreetMap (OSM) is een enorme verzameling vrijwillige geografische informatiearchieven in verschillende soorten bestanden, waarbij verschillende coderingsschema's worden gebruikt om deze gegevens in bits en bytes om te zetten. OSM is een gezamenlijke inspanning om een gratis bewerkbare wereldkaart te maken. De primaire output van deze gezamenlijke inspanning zijn geografische gegevens in plaats van de kaart zelf. De beperkingen op het gebruik of de beschikbaarheid van geografische informatie over een groot deel van de wereld leiden tot de noodzaak om een OSM te creëren. De gegevens die beschikbaar zijn van OSM zijn klaar om Google Maps te vervangen voor klassieke toepassingen (Facebook, Craigslist enz.) en standaardgegevens voor toepassingen van de GPS-ontvanger.^^ ^^Hoewel de gegevenskwaliteit over de hele wereld divers is, kunnen OpenStreetMap-gegevens gemakkelijk worden vergeleken met patenten data bronnen.

## Korte geschiedenis ##

Geïnspireerd door het succes van Wikipedia, creëerde Steve Coast, een Britse ondernemer, in 2004 dit community-based wereldkaartproject in het VK. Hij richtte zich aanvankelijk op het in kaart brengen van het Verenigd Koninkrijk. OpenStreetMap Foundation werd voor het eerst opgericht in april 2006 om de ontwikkeling, uitbreiding en verspreiding van gratis geospatial voor iedereen te ondersteunen. In december 2006 hielp Yahoo OpenStreetMap met zijn luchtfotografie voor de productie van kaarten. Volledige weggegevens voor Nederland en hoofdweggegevens voor India en China werden in april 2007 aan OSM toegevoegd door Automotive Navigation Data (AND). In december 2007 was Oxford University de meest prominente organisatie die OpenStreetMap-gegevens integreerde in hun hoofdwebsite. Sindsdien dragen meer dan 2 miljoen geregistreerde gebruikers gegevens bij aan dit project met behulp van GPS-apparaten, luchtfotografie en handmatige enquêtes. Deze door de gemeenschap bijgedragen gegevens worden beschikbaar gesteld onder de Open Database-licentie. Een in Engeland geregistreerde non-profitorganisatie OpenStreetMap Foundation onderhoudt de OSM-site.

## OSM-bestandsindeling ##

Er zijn veel manieren en bestandsindelingen om geografische gegevens op te slaan, maar de **OSM**-bestandsindeling is beperkt tot OpenStreetMap. OSM is een speciaal ontworpen standaardformaat dat bedoeld is om gemakkelijk over het internet te worden getransporteerd. Een gestructureerd geordend formaat, gecodeerd in XML, vormt een .osm-bestand. In OpenStreetMap zijn er vier spilelementen om de topologische gegevensstructuur op te slaan:

{{< figure src="../OSM.png" alt="OSM-bestandsindeling" >}}


|Knooppunten|Wegen|Relaties|Tags
---|---|---|---|
|<ul><li> Vertegenwoordigt de geografische positie die is opgeslagen als paren van een breedtegraad en een lengtegraad.</li><li> Wordt gebruikt om kaartkenmerken weer te geven zonder grootte, zoals bergtoppen.</li></ul> |<ul><li> Gesorteerde lijsten met knopen, die een polylijn of een polygoon aanduiden</li><li> Vertegenwoordigen lineaire kenmerken zoals wegen en rivieren, en zones, zoals parkeerplaatsen, oerwouden en parken.</li></ul> |<ul><li> Gesorteerde lijsten van knooppunten en wegen vertegenwoordigen hun relatie zoals barrières en bochten op wegen, snelwegen overspannen verschillende bestaande wegen en gebieden met gaten.</li></ul> |<ul><li> Bewaar metadata over de kaartobjecten.* Altijd gekoppeld aan een knoop, weg of relatie</li></ul>


Tags worden gebruikt om fysieke kenmerken op de grond (gebouwen en wegen enz.) in OpenStreetMap te karakteriseren. Elke tag heeft betrekking op een geografisch kenmerk van het kenmerk dat wordt vertegenwoordigd door dat specifieke knooppunt of die specifieke relatie. In dit gratis tagging-systeem kan een onbeperkt aantal attributen worden opgenomen in een kaart om een kenmerk te beschrijven. Specifieke sleutel- en waardecombinaties die door geregistreerde gebruikers worden onderschreven, fungeren als informele standaarden voor de veelgebruikte tags. Er kunnen echter nieuwe tags worden gemaakt wanneer nieuwe aspecten het nodig hebben om eerder niet-toegewezen kenmerken van de kenmerken te analyseren. De meeste functies gebruiken slechts een klein aantal tags voor beschrijving.

OSM gebruikt drie soorten bestanden om de belangrijkste gegevens op te slaan.

OSM behandelt al deze bestanden met de informatie over hun opmaakdetails. Maar dezelfde interne objecten worden door deze bestanden geproduceerd. Voor gegevensbestanden is de zichtbare vlag op OSM-objecten altijd waar, wat niet het geval is voor geschiedenis- en wijzigingsbestanden.

In algemeen gebruik is er een diversiteit aan OSM-bestandsindelingen. Bestandsindelingen definiëren de inhoudcodering op schijf of draad in bits en bytes. OSM kan maximaal van deze formaten lezen en schrijven.

**XML**

Het originele OSM-formaat is gebaseerd op XML. De retourgegevens van de hoofddatabase-API van OSM zijn in XML-indeling.

**PBF**

Protocol Buffers-codering staat op binair formaat en is een van de meest compacte formaten.

**O5M/O5C**

Op binair formaat gebaseerd eenvoudiger formaat, maar relatief minder gebruikt. OSM kan dit formaat lezen maar niet schrijven.

**OPL**

Een eenvoudig formaat dat wordt voorgesteld om te gebruiken met standaard UNIX-opdrachtregelprogramma's. Dicht bij CSV-bestanden, staat één OSM-entiteit op één regel toe.

**DEBUG**

Een op tekst gebaseerd formaat dat bedoeld is om te maken voor foutopsporing. De OSM kan dit formaat schrijven, maar niet lezen.

**ZWARTGAT**

Een dummy-indeling die alle gegevens weggooit. De OSM kan dit formaat schrijven maar niet lezen.

## OSM-gegevensopslag ##

De belangrijkste **PostgreSQL**-database van OSM bewaart de hoofdkopie van de gegevens van OSM met de extensie PostGIS. Voor elke gegevensprimitief houdt de hoofddatabase een tabel bij waarvan de rijen individuele objecten opslaan. Alle bewerkingen werken deze database bij en alle andere formaten worden gevormd met behulp van deze database. Er worden talloze downloadbare databasepools gemaakt om gegevens van de ene plaats naar de andere over te dragen. Twee formaten, een met XML en een andere met behulp van Protocol Buffer Binary Format (PBF) definiëren deze pools. De volledige gegevens worden opgeslagen in een bestand genaamd planet.osm

## Compressie in OSM-bestanden ##

Op tekst gebaseerde formaten (XML, OPL en Debug) gebruiken optioneel gzip- of bzip2-compressie.

## Referenties ##

* [OSM-handleiding voor bestandsindelingen](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#Geschiedenis)
* [Leer OSM](https://learnosm.org/en/osm-data/getting-data/)

