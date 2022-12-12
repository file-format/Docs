{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook e-mail formátum",
  "description":"További információ az MSG fájlformátumról és az MSG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az MSG fájl?

Az MSG egy fájlformátum, amelyet a [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) és az Exchange használ e-mail üzenetek tárolására. , kapcsolatfelvétel, időpont egyeztetés vagy egyéb feladatok. Az ilyen üzenetek egy vagy több e-mail mezőt tartalmazhatnak a feladóval, a címzettel, a témával, a dátummal és az üzenet törzsével, vagy kapcsolattartási adatokkal, találkozó részleteivel és egy vagy több feladatmeghatározással. A Message objektumot alkotó tulajdonságok, beleértve az MSG fájl részét is. Az MSG-fájl fejléceket, fő üzenettörzset és hiperhivatkozásokat tartalmaz egyszerű ASCII-szövegként. Az MSG fájlok a Microsoft Messaging Applications Programming Interface-t (MAPI) igénylő programokkal is használhatók.

## MSG fájl szerkezet

A CFB_3 formátum az MSG fájl alapja. A paradigma a tároló- és adatfolyam-koncepciókon alapul, meglehetősen közel a könyvtárakhoz és fájlokhoz. Ezért az előbbiben a fő különbség a teljes hierarchia, amely egy külön fájlba van csomagolva, amelyet összetett fájlnak neveznek. Az objektumok alkotják az üzenetfájlokat, és egyetlen tulajdonságból vagy annak gyűjteményeiből állnak. Ez a képesség lehetővé teszi az alkalmazások számára, hogy bonyolult, strukturált adatokat egyetlen fájlban tároljanak. Ez a formátum több tárolót is meghatároz, mindegyik tároló az Üzenet objektumot jelenti fő összetevőként. Ezek a tárolók számos adatfolyamot tartalmaznak, amelyek az adott összetevő egy tulajdonságát képviselik. Raktár beágyazása is lehetséges.

## Mapi tulajdonságai

Az .msg fájl legfelső szintjén a tárolók olyan adatfolyamokat tartalmaznak, amelyek tulajdonságokat tárolnak bennük. Az ingatlanok a következő kategóriákba sorolhatók:

* Rögzített hosszúságú tulajdonságok
* Változó hosszúságú tulajdonságok
* Több értékű tulajdonságok

A kategóriától függetlenül egy tulajdonság címkézett vagy elnevezett. A megnevezett tulajdonságokhoz azonban megfelelő leképezési információra van szükség, ahogyan azt a leképezési tárhelyük meghatározza.

## Tárolók

A tárolók az Üzenetobjektum kulcsfontosságú összetevői. Az MSG fájlformátum a következő tárolókat tartalmazza:

## Legfelső szintű szerkezet

Az üzenetobjektum az MSG fájlformátum teljes felső szintjét képviseli. A típustól, tulajdonságoktól, a címzett és a melléklet objektumok számától függően egy üzenetobjektum különböző adatfolyam-tárolókkal rendelkezhet a megfelelő .MSG fájlban.

### Kapcsolat más struktúrákkal

Az Msg fájlformátumnak a következő kapcsolatai vannak más struktúrákkal:

* Az .msg alapja az összetett fájl bináris fájlformátum.
* Ez a formátum az Message and Attachment Object Protocol által használt tulajdonságokat használja.

## Forgatókönyvek az MSG formátumok elkerülésére

Az üzenetobjektum megosztható az .msg fájlrendszert használó ügyfelek vagy üzenettárolók között. Kevés olyan körülmény van, amikor nem lenne megfelelő egy Üzenetobjektumot .msg fájlformátumban tárolni. Például:

* Nagyméretű önálló archívum fenntartása esetén jobb, ha olyan teljes értékű formátumot használunk, amelyben a nézetek pontosabban jeleníthetők meg.
* Ha a vevő ismeretlen, előfordulhat, hogy a formátumot a vevőoldal nem támogatja, és privát vagy irreleváns lesz kézbesítve.

## MSG fájl példa

Ha képet szeretne kapni arról, hogyan néz ki egy MSG-fájl, töltsön le egy [minta MSG-fájlt] (https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg), és nyissa meg számítógépen a tartalmának megtekintéséhez.

## Hivatkozások

* [[MS-OXMSG]: Outlook MSG fájlformátum](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

