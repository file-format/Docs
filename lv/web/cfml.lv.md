{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML — ColdFusion iezīmēšanas valodas fails",
  "description": "Uzziniet, kas ir CFML fails un API, kas var izveidot un atvērt CFML failus.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-lvl"
}
},
  "lastmod": "2021-08-19"
}

## Kas ir CFML fails?

Fails ar paplašinājumu .cfml ir ColdFusion iezīmēšanas valodas fails, ko izmanto tīmekļa lapas izveidei. Tas attiecas uz noteikumu kopumu, ko izmanto, lai noteiktu, kā programmētājs izstrādās ColdFusion lietojumprogrammu. ColdFusion ir programmēšanas valoda, ko izmanto, lai izveidotu servera puses tīmekļa lietojumprogrammas ātri un ar mazāk nekā citām tehnoloģijām, piemēram, [ASP](/web/asp/), [PHP](/programming/php/) utt. Dažas no lietojumprogrammām, kas var atvērt CML failus, ietver Adobe ColdFusion 2018, Adobe ColdFusion Builder un Adobe Dreamweaver.

## CFML faila formāts — vairāk informācijas

CFML faili ir iezīmēšanas faili un satur tīmekļa elementus tagu veidā. Tie ir teksta faili, kurus var atvērt un rediģēt jebkurā teksta redaktorā. CFML faili sastāv no vairākiem tagiem, kas ir līdzīgi [HTML](/web/html/) un parasti sastāv no sākuma un beigu taga. Šajos tagos var būt arī viens vai vairāki atribūti.

### Tagu sintakse

Tālāk ir sniegta vispārīgā CFML tagu sintakse.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Lielākā daļa tagu pieņem atribūtus un ir definēti šādi.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Daži no šiem tagiem pieņem arī vairākus atribūtus ar šādu sintaksi.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML koda piemērs

Šeit ir piemērs, kurā tiek izmantots faktiskais CFML tags — tags cfoutput:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Atsauces

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


