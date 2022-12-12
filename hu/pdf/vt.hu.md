{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT fájlformátum",
  "description":"Tudjon meg többet a PDF/VT fájlformátumról és az API-król, amelyekkel PDF/VT fájlokat hozhat létre és nyithat meg.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Mi az a PDF/VT? #

A 2010 augusztusában szabványként [ISO 16612-2](https://www.iso.org/standard/46428.html) néven közzétett PDF/VT-t úgy tervezték, hogy lehetővé tegye a változó dokumentumok nyomtatását (VDP) különféle környezetek. A szabvány a változó információk és a tranzakciós nyomtatást teszi a szabvány alapjául. A Változó adatok nyomtatása akkor használatos, ha az információ egy része a tartalom minden egyes címzettje esetében eltérő. A tranzakciós nyomtatás számlákat, kivonatokat és egyéb dokumentumokat tartalmaz, amelyek a számlázási információkat marketinginformációkkal kombinálják. Ez a képek, szövegek és egyéb tartalomtípusok jobb feldolgozását eredményezi. A PDF/VT lehetővé teszi az oldalak megbízható és dinamikus kezelését a nagy volumenű tranzakciós kimeneti (HVTO) nyomtatási adatokhoz a dokumentumrész-metaadat (DPM) koncepció használatával. A PDF/VT fájlok megnyithatók az Adobe Acrobat Viewerben anélkül, hogy bármilyen más összetevőt kellene hozzáadni.

## Dokumentum rész hierarchia ##

A dokumentumrész (DPart) hierarchia olyan, mint a dokumentumrész-csomópontok fastruktúrája, amely a dokumentum összes lapján alapul. A fa elemeit DPart csomópontoknak nevezzük. Minden belső csomópont tartalmaz további DPart csomópontokat, és mindegyik levélcsomópont egy vagy több oldalt határoz meg egy címzett számára. Lényegében a DPart hierarchia határozza meg a PDF/VT-fájlban lévő dokumentumok vagy dokumentumrészek sorrendjét és kapcsolatát. A DPart csomópontok fastruktúrája könnyen reprezentálja a PDF/VT-dokumentumok belső tartalmát, mivel számos címzett számára tartalmazhat aldokumentumot, és minden dokumentumrész egyetlen címzett oldalainak felel meg. A DPart hierarchia szükséges a PDF/VT fájlokban.

## Dokumentumrész metaadatai (DPM) ##

A dokumentumrész-metaadatok (DPM) a dokumentumrész-hierarchia minden csomópontjához vannak társítva, és felhasználhatók információk közlésére egy adott címzett aldokumentumáról és annak részeiről. Különösen a DPM tartalmazhat információkat a tulajdonságokról vagy információkat a címzettekről kódolt formában.

## Megfelelőségi szintek ##

A PDF/VT a következő három megfelelőségi szintre vonatkozik. Ezek mind a [PDF](/hu/pdf/) 1.6-on alapulnak.

* `PDF/VT-1` – PDF/X-4 alapú, és tartalmazza a PDF-dokumentum megjelenítéséhez szükséges összes erőforrást.
* `PDF/VT-2` – Több fájlcserére tervezték, a PDF/VT-2 dokumentumok hivatkozhatnak külső kimeneti célokra, külső tartalomra vagy mindkettőre. A PDF/VT-dokumentumot és az összes hivatkozott PDF-fájlt és külső kimeneti szándékot összefoglalóan PDF/VT-2-fájlkészletnek nevezzük. Az Acrobat 9 és támogatja ezt a funkciót.
* "PDF/VT-2s" - Támogatja a PDF/VT-2 élő közvetítést. Ez lehetővé teszi az adatok szegmentált szakaszainak feldolgozását.

## Hivatkozások ##

* [PDF/VT – a Wikipédia által](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Graphic Technology](https://www.iso.org/standard/46428.html)

