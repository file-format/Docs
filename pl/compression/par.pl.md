{
"data":"2023-07-18",
   "keywords":[
"PAR",
"Plik PAR",
"jak otworzyć plik par",
"plik",
"rozszerzenie pliku PAR",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku PAR - plik indeksu archiwalnego",
   "description":"Dowiedz się o formacie PAR i interfejsach API, które umożliwiają tworzenie i otwieranie plików PAR.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Czym jest plik PAR?

W archiwach Parchive (PAR) plik .par odnosi się do pliku indeksu zawierającego grupę woluminów lub bloków parzystości. Ten plik indeksu służy do wykrywania błędów i odzyskiwania danych w przypadku utraty lub uszkodzenia jednego lub większej liczby plików w archiwum.

Archiwum Parchive zazwyczaj składa się zarówno z oryginalnych plików danych, jak i odpowiadających im woluminów parzystości. Woluminy parzystości tworzone są przy użyciu algorytmów korekcji błędów Reeda-Solomona. Te woluminy parzystości zawierają nadmiarowe informacje, których można użyć do odzyskania oryginalnych plików danych.

Plik .par, nazywany także zestawem woluminów z parzystością, zawiera informacje o strukturze i lokalizacji woluminów z parzystością w archiwum. Służy jako indeks lub mapa procesu odzyskiwania. Korzystając z pliku .par, specjalistyczne oprogramowanie PAR może określić, które woluminy parzystości są potrzebne i w jaki sposób należy je wykorzystać do zrekonstruowania brakujących lub uszkodzonych plików.

Kiedy jeden lub więcej plików w archiwum Parchive stanie się niedostępnych lub uszkodzonych, plik .par można wykorzystać w połączeniu z dostępnymi woluminami parzystości w celu odzyskania utraconych danych. Oprogramowanie PAR odczytuje plik .par, identyfikuje brakujące lub uszkodzone pliki i wykorzystuje woluminy parzystości do ich rekonstrukcji.

## Jak otworzyć plik PAR?

Do otwierania i używania plików .par potrzebne będzie specjalistyczne oprogramowanie PAR. Oto kilka popularnych opcji oprogramowania obsługujących pliki .par:

- **QuickPar:** QuickPar to powszechnie używane oprogramowanie PAR dla systemu Windows. Umożliwia tworzenie, weryfikację i naprawę plików PAR. Możesz otworzyć plik .par w QuickPar, aby sprawdzić jego integralność lub użyć go do naprawy uszkodzonych lub brakujących plików w archiwum Parchive.

- **MultiPar:** MultiPar to kolejne popularne oprogramowanie PAR dostępne dla systemu Windows. Obsługuje formaty plików PAR i PAR2 i zapewnia zaawansowane funkcje tworzenia, weryfikowania i naprawiania archiwów. MultiPar może otwierać pliki .par i wykonywać operacje wykrywania błędów i odzyskiwania w oparciu o dostarczone woluminy parzystości.

- **MacPAR deLuxe:** MacPAR deLuxe to oprogramowanie PAR zaprojektowane specjalnie dla systemu macOS. Obsługuje formaty plików PAR i PAR2 i zapewnia podobną funkcjonalność jak QuickPar i MultiPar. MacPAR deLuxe może otwierać pliki .par i pomagać w weryfikacji archiwów oraz odzyskiwaniu uszkodzonych lub brakujących plików.

## Format pliku PAR — więcej informacji

Format pliku PAR, powszechnie określany jako Parchive, to specyficzny format pliku używany do tworzenia danych parzystości oraz wykrywania i odzyskiwania błędów w archiwach plików. Format pliku PAR składa się zazwyczaj z trzech typów: PAR, PAR2 i PAR3.

- **PAR:** Oryginalny format pliku PAR, znany również jako PAR1, został opracowany w ramach projektu Parchive. Zawiera dane parzystości wygenerowane z oryginalnych plików danych. Pliki PAR zapewniają podstawowy poziom wykrywania i odzyskiwania błędów, ale mają ograniczenia w zakresie możliwości korekcji błędów.

- **PAR2:** PAR2 to ulepszona wersja formatu pliku PAR. Oferuje bardziej zaawansowane możliwości korekcji błędów i ulepszone funkcje odzyskiwania. Pliki PAR2 są zwykle używane do tworzenia danych parzystości, które umożliwiają odzyskanie utraconych lub uszkodzonych plików w archiwum. Pliki PAR2 zapewniają lepszą ochronę przed uszkodzeniem danych i są szeroko stosowane do celów archiwizacji plików.

- **PAR3:** PAR3 to najnowsza wersja formatu pliku PAR, zapewniająca dalsze ulepszenia w zakresie korekcji błędów i odzyskiwania. Oferuje jeszcze wyższy poziom redundancji i możliwości korekcji błędów w porównaniu do PAR2. Pliki PAR3 zaprojektowano w celu zapewnienia solidniejszych opcji ochrony i odzyskiwania danych przechowywanych w archiwach.

Zarówno formaty plików PAR2, jak i PAR3 są szeroko obsługiwane przez oprogramowanie PAR i oferują możliwość weryfikacji integralności plików w archiwum oraz odzyskiwania utraconych lub uszkodzonych danych. Pliki PAR i PAR2 są nadal powszechnie używane, natomiast pliki PAR3 stopniowo zyskują na popularności ze względu na ich ulepszone możliwości korekcji błędów.

## Bibliografia
* [Parchiwum](https://en.wikipedia.org/wiki/Parchiwum)

