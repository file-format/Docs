{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "mhtml-bestand", "mhtml-bestandsindeling", "mhtml-bestandstype", "bestand", "type", "wat is een mhtml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML-bestand",
  "description":"Meer informatie over MHTML-bestandsindeling en API's die MHTML-bestanden kunnen maken en openen.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een MHTML-bestand?

Bestanden met de extensie MHTML vertegenwoordigen een archiefindeling voor webpagina's die door een aantal verschillende toepassingen kan worden gemaakt. Het formaat staat bekend als archiefformaat omdat het de webcode **[HTML](/nl/web/html/)** en bijbehorende bronnen in één bestand opslaat. Deze bronnen omvatten alles dat aan de webpagina is gekoppeld, zoals afbeeldingen, applets, animaties, audiobestanden enzovoort. MHTML-bestanden kunnen in verschillende toepassingen worden geopend, zoals Internet Explorer en Microsoft Word. Microsoft Windows gebruikt de MHTML-bestandsindeling voor het opnemen van scenario's van problemen die zijn waargenomen tijdens het gebruik van een toepassing op Windows die problemen oplevert. Het MHTML-bestandsformaat codeert de pagina-inhoud vergelijkbaar met de specificaties die zijn gedefinieerd in message/rfc822, wat e-mailgerelateerde specificaties in platte tekst zijn. De feitelijke specificaties van het formaat zijn zoals beschreven in [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML-bestandsindeling

MHTML is ook bekend als MIME Encapsulation of Aggregate HTML-documenten vanwege de mogelijkheid om HTML-webpagina's samen met de bronnen te coderen in een enkel webarchief. Volgens de RFC 2557-specificaties is een geaggregeerd document een MIME-gecodeerd bericht dat een root-resource (object) bevat, evenals andere resources die eraan zijn gekoppeld via URI's. Dergelijke andere bronnen kunnen representatie zijn van inline afbeeldingen, stylesheets, applets, enz. Bovendien kunnen deze de root zijn van andere multimediadocumenten. De volledige documentspecificaties voor het MHTML-bestandsformaat zijn zoals beschreven in de [RFC 2557](https://tools.ietf.org/html/rfc2557) en er moet naar worden verwezen voor elke vorm van applicatie-ontwikkeling voor het lezen/schrijven van dit bestandsformaat. De norm specificeert dat de lichaamsdelen waarnaar verwezen wordt, geïdentificeerd kunnen worden door een Content-ID of door een Content-Location.

### MIME-inhoudskoppen

Een MIME-inhoudsheader, Content-Location, is gedefinieerd om URI-verwijzingen naar bronnen in andere lichaamsdelen op te lossen. Deze koptekst kan in elke bericht- of inhoudskop voorkomen.

### Content-Locatie Header

Een Content-Location is een weergave van een URI die de inhoud van een lichaamsdeel waar deze is geplaatst, labelt. De waarde kan een absolute of een relatieve URI zijn. Het kan worden gebruikt om een bron te labelen die niet kan worden opgehaald door sommige of alle ontvangers van een bericht. Een enkel bericht mag slechts een enkele Content-Location-header hebben. Voorbeeld van een meerdelige/gerelateerde structuur met lichaamsdelen met zowel Content-Location- als Content-ID-labels:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI's van MHTML-aggregaten

De URI van MHTML-aggregaat is anders dan die van de hoofd-URI. Het kopveld Content-Locatie moet van toepassing zijn op het hele aggregaat als het wordt gebruikt in de kop van een meerdelige/gerelateerde kop. Evenzo kan de opgehaalde set bronnen verschillen van de set bronnen die is opgehaald met behulp van de inhoudslocaties van de onderdelen ervan wanneer de URI die verwijst naar het MHTML-aggregaat wordt gebruikt om dit aggregaat op te halen. Het ophalen van een MHTML-aggregaat kan bijvoorbeeld een oude versie retourneren, terwijl het ophalen van de root-URI en de in-line gekoppelde objecten een nieuwere versie kan retourneren.

## Referenties

* [MIME-inkapseling van geaggregeerde documenten - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML-bestandsindeling - door Wikipedia](https://en.wikipedia.org/wiki/MHTML)

