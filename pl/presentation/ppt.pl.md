{
  "date" : "2019-12-13",
  "keywords" :[ "plik ppt", "format pliku ppt", "co to jest plik ppt", "plik", "przykład ppt", "rozszerzenie pliku ppt", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików PPT i interfejsy API, które mogą tworzyć i otwierać pliki PPT.",
  "title" :"PPT - format pliku programu PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PPT?

Plik z rozszerzeniem PPT reprezentuje plik PowerPoint, który składa się z kolekcji slajdów do wyświetlenia jako pokaz slajdów. Określa format pliku binarnego używany przez program Microsoft PowerPoint 97-2003. Plik PPT może zawierać kilka różnych typów informacji, takich jak tekst, wypunktowane punkty, obrazy, multimedia i inne osadzone obiekty OLE. Firma Microsoft opracowała nowszy format plików dla programu PowerPoint, znany jako [PPTX](/pl/presentation/pptx/), począwszy od 2007 r., który jest oparty na Office OpenXML i różni się od binarnego formatu plików. Kilka innych aplikacji, takich jak OpenOffice Impress i Apple Keynote, może również tworzyć pliki PPT.

## Krótka historia ##

Firma Microsoft wprowadziła format pliku PPT wraz z wydaniem programu PowerPoint w 1987 r. Stabilny format binarny był udostępniany jako domyślny w programie PowerPoint 97-2003 dla systemu Windows. Format pliku binarnego jest obsługiwany do odczytu i zapisu przez najnowsze wersje programu PowerPoint, w tym PowerPoint 2016.

## Specyfikacje formatu plików ##

Od momentu wprowadzenia format pliku PPT przeszedł kilka zmian w celu dodania nowych funkcji i ulepszeń. Najnowsze dostępne specyfikacje wersji to wersja 6.0 opublikowana w sierpniu 2018 r., której nie należy mieszać z rzeczywistym numerem produktu w formacie pliku PPT, ponieważ firma Microsoft nie zapewnia już modyfikacji tego formatu.

### Omówienie formatu pliku ###

Niektóre z kluczowych elementów formatu pliku PPT są następujące:

#### Slajdy ####

Dane użytkownika, takie jak kształty, tekst, animacje i multimedia, są dodawane do prezentacji wewnątrz slajdu. Prezentacja może zawierać jeden lub więcej slajdów, które są wyświetlane jako pokaz slajdów po uruchomieniu prezentacji. Prezentacja zawiera wzorcowe slajdy i tytułowe slajdy wzorcowe, które pełnią rolę szablonu dla typowych właściwości wizualnych slajdów prezentacji. Dostępny jest również slajd wzorcowy notatek i slajd wzorcowy materiałów informacyjnych, które służą podobnemu celowi i zapewniają wspólne właściwości wizualne dla wszystkich slajdów notatek i wszystkich drukowanych materiałów informacyjnych.

#### Kształty ####

Kształty to obiekty, które umożliwiają użytkownikom dodawanie różnych treści do slajdu w postaci zastępczych kształtów, obrazów i wykresów. Kształty na slajdzie wzorcowym definiują wspólne dane dla grup kształtów.

#### Symbole zastępcze Kształty ####

Są to specjalne symbole zastępcze, które służą jako pojemniki na różne obiekty. Różne kształty symboli zastępczych mogą służyć jako wskazówki dotyczące wstawiania określonych typów kształtów, takich jak tabele lub wykresy. Wewnątrz slajdu kształt zastępczy przyjmuje właściwości wizualne głównego slajdu wzorcowego, wzorcowego slajdu tytułowego lub wzorcowego slajdu notatek.

#### Obiekty zewnętrzne ####

W slajdzie można osadzać obiekty zewnętrzne, takie jak osadzone i połączone audio, połączone wideo, osadzone i połączone obiekty OLE oraz hiperłącza. Tych obiektów można używać do aktywowania obiektów połączonych w celu uzyskania dostępu do zasobów zewnętrznych podczas pokazu slajdów.

### Struktury formatu plików ###

Formaty plików binarnych programu PowerPoint składają się z następujących strumieni reprezentujących ogólną strukturę dokumentu i dane.

* Bieżący strumień użytkowników
* Strumień dokumentów programu PowerPoint
* Strumień zdjęć
* Informacje podsumowujące i Informacje podsumowujące dokument (opcjonalnie)

Pełną specyfikację formatu pliku DOC można znaleźć w witrynie [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) i należy się z nią zapoznać w odniesieniu do sekcji wymienionych w poniższych szczegółach.

#### Bieżący strumień użytkownika ####

Przechowuje informacje o ostatnim użytkowniku, który otworzył dokument, a jego nazwa musi brzmieć „Current User”.

#### Strumień dokumentów programu PowerPoint ####

Przechowuje wszystkie informacje o prezentacji programu PowerPoint oraz objaśnia jej układ i zawartość. Jest to wymagany strumień, którego nazwa MUSI brzmieć „Dokument programu PowerPoint”. Zawartość tego strumienia jest określona przez sekwencję rekordów najwyższego poziomu. Częściowe ograniczenia porządkowania sekwencji rekordów są określone w rekordach PersistDirectoryAtom i UserEditAtom.

Jako rekordy kontenerów, rekordy DocumentContainer, MainMasterContainer (sekcja 2.5.3), HandoutContainer (sekcja 2.5.8), SlideContainer (sekcja 2.5.1) i NotesContainer (sekcja 2.5.6) są korzeniami drzewa rekordów kontenerów i rekordy atomowe. Wewnątrz dowolnego rekordu kontenera mogą istnieć inne rekordy, które nie są jawnie wymienione jako rekordy podrzędne. Nieznane rekordy są identyfikowane, gdy pole recType struktury RecordHeader (sekcja 2.3.1) zawiera wartość nieokreśloną w wyliczeniu RecordType (sekcja 2.13.24). Te nieznane rekordy, jeśli zostaną napotkane, MUSZĄ zostać zignorowane i MOGĄ<1> zostać zachowane. Nieznane rekordy można zignorować, wyszukując w przód recLen bajtów od końca struktury RecordHeader.

Za każdym razem, gdy ten strumień jest zapisywany, nowe rekordy najwyższego poziomu, edytowane przez użytkownika, mogą zostać dołączone do istniejącego strumienia lub cała zawartość strumienia może zostać zastąpiona zaktualizowaną sekwencją rekordów najwyższego poziomu. Jeśli cały strumień nie zostanie zastąpiony, wszelkie poprzednio istniejące rekordy najwyższego poziomu, które obejmowały poprzednie zmiany dokonane przez użytkownika, mogą stać się przestarzałe przez dołączone później rekordy najwyższego poziomu, które obejmują bieżące zmiany dokonane przez użytkownika.

#### Strumień zdjęć ####

Jest to opcjonalny strumień zawierający dane o obrazach zawartych w prezentacji programu PowerPoint. Jego nazwa MUSI brzmieć „Pictures”. Zawartość tego strumienia jest określona przez rekord OfficeArtBStoreDelay, jak określono w sekcji [MS-ODRAW] 2.2.21.

#### Strumień informacji podsumowujących ####

Przechowuje statystyki dotyczące dokumentu zgodnie ze standardem Microsoft Office. Strumień informacji podsumowujących musi mieć nazwę „\005Informacje podsumowujące”, gdzie \005 to znak o wartości 0x0005, a nie literał łańcuchowy „\005”. Ten strumień POWINIEN zostać pominięty w przypadku zaszyfrowanych dokumentów. Zawartość tego strumienia jest określona w sekcji [MS-OSHARED] 2.3.3.2.1.

#### Strumień informacji podsumowujących dokument ####

Opcjonalny strumień, którego nazwa MUSI być „\005DocumentSummaryInformation”, gdzie \005 to znak o wartości 0x0005, a nie literał łańcuchowy „\005”. Ten strumień MOŻE<2> zostać pominięty w przypadku zaszyfrowanych dokumentów. Zawartość tego strumienia jest określona w sekcji [MS-OSHARED] 2.3.3.2.2.

#### Zaszyfrowany strumień informacji podsumowujących ####

Opcjonalny strumień, którego nazwa MUSI brzmieć „EncryptedSummary”. Ten strumień istnieje tylko w zaszyfrowanym dokumencie. Zawartość tego strumienia jest określona w sekcji [MS-OFFCRYPTO] 2.3.5.4.

#### Przechowywanie podpisów cyfrowych ####

Opcjonalny magazyn, którego nazwa MUSI być „_xmlsignatures”. MOŻE zostać pominięty i MOŻE być zignorowany. Zawartość tego magazynu jest określona w sekcji [MS-OFFCRYPTO] 2.5.2.

#### Niestandardowe przechowywanie danych XML ####

Opcjonalny magazyn, którego nazwa MUSI być „MsoDataStore”. Zawartość magazynu jest określona w sekcji [MS-OSHARED] 2.3.6.

#### Strumień podpisów ####

Opcjonalny strumień, którego nazwa MUSI być „_signatures”. POWINIEN zostać pominięty i MOŻE być zignorowany. Zawartość tego strumienia jest określona w sekcji [MS-OFFCRYPTO] 2.5.1.

## Bibliografia ##

* [Specyfikacja formatu pliku PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Wspólne typy danych i struktury obiektów pakietu Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] — struktura kryptograficzna dokumentów pakietu Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formaty plików programu PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

