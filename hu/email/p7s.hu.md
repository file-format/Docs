{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S fájl – digitálisan aláírt e-mail üzenet",
  "description":"További információ a P7S fájlformátumról és az API-król, amelyek P7S fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Mi az a P7S fájl?

A P7S fájl egy digitális aláírás, amelyet digitálisan aláírt e-mailben kapnak. Ennek a fájlnak az e-mail mellékleteként való jelenléte igazolja, hogy az e-mail hiteles forrásból érkezett. Ez biztosítja, hogy a feladó számítógépén telepítve legyen egy e-mail aláírási tanúsítvány. Amikor ilyen aláírt e-mailt küldenek a felhasználó számítógépéről, a P7S fájl csatolva van hozzá, amely tartalmazza a feladó nevét. Az aláírt e-maileket támogató e-mail kliensek láthatják a feladó adatait.

## P7S fájlformátum – További információ

Az S/MIME (biztonságos/többcélú internetes levelezőbővítmények) P7S fájlok egyszerű szöveges formátumban tartalmazzák az információkat, amelyek ember által olvashatók. Az e-mail kliensek, például a Microsoft Outlook, az Apple Mail és a Mozilla Thunderbird támogatják az S/MIME e-mailek digitálisan aláírt információinak olvasását. Az e-mail aláírása ellenőrzi a feladó személyazonosságát, és jelzi a címzettnek, hogy az üzenet hiteles. Amikor e-maileket tölt le levelezőprogramokból ([EML](/hu/email/eml/) vagy [MSG](/hu/email/msg/)), ezek a P7S-fájlok az e-mailekhez csatolva lesznek.

A P7S fájl a következő információkat tartalmazza:

* Az e-mail származási forrása
* Elküldés dátuma és időpontja,
* Az átvitel során módosult-e

Ezeket az információkat a nyilvános kulcsú titkosítási szabvány #7 (PKCS7) technológiája segítségével ágyazzák be a titkosított aláírások e-mailhez való digitális csatolásához.

## Referenciák ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

