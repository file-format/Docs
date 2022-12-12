{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ Compiled Resource Script",
  "description":"Tudjon meg többet a RES fájlformátumról RES példával és API-kkal, amelyek RES fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az a RES fájl?
A .res utótaggal vagy kiterjesztéssel rendelkező fájl számos fájlformátum-kategóriához tartozhat. Itt a RES fájlformátumról beszélünk, amely egy C++ Compiled Resource Script; a Microsoft Resource Compiler (rc) által létrehozott bináris fájl, amely erőforrásadatokat tartalmaz; az erőforrás-definíciós fájl tartalma alapján; szülőszoftver-projektje szempontjából releváns. A .res fájlt általában erőforrásobjektum-fájllá formázzák át, hogy összekapcsolják egy alkalmazás végrehajtható fájljával.

## RES fájlformátum
A RES fájlformátum a Microsoft Resource Compiler (rc) programhoz tartozik. Az erőforrás-fordító egy olyan eszköz, amely összeállítja az alkalmazás által használt erőforrásokat, például kurzorokat, ikonokat, menüket és párbeszédpaneleket. Az erőforrásfájlok általában .res kiterjesztéssel rendelkeznek; erőforrásokat tartalmaz, például kurzorokat, képeket és verzióinformációkat. A RES fájl lehet 16 vagy 32 bites erőforrásfájl.
## Erőforrás fájl szerkezete
Az erőforrásfájl különféle erőforrás-bejegyzések sorozatát tartalmazza. Minden bejegyzés egy erőforrásfejlécet és releváns adatokat tartalmaz. Az erőforrásfejléc általában duplaszó-igazítású a fájlban, és a következőket tartalmazza:

- Egy **DWORD** az erőforrásfejléc méretének megadásához
- Egy **DWORD** az erőforrásadatok méretének megadásához
- Az erőforrás típusa
- Az erőforrás neve
- További információ a forrásokról

Az erőforrás fejléc szerkezete határozza meg a RES fájl formátumát. Az erőforrás adatai az erőforrás fejlécet követik. Egyes erőforrások erőforrás-specifikus csoportfejléc-mintát is adnak hozzá, hogy információkat nyújtsanak az erőforrások csoportjáról. Az alábbiakban felsorolunk néhány erőforrás-bejegyzéstípust és leírásukat:

### Accelerator Table Resources
A gyorsítótábla egy erőforrás-bejegyzés egy RES-fájlban, csoportfejléc nélkül. Az **ACCELTABLEENTRY** minta határozza meg a gyorsítótáblázat minden bejegyzését. Egy RES fájlnak több gyorsítótáblája is lehet.

### Kurzor és ikon források
Bár a rendszer minden ikont és kurzort egyetlen fájlnak tekint, de ezeket a RES fájlokban ikon-erőforrások csoportjaként vagy kurzorerőforrások csoportjaként tárolja. Az ikon- és kurzorerőforrások fájlformátuma megegyezik. Az erőforráscsoport-fejléc a .res fájlban található összes ikon- vagy kurzorcsoport-összetevőt követi.

### A párbeszédpanel forrásai
Egy párbeszédpanel erőforrás-bejegyzésként is megvalósul a RES fájlban. Tartalmaz egy **DLGTEMPLATE** párbeszédpanel fejlécmintát és egy **DLGITEMTEMPLATE** mintát a párbeszédpanel minden egyes vezérlőeleméhez. A **DLGTEMPLATEEX** és a **DLGITEMTEMPLATEEX** minták magyarázzák a kiterjesztett párbeszédpanel-erőforrások formátumát.

### Betűkészlet-források
Egy menüerőforrás tartalmaz egy **MENUHEADER** mintát, majd egy vagy több **NORMALMENUITEM** vagy **POPUPMENUITEM** mintát, egyet a menüsablon minden menüpontjához. A **MENUEX_TEMPLATE_HEADER** és a **MENUEX_TEMPLATE_ITEM** minták magyarázzák a kiterjesztett menüforrások formátumát.

### Üzenettáblázat-források
Az üzenettáblázat formázott szövegből áll, amely hibaüzenetként vagy üzenetdobozban jelenik meg. Az üzenettábla-erőforrás fő mintája a **MESSAGE_RESOURCE_DATA** struktúra.

### Verzióforrások
A verzió-erőforrás fő mintája a **VS_FIXEDFILEINFO**. További minták közé tartozik a **VarFileInfo** a nyelvi információkkal kapcsolatos adatok tárolására és a **StringFileInfo** az egyéni karakterlánc-információk tárolására.




## Hivatkozások

* [Forrásfájl-formátumok](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



