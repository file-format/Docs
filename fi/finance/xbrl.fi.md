{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - Liiketoiminnan ja taloudellisen raportoinnin tiedostomuoto",
  "description":"Opi XBRL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XBRL-tiedostoja.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-fi",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Mikä on XBRL-tiedosto?

Tiedosto, jonka laajennus on .xbrl (eXtensible Business Reporting Language), on vapaasti saatavilla oleva ja maailmanlaajuinen kehys yritystietojen vaihtamiseen. Sitä käytetään nykyään laajalti yhtenä standardimuotona, joka on korvannut vanhemmat paperipohjaiset raportit hyödyllisemmillä ja tarkemmilla digitaalisilla tietueilla. XBRL-tiedostoilla vaihdetut tiedot sisältävät reskontrat, taloudelliset tiedot ja taseet. Se tukee datatunnisteita, jotka mahdollistavat kaikenlaisten yritystietojen tietojen käsittelyn valmistelusta analyysivaiheeseen. XBRL-tiedostoja voidaan avata käyttämällä ohjelmistoja, kuten Rivet Software Dragon View XBRL Viewer, ja API:ita, kuten [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL-tiedostomuoto

XBRL on digitaalisen liiketoiminnan raportoinnin avoin kansainvälinen standardi, jota käytetään laajasti maailmanlaajuisesti. Se on [XML](/web/xml/)-pohjainen kieli, joka käyttää XBRL-elementtejä, joita kutsutaan tunnisteiksi, kuvaamaan jokaista yritystietokohdetta tietojen muodostamiseksi raporttien lajittelua ja analysointia varten. XBRL-tiedostomuotomääritykset on kehittänyt ja julkaissut XBRL International, Inc. [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) on tällä hetkellä käyttäjien saatavilla.

### XBRL-asiakirjan rakenne

Ohjelmoijat voivat viitata täydellisiin tietoihin [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html):sta kirjoittaakseen sovelluksia tämän tiedostomuodon käyttöä varten. XBRL koostuu XBRL-instanssista ja taksonomioiden kokoelmasta.

**`XBRL-instanssi`** - XBRL-ilmentymä alkaa kirjaimella<xbrl> juurielementti. Suuri XML-dokumentti voi sisältää enemmän kuin yhden XBRL-ilmentymän upotettuna.

**`XBRL Taxonomy`** - {{HYPERLINKKI}} määritellään XML-skeeman rakenteiksi ja suoraan viitattujen ulkoisten linkkien joukoksi. Skaalautuva taksonomiakaavio, joka näyttää linkkikantaviittaukset, on seuraava.

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


## Viitteet ##

* [XBRL - Wikipedia](https://en.wikipedia.org/wiki/XBRL)

* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


