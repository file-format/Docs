{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML Paper Specifications", "File", "Extension", "Fil Format", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Filformat för sidlayout",
  "description":"Läs mer om XPS-filformat och API:er som kan skapa och öppna XPS-filer.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är XPS fil? ##

En XPS-fil representerar sidlayoutfiler som är baserade på XML Paper Specifications skapade av Microsoft. Det utvecklades som en ersättning för EMF-filformatet och liknar filformatet [PDF](/sv/pdf/), men använder XML i layout, utseende och utskriftsinformation för ett dokument. Det är faktiskt mer berättigat att säga att XPS är ett försök på PDF, men att det inte kunde få tillräckligt med popularitet som ägt av PDF av många anledningar. Microsoft tillhandahåller XPS Document Writer som standard från Windows 7 och framåt för att skapa XPS-filer. XPS-filer kan genereras genom att välja "Microsoft XPS Document Writer" som skrivare medan du skriver ut dokumentet.

XPS-visningsprogram är integrerade som en del av Windows Vista, Windows 7, Windows 8 och Internet Explorer 6 eller senare. XPS-filer blir skrivskyddade när de har skapats. Detta ökar användarens förtroende för mottagna dokument som skickas som XPS för dokumentets äkthet. Ett XPS-dokument kan innehålla en eller flera sidor som konverterats från originaldokumentet.

## Kortfattad bakgrund ##

Microsoft lämnade in XPS-specifikationen till Ecma International. I juni 2007 inrättades Ecma Technical Committee 46 (TC46) för att utveckla en standard baserad på OpenXPS Paper Specifications. Ecma International godkände Ecma Standard (ECMA-388) [XPS-specifikationer](http://www.ecma-international.org/publications/standards/Ecma-388.htm) i juni 2009 vid den 97:e generalförsamlingen.

## XPS-filformat ##

XPS-formatet består av XML-uppmärkning som definierar sammansättningen av ett dokument och det visuella utseendet på varje sida tillsammans med renderingsregler för att visa eller skriva ut dokumentet. Den behåller all information för att återskapa ett dokument på vilket system som helst, vilket gör det oberoende av de resurser som finns tillgängliga på det systemet. Formatet är i huvudsak ett ZIP-arkiv och om du byter namn på filtillägget till ZIP kommer du att se de ingående filerna som innehåller dokumentdata. Dessa dokument inkluderar:

* dokumentsidafiler (.fpage) - Innehåller dokumentinnehåll och dokumentformatinställningar. Varje sida i XPS-dokumentet har en FPAGE-fil.
* dokumentinställningsfil (.fdoc) - Lagrar inställningar som ingår i XPS-arkivet.
* dokumentfragmentfiler (.frag) - Definierar inställningarna för den faktiska XPS-filen och varje sida i dokumentet har sin egen .frag-fil.

{{< figure src="../XPS-1.png" alt="XPS filformat" >}}

Dessa filer behåller dokumentinnehållet på ett sådant sätt att om, till exempel, någon inte har samma typsnitt installerade på sin dator, kommer XPS-visningsprogrammet fortfarande att återge de ursprungliga teckensnitten. Detta innebär inkludering av XML-uppmärkningsfil för varje:

* Sida
* Text
* Inbäddade typsnitt
* Rasterbilder
* 2D vektorgrafik
* Digital rättighetshantering

XPS-dokumentformatet innehåller en väldefinierad uppsättning delar och relationer, som var och en uppfyller ett visst syfte i dokumentet. Formatet utökar också paketets funktioner, inklusive digitala signaturer, miniatyrer och interfoliering.

Ett typiskt XPS-dokument ser ut som följer och kan analyseras i ljuset av XPS-filformat [specifikationer](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS filformat" >}}


## Referenser ##

* [XPS-filformatsspecifikationer](http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS - av Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

