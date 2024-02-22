{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg a DLIS fájlformátumot és az API-kat, amelyekkel DLIS fájlokat hozhat létre és nyithat meg.",
  "title" : "DLIS fájl formátum - Well Log Data File",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-hu",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Mi az a DLIS fájl?

A .dlis fájlformátum egy szabványos fájlformátum a kútnapló adatok tárolására és cseréjére az olaj- és gáziparban. A formátumot a Logging Industry Data Standard (LIDS) bizottság fejlesztette ki, és a Digital Log Information Standard” rövidítése. A formátumot úgy tervezték, hogy jól olvasható, írható és könnyen cserélhető módon tárolja a naplóadatokat.

A DLIS fájlok logikai rekordokat tartalmaznak, amelyek leírják a kútnapló adatait és jellemzőit, például a naplóadatok típusát (pl. fajlagos ellenállás, gammasugárzás), a mértékegységeket és az adatok helyét a kútban. A tényleges naplóadatokat külön bináris fájlok tárolják, és a DLIS fájl logikai rekordjai hivatkoznak rájuk.

## Rövid információ a kútnapló adatokról

A kútnapló adatok egy kút különböző mélységein végzett mérések feljegyzései, jellemzően a fúrási folyamat során vagy a kút fúrása után. Ezek a mérések magukban foglalhatják a kútban lévő kőzet és folyadékok különböző fizikai, kémiai és/vagy geofizikai tulajdonságait. Néhány példa a kútnapló adatokra:

- Elektromos ellenállás: a kőzet azon képességének mértéke, hogy ellenálljon az elektromos áram áramlásának
- Gammasugár: a kőzet természetes radioaktivitásának mértéke
- Porozitás: a kőzetben lévő nyitott terek vagy pórusok mennyiségének mértéke
- Sonic: annak az időnek a mértéke, amely alatt a hanghullám áthalad a sziklán
- Sűrűség: a kőzet térfogategységenkénti tömegének mértéke
- Litológia: a kőzettípus vagy képződmény mértéke

A kútnapló adatait különféle célokra használják fel az olaj- és gáziparban, például:

- A szénhidrogén tartalmú képződmények elhelyezkedésének és minőségének meghatározása
- Kút termelési potenciáljának felmérése
- Kút befejezésének, serkentésének tervezése, nyomon követése
- A kút viselkedésének időbeli megfigyelése

## Kapcsolat a PPDM-mel

A PPDM (Professional Petroleum Data Management) egy olaj- és gázipari adatkezelési szabvány, amely közös adatmodellt biztosít a kút- és termelési adatok kezelésére. A PPDM adatmodell szabványos adatobjektumok és kapcsolatok készletét határozza meg, amelyek felhasználhatók a kútnapló adatok, köztük a DLIS adatok rendezésére és kezelésére.

A PPDM adatmodell adatobjektumokat tartalmaz a kút- és termelési adatokhoz, például kutakhoz, kútfejlécekhez, kútnaplókhoz és termelési adatokhoz. Tartalmazza ezen adatobjektumok közötti kapcsolatokat is, például a kút és a hozzá társított kútnaplók közötti kapcsolatot.

A PPDM adatmodell konzisztens, iparági szabványos módot biztosít a naplóadatok, köztük a DLIS adatok rendszerezésére és kezelésére. Lehetővé teszi a különböző szervezetek számára az adatok megosztását és cseréjét egy közös adatmodell használatával, javítva az adatok interoperabilitását és csökkentve az adatintegrációs költségeket.

A PPDM adatmodell és a DLIS adatok együttes használata lehetővé teszi a naplóadatok tárolását és kezelését olyan módon, amely összhangban van az iparági szabványokkal, és könnyen elérhető más rendszerek és alkalmazások számára.


