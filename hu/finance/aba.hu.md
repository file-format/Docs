{
  "date" : "2019-10-11",
  "keywords" :[ "aba fájl", "aba fájlformátum", "mi az aba fájl", "fájl", "aba példa", "aba fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText fájlformátum",
  "description":"További információ az ABA-fájlformátumról és az API-król, amelyek ABA-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Mi az ABA fájl?

Az .aba kiterjesztésű fájl az Australian Bankers Association (ABA) vagy a [Cemtext](https://www.cemtexaba.com/) fájlformátum, amelyet a bankok kötegelt tranzakciókhoz használnak. A legtöbb bank pénzügyi nyilvántartás vezetésére használja. A Direct Entry fájlként is ismert ABA fájlformátumot a legtöbb ausztrál bank elfogadta alapértelmezett formátumként a kötegelt tranzakciókhoz. Még mindig nem ismeri fel szabványos formátumként, annak ellenére, hogy a Bank of Queensland, a NAB és a Westpac használja. Az ABA-fájlok bármely szövegszerkesztővel megnyithatók, például a Notepad++-val.


## ABA fájlformátum

Az ABA-fájl az ASCII formátumot használja az adatok banki rendszerbe történő továbbításához vagy betöltéséhez. A formátumot egyszerűvé tették, hogy megkönnyítsék a vállalatok saját pénzügyi rendszerébe történő integrálását a tranzakciók kötegeinek feldolgozásához. Például egy bérszámfejtő rendszerben egy köteg tranzakciót lehet feltölteni, hogy egy találattal feldolgozzák. Az ABA fájlformátum specifikációi teljes átiratként elérhetők a [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) webhelyen, és fejlesztői hivatkozásként hivatkozhatnak rájuk. .

Egy ABA-fájl több sorból áll, amelyek mindegyike "rekord" néven ismert. Három fő rekord van egy ABA-fájlban:

* Leíró feljegyzés
* Részletek Record
* File Total Record

### Leíró rekord

A „Leíró rekord” olyan információkat tartalmaz, mint a tekercs sorszáma, a felhasználó pénzügyi intézményének neve, a szolgáltató fájl felhasználási neve és egyéb információk.

### Részletfelvétel

A „Részletrekord” típus olyan információkat tartalmaz, mint a bank/állam/fiókszám, a jóváírandó/terhelendő számlaszám, az indikátor, a tranzakció kódja, az összeg és egyéb információk.

### Fájl teljes rekordja

A „Fájl teljes rekordja” típus tartalmazza a 7. rekordtípust, a BSB formátumkitöltőt, a fájl (felhasználói) nettó teljes összegét, a fájl (felhasználói) jóváírás teljes összegét, a fájl (felhasználói) terhelési teljes összegét és egyéb információkat.

### Tranzakciós kódok

Az érvényes tranzakciós kódok listája a következő. A legtöbb esetben az "53 - Pay" kódot használják az ABA-fájlokban. Ezek a tranzakciós kódok a terhelésekre, a jóváírásokra és a forrásadókra vonatkoznak.

|Kód|Tranzakció leírása|
---|---|
|13|Külsőleg kezdeményezett terhelési tételek|
|50|Külsőleg kezdeményezett jóváírási tételek, kivéve a Tranzakciós kódokat viselők|
|51|Ausztrál kormánybiztonsági érdek|
|52|Családi pótlék|
|53|Fizetés|
|54|Nyugdíj|
|55|Kiosztás|
|56|Osztalék|
|57|Kötvény/kötvénykamat|

## ABA fájl példa

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Hivatkozások

* [Cemtext ABA](https://www.cemtexaba.com/)

