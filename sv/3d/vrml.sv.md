{
  "date" : "2019-10-11",
  "keywords" :[ "vrml-fil", "vrml-filformat", "vad är en vrml-fil", "fil", "vrml-exempel", "vrml-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VRML-filformat",
  "description":"Läs mer om VRML-filformat och API:er som kan öppna och skapa VRML-filer.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en VRML fil?
Virtual Reality Modeling Language (VRML) är ett filformat för representation av interaktiva [3D](/sv/3d/) världsobjekt över World Wide Web (www). Den finner sin användning i att skapa tredimensionella representationer av komplexa scener som illustrationer, definitioner och presentationer av virtuell verklighet. Formatet har ersatts av [X3D](/sv/3d/x3d/). Många 3D-modelleringsapplikationer kan spara objekt och scener i VRML-format.

## VRML filformat

VRML är ett textfilformat som specificerar information som hörn och kanter på en 3D-polygon tillsammans med information som ytfärg, UV-mappade texturer, glans, transparens och så vidare. Den har förmågan att representera statiska och animerade objekt förutom att ha hyperlänkar till andra medier som ljud, filmer och bilder. Detta gör det möjligt att öppna hyperlänkade element när användaren klickar på dessa objekt.

TVRML-filer i vanlig terminologi kallas "världar" och har tillägget .wrl. Den textmässiga karaktären hos dessa filer gör det möjligt att minska filstorleken med hjälp av komprimeringsformat som gzip, vilket gör dem mer gynnsamma för snabb överföring över internet. Filformatspecifikationerna för [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) fungerar som utvecklarens referens för att skapa applikationer som är kompatibla för att läsa/skriva dessa filer.

## Designkriterium ##

Syftet och utformningen av VRML kretsar kring följande krav.

* **Authorability** - Gör det möjligt att utveckla applikationsgeneratorer och redigerare och importera data från andra industriella format
* **Fullständighet** - Tillhandahåller all information som behövs för implementering och adresserar en komplett funktionsuppsättning för bred branschacceptans
* **Komposerbarhet** - Möjligheten att använda delar av VRML i kombination och därmed tillåta återanvändning.
* **Utökbarhet** - Möjligheten att lägga till nya element.
* **Implementerbarhet** -Kan implementeras på ett brett spektrum av system.
* **Multi-användarpotential** - Bör inte utesluta implementeringen av multi-användarmiljöer.
* **Ortogonalitet** - Elementen i VRML bör vara oberoende av varandra, eller så bör eventuella beroenden vara strukturerade och väldefinierade.
* **Prestanda** - Elementen bör utformas med tonvikt på interaktiv prestanda på en mängd olika datorplattformar.
* **Skalbarhet** - Elementen i VRML bör utformas för oändligt stora kompositioner.
* **Standardpraxis** - Endast de element som återspeglar befintlig praxis, som är nödvändiga för att stödja befintlig praxis eller som är nödvändiga för att stödja föreslagna standarder bör standardiseras.
* **Välstrukturerat** - Ett element ska ha ett väldefinierat gränssnitt och ett enkelt uttryckt ovillkorligt syfte. Multifunktionella element och biverkningar bör undvikas.

## Referenser ##

* [VRML - av Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [VRML v 2.0 filformatspecifikationer](http://gun.teipir.gr/VRML-amgem/spec/index.html)

