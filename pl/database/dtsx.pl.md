{
  "date" : "2020-11-11",
  "keywords" :["DTSX", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku DTSX i interfejsy API, które mogą tworzyć i otwierać pliki DTSX.",
  "title" :"Format pliku DTSX — plik ustawień DTS programu SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik DTSX?

Plik z rozszerzeniem .dtsx (Data Transformation Services Package XML) to plik Data Transformation Services (DTS), który jest używany przez Microsoft SQL do odwoływania się do kroków/reguł migracji danych w celu przesyłania danych z jednej bazy danych do drugiej. Obejmuje to przekształcenia i wszelkie opcjonalne etapy przetwarzania, które mogą być wymagane podczas przesyłania danych między punktami początkowymi i docelowymi. SQL Server Integration Services (SSIS), składnik Microsoft SQL Server, używa plików DTSX do identyfikowania kroków przetwarzania danych między serwerami baz danych. Pliki DTSX można otwierać za pomocą Microsoft SQL Server 2019.

## Format pliku DTSX

Przenoszenie danych między serwerami baz danych wymaga reguł i kroków przetwarzania w celu zapewnienia integralności danych podczas tej operacji. SSIS zapewnia, że wszystkie te czynności, polegające na przenoszeniu i dopasowywaniu danych z różnych źródeł w przedsiębiorstwie, odbywają się w wygodny sposób. Właśnie tam pojawia się DTSX, który definiuje struktury, które mają być używane przez SSIS w celu ustalenia kroków, w których dane mogą być przetwarzane zgodnie z tymi krokami.

Przepływ danych opisany przez DTSX jest pokazany na poniższej ilustracji.

{{< figure src="../DataFlowDTSX.png" alt="Przepływ danych DTSX" >}}

DTSX jest oparty na [XML](/pl/web/xml/) i jest udokumentowany w [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). Udoskonalona refaktoryzacja DTSX XML to DTSX 2.0, która obejmuje nowe atrybuty struktur, zastąpienie nazwanych właściwości jako nadrzędnych atrybutów XML, określenie wartości domyślnych dla większości wartości atrybutów oraz umieszczenie powtarzających się elementów wewnątrz elementu nadrzędnego. Struktury DTSX są opisane przy użyciu tych [schematów XML](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1), a format strukturalny to tekst celarowy XML.

## Bibliografia

* [Format DSX — Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Format DSX 2 — firma Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

