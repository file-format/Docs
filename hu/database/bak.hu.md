{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "kiterjesztés", "fájl", "fájlformátum", "BAK fájltípus", "BAK fájl kiterjesztése", "adatbázisfájl típusa", "adatbázisfájl formátum", "adatbázis fájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a BAK fájlformátumról és az API-król, amelyek BAK-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"BAK fájlformátum - adatbázis biztonsági mentési fájl",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Mi az a BAK fájl?

A .bak kiterjesztésű fájlok általában biztonsági mentési fájlok, amelyeket különböző szoftvereszközök használnak az adatok biztonsági másolatainak tárolására. Az adatbázis szempontjából a Microsoft SQL Server egy BAK-fájlt használ az adatbázis tartalmának tárolására. Az adatbázishoz kapcsolódó összes adat és fájl ebben a fájlformátumban kerül tárolásra, és visszakereshető arra az esetre, ha az adatbázis bármilyen okból megsérülne vagy érvénytelenné válna. A biztonsági mentési fájlok biztonsági okokból más szervereken is tárolhatók és indexelhetők. Számos alkalmazás hozhat létre BAK-fájlokat, például az SQL Server Management Studio, a Transact-SQL és a Windows PowerShell.

## BAK fájl formátum

A BAK-fájlok belső részletei nem ismertek, de széles körben azt feltételezik, hogy a Microsoft Tape Format (MTF) formátumon alapul. Az MTF specifikációk rendelkezésre állnak, és ezekre hivatkozni lehet a fájl szerkezetének megértéséhez. A dokumentum az MTF-tárolásról nyújt részleteket mindenki számára, aki általános ismeretekkel rendelkezik a tároláskezelési műveletekről, a szalagos meghajtókról és a fájlrendszerekről.

### Adatkészletek

Az adatkészlet olyan objektumok gyűjteménye, amelyek adatmentés vagy visszaállítás során adathordozóra (szalagra, optikai lemezre stb.) íródnak. Az adatkészletek több adathordozót tartalmaznak nagy mennyiségű adat esetén.

### Az MTF alapvető elemei

Az MTF-fájl néhány alapvető elemből áll, amelyek az építőköveit alkotják. Ezek az elemek a következők:

#### Leíró blokkok

A leíró blokkok (DBLK) a formátumszabályozásra szolgálnak, és az MTF-fájlok elsődleges alapjait alkotják. Egyetlen MTF-fájl több DBLK-t határoz meg minden egyedi szerepkörhöz. Minden DBLK változó hosszúságú adatblokk, amely a következő négy részre oszlik:

* `Common Block Header` - Rögzített hosszúságú struktúra, amely minden DBLK-ban közös. Ez az egyetlen szükséges blokkfejléc.
* `DBLK típusinformáció` - Rögzített hosszúságú blokk, amely a definiálandó DBLK típusától függ
* "Operációs rendszer adatai" - A DBLK és az operációs rendszerek típusa alapján meghatározott konkrét adatok
* `DBLK információ` - Változó hosszúságú DBLK-specifikus információ, amely nem menthető a rögzített hosszúságú DBLK információval.

 {{< figure src="../bak.png" alt="Microsoft SQL biztonsági mentési fájlformátum" >}}

#### Adatfolyam

Az MTF-fájlban lévő adatfolyamokat az adatok tokozására és igazítására használják. Ez egy adatfolyam fejlécből, majd az adatfolyam-adatokból áll. Egy adatfolyam fejléc csak egyetlen adatfolyam-típust tartalmazhat.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL biztonsági mentési fájlformátum" >}}

#### FileMarks

A fájljelző a logikai elválasztásra és az adathordozón belüli gyors elérésre szolgál. A fájljeleket az eszközillesztő vagy a Soft Filemark Descriptor blokk emulálja, ha a használt eszköz nem biztosít fájljeleket.

## Hivatkozások ##

* [[MS-BCP]: Tömeges másolási formátum](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?MSDN)

