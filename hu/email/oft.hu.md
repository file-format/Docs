{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Microsoft Outlook e-mail sablonfájl",
  "description":"További információ az OFT fájlformátumról és az OFT-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az OFT fájl?

Az .oft kiterjesztésű fájlok a Microsoft Outlook segítségével létrehozott sablonfájlok. Az üzenetsablonokhoz előre formázott elrendezést ezután a rendszer a közös információkat tartalmazó e-mailek kiküldésére használja, hogy időt takarítson meg. Ilyen fájlok hozhatók létre egy új e-mail létrehozásával, a szükséges információk hozzáadásával, majd a Microsoft Outlook Mentés Office-sablonként (.oft) legördülő menüjével. A felhasználók dupla kattintással megnyithatják az OFT fájlokat, és megnyílik az adott rendszer kapcsolódó alkalmazásában.

## OFT fájlstruktúra ##

Az .OFT fájlformátum az [MSG](/hu/email/msg/) fájlformátumot használja alapjában. Az egyetlen különbség az, hogy az OFT fájlok tárolási osztálya a CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) (WriteClassStg), míg az MSG fájlok a CLSID_MailMessage ({00020D-0-0B-060000000600000000000000000000000000000.

A CFB_3 formátum az MSG fájl alapja. A paradigma a tároló- és adatfolyam-koncepciókon alapul, meglehetősen közel a könyvtárakhoz és fájlokhoz. Ezért az előbbiben a fő különbség a teljes hierarchia, amely egy külön fájlba van csomagolva, amelyet összetett fájlnak neveznek. Az objektumok alkotják az üzenetfájlokat, és egyetlen tulajdonságból vagy annak gyűjteményeiből állnak. Ez a képesség lehetővé teszi az alkalmazások számára, hogy bonyolult, strukturált adatokat egyetlen fájlban tároljanak. Ez a formátum több tárolót is meghatároz, mindegyik tároló az Üzenet objektumot jelenti fő összetevőként. Ezek a tárolók számos adatfolyamot tartalmaznak, amelyek az adott összetevő egy tulajdonságát képviselik. Raktár beágyazása is lehetséges.

### OFT tulajdonságok

Az .msg fájl legfelső szintjén a tárolók olyan adatfolyamokat tartalmaznak, amelyek tulajdonságokat tárolnak bennük. Az ingatlanok a következő kategóriákba sorolhatók:

* Rögzített hosszúságú tulajdonságok
* Változó hosszúságú tulajdonságok
* Több értékű tulajdonságok

A kategóriától függetlenül egy tulajdonság címkézett vagy elnevezett. A megnevezett tulajdonságokhoz azonban megfelelő leképezési információra van szükség, ahogyan azt a leképezési tárhelyük meghatározza.

### OFT tárolók

A tárolók az Üzenetobjektum kulcsfontosságú összetevői. Az MSG fájlformátum a következő tárolókat tartalmazza:

### Legfelső szintű struktúra

Az üzenetobjektum az Msg fájlformátum teljes felső szintjét képviseli. A típustól, a tulajdonságoktól, a címzett és a melléklet objektumok számától függően egy üzenetobjektum különböző adatfolyam-tárolókkal rendelkezhet a megfelelő .MSG fájlban.

#### Kapcsolat más struktúrákkal

Az MSG/OFT fájlformátumnak a következő kapcsolatai vannak más struktúrákkal:

* Az .msg alapja az összetett fájl bináris fájlformátum.
* Ez a formátum az Message and Attachment Object Protocol által használt tulajdonságokat használja.

## Hivatkozások

* [[MS-OXMSG]: Outlook MSG fájlformátum](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

