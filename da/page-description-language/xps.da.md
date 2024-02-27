{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"XML-papirspecifikationer",
"Fil",
"Udvidelse",
"Filformat",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS - Sidelayout-filformat",
  "description": "Lær om XPS-filformat og API'er, der kan oprette og åbne XPS-filer.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-das"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er en XPS fil?

En XPS-fil repræsenterer sidelayoutfiler, der er baseret på XML Paper Specifications oprettet af Microsoft. Det blev udviklet som en erstatning for EMF-filformatet og ligner [PDF](/pdf/)-filformatet, men bruger XML i layout, udseende og udskrivning af et dokument. Det er faktisk mere berettiget at sige, at XPS er et forsøg på PDF, men af mange grunde ikke kunne få nok popularitet som ejet af PDF. Microsoft leverer XPS Document Writer som standard fra Windows 7 og frem til oprettelse af XPS-filer. XPS-filer kan genereres ved at vælge Microsoft XPS Document Writer som printer, mens dokumentet udskrives.

XPS-fremvisere er integreret som en del af Windows Vista, Windows 7, Windows 8 og Internet Explorer 6 eller nyere. XPS-filer bliver skrivebeskyttet, når de er genereret. Dette øger brugerens tillid til modtagne dokumenter sendt som XPS for dokumentets ægthed. Et XPS-dokument kan indeholde en eller flere sider som konverteret fra det originale dokument.

## Kort historie ##

Microsoft indsendte XPS-specifikationen til Ecma International. I juni 2007 blev Ecma Technical Committee 46 (TC46) nedsat for at udvikle en standard baseret på OpenXPS Paper Specifications. Ecma International godkendte Ecma Standard (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) i juni 2009 på den 97. generalforsamling.

## XPS-filformat ##

XPS-formatet består af XML-markering, der definerer sammensætningen af et dokument og det visuelle udseende af hver side sammen med gengivelsesregler for visning eller udskrivning af dokumentet. Det beholder alle oplysninger til at genskabe et dokument på ethvert system, hvilket gør det uafhængigt af de ressourcer, der er tilgængelige på det pågældende system. Formatet er i det væsentlige et ZIP-arkiv, og hvis du omdøber filtypenavnet til ZIP, vil du se de bestanddele, der indeholder dokumentdataene. Disse dokumenter omfatter:

* dokumentsidefiler (.fpage) - Indeholder dokumentindhold og dokumentformatindstillinger. Hver side i XPS-dokumentet har én FPAGE-fil.

* dokumentindstillingsfil (.fdoc) - Gemmer indstillinger inkluderet i XPS-arkivet.

* dokumentfragmentfiler (.frag) - Definerer indstillingerne for den faktiske XPS-fil, og hver side i dokumentet har sin egen .frag-fil.


{{< figure src="../XPS-1.png" alt="XPS filformat" >}}

Disse filer beholder dokumentindholdet på en sådan måde, at hvis nogen f.eks. ikke har de samme skrifttyper installeret på deres maskine, vil XPS-fremviseren stadig gengive disse originale skrifttyper. Dette indebærer medtagelse af XML-markup-fil for hver:

* Side

* Tekst

* Indlejrede skrifttyper

* Rasterbilleder

* 2D vektorgrafik

* Forvaltning af digitale rettigheder


XPS-dokumentformatet inkluderer et veldefineret sæt af dele og relationer, der hver opfylder et bestemt formål i dokumentet. Formatet udvider også pakkefunktionerne, herunder digitale signaturer, thumbnails og interleaving.

Et typisk XPS-dokument ser ud som følger og kan analyseres i lyset af XPS-filformatet [specifications](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS filformat" >}}


## Referencer ##

* [XPS-filformatspecifikationer](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)

* [XPS - af Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)


