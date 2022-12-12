{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - e-mail üzenet",
  "description":"További információ az EML fájlformátumról és az API-król, amelyek EML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Mi az EML fájl?

Az EML fájlformátum az Outlook és más releváns alkalmazások segítségével mentett e-mail üzeneteket jelöli. Szinte minden levelező kliens támogatja ezt a fájlformátumot, hogy megfeleljen az RFC-822 internetes üzenetformátum szabványnak. A Microsoft Outlook az alapértelmezett szoftver az EML üzenettípusok megnyitásához. Az EML fájlok lemezre menthetők, valamint kommunikációs protokollok segítségével kiküldhetők a címzetteknek.

## Az EML rövid története

Az EML fájlformátum specifikációi az [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) szabványos formátum szerint érhetők el. Az RFC-822 előtt az RFC-733 szabályozta a hálózati üzenetváltás szabályait 1982-ig, az előbbit a laterális továbbfejlesztéseként hozták létre az ARPA szabványok létrehozásával. Ezzel egy időben a Microsoft létrehozta saját COM moduljait saját levelezőprogramja, azaz az Outlook Express fejlesztéséhez. Az RFC-822 szabadalmaztatott formátumként való létrehozásának útját választotta, amikor a Microsoft eltért a nyílt szabványtól, és létrehozta a [PST](/hu/email/pst/) fájlformátumot, amelyben az e-maileket egy rendkívül strukturált adatbázis-formátumba menti. Ez problémákat okozott a nem Microsoft levelezőprogramok felhasználóinak, amikor az e-maileket a Microsoft Outlookból továbbították.

2001-ben történt, amikor a 822-es szabványt 2822-re fejlesztették – Internet Message Format, amelyet jelenleg EML-üzenetek létrehozására, olvasására és küldésére használnak MIME RFC-822 formátumban.

## Az EML fájlformátum specifikációi

Az EML fájlok két megkülönböztetett részből állnak:

* Fejlécek – Információkat tartalmaz az üzenet fejlécéről
* Üzenettörzs – Információsorozatot tartalmaz, amely tartalmazhat üzenettartalmat, beágyazott képeket és mellékleteket

### Fejlécek információi ###

Az EML-fájl fejlécadatokból és opcionálisan üzenettörzsből áll. Az EML-ben minden fejlécsor két részből áll, amelyeket kettősponttal ":" választ el. Az első a fejléc neve, a kettőspontot követő pedig a fejléc törzse. Ilyen fejlécek például a következők:

* Feladó e-mail címe
* A címzett e-mail címe
* Az e-mail tárgya
* Az üzenet idő- és dátumbélyegzője

**Példa fejléc**

Tól től:<John@bmw.eml.light.com>

Nak nek:<Andy@fileformat.com>

Dátum: 2018. március 8., csütörtök, 10:43:37 +0100

Tárgy: bmw eml light

### Üzenettörzs ###

Az EML-üzenet törzse az e-mail elsődleges információit tartalmazza szöveg, hiperhivatkozások és mellékletek formájában. Az e-mail törzse tartalmazhat egyszerű olvasható szöveget, de ez nem szükséges. Ebben az esetben az üzenet törzse lehet üres, vagy tartalmazhat kódolt mellékletadatokat.

Az üzenettörzs tartalmát a tartalomtípus írja le, amely lehetővé teszi az olvasóalkalmazások számára, hogy a megfelelő formátumban olvassák el az információkat. Valójában egy dokumentum természetét és formátumát képviseli. A MIME típus vagy tartalomtípus felépítése nagyon egyszerű; egy típusból és egy altípusból áll, két karakterláncból, amelyeket „/” jel választ el. Nincs hely megengedett. A "típus" a kategóriát jelöli, és lehet diszkrét vagy többrészes típus. Az "altípus" minden típusra jellemző. A Tartalomtípus kategóriába tartozó típusok listája hosszú, de néhány fontos tartalomtípus a következő:


|**Típus**|**Leírás**|**Példa az altípusokra**
---|---|---|
|text|Ember által olvasható formátumot jelent|szöveg/sima, szöveg/html, szöveg/css, szöveg/javascript
|image|Bármilyen típusú képet képvisel, kivéve a videókat|image/bmp, image/png, image/jpg, image/gif
|audio|Bármilyen hangfájlformátumot képvisel|audio/mdi, audio/wav
|alkalmazás|Bármilyen bináris adatot jelöl|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### A kötődés ábrázolása az EML törzsben ###

Az EML törzse határokat tartalmaz minden benne lévő tartalomtípushoz. Az üzenettörzsben található mellékletet a tartalomtípus és a tartalomelrendezés azonosítja, amint az a következő példában látható:

Tartalom típusa: szöveges/sima; karakterkészlet#"windows-1252"; name#"apple app store.txt"
Tartalom-Diszpozíció: kötődés; fájlnév#"apple app store.txt"
Tartalom-átvitel-kódolás: base64
X-Attachment-Id: f_jkhztmd02

Mint látható, a mellékletre beállított Content-Disposition lehetővé teszi az olvasóalkalmazások számára a mellékletekkel kapcsolatos információk, például a mellékletfájl nevének és az átviteli kódolásnak a megszerzését. A melléklet fejlécének információit kódolt melléklet-tartalom követi, amelyet be kell olvasni.

#### Példa a táblázatra mellékletként ####

Tartalom típusa: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Tartalom-Diszpozíció: kötődés; fájlnév#"english_spodr.xlsx"
Tartalom-átvitel-kódolás: base64
X-Attachment-Id: f_jkhztmd43

## Hivatkozások

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

