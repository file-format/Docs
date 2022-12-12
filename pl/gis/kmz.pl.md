{
  "date" : "2019-10-11",
  "keywords" :["plik kmz", "co to jest plik kmz", "plik", "przykład kmz", "rozszerzenie pliku kmz", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Spakowany format pliku KML",
  "description":"Dowiedz się o formacie pliku KMZ i interfejsach API, które mogą tworzyć i otwierać pliki KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik KMZ?

Plik KMZ (KML Zipped) jest reprezentacją skompresowanego pliku [KML](/pl/gis/kml/), który zawiera informacje geoprzestrzenne widoczne w aplikacjach GIS, takich jak Google Earth. Informacje o oznaczeniach miejsc są reprezentowane w pliku jako szerokość i długość geograficzna wraz z niestandardową nazwą. Pojedynczy spakowany plik KMZ można łatwo udostępniać innym użytkownikom. Pliki KMZ mogą również zawierać dane modelu 3D do reprezentacji geograficznej modelu. Plik KMZ można otworzyć w Mapach Google, zapisując plik w lokalizacji online, a następnie wpisując adres URL w polu wyszukiwania w Mapach Google.

## Struktura plików ##

Zawartość pliku MKZ składa się z głównego pliku KML i zero lub więcej powiązanych plików. Można go wyodrębnić za pomocą standardowego narzędzia do dekompresji, takiego jak WinZIP. Format pliku KMZ jest również kompresowany do archiwum ze współczynnikiem kompresji 10:1. Możesz eksportować dane z Google Earth, takie jak aplikacje, bezpośrednio do formatu pliku KMZ. Główny plik KML nosi nazwę **doc.kml**. Podczas pakowania pliku KMZ można dodać do niego więcej niż jeden plik KML, ale nie przyniesie to korzyści, ponieważ program Google Earth wyszukuje pierwszy plik KML podczas otwierania pliku KMZ i odczytuje go. Ignoruje wszelkie dalsze pliki KML znalezione w archiwum. Aby mieć pewność, że żądany plik KML zostanie odczytany przez program Google Earth, zaleca się umieszczenie tylko jednego pliku KML w pliku KMZ.

Obrazy, modele, tekstury, pliki dźwiękowe i inne zasoby, do których odwołuje się plik doc.kml, są umieszczane w innym podfolderze w folderze głównym. Może to również wiązać się z pewną złożonością w zależności od liczby plików pomocniczych. Linki do tych zasobów składowych mogą być odniesieniami względnymi lub bezwzględnymi.

### Odniesienia względne ###

Gdy zasoby są umieszczane obok głównego pliku doc.kml w podfolderze w folderze głównym, odniesienia względne mogą wskazywać na te pliki pomocnicze, jak pokazano w poniższym przykładzie (tylko dla ikon).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Bezwzględne odniesienie ###

Do zasobów można również odwoływać się absolutnie. Odniesienia bezwzględne zawierają pełny adres URL połączonego pliku. Gdy pliki są umieszczane na centralnym serwerze, odniesienia bezwzględne gwarantują, że pozostaną one jednoznaczne w porównaniu z odniesieniami względnymi. Nie zaleca się bezwzględnego odwoływania się do pliku lokalnego, ponieważ linki te zostaną przerwane, gdy pliki zostaną przeniesione do nowego systemu. Przykład odwołania bezwzględnego jest następujący:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Zobacz też ##

* [GeoJSON](/pl/gis/geojson/)

## Bibliografia ##

* [Pliki Google Earth i KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

