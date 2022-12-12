{
  "date" : "2019-12-12",
  "keywords" :["JT", "plik", "rozszerzenie", "format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku JT i interfejsy API, które mogą tworzyć i otwierać pliki JT.",
  "title" :"JT - format pliku teselacji Jowisza",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik JT?

**JT** (Jupiter Tessellation) to wydajny, branżowy i elastyczny format danych 3D zgodny ze standardem ISO, opracowany przez firmę Siemens PLM Software. Mechaniczne domeny CAD w przemyśle lotniczym, motoryzacyjnym i ciężkim używają JT jako najbardziej wiodącego formatu wizualizacji 3D.

Format JT to wykres sceny, który obsługuje atrybuty i węzły specyficzne dla CAD. Do przechowywania danych fasetowych (trójkątów) wykorzystywane są zaawansowane techniki kompresji. Ten format ma strukturę umożliwiającą obsługę atrybutów wizualnych, informacji o produkcie i produkcji (PMI) oraz metadanych. Istnieje dobre wsparcie dla asynchronicznego przesyłania strumieniowego treści. W przemyśle mechaniki ciężkiej profesjonaliści używają pliku JT w swoich rozwiązaniach CAD i oprogramowaniu do zarządzania cyklem życia produktu (PLM) do badania geometrii skomplikowanych towarów.

Ponieważ JT obsługuje prawie wszystkie ważne formaty CAD 3D, jego montaż może obsługiwać różne kombinacje znane jako „multi-CAD”. To złożenie multi-CAD jest zawsze dobrze zarządzane i aktualne, ponieważ synchronizacja między rodzimymi plikami opisu produktu CAD z powiązanymi z nimi plikami JT odbywa się automatycznie. Pliki JT są pierwotnie lekkie, dlatego uważa się je za odpowiednie do współpracy internetowej. Firmy współpracują poprzez przesyłanie wizualizacji 3D za pośrednictwem nośników znacznie łatwiej w porównaniu z „ciężkimi” oryginalnymi plikami CAD. Ponadto pliki JT zapewniają wiele funkcji bezpieczeństwa, które sprawiają, że udostępnianie własności intelektualnej jest bezpieczniejsze.

## Krótka historia formatu pliku JT

Engineering Animation, Inc. i Hewlett Packard byli oryginalnymi projektantami JT, którzy opracowali ten format jako zestaw narzędzi Direct Model. Po przejęciu EAI przez UGS Corp. JT stał się częścią pakietu UGS. Na początku 2007 roku firma UGS ogłosiła JT jako główny format 3D. W tym samym roku Siemens AG kupił UGS i okazał się Siemens PLM Software. Siemens używa JT jako wspólnego formatu interoperacyjności i formatu archiwizacji danych. W 2009 roku ISO zaakceptowało specyfikację JT do publikacji jako publicznie dostępną specyfikację ISO (PAS). W połowie 2010 roku firma ProSTEP iViP ogłosiła, że na poziomie przemysłowym JT i STEP AP 242 XML mogą być używane razem, aby osiągnąć maksymalne korzyści w przetwarzaniu danych scenariusze wymiany. W 2012 roku JT został oficjalnie uznany za format wizualizacji 3D znormalizowany przez ISO (ISO 14306:2012 (ISO JT V1)).

## Format pliku JT ##

Wszystkie obiekty w formacie JT są reprezentowane przez identyfikator obiektu, a odniesienia między obiektami są obsługiwane przez identyfikator obiektu, do którego się odwołuje. Integralność tych odniesień do obiektów może być zachowana poprzez unswizzling/swizzling wskaźników.

Plik JT jest ułożony jako seria bloków, a blok nagłówka jest zawsze pierwszym blokiem danych w pliku. Seria segmentów danych i segment TOC bezpośrednio następują po bloku nagłówka. Jeden segment danych (6 segmentów LSG) posiada zawsze plik JT zgodny z referencjami. Segment TOC zawiera informacje o lokalizacji wszystkich innych segmentów danych tego pliku.

{{< figure src="../JT-1.png" alt="Format pliku JT" >}}

### Nagłówek pliku ###

Nagłówek pliku to pierwszy blok w hierarchii danych pliku JT. Informacje o wersjach i lokalizacji TOC są zawarte w nagłówku, co ułatwia programom ładującym odczytywanie plików. Zawartość nagłówka pliku jest ułożona w następujący sposób.

### Segment spisu treści ###

Segment TOC musi istnieć w pliku i zawierać informacje identyfikacyjne i lokalizacyjne wszystkich pozostałych segmentów danych. Rzeczywista lokalizacja segmentu TOC jest określona przez pole TOC Offset w nagłówku pliku. Każdy indywidualnie adresowalny Segment Danych jest reprezentowany przez wpis TOC w segmencie TOC.

### Segment danych ###

Plik JT definiuje wszystkie przechowywane dane w segmencie danych. Niektóre segmenty danych mogą kompresować wszystkie bajty danych, które pozostały w segmencie. Segmenty danych mają następującą strukturę:

![alt text](../JT-2.png "JT Data Segment")

W poniższej tabeli opisano różne typy segmentów danych:

|Nazwa|Opis
---|---|
|Segment LSG|Zawiera zbiór obiektów połączonych przez skierowane odniesienia w celu utworzenia LSG (skierowana acykliczna struktura grafu)
|Segment LOD kształtu|zawiera dane definiujące kształty geometryczne (np. wierzchołki, normalne, wielokąty itp.)
|JT B-Rep Segment|Posiadający element danych reprezentujący dokładną granicę geometryczną dla pojedynczej części w formacie JT B-Rep.
|XT B-Rep segment|Posiadanie elementu dla danych reprezentujących dokładną granicę geometryczną dla pojedynczej części w formacie reprezentacji granicy
|Segment modelu szkieletowego|Dane reprezentują precyzyjny model szkieletowy 3D dla określonej części zdefiniowanej przez element zawarty w tym segmencie.
|Meta segment danych|Pozwala przechowywać metadane w odrębnych adresowalnych segmentach.
|JT Segment ULP|Posiadający element danych reprezentujący półprecyzyjną granicę geometryczną dla pojedynczej części w formacie JT ULP.
|JT Segment LWPA|Zawiera element definiujący dane analityczne dla określonej części. LWPA zawiera zbiór powierzchni analitycznych w definicji b-rep części.

## Kompresja ##

Wymagania dotyczące transmisji i przechowywania modeli 3D są bardziej wymagające, więc pliki JT mogą korzystać z kompresji. Model danych JT może składać się z różnych plików wykorzystujących różne techniki kompresji, ale proces kompresji jest przejrzysty dla użytkownika danych JT.

Do tej pory JT Open Toolkit (w standardzie) i zaawansowana kompresja to dwie techniki kompresji plików JT. JT Open Toolkit wykorzystuje łatwy, bezstratny algorytm kompresji, podczas gdy zaawansowana kompresja wykorzystuje bardziej wyrafinowaną, specyficzną dla domeny technikę kompresji, prowadzącą do stratnej kompresji geometrii. Aplikacje klienckie wolą zaawansowaną kompresję niż standardową, ponieważ zaawansowana kompresja zapewnia dość wysokie współczynniki kompresji. Kompatybilność wsteczna ze zwykłymi aplikacjami do przeglądania plików JT jest zachowana dzięki zastosowaniu standardowej kompresji. Forma kompresji musi być kompatybilna z wersją formatu pliku JT, którą można zobaczyć, gdy plik JT zostanie otwarty za pomocą edytora tekstu i zawarty w informacjach nagłówka ASCII.

## Bibliografia ##

* [Odniesienie do formatu pliku JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (format wizualizacji)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

