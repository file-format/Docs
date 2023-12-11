{
"data":"2023-10-11",
   "keywords":[
"mtl",
"plik mtl",
"plik biblioteki szablonów materiałów mtl obj",
"jak otworzyć plik mtl",
"plik",
"rozszerzenie pliku mtl",
"rozszerzenie",
"plik"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"Format pliku MTL - plik biblioteki szablonów materiałów OBJ",
   "description":"Dowiedz się więcej o formacie pliku biblioteki szablonów materiałów MTL OBJ i interfejsach API, które umożliwiają tworzenie i otwieranie plików MTL.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Czym jest plik MTL?

Plik MTL, skrót od **Material Template Library**, to format pliku towarzyszącego używany w grafice komputerowej 3D i modelowaniu. Często jest kojarzony z **formatem pliku Wavefront OBJ**, który jest powszechnym formatem przechowywania modeli 3D oraz powiązanych z nimi materiałów i tekstur.

## Biblioteka szablonów materiałów

Oto ważne informacje na temat plików MTL:

1. **Definicje materiałów**: Plik ".mtl" zawiera definicje materiałów stosowanych do obiektów 3D w odpowiednim pliku OBJ. Każda definicja materiału określa różne właściwości, takie jak kolor, połysk, przezroczystość i mapy tekstur.
    





2. **Format tekstowy**: Pliki ".mtl" to zazwyczaj zwykłe pliki tekstowe, co oznacza, że można je łatwo edytować za pomocą edytora tekstu. Każda definicja materiału składa się z zestawu stwierdzeń, które definiują atrybuty materiału.
    





3. **Mapowanie tekstur**: Jedną z podstawowych funkcji pliku ".mtl" jest zdefiniowanie sposobu mapowania tekstur (plików obrazów) na powierzchnie modelu 3D. Określa ścieżkę pliku tekstury oraz sposób jej zawinięcia lub zastosowania do modelu.
    





4. **Przykładowe wyciągi MTL**: Oto kilka przykładowych wyciągów, które możesz znaleźć w pliku ".mtl":
    





- `newmtl MaterialName`: Definiuje nowy materiał o nazwie "MaterialName".
- `Ka rgb`: Kolor otoczenia materiału określony w wartościach RGB.
- `Kd rgb`: Rozproszony kolor materiału, określony w wartościach RGB.
- `Ks rgb`: Odblaskowy kolor materiału, określony w wartościach RGB.
- `Wartość Ns`: Połysk lub wykładnik lustrzany materiału.
- `map_Kdtexturefile.jpg`: Określa mapę rozproszonej tekstury materiału.
5. **Wiele materiałów**: Plik OBJ może odwoływać się do wielu materiałów, a każdy materiał jest zdefiniowany w pliku ".mtl". Pozwala to na tworzenie złożonych modeli 3D z różnymi materiałami zastosowanymi do różnych części.
    





6. **Kompatybilność**: Pliki ".mtl" są szeroko obsługiwane przez oprogramowanie do modelowania 3D i silniki renderujące, umożliwiając przesyłanie modeli 3D i ich materiałów pomiędzy różnymi aplikacjami.

## Jak otworzyć plik MTL?

Plik MTL to pliki tekstowe, więc można je otworzyć za pomocą dowolnego edytora tekstu, w tym

- Notatnik (Windows)
- Notatnik++ (Windows)
- Kod Visual Studio
- Wzniosły tekst
- Atom
- TextEdit (macOS)

Programy otwierające pliki MTL lub odwołujące się do nich obejmują

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Gepard3D

**Podtyp:** Pliki obrazów 3D

## Bibliografia
* [Plik Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

