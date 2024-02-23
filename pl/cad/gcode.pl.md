{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Plik GCODE - Co to jest plik .gcode i jak go otworzyć?",
   "description":"Dowiedz się o formacie pliku GCODE i interfejsach API, które umożliwiają tworzenie i otwieranie plików GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-pl",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Co to jest plik GCODE?

**Plik GCODE** to zwykły plik tekstowy zawierający instrukcje dotyczące sterowania skomputeryzowanymi obrabiarkami i drukarkami 3D; Kod G, czyli kod geometryczny”, to język używany do sterowania ruchami i działaniami maszyn **CNC (Computer Numerical Control)**; Do maszyn CNC zaliczają się frezarki, tokarki, routery i drukarki 3D.

Polecenia kodu G są zapisane w określonej składni, zazwyczaj składającej się z liter i cyfr; każde polecenie instruuje maszynę, aby wykonała określoną czynność, taką jak przesunięcie narzędzia do określonej pozycji, zmiana narzędzia lub regulacja prędkości.

Kod G jest często generowany przez oprogramowanie **CAM (Computer Aided Manufacturing)**; Oprogramowanie CAM pobiera model 3D lub projekt 2D i generuje odpowiednie ścieżki narzędzia oraz instrukcje w kodzie G; plik kodu G jest następnie ładowany do maszyny CNC lub drukarki 3D w celu wykonania.

Pliki G-code mają zazwyczaj rozszerzenie .nc” lub .gcode”, na przykład program.nc” lub print.gcode”.

## Struktura pliku GCODE:

Pliki GCODE to zwykłe pliki tekstowe, w których każda linia zawiera określone polecenie; polecenia te obejmują sterowanie ruchem maszyny, regulację temperatury, prędkości i innych parametrów kluczowych dla wytworzenia obiektu.

Składnia GCODE obejmuje kombinację liter i cyfr; każdy reprezentuje odrębną akcję lub parametr; typowe polecenia obejmują G0 i G1 do ruchu, M3 i M5 do sterowania wrzecionem oraz S i F do regulacji prędkości i posuwu.

## Generowanie GCODE:

Oprogramowanie do krojenia, takie jak **Simplify3D** i **Slic3r**, tłumaczy rysunki CAD na GCODE; Oprogramowanie CAD służy do tworzenia modeli 3D, które są następnie eksportowane w formatach takich jak STL; oprogramowanie do krojenia pobiera te modele i generuje plik GCODE określający szczegóły, takie jak wysokość warstwy, prędkość drukowania i ustawienia temperatury.

## Przykład GKODU

Oto prosty przykład kodu G dla ruchomej maszyny CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Jak otworzyć plik GCODE?

Do otwarcia pliku G-code możesz użyć różnych typów oprogramowania, w zależności od potrzeb.

Jeśli wygenerowałeś kod G dla drukarki 3D; możesz go otworzyć za pomocą oprogramowania dołączonego do drukarki 3D lub dedykowanego oprogramowania do krojenia; przykłady obejmują **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** lub **Repetier-Host**; programy te często mają przyjazny dla użytkownika interfejs, który umożliwia ładowanie i wizualizację kodu G.

Pliki GCODE są zwykłym tekstem, więc można je otworzyć w dowolnym edytorze tekstu; popularne edytory tekstu to **Notatnik (w systemie Windows)**, **TextEdit (w systemie macOS)** lub **Gedit (w systemie Linux)**; po prostu **kliknij prawym przyciskiem myszy** plik kodu G, wybierz **Otwórz za pomocą”** i wybierz edytor tekstu.

