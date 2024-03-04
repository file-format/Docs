{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL – verslo ir finansinės atskaitomybės failo formatas",
  "description":"Sužinokite apie XBRL failo formatą ir API, kurios gali kurti ir atidaryti XBRL failus.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-lt",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Kas yra XBRL failas?

Failas su plėtiniu .xbrl (išplėstinė verslo ataskaitų kalba) yra laisvai prieinama ir visuotinė verslo informacijos mainų sistema. Dabar jis plačiai naudojamas kaip vienas iš standartinių formatų, pakeitęs senesnes popierines ataskaitas naudingesniais ir tikslesniais skaitmeniniais įrašais. Duomenys, kuriais keičiamasi naudojant XBRL failus, apima knygas, finansinę informaciją ir balansus. Tai palaiko duomenų žymas, leidžiančias apdoroti duomenis nuo parengimo iki visų rūšių verslo informacijos analizės etapo. XBRL failus galima atidaryti naudojant programinę įrangą, pvz., Rivet Software Dragon View XBRL Viewer ir API, pvz., [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL failo formatas

XBRL yra atviras tarptautinis skaitmeninio verslo ataskaitų teikimo standartas, plačiai naudojamas visame pasaulyje. Tai yra [XML](/web/xml/) pagrįsta kalba, kuri naudoja XBRL elementus, vadinamus žymomis, kad apibūdintų kiekvieną verslo duomenų elementą ir suformuluotų duomenis ataskaitoms rūšiuoti ir analizuoti. XBRL failo formato specifikacijas sukūrė ir paskelbė XBRL International, Inc. šiuo metu naudotojams pasiekiama [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html).

### XBRL dokumento struktūra

Programuotojai gali nurodyti visą informaciją apie [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html), norėdami parašyti programas, skirtas dirbti šiuo failo formatu. XBRL susideda iš XBRL egzemplioriaus ir taksonomijų rinkinio.

**`XBRL egzempliorius`** – XBRL egzempliorius prasideda<xbrl> šakninis elementas. Dideliame XML dokumente gali būti daugiau nei vienas XBRL egzempliorius.

**`XBRL taksonomija`** – [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) apibrėžiamas kaip XML schemos struktūros ir tiesiogiai nurodytų išorinių nuorodų elementų rinkinys. Mastelio keitimo taksonomijos schema, rodanti nuorodų bazės nuorodas, yra tokia.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Nuorodos Nr.

* [XBRL – Vikipedija](https://en.wikipedia.org/wiki/XBRL)

* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


