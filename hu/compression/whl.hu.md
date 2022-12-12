{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL fájlformátum - Python Wheel csomagfájl",
  "description":"További információ a WHL fájlformátumról és az API-król, amelyek WHL-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Mi az a WHL fájl?

A WHL (Wheel) fájl egy Python kerék formátumban mentett terjesztési csomagfájl. Ez a Python disztribúciók szabványos formátumú telepítése, és tartalmazza a telepítéshez szükséges összes fájlt és metaadatot. A WHL-fájl a kerékfájl által támogatott Python-verziókról és platformokról is tartalmaz információkat. Az [MSI](/hu/executable/msi/) telepítőfájlhoz hasonlóan a WHL-fájlformátum egy telepítésre kész formátum, amely lehetővé teszi a telepítőcsomag futtatását a forrásterjesztés felépítése nélkül.

## WHL fájlformátum

A WHL fájlformátum egy [ZIP](/hu/compression/zip/) (.zip) archívum, amely tartalmazza a telepítők által a csomagok telepítéséhez szükséges összes telepítőfájlt és metaadatot. Ezek a WHL-fájlok kicsomagolhatók kicsomagolási opcióval vagy szabványos kicsomagoló szoftveralkalmazásokkal, mint például a WinZIP és a WinRAR.

### WHL fájlnévegyezmény

A WHL-fájlok elnevezése a következő konvenció szerint történik.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

A WHL fájlnév példája a következő.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* "kriptográfia" a csomag neve.
* A `2.9.2` a kriptográfia csomagváltozata. A verzió egy PEP 440-kompatibilis karakterlánc, például 2.9.2, 3.4 vagy 3.9.0.a3.
* A `cp35` a Python címke, és azt a Python-megvalósítást és verziót jelöli, amelyet a kerék megkövetel.
* Az "abi3" az ABI címke. Az ABI az alkalmazás bináris interfész rövidítése.
* A `macosx_10_9_x86_64` a platformcímke, ami történetesen elég nagy falat.

## Hivatkozások

* [Mik azok a Python-kerekek, és miért érdemes foglalkozni vele?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

