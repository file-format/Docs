{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","fișier xbrl", "format fișier xbrl", "tip fișier xbrl", "fișier", "tip", "ce este un fișier xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Format de fișier de raportare financiară și de afaceri",
  "description":"Aflați despre formatul de fișier XBRL și despre API-urile care pot crea și deschide fișiere XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Ce este un fișier XBRL?

Un fișier cu extensia .xbrl (eXtensible Business Reporting Language) este un cadru global disponibil gratuit pentru schimbul de informații despre afaceri. Acum este utilizat pe scară largă ca unul dintre formatele standard care a înlocuit rapoartele mai vechi pe hârtie cu înregistrări digitale mai utile și mai precise. Datele schimbate folosind fișierele XBRL includ registre, detalii financiare și bilanţuri. Suportă etichete de date care permit prelucrarea datelor de la pregătire până la etapa de analiză a informațiilor de afaceri de toate tipurile. Fișierele XBRL pot fi deschise folosind software precum Rivet Software Dragon View XBRL Viewer și API-uri precum [Aspose.Finance](https://products.aspose.com/finance).

## Format de fișier XBRL

XBRL este un standard internațional deschis pentru raportarea digitală a afacerilor, care este utilizat pe scară largă la nivel global. Este un limbaj bazat pe [XML](/ro/web/xml/) care utilizează elemente XBRL, cunoscute sub numele de etichete, pentru a descrie fiecare element de date comerciale pentru a formula date pentru sortarea și analiza rapoartelor. Specificațiile de format de fișier XBRL sunt dezvoltate și publicate de XBRL International, Inc, cu [XBRL versiunea 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) în prezent disponibile utilizatorilor.

### Structura documentului XBRL

Informații complete despre [etichetele XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) pot fi îndrumați de către programatori pentru a scrie aplicații pentru lucrul cu acest format de fișier. Un XBRL constă dintr-o instanță XBRL și o colecție de taxonomii.

**`XBRL Instance`** - Instanța XBRL începe cu<xbrl> element rădăcină. Un document XML mare poate conține mai mult de o instanță XBRL încorporată în el.

**`Taxonomia XBRL`** - [Taxonomia XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) este definit ca o schemă XML și un set de elemente de link-uri externe la care se face referire directă. O schemă de taxonomie scalabilă care arată referințele la baza de linkuri este următoarea.

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


## Referințe ##

* [XBRL - După Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

