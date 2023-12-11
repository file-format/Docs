{
"data":"2023-10-11",
   "keywords":[
"chr",
"plik chr",
"plik znakowy chr Cryengine",
"jak otworzyć plik chr",
"plik",
"rozszerzenie pliku chr",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku CHR - plik znakowy CryENGINE",
   "description":"Dowiedz się o formacie pliku znakowego CHR CryENGINE i interfejsach API, które umożliwiają tworzenie i otwieranie plików CHR.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Czym jest plik CHR?

Plik CHR w kontekście CryENGINE odnosi się do **pliku znaków CryENGINE**. CryENGINE to silnik gier opracowany przez Crytek, a pliki te służą do przechowywania modeli postaci i powiązanych danych do wykorzystania w grach wideo i innych aplikacjach czasu rzeczywistego.

## Plik znaków CryENGINE

Plik znaków CryENGINE zazwyczaj zawiera następujące komponenty:

1. **Model postaci**: Jest to model postaci 3D, obejmujący jej geometrię, tekstury i animacje. Modele te są często tworzone przy użyciu oprogramowania takiego jak Autodesk Maya lub Blender, a następnie importowane do CryENGINE.
    




















2. **Dane animacji**: CryENGINE obsługuje złożone animacje postaci, więc plik ".chr" może zawierać różne animacje, takie jak chodzenie, bieganie, skakanie i inne. Te animacje są zwykle przechowywane jako dane klatek kluczowych.
    




















3. **Informacje o riggingu**: Rigging odnosi się do procesu tworzenia szkieletu modelu postaci, który pozwala na zastosowanie animacji do modelu. Plik ".chr" może zawierać informacje o hierarchii kości i sposobie połączenia siatki postaci z tym szkieletem.
    




















4. **Dane dotyczące materiałów i tekstur**: Informacje o materiałach użytych w modelu postaci i powiązanych mapach tekstur mogą być zawarte w pliku ".chr". CryENGINE obsługuje renderowanie oparte na fizyce, więc te materiały mogą być dość szczegółowe.
    




















5. **Dane fizyczne**: Jeśli postać ma wchodzić w interakcję ze światem gry, plik ".chr" może zawierać dane fizyczne, takie jak kształty kolizji lub ograniczenia fizyki ragdoll.
    




















6. **Ustawienia konfiguracyjne**: Różne ustawienia konfiguracyjne związane z zachowaniem postaci w świecie gry, takie jak zachowanie AI lub zdarzenia skryptowe, mogą również być częścią pliku ".chr".

## CryENGINE

CryENGINE to potężny silnik gier opracowany przez Crytek, niemiecką firmę produkującą gry wideo. Jest znany ze swoich najnowocześniejszych możliwości graficznych i został wykorzystany do stworzenia oszałamiających wizualnie i zaawansowanych technologicznie gier wideo. Oto kilka kluczowych funkcji i informacji o CryENGINE:

1. **Grafika i renderowanie**: CryENGINE słynie z zaawansowanych możliwości graficznych. Obsługuje takie funkcje, jak globalne oświetlenie w czasie rzeczywistym, wysokiej jakości dynamiczne oświetlenie i cienie, renderowanie fizyczne (PBR) i tekstury o wysokiej rozdzielczości. Funkcje te przyczyniają się do tworzenia oszałamiających wizualnie i realistycznych światów gier.
    




















2. **Silnik fizyczny**: CryENGINE zawiera wbudowany silnik fizyczny, który pozwala na realistyczne interakcje pomiędzy obiektami w świecie gry. Obsługuje takie funkcje, jak fizyka ciała sztywnego, fizyka ciała miękkiego i fizyka ragdoll, dzięki czemu nadaje się do tworzenia dynamicznych i wciągających środowisk.
    




















3. **Teren i roślinność**: CryENGINE zapewnia narzędzia do tworzenia rozległych i szczegółowych środowisk zewnętrznych. Obsługuje edycję terenu, rozmieszczanie roślinności i dynamiczne systemy pogodowe, umożliwiając programistom tworzenie ekspansywnych i realistycznych scenerii zewnętrznych.
    




















4. **Animacja postaci**: CryENGINE zawiera solidne narzędzia do animacji postaci. Obsługuje złożone zestawy postaci, animację twarzy i system drzewa mieszania, który umożliwia programistom tworzenie realistycznych ruchów i animacji postaci.
    




















5. **System AI**: Silnik posiada system AI, który pozwala na tworzenie inteligentnych NPC (postaci niezależnych) i AI wroga. Programiści mogą skryptować zachowania i interakcje sztucznej inteligencji, aby tworzyć wymagające i wciągające doświadczenia związane z rozgrywką.
       





















6. **Skrypty**: CryENGINE używa języka skryptowego zwanego "Schematyc", który umożliwia programistom tworzenie logiki rozgrywki i interakcji. Dodatkowo obsługuje C++ dla bardziej zaawansowanych potrzeb programistycznych.

## Formaty plików używane przez CryENGINE

Oto kilka typowych typów plików powiązanych z CryENGINE:

1. **cryproj**: pliki projektu CryENGINE. Pliki te przechowują ustawienia i konfiguracje specyficzne dla konkretnego projektu gry.
    




















2. **.level**: Pliki poziomów zawierają dane świata gry 3D, w tym teren, obiekty, oświetlenie i inne ustawienia specyficzne dla poziomu. Poziomy są podstawowym elementem projektowania gier w CryENGINE.
    




















3. **.cgf**: Format geometrii znaku. Pliki te zawierają dane modelu 3D postaci, obiektów i innych zasobów gry. Pliki CGF mogą zawierać dane dotyczące geometrii, tekstur i animacji.
    




















4. **.chrparams**: Pliki parametrów znaków. Pliki te przechowują ustawienia i konfiguracje modeli postaci i ich animacji.
    




















5. **.dds**: Format tekstury DirectX. CryENGINE powszechnie używa plików DDS do przechowywania tekstur, w tym map rozproszonych, normalnych i innych typów tekstur.
    




















6. **.cryshader**: Pliki modułu cieniującego CryENGINE. Pliki te definiują sposób renderowania materiałów i obiektów w świecie gry, określając shadery, właściwości materiałów i nie tylko.
    




















7. **.crytif**: Plik informacji o teksturze. Pliki te przechowują dodatkowe informacje o teksturach, takie jak ustawienia kompresji, mipmapy i inne szczegóły związane z teksturami.
    




















8. **.cdf**: Plik definicji znaków. Pliki CDF służą do definiowania zasobów postaci i ich właściwości, w tym załączników, stanów animacji i ustawień związanych z postaciami.
    




















9. **.dds**: CryENGINE wykorzystuje także pliki DDS (DirectDraw Surface) dla różnych map tekstur, takich jak mapy normalne, mapy lustrzane i mapy rozproszone.
    




















10. **.anim**: Pliki animacji. Pliki te przechowują dane animacji postaci i obiektów, w tym klatki kluczowe, pozycje kości i sekwencje animacji.
    




















11. **.xml**: Pliki XML mogą być używane do różnych konfiguracji i definicji danych w CryENGINE, takich jak logika gry, zachowanie AI i nie tylko.
    




















12. **.pak**: [pliki PAK](/pl/game/pak/) to pliki archiwalne używane do pakowania zasobów i zasobów gry, dzięki czemu jest ona bardziej wydajna przy dystrybucji i ładowaniu gier.

## Jak otworzyć plik CHR?

Programy otwierające pliki CHR obejmują

- **Crytek CryENGINE SDK** (bezpłatna wersja próbna) dla systemu Windows

**Podtyp:** Pliki obrazów 3D

## Inne pliki CHR

Oto inne typy plików, które korzystają z rozszerzenia **.chr**.

**3D**
- [CHR – plik znaków CryENGINE](/pl/3d/chr-cryengine/)
- [CHR - plik znaków 3ds Max](/pl/3d/chr-3ds/)

**Czcionka i gra**
- [CHR - Zestaw znaków Borland](/pl/font/chr/)
- [CHR - Klub Literacki Doki Doki! Plik postaci](/pl/game/chr-doki/)

## Bibliografia
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

