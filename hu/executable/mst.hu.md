{
  "date" : "2021-06-30",
  "keywords" :[ "mst fájl", "mst fájl formátum", "mi az mst fájl", "fájl", "mst példa", "mst fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az MST-fájlformátumról és az MST-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"MST - Windows Installer csomagfájl",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Mi az MST fájl?
Az .mst kiterjesztésű fájlokat az MSI-csomagok tartalmának átalakítására használják. Általában a rendszergazdák használják az egyéni beállítások alkalmazására egy meglévő MSI-fájlra. Az MST-fájlokat az eredeti MSI-csomaggal együtt használják szoftverelosztó rendszereikben, például csoportházirendekben. Az MST fájlokat általában szoftverfejlesztésben és tesztelésben használják a szoftver fejlesztés alatt álló verzióinak konfigurálására.

## MST fájlformátum
Az MST vagy Transform fájl a Microsoft Windows Installert fájlban használó programok telepítési opcióinak összegyűjtésére szolgál. Ezeket a fájlokat általában az Installer (MSIEXEC.EXE) parancssorban vagy a szoftvertelepítési csoportházirendben használják; egy Microsoft Active Directory tartományban. Az MST-fájlok csomagolt végrehajtható telepítőkkel is használhatók. Általános eset, hogy valaki parancssori paramétereket akar átadni a becsomagolt telepítőnek. Ehhez szüksége van egy MST-fájlra, amely hozzáadja a WRAPPED_ARGUMENTS tulajdonságot a tulajdonságtáblához. Ezeket a fájlokat nem lehet általános szerkesztőkkel létrehozni vagy szerkeszteni. Erre a célra speciális eszközök állnak rendelkezésre.

### Hogyan kell használni az MST fájlokat?
Az MST-fájlok különféle eszközökkel hozhatók létre, és az Ocra-t általában MST-fájlok generálására használják. Ezután a beállítások testreszabhatók az igényeknek megfelelően, és elmenthetők egy adott helyre. Ezt követően az MST fájlok az MSI fájlokkal együtt használhatók. Ha szeretné tesztelni ezeket a fájlokat; használja a következő szintaxist a parancssorban

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS tulajdonság

Használhatja a Windows telepítő **TRANSFORMS** tulajdonságát is, amely valójában azon átalakítások listája, amelyeket a telepítő alkalmaz a csomag telepítésekor. A telepítő az átalakításokat a TRANSFORM tulajdonságban felsorolt sorrendben hajtja végre. Az átalakítások megadhatók .mst kiterjesztésű fájlnévvel vagy teljes elérési úttal. Egynél több átalakítás megadásához válassza el az egyes fájlneveket vagy pontosvesszőt a következő példa szerint.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Hivatkozások

* [MST Transformation Files](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS tulajdonság](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


