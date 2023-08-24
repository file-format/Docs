{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion Markup Language-bestand",
  "description" :"Meer informatie over wat een CFML-bestand is en API's die CFML-bestanden kunnen maken en openen.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Wat is een CFML-bestand?

Een bestand met de extensie .cfml is een ColdFusion Markup Language-bestand dat wordt gebruikt om een webpagina te maken. Het verwijst naar een reeks regels die worden gebruikt om te definiëren hoe de ColdFusion-toepassing door de programmeur zal worden ontwikkeld. ColdFusion is een programmeertaal die wordt gebruikt om snel en met minder dan andere technologieën zoals [ASP](/nl/web/asp/), [PHP](/nl/programming/php/), enz. sever-side webapplicaties te maken. Sommige van de toepassingen die CML-bestanden kunnen openen, zijn Adobe ColdFusion 2018, Adobe ColdFusion Builder en Adobe Dreamweaver.

## CFML-bestandsindeling - Meer informatie

CFML-bestanden zijn opmaakbestanden en bevatten webelementen in de vorm van tags. Dit zijn tekstbestanden die in elke teksteditor kunnen worden geopend en bewerkt. CFML-bestanden bestaan uit verschillende tags die lijken op [HTML](/nl/web/html/) en bestaan meestal uit een openings- en een sluittag. Deze tags kunnen ook een of meer attributen bevatten.

### Syntaxis van tags

Hieronder volgt de algemene syntaxis van CFML-tags.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

De meeste tags accepteren attributen en worden als volgt gedefinieerd.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Sommige van deze tags accepteren ook meerdere attributen met de volgende syntaxis.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Voorbeeld van CFML-code

Hier is een voorbeeld dat een echte CFML-tag gebruikt - de `cfoutput`-tag:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referenties

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

