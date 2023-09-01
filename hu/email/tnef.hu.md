{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"További információ a TNEF fájlformátumról és az API-król, amelyek TNEF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TNEF fájl?

A Transport Neutral Encapsulation Format (TNEF) a Microsoft által védett e-mail mellékletek beágyazásához az üzenetküldő alkalmazásprogramozási felületen (**MAPI**) alapul. A Microsoft Outlook és a Microsoft Exchange Server teljes mértékben támogatja a TNEF-et, míg később dekódolja a TNEF-et MAPI-ba, és megjeleníti a formázott leveleket. A TNEF kódolású e-mail mellékletek MIME típusú MS-TNEF típusúak, és winmail/win.dat néven tárolódnak. A winmail .dat fájl melléklete a következő információkat tartalmazza:


|Üzenet|OLE-objektumok|Outlook-szolgáltatások
---|---|---|
|<ul><li> Eredeti üzenet mellékletei</li><li> Eredeti formázott változat</li><li> betűtípusok, szövegméretek és szövegszínek</li></ul> |<ul><li> beágyazott képek</li><li> beágyazott Office dokumentumok</li></ul> |<ul><li> egyedi nyomtatványok</li><li> szavazógombok</li><li> találkozási kérések</li></ul>


Más e-mail szolgáltatások, amelyek nem támogatják a TNEF-et, egyszerű szöveget jelenítenek meg a TNEF formátumú üzenetekhez. Az Outlook az üzenetek gazdag formátumát beágyazza TNEF-fájlokba (OLE) vagy bizonyos Outlook-szolgáltatásokba (űrlapok, lekérdezési gombok és konferenciakérések). Az explicit TNEF kódolás szankcionálása az Outlook e-mail kliensen belül nem lehetséges, azonban az RTF formátum kiválasztása az e-mailek elküldéséhez implicit módon megkönnyíti a TNEF kódolást.

## TNEF fájlformátum

A TNEF adatalgoritmus gazdag hierarchikus üzenettulajdonságokból egy lapított struktúrát hoz létre. Ezek az összelapított struktúrák aztán egy soros adatfolyamot ábrázolnak, amely meghatározott tulajdonságokból áll.

Egyes helyzetekben, amikor a tulajdonságok csoportokban fordulnak elő, vagy több értékkel rendelkeznek, az adatfolyam számlálókat és kitöltéseket tartalmazhat egy adott adatigazítás kikényszerítése érdekében. Különleges helyzet, amikor ennek az algoritmusnak a használata előnyös, a nem támogatott üzenetküldési környezetben van. Ilyen környezetekben egy gazdag üzenettulajdonságot egy TNEF Writer kódol soros adatfolyamba. Továbbá a mögöttes TNEF-hez nem tartozó tulajdonságok beágyazhatók az átvitel során. Ezeket a beágyazott tulajdonságokat ezután TNEF-en keresztüli dekódolással teszik elérhetővé, hogy biztosítsák az eredeti üzenet összes tulajdonságának elérhetőségét az ügyfélalkalmazás számára.

A TNEF-ben minden numerikus adattípus kisméretű, és méretük nagyobb, mint egy bájt. Ezeknek a numerikus értékeknek a nem kis végű platformokon történő kezelése megköveteli a megfelelő átalakítások végrehajtását a helyes értékek eléréséhez. A karakterlánc-értékek kiterjesztett Backus-Naur Form (ABNF) formátumban jelennek meg az [RFC5234] specifikációi szerint. Ha a karakterlánc null karakterrel végződik, akkor az is szerepel; például `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="TNEF fájlformátum" >}}

## TNEF attribútumok és feldolgozási szabályok ##

Az adatfolyam a TNEF-ben egy örökölt verziószámmal, egy aláírással, egy primitív kulcsértékkel és egy attribútum kódlappal kezdődik. Ez a kódlap akkor jön létre, amikor a kódoló ANSI-attribútumokat és tulajdonságokat rögzít. Ezt követően az adatfolyam attribútumok sorozata lett, amelyben először az üzenetattribútumok sorakoztak, majd a melléklet attribútumai következtek. Különböző üzenet- és mellékletjellemzőket tartalmaznak olyan speciális attribútumok, mint az attMsgProps, attAttachment és attRecipTable. A TNEF adatfolyamban megjelenő attribútumok tartalmazzák a szerkezetet, az üzenettulajdonságokat és a konverziókat, amelyek szükségesek ahhoz, hogy összekapcsolják őket az üzenettulajdonságokkal. Minden attribútum egy azonosítóból, az attribútum méretéből és adataiból, egy ellenőrző összegből és az alkalmazásának megfelelő szintből áll.

## Protokollokkal és más algoritmusokkal való kapcsolat ##

Azoknak a rendszereknek, amelyeknek gyenge a mechanizmusa a gazdag üzenetformátum natív megjelenítéséhez, TNEF adatalgoritmusra van szükségük a szállításhoz. Az ms-TNEF médiatípust használva az algoritmus kimenete egy csatolmányfájlból (winmail.dat) és az [RFC2045]-ben meghatározott MIME törzsrészből áll. Az egyszerű szöveges üzenettörzs UUENCODE használatával kerül továbbításra az [MSDN-UAF] specifikáció szerint, és ez az üzenettörzs vagy azzal egyenértékű módszer dekódolása a címzett oldalon. Ezenkívül a TNEF különféle internetes protokollok, például SMTP, POP3, IMAP4 és az RFC2045 szabvány szerinti MIME-t integráló protokollok használatával is képes üzenetadatokat továbbítani.

## Alkalmazhatósági nyilatkozat ##

Az egyszerű üzenetátvitelen túlmenően a TNEF eredeti alkalmazását üzenetosztályok használatára és további szolgáltatások támogatására tervezték, amelyek eredetileg nem támogatják a szállítási protokollt. Ezt az alkalmazást tovább finomították a gazdag üzenettulajdonságok és elnevezett tulajdonságok továbbítására, amelyeket a modern üzenetküldő kliensek manapság használnak. Az eredeti megvalósításnak való megfelelés érdekében az eredeti attribútum szintaxisa megmarad, és egy speciális attribútum külön tárolja az új üzenet tulajdonságait.

## Hivatkozások

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [E-mail címek és címjegyzékek az Exchange Serverben](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) adatalgoritmus](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

