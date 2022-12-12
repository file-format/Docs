{
  "date" : "2019-10-11",
  "keywords" :[ "vssm fájl", "vssm fájlformátum", "mi az a vssm fájl", "fájl", "vssm példa", "vssm fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM – Microsoft Visio Macro Enabled File Format",
  "description":"További információ a VSSM fájlformátumról és az API-król, amelyek VSSM fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VSSM fájl?

A .vssm kiterjesztésű fájlok olyan Microsoft Visio Stencil fájlok, amelyek támogatják a makrókat. A VSSM-fájl megnyitásakor lehetővé teszi a makrók futtatását a kívánt formázás és az alakzatok diagramon belüli elhelyezése érdekében. Általánosságban elmondható, hogy a Microsoft Visio olyan rajzszoftver, amely lehetővé teszi olyan fájlok létrehozását, amelyek különböző formájú felhasználó által meghatározott információkat tartalmazhatnak és ábrázolhatnak. Ezek közül a leggyakoribbak többek között az UML diagramok, folyamatábrák, vizuális objektumok, információáramlás, szervezeti diagramok, szoftver diagramok, hálózati elrendezés, adatbázismodellek, objektumleképezés és egyéb hasonló információk. A Visio segítségével létrehozott fájlok különböző fájlformátumokba is konvertálhatók, például [PNG](/hu/Image/PNG/), [BMP](/hu/Image/BMP/), [PDF](/hu/pdf/) és mások.

## VSSM fájlformátum

A VSSM fájlformátumot a Microsoft Visio 2013-ban vezették be, amely az OpenOffice XML specifikációkon alapul. Bizonyos egyéb fájltípusok, amelyek a Visio 2013 fájlformátumot tartalmazzák, a következők:

* .vsdm (Visio makró-kompatibilis rajz)
* .vssx (Visio stencil)
* .vssm (Visio makró-kompatibilis sablon)
* .vstx (Visio sablon)
* .vstm (Visio makró-kompatibilis sablon)

A motorháztető alatt a Visio 2013 fájlformátum strukturált módon tárolja az alkalmazásadatokat a kapcsolódó erőforrásokkal együtt egy archívumban, például [ZIP](/hu/Compression/ZIP/). A ZIP fájl bármely szabványos kicsomagoló segédprogrammal kibontható, ahol más típusú fájlokat is tartalmaz.

Minden Visio-fájlt más fájlokat vagy részeket tartalmazó csomagnak neveznek. A csomag része lehet XML fájl, kép vagy akár VBA-megoldás is. A csomagon belüli részek feloszthatók „dokumentum” és „kapcsolat” részekre.

## Referenciák ##

* [Bevezetés a Visio fájlformátumba](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

