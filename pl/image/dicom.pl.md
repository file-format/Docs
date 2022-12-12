{
  "date" : "2019-10-11",
  "keywords" :[ "plik dicom", "format pliku dicom", "co to jest plik dicom", "plik", "przykład dicom", "rozszerzenie pliku dicom", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM — cyfrowy format plików obrazowania i komunikacji",
  "description":"Poznaj format pliku DICOM i interfejsy API, które mogą tworzyć i otwierać pliki DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DICOM?

DICOM to skrót od Digital Imaging and Communications in Medicine i odnosi się do dziedziny informatyki medycznej. DICOM służy do integracji urządzeń do obrazowania medycznego, takich jak drukarki, serwery, skanery itp. pochodzących od różnych dostawców, a także zawiera dane identyfikacyjne każdego pacjenta w celu zapewnienia wyjątkowości. Pliki DICOM mogą być udostępniane między dwiema stronami, jeśli są one w stanie odbierać dane obrazu w formacie DICOM. Część komunikacyjna DICOM jest protokołem warstwy aplikacji i wykorzystuje protokół TCP/IP do komunikacji między podmiotami. Wersje obsługiwane przez usługi internetowe to 1.0, 1.1, 2 lub nowsze.

## Historia ##

DICOM został opracowany wspólnie przez American College of Radiology (ACR) i National Electrical Manufacturers Association (NEMA) w celu wymiany i przeglądania obrazów medycznych, takich jak MRI, tomografia komputerowa i obrazy ultrasonograficzne. Początkowo trudno było rozszyfrować obrazy wytwarzane przez maszyny. Dlatego ACR i NEMA wspólnie utworzyły zespół w 1983 roku, który wydał swój pierwszy standard, ACR/NEMA 300 w 1985 roku. Druga wersja została wydana w 1988 roku i była bardziej popularna wśród dostawców, ale wkrótce zdano sobie sprawę, że druga wersja również wymaga udoskonalenia. Trzecia wersja standardu została wydana w 1993 roku jako „DICOM”. 3.0 to nadal najnowsza wersja, ale jest stale aktualizowana od 1993 roku.

## Format pliku DICOM ##

DICOM to połączenie definicji formatu plików i protokołu komunikacji sieciowej. DICOM używa rozszerzenia .DCM. .DCM istnieje w dwóch różnych formatach, tj. formacie 1.x i formacie 2.x. DCM Format 1.x jest ponadto dostępny w dwóch wersjach normalnej i rozszerzonej. Protokoły HTTP i HTTPS są używane w usługach sieciowych DICOM.

### Nagłówek pliku ###

Nagłówek pliku zawiera 128-bajtową preambułę pliku i 4-bajtowy prefiks DICOM.

**Preambuła nr 128 bajtów**|**Prefiks nr 4 bajtów „D, I, C, M**

**Preambuła** służy do uzyskiwania dostępu do obrazów i innych danych w pliku DICOM, zapewniając zgodność z powszechnie używanymi formatami plików graficznych.

**Prefiks** zawiera ciąg znaków „DICM” pisany wielkimi literami.

### Zestaw danych ###

Każdy plik musi zawierać pojedynczy zestaw danych reprezentujący instancję SOP i klasę SOP wraz z powiązanym IOD. Zbiór danych to reprezentacja informacji ze świata rzeczywistego. Zbiór danych zawiera elementy danych, a elementy danych zawierają wartości atrybutów tego obiektu. Struktura atrybutów jest określona w IOD. Obiekt danych DICOM składa się z wielu atrybutów, w tym elementów takich jak nazwa, identyfikator itp., a także jednego specjalnego atrybutu zawierającego dane dotyczące pikseli obrazu.

### Elementy danych ###

Element danych składa się z elementu danych Tag, długości wartości i wartości elementu danych. Istnieje 5 typów elementów danych, a mianowicie: wymagane elementy danych typu 1, warunkowe elementy danych typu 1C, wymagane elementy danych typu 2, warunkowe elementy danych typu 2C i opcjonalne elementy danych typu 3. Podstawowe Trzy typy struktur elementów danych są następujące.

**Element danych z jawną rzeczywistością wirtualną**

|Numer grupy|Numer elementu|Reprezentacja wartości|Zarezerwowane|Długość wartości|Pole wartości
---|---|---|---|---|---|
|2 bajty|2 bajty|2 bajty|2 bajty # 0x00, 0x00|4 bajty|"Długość bajtów"

**Element danych z jawną rzeczywistością wirtualną**

|Numer grupy|Numer elementu|Reprezentacja wartości|Długość wartości|Pole wartości
---|---|---|---|---|
|2 bajty|2 bajty|2 bajty|2 bajty|"Długość bajtów wartości"

**Element danych z niejawną rzeczywistością wirtualną**


|Numer grupy|Numer elementu|Długość wartości|Pole wartości
---|---|---|---|
|2 bajty|2 bajty|4 bajty|"Długość bajtów wartości"

1. **Etykieta elementu danych**: Uporządkowana liczba całkowita reprezentująca numer grupy i numer elementu
1. **Reprezentacja wartości VR**: VR to ciąg znaków reprezentujący VR elementu danych.
1. **Długość wartości**: czy liczba całkowita bez znaku reprezentuje jawną długość pola wartości.
1. **Pole wartości**: opisuje wartości elementów danych.

## Składnia transferu ##

Składnia transferu to zestaw reguł kodowania w celu jednoznacznego przedstawienia bardziej abstrakcyjnych składni. Za pomocą transferu składni komunikujące się podmioty negocjują wspólne techniki kodowania, które obsługują.

## standardowe procedury operacyjne ##

Unia IOD i DIMSE definiuje klasę SOP. Definicja Klasy SOP zawiera zasady i semantykę, które mogą ograniczać korzystanie z usług w Grupie Usług DIMSE lub Atrybutów IOD. Przykładami elementów usług są Store, Get, Find, Move itp. Przykładami obiektów są obrazy CT, obrazy MR, ale obejmują również listy harmonogramów, kolejki drukowania itp.

## Usługi ##

DICOM świadczy różne usługi, głównie związane z przesyłaniem danych. Każdy z nich został krótko opisany poniżej:


**Przechowywanie:** usługa DICOM Store wysyła obrazy lub inne obiekty do systemu archiwizacji i komunikacji obrazów (PACS) lub serwera.


**Zobowiązanie do przechowywania:** usługa zobowiązania do przechowywania służy do potwierdzania, że obraz został trwale zapisany na urządzeniu na dowolnym nośniku.


**Zapytanie/odzyskanie:** ta usługa umożliwia stacji roboczej znalezienie list obrazów lub innych obiektów, a następnie pobranie ich z systemu PACS.


**Lista robocza modalności:** Usługa listy roboczej modalności zawiera listę procedur obrazowania, które zostały zaplanowane do wykonania przez urządzenie do akwizycji obrazu.


**Drukuj:** Ta usługa wysyła obrazy do drukarki.

## Numery portów przez IP ##

DICOM używa następujących portów TCP i UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Bibliografia ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

