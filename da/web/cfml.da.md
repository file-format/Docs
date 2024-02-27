{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML - ColdFusion Markup Language File",
  "description": "Lær om, hvad en CFML-fil og API'er er, der kan oprette og åbne CFML-filer.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-dal"
}
},
  "lastmod": "2021-08-19"
}

## Hvad er en CFML fil?

En fil med filtypen .cfml er en ColdFusion Markup Language-fil, der bruges til at oprette en webside. Det refererer til et sæt regler, der bruges til at definere, hvordan ColdFusion-applikationen vil blive udviklet af programmøren. ColdFusion er et programmeringssprog, der bruges til at skabe serverside-webapplikationer hurtigt og med mindre end andre teknologier såsom [ASP](/web/asp/), [PHP](/programming/php/) osv. Nogle af de programmer, der kan åbne CML-filer, inkluderer Adobe ColdFusion 2018, Adobe ColdFusion Builder og Adobe Dreamweaver.

## CFML-filformat - flere oplysninger

CFML-filer er markup-filer og indeholder webelementer i form af tags. Disse er tekstfiler, der kan åbnes og redigeres i enhver teksteditor. CFML-filer består af flere tags, der ligner [HTML](/web/html/) og består normalt af et åbnings- og et afsluttende tag. Disse tags kan også indeholde en eller flere attributter.

### Tags Syntaks

Følgende er den generaliserede syntaks for CFML-tags.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

De fleste tags accepterer attributter og er defineret som følger.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Nogle af disse tags accepterer også flere attributter med følgende syntaks.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Eksempel på CFML-kode

Her er et eksempel, der bruger et faktisk CFML-tag - `cfoutput`-tagget:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referencer

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


