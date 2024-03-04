{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML – ColdFusion žymėjimo kalbos failas",
  "description": "Sužinokite, kas yra CFML failas ir API, kurios gali kurti ir atidaryti CFML failus.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-ltl"
}
},
  "lastmod": "2021-08-19"
}

## Kas yra CFML failas?

Failas su plėtiniu .cfml yra ColdFusion Markup Language failas, naudojamas kuriant tinklalapį. Tai reiškia taisyklių rinkinį, naudojamą apibrėžti, kaip programuotojas sukurs ColdFusion programą. ColdFusion yra programavimo kalba, naudojama norint greitai ir naudojant mažiau nei kitas technologijas kurti serverio žiniatinklio programas, pvz., [ASP](/web/asp/), [PHP](/programming/php/) ir kt. Kai kurios programos, galinčios atidaryti CML failus, yra Adobe. ColdFusion 2018, Adobe ColdFusion Builder ir Adobe Dreamweaver.

## CFML failo formatas – daugiau informacijos

CFML failai yra žymėjimo failai ir juose yra žiniatinklio elementų žymų pavidalu. Tai tekstiniai failai, kuriuos galima atidaryti ir redaguoti bet kuriame teksto rengyklėje. CFML failus sudaro kelios žymos, panašios į [HTML](/web/html/) ir paprastai susideda iš pradžios ir pabaigos žymų. Šiose žymose taip pat gali būti vienas ar daugiau atributų.

### Žymos sintaksė

Toliau pateikiama apibendrinta CFML žymų sintaksė.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Dauguma žymų priima atributus ir yra apibrėžiamos taip.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Kai kurios iš šių žymų taip pat priima kelis atributus su tokia sintaksė.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML kodo pavyzdys

Štai pavyzdys, kuriame naudojama tikroji CFML žyma – žyma cfoutput:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Nuorodos

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


