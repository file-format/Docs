{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Specyfikacje papieru XML", "Plik", "Rozszerzenie", "Format pliku", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - format pliku układu strony",
  "description":"Poznaj format pliku XPS i interfejsy API, które mogą tworzyć i otwierać pliki XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Czym jest plik XPS? ##

Plik XPS reprezentuje pliki układu strony, które są oparte na specyfikacjach papieru XML stworzonych przez firmę Microsoft. Został opracowany jako zamiennik formatu pliku EMF i jest podobny do formatu pliku [PDF](/pl/pdf/), ale wykorzystuje XML w układzie, wyglądzie i informacjach o drukowaniu dokumentu. W rzeczywistości bardziej uzasadnione jest stwierdzenie, że XPS jest próbą PDF, ale z wielu powodów nie mógł zdobyć wystarczającej popularności jako własność PDF. Firma Microsoft domyślnie udostępnia program XPS Document Writer począwszy od systemu Windows 7 do tworzenia plików XPS. Pliki XPS można generować, wybierając „Microsoft XPS Document Writer” jako drukarkę podczas drukowania dokumentu.

Przeglądarki XPS są zintegrowane z systemami Windows Vista, Windows 7, Windows 8 i Internet Explorer 6 lub nowszym. Pliki XPS stają się tylko do odczytu po ich wygenerowaniu. Zwiększa to zaufanie użytkownika do otrzymanych dokumentów wysłanych jako XPS pod kątem autentyczności dokumentu. Dokument XPS może zawierać jedną lub więcej stron przekonwertowanych z oryginalnego dokumentu.

## Krótka historia ##

Firma Microsoft przedłożyła specyfikację XPS firmie Ecma International. W czerwcu 2007 r. powołano Komitet Techniczny Ecma 46 (TC46) w celu opracowania standardu opartego na specyfikacjach papieru OpenXPS. Firma Ecma International zatwierdziła standard Ecma (ECMA-388) [specyfikacje XPS](http://www.ecma-international.org/publications/standards/Ecma-388.htm) w czerwcu 2009 r. na 97. Zgromadzeniu Ogólnym.

## Format pliku XPS ##

Format XPS składa się ze znaczników XML, które definiują kompozycję dokumentu i wygląd każdej strony wraz z regułami renderowania do wyświetlania lub drukowania dokumentu. Zachowuje wszystkie informacje potrzebne do odtworzenia dokumentu w dowolnym systemie, co czyni go niezależnym od zasobów dostępnych w tym systemie. Format jest zasadniczo archiwum ZIP, a jeśli zmienisz nazwę rozszerzenia pliku na ZIP, zobaczysz pliki składowe zawierające dane dokumentu. Dokumenty te obejmują:

* Pliki strony dokumentu (.fpage) — Zawiera zawartość dokumentu i ustawienia formatu dokumentu. Każda strona w dokumencie XPS ma jeden plik FPAGE.
* plik ustawień dokumentu (.fdoc) - Przechowuje ustawienia zawarte w archiwum XPS.
* pliki fragmentów dokumentów (.frag) — definiuje ustawienia dla rzeczywistego pliku XPS, a każda strona w dokumencie ma swój własny plik .frag.

{{< figure src="../XPS-1.png" alt="Format pliku XPS" >}}

Pliki te zachowują zawartość dokumentu w taki sposób, że jeśli na przykład ktoś nie ma zainstalowanych tych samych czcionek na swoim komputerze, przeglądarka XPS nadal będzie renderować te oryginalne czcionki. Oznacza to włączenie pliku znaczników XML dla każdego:

* Strona
* Tekst
* Czcionki osadzone
* Obrazy rastrowe
* Grafika wektorowa 2D
* Zarządzanie Prawami Cyfrowymi

Format dokumentu XPS obejmuje dobrze zdefiniowany zestaw części i relacji, z których każda spełnia określony cel w dokumencie. Format rozszerza również funkcje pakietu, w tym podpisy cyfrowe, miniatury i przeplatanie.

Typowy dokument XPS wygląda następująco i można go analizować w świetle [specyfikacji] formatu pliku XPS (https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Format pliku XPS" >}}


## Bibliografia ##

* [Specyfikacje formatu plików XPS] (http://www.ecma-international.org/publications/standards/Ecma-388.htm)
* [XPS — z Wikipedii](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

