{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf fájl", "fájlformátum", "mi az .ovf fájl", "fájl", "fájl kiterjesztése"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az .ovf fájlformátumról és az API-król, amelyek OVF fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"OVF fájlformátum - Virtualizációs fájl megnyitása",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Mi az OVF fájl?

Az OVF-fájl egy szöveges fájl, amely egy virtuális gépen futó szoftver csomagolásáról és terjesztéséről tartalmaz információkat. Az [Open Virtualization Standard Specifications] (https://www.dmtf.org/standards/ovf) szerint van formázva, amely leírja az alkalmazások virtuális gépeken való futtatásához szükséges összes követelményt (például biztonság, hordozhatóság, hatékonyság és bővíthetőség). A Nemzetközi Szabványügyi Szervezet (ISO) az OVF-et ISO 17203 szabványként fogadta el.

## Az OVF fájlformátum rövid története

Az OVF fájlformátumot a DMTF (Distributed Management Task Force) vezette be, amely nyílt kezelhetőségi szabványokat hoz létre. Független minden adott hipervizortól vagy utasításkészlet-architektúrától. Az OVF csomag egy vagy több virtuális rendszert tartalmaz, amelyek mindegyike telepíthető egy virtuális gépre.

## OVF fájlformátum - További információ

Egy OVF-csomag több fájlból áll, amelyek egyetlen könyvtárban vannak elhelyezve. Ezek közül pontosan egy OVF-leíró (.ovf kiterjesztéssel) fájlt tartalmaz, amely [XML](/hu/web/xml/) fájlformátumban van tárolva. Leírja a csomagolt virtuálisgép-információkat és az OVF-csomag metaadat-információit, például:

* név
* hardverkövetelmények
* hivatkozások az OVF csomag többi fájljára, és
* ember által olvasható leírások

Az OVF-csomagban található egyéb fájlok közé tartozik egy vagy több lemezkép és opcionálisan tanúsítványfájlok és egyéb segédfájlok.

## Hivatkozások

* [Nyílt virtualizációs formátum – DMTF](https://www.dmtf.org/standards/ovf)
* [OVF fájlformátum specifikációi](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

