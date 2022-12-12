{
  "date" : "2021-04-08",
  "keywords" :[ "plik wiosła", "format pliku wiosła", "co to jest plik wiosła", "plik", "przykład wiosła", "rozszerzenie pliku wiosła", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - format pliku archiwum OpenSimulator",
  "description":"Poznaj format plików OAR i interfejsy API, które mogą tworzyć i otwierać pliki OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Czym jest plik OAR?

Plik z rozszerzeniem .oar to plik archiwum używany przez aplikację OpenSimulator, która jest serwerem aplikacji 3D typu open source do tworzenia środowiska wirtualnego dostępnego dla wielu użytkowników przez sieć. Format pliku OAR zapewnia niezbędne dane o zasobach wymagane do pełnego załadowania terenu, tekstur obiektów i zapasów w innym systemie. OpenSimulator ma również opcjonalną hipersiatkę, która pozwala użytkownikom odwiedzać inne instalacje OpenSimulator w Internecie. Pliki OAR mają internetową aplikację / wiosło typu MIME i zawierają jeden lub więcej zarchiwizowanych plików.


## Format pliku OAR

OAR to pliki binarne, które są przechowywane w formacie skompresowanego pliku archiwalnego. Najnowsza wersja formatu pliku OAR to [wersja 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), która zawiera znaczne zmiany w stosunku do poprzedniej [wersji 0.8](http://opensimulator.org/wiki/OAR_Format_0 .8). Najnowsza wersja obsługuje przechowywanie wielu regionów w jednym OAR i nie jest wstecznie kompatybilna z wersjami OpenSimulator przed 0.7.5. Plik OAR to plik tar spakowany gzipem (tar.gz) w oryginalnym formacie unix tar (nie USTAR).

## Przykład regionów OAR
Pliki AOR mogą zawierać wiele regionów. Struktura archiwum jest następująca (ten przykład zawiera 4 regiony):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Archiwum OAR.xml

Plik kontrolny archiwum zawiera główny numer wersji służący do określania zgodności z przyszłymi zmianami formatu. Obecność zasobów w formacie OAR jest wskazywana przez element boolowski<assets_included> . Informacje o uwzględnionych regionach są zawarte w manifeście znajdującym się w pliku kontrolnym. Przykład Archive.xml jest następujący.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Bibliografia

* [Format OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

