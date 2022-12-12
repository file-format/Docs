{
  "date" : "2019-10-11",
  "keywords" :["xbrl","plik xbrl", "format pliku xbrl", "typ pliku xbrl", "plik", "typ", "co to jest plik xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL – format pliku sprawozdawczości biznesowej i finansowej",
  "description":"Poznaj format pliku XBRL i interfejsy API, które mogą tworzyć i otwierać pliki XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Czym jest plik XBRL?

Plik z rozszerzeniem .xbrl (eXtensible Business Reporting Language) to swobodnie dostępna i globalna platforma wymiany informacji biznesowych. Jest obecnie szeroko stosowany jako jeden ze standardów, który zastąpił starsze raporty papierowe bardziej użytecznymi i dokładnymi zapisami cyfrowymi. Dane wymieniane za pomocą plików XBRL obejmują księgi rachunkowe, dane finansowe i bilanse. Obsługuje znaczniki danych, które umożliwiają przetwarzanie danych od przygotowania do etapu analizy wszelkiego rodzaju informacji biznesowych. Pliki XBRL można otwierać za pomocą oprogramowania, takiego jak Rivet Software Dragon View XBRL Viewer i interfejsów API, takich jak [Aspose.Finance](https://products.aspose.com/finance).

## Format pliku XBRL

XBRL to otwarty międzynarodowy standard cyfrowej sprawozdawczości biznesowej, szeroko stosowany na całym świecie. Jest to język oparty na [XML](/pl/web/xml/), który używa elementów XBRL, znanych jako znaczniki, do opisywania każdego elementu danych biznesowych w celu sformułowania danych do sortowania i analizy raportów. Specyfikacje formatu plików XBRL są opracowywane i publikowane przez XBRL International, Inc, z [XBRL wersja 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) obecnie dostępne dla użytkowników.

### Struktura dokumentu XBRL

Pełne informacje o [znacznikach XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) mogą być kierowane przez programistów do pisania aplikacji obsługujących ten format plików. XBRL składa się z instancji XBRL i zbioru taksonomii.

**`Instancja XBRL`** — Instancja XBRL zaczyna się od<xbrl> element główny. Duży dokument XML może zawierać więcej niż jedną osadzoną w nim instancję XBRL.

**`Taksonomia XBRL`** — [Taksonomia XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) jest zdefiniowana jako struktura schematu XML i zestaw bezpośrednio przywoływanych elementów linków zewnętrznych. Skalowalny schemat taksonomii przedstawiający odniesienia do bazy łączy jest następujący.

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


## Bibliografia ##

* [XBRL – z Wikipedii](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

