{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku WSDL — plik języka opisu usług sieciowych",
  "description":"Dowiedz się, co to jest plik WSDL i interfejsy API, które mogą tworzyć i otwierać pliki WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Czym jest plik WSDL?

Plik WSDL to plik Web Services Description Language, który jest napisany w języku XML do opisywania usług Web. Zawiera informacje o punktach końcowych lub interfejsach łączności ze światem zewnętrznym w powszechnie akceptowanym formacie. [Specyfikacja formatu pliku WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (utrzymywane przez W3C.org) definiuje warunki publikowania strumieni danych w celu wymiany danych w celu zdalny dostęp aplikacji przez porty i punkty końcowe.

## Format pliku WSDL — więcej informacji

Pliki WSDL są zapisywane jako pliki XML, które są czytelne dla człowieka i można je otworzyć w dowolnym edytorze tekstu w celu wyświetlenia zawartości.

## Opis usługi WSDL

Specyfikacje formatu plików WSDL 2.0 opisują usługę WSDL jako składającą się z dwóch etapów:

- Etap abstrakcyjny
- Scena betonowa

Ponowne wykorzystanie opisu i projektów niezależnego koncernu jest regulowane przez serwis internetowy. Osiąga się to za pomocą kilku różnych typów elementów, w tym typów (definicji typów danych), komunikatów (przekazywanych danych), operacji (akcji) i protokołów używanych przez usługę. Wszystkie te są zarządzane na poziomie abstrakcyjnym. Powiązanie szczegółów transportu i formatu łącza jest określone przez powiązanie, które grupuje punkty końcowe w celu zaimplementowania wspólnego interfejsu.

### Jakich technologii można używać do łączenia się z usługami WSDL?

Do komunikacji z usługami WSDL można użyć kilku różnych technologii, w tym aplikacji ASP.NET, C/C++ i Java.

## Przykład WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

W tym przykładzie typ portu „glossaryTerms” definiuje operację jednokierunkową o nazwie „setTerm”.

## Bibliografia

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Specyfikacja formatu plików WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

