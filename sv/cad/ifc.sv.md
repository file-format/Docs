{
  "date" : "2020-03-16",
  "keywords" :[ "IFC-fil", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om IFC-filformat och API:er som kan skapa och öppna IFC-filer.",
  "title" :"IFC-filformat",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en IFC fil?

Filer med IFC-tillägg hänvisar till filformatet Industry Foundation Classes (IFC) som fastställer internationella standarder för att importera och exportera byggnadsobjekt och deras egenskaper. Detta filformat ger interoperabilitet mellan olika programvaror. Specifikationer för detta filformat är utvecklade och underhållna av buildingSMART International som dess datastandard. Det yttersta målet med IFC-filformat är att förbättra kommunikation, produktivitet, leveranstid och kvalitet under en byggnads livscykel.

På grund av de etablerade standarderna för vanliga objekt i byggbranschen, minskar det förlusten av information under överföring från en applikation till en annan. IFC kan hålla data för geometri, beräkning, kvantiteter, anläggningsförvaltning, prissättning etc. för många olika yrken (arkitekt, el, VVS, konstruktion, terräng etc.).

## Kortfattad bakgrund ##

IFC-initiativet togs 1994 av Autodesk för att stödja integrerad applikationsutveckling och inkluderade företag som Honeywell, Butler Manufacturing och AT&T. 1995 öppnades medlemskapet för alla och namnet ändrades till International Alliance for Interoperability. Den ideella avsikten var att publicera Industry Foundation Class (IFC) som en AEC-produktmodell. 2005 ändrades namnet igen och buildSMART behåller det nu.

## IFC-filformat ##

IFC-filformatet har genomgått flera förändringar under det senaste för att nå filformatspecifikationerna v4. Flera mindre förändringar inträffade då och då och som har gjorts till en del av specifikationerna som tillägg. Nedan följer en lista över olika versioner av filspecifikationer som har gjorts offentliga under det förflutna.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (mars 2013) ifcXML2x3 (juni 2007)
* IFC2x3 (februari 2006) ifcXML2 för IFC2x2 add1 (RC2)
* IFC2x2 Tillägg 1 (juli 2004)ifcXML2 för IFC2x2 (RC1)
* IFC 2x2IFC 2x Tillägg 1ifcXML1 för IFC2x och
* IFC2x Tillägg 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

De senaste versionerna av IFC-filformatspecifikationerna är alltid tillgängliga på buildingSMARTs webbplats och utvecklare bör konsultera dessa för alla typer av applikationer de planerar att utveckla. När den här artikeln skrevs är specifikationerna för version 4 de senaste tillgängliga online.

### IFC-datafilformat ###

IFF-filformat stöder datautbyte mellan applikationer som använder olika format enligt listan nedan:

**IFC:** Detta är standardutbytesformatet för IFC och använder STEP fysiska filstruktur enligt ISO 10303-21. Det här filformatet har filtillägget .ifc och är det mest använda IFC-formatet.

**IFC-XML:** Det är en XML-filformatsversion av IFC som kan genereras direkt av den sändande applikationen enligt ISO 10303-28-strukturen, även kallad STEP-XML. IFC-XML-filformatet anses lämpligt för interoperabilitet mellan XML-verktyg. Jämfört med IFC-filformatet är IFC-XML 300-400 % större i storlek.

**IFC-ZIP:** Det är en [ZIP](/sv/compression/zip/) komprimerad version av IFC eller IFC-XML där den av dessa filer är huvudkatalogen i zip-arkivet. Det här formatet komprimerar en .ifc med 60-80 % och en .ifc XML-fil med 90-95 %.

### IFC-arkitektur ###

IFC-specifikationen inkluderar termer, begrepp och dataspecifikationsobjekt som härrör från användning inom discipliner, branscher och yrken inom bygg- och anläggningsförvaltningsindustrin. Termer och begrepp använder de vanliga engelska orden, dataposterna i dataspecifikationen följer en namnkonvention.

datapostnamnen för typer, entiteter, regler och funktioner börjar med prefixet "Ifc" och fortsätter med de engelska orden i CamelCase-namnkonventionen (ingen understreck, första bokstaven i ord med versaler); attributnamnen inom en enhet följer CamelCase-namnkonventionen utan prefix; egenskapsuppsättningsdefinitionerna som är en del av denna standard börjar med prefixet "Pset_" och fortsätter med de engelska orden i CamelCase-namnkonventionen; kvantitetsuppsättningsdefinitionerna som ingår i denna standard börjar med prefixet "Qto_" och fortsätter med de engelska orden i CamelCases namnkonvention.

Dataschemaarkitekturen i IFC definierar fyra konceptuella lager, varje enskilt schema tilldelas exakt ett konceptuellt lager.

**Resurslager** — det lägsta lagret inkluderar alla individuella scheman som innehåller resursdefinitioner, dessa definitioner inkluderar inte en globalt unik identifierare och ska inte användas oberoende av en definition som deklareras i ett högre lager;

**Kärnlager** — nästa lager inkluderar kärnschemat och kärnextensionsschemana, som innehåller de mest allmänna enhetsdefinitionerna, alla enheter definierade i kärnskiktet eller ovan har ett globalt unikt ID och eventuellt ägare och historikinformation;

**Interoperabilitetsskikt** — nästa skikt innehåller scheman som innehåller enhetsdefinitioner som är specifika för en allmän produkt-, process- eller resursspecialisering som används inom flera discipliner, dessa definitioner används vanligtvis för utbyte mellan domäner och delning av konstruktionsinformation;

**Domänskikt** — det högsta skiktet inkluderar scheman som innehåller enhetsdefinitioner som är specialiseringar av produkter, processer eller resurser som är specifika för en viss disciplin, dessa definitioner används vanligtvis för utbyte inom domänen och delning av information.

## Referenser ##

* [Industry Foundation Classes - Av Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

