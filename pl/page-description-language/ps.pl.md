{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PS",
  "description":"Poznaj format plików PS i interfejsy API, które mogą tworzyć i otwierać pliki PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik .PS? ##

PostScript (PS) to język opisu strony ogólnego przeznaczenia, używany w branży komputerowej i publikacji elektronicznych. Głównym celem PostScript (PS) jest ułatwienie dwuwymiarowego projektowania graficznego. Większość języków wymaga odrębnego etapu kompilacji przed wykonaniem kodu, podczas gdy format Post Script (PS) obsługuje prostą interpretację w czasie wykonywania. Jego wczesna wersja definiuje kształty graficzne, różne wyglądy tekstu i modelowane obrazy na drukowanych lub wyświetlanych stronach, zgodnie z zasadami modelu obrazowania Adobe. Program PS jest w stanie komunikować opis dokumentu między systemem składu a systemem drukowania, utrzymując urządzenie niezależnie i na wysokim poziomie. Ponadto program ten jest w stanie zarządzać wyglądem tekstu i grafiki na wyświetlaczu.

Opis strony PostScript jest dostępny do renderowania, wyświetlania na drukarce i innym urządzeniu wyjściowym za pomocą interpretera PostScript urządzenia. Ponieważ polecenia drukowania znaków, kształtów graficznych i obrazów są wykonywane przez interpreter, dla tego konkretnego urządzenia opis PostScript wysokiego poziomu jest konwertowany na format danych rastrowych niskiego poziomu. Ogólnie rzecz biorąc, różne aplikacje, takie jak ilustratorzy, systemy składu dokumentów i projektowanie wspomagane komputerowo (CAD), są zautomatyzowane w celu generowania opisów stron PostScript. Generalnie programiści muszą pisać programy PostScriptowe podczas tworzenia nowych aplikacji. Jednak programista może skorzystać z możliwości języka PostScript, które nie są dostępne w żadnej aplikacji, pisząc PS program dla tej szczególnej sytuacji.

## Krótka historia ##

Pojęcie języka PostScript zostało po raz pierwszy wprowadzone przez Johna Warnocka. W 1966 roku pracował nad projektem New York Harbor. Starał się opracować interpreter dla dużej trójwymiarowej grafiki dla bazy danych tego projektu. Do przetwarzania tych grafik John Warnock wymyślił język Design System. W międzyczasie firma Xerox PARC szukała standardowego sposobu definiowania obrazów stron dla swojej pierwszej drukarki laserowej. Chociaż Bob Sproull i William Newman w latach 1975-76 opracowali format Press (format danych) do obsługi drukarek laserowych, potrzebny był język zapewniający większą elastyczność. W 1978 Warnock dołączył do Martina Newella w Xerox PARC i przepisał język interpretacyjny, JaM, który później został rozwinięty i rozszerzony na język Interpress. Warnock założył firmę Adobe Systems w grudniu 1982 roku wraz z Chuckiem Geschke, Dougiem Brotzem, Edem Taftem i Billem Paxtonem. Zaczęli pracować nad prostszym językiem o nazwie PostScript, podobnym do Interpress, który został wprowadzony na rynek w 1984 roku. Odwiedził ich Steve Jobs z Apple i doradził im dostosowanie PostScript do obsługi drukarek laserowych.

W marcu 1985 roku pierwszą drukarką z wbudowanym interpreterem PostScript był LaserWriter firmy Apple, który zrewolucjonizował DTP. Techniczna solidność i powszechna dostępność sprawiły, że PostScript stał się językiem wybieranym do publikacji komputerowych i elektronicznych. W roku 1990 tłumacz języka PostScript był istotną częścią drukarek laserowych.

## Główne cechy ##

Możliwości języka PostScript w zakresie obsługi interaktywnej grafiki i opisu strony charakteryzują się następującymi cechami:

**Kształty:** mają charakter dowolny, mogą składać się z linii prostych, krzywych, kwadratów i krzywych sześciennych, które mogą być zarówno samoprzechodzące, jak i rozłączne (w przekrojach i otworach).

**Operatorzy malowania:** zezwalają na zarys kształtu o dowolnej grubości, kolorze, wypełnieniu lub pozwalają narysować kształt jako wycinek, aby umożliwić przycięcie dowolnej innej grafiki.

**Kolory:** mają różnorodność, taką jak skala szarości, RGB, CMYK i CIE. Specjalne rodzaje kolorów są modelowane jako różne cechy: kolory dodatkowe, mapowanie kolorów, a nawet cieniowanie i powtarzające się wzory.

**Tekst:** w pełni zintegrowany z grafiką. Ponadto model Adobe Imaging umożliwia wyświetlanie znaków tekstowych jako kształtów graficznych, które mogą być obsługiwane przez zwykłych operatorów graficznych.

**Spróbkowane obrazy**: pobrane z oryginalnych źródeł (zeskanowanych fotografii) lub mogą być wytworzone syntetycznie. Język PostScript oferuje różnorodne sposoby odtwarzania obrazów w dowolnej rozdzielczości i zgodnie z różnymi modelami kolorów na urządzeniu wyjściowym.

Język programowania ogólnego przeznaczenia może wykorzystać możliwości graficzne języka PostScript, osadzając Ps w jego ramach. Prymitywne typy danych, takie jak liczby, znaki, tablice i łańcuchy; prymitywy kontrolne, takie jak pętle, procedury i instrukcje warunkowe; a niektóre niekonwencjonalne funkcje, takie jak słowniki, są określone w języku. Te funkcje ułatwiają programistom pisanie poleceń w celu wywołania operacji wyższego poziomu. Te operacje na wysokim poziomie spełniają potrzeby złożonych aplikacji. Taka praktyka jest bardziej zwarta i wydajniejsza niż stosowanie stałego zestawu podstawowych operacji.

Programy napisane w PostScript mogą być tworzone, przekazywane i interpretowane w postaci tekstu źródłowego ASCII. Cały język można zdefiniować w postaci drukowalnych znaków i spacji. Ta reprezentacja pomaga programistom w łatwym tworzeniu, manipulowaniu i zrozumieniu języka. Ponadto przechowywanie i przesyłanie plików między różnymi komputerami i systemami operacyjnymi było wygodne dzięki niezależności maszyn.

Binarnie zakodowane formy języka są możliwe, gdy program ma zagwarantowaną w pełni przejrzystą ścieżkę komunikacyjną do interpretera PostScript. Ścisła spójność z reprezentacją ASCII programów PS jest zalecana przez firmę Adobe w przypadku wymiany dokumentów lub przechowywania archiwalnego.

## Wersje ##

PS(.ps) to rozszerzenie pliku dokumentu PostScript. Archiwa Narodowe Wielkiej Brytanii kategoryzują pięć chronologicznych wersji pliku PostScript, zdefiniowanych w wersji DSC: wersje 1.0, 2.0, 2.1, 3.0, 3.1. Każda wersja definiuje ważne komentarze dotyczące struktury. Encapsulated PostScript File (EPS) to specjalny podtyp pliku PostScript, który wykorzystuje język do określenia prostokątnej grafiki. Podręcznik referencyjny języka PostScript opisuje plik EPS w następujący sposób: „Enkapsulowany plik PostScript (EPS) to program PostScript opisujący co najwyżej pojedynczą stronę w formie, którą można zaimportować przez inne aplikacje w celu osadzenia w dokumencie zawierającym”. Plik dokumentu PostScript może zawierać w sobie plik EPS. Dodatkowe użycie PostScript jest wymienione jako Display PostScript (DPS). DPS generuje grafikę na ekranie za pomocą silnika graficznego, który wykorzystuje model i język obrazowania PostScript.

## Bibliografia ##

* [Rodzina formatów PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

