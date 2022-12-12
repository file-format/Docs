{
  "date" : "2019-11-25",
  "keywords" :[ "jpeg fájl", "jpeg fájl formátum", "mi az a jpeg fájl", "fájl", "jpeg példa", "jpeg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Képfájl formátum",
  "description":"További információ a JPEG fájlformátumról és az API-król, amelyek JPEG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Mi az a JPEG fájl? ##

A JPEG egy olyan képformátum, amelyet veszteséges tömörítési módszerrel mentenek el. A kimeneti kép a tömörítés eredményeként kompromisszumot jelent a tárhely mérete és a képminőség között. A felhasználók beállíthatják a tömörítési szintet a kívánt minőségi szint eléréséhez, ugyanakkor csökkenthetik a tárhely méretét. A képminőséget elhanyagolható mértékben befolyásolja, ha 10:1-es tömörítést alkalmaznak a képen. Minél nagyobb a tömörítési érték, annál nagyobb a képminőség romlása.

## Fájlformátum specifikációi ##

A JPEG képfájlformátumot a Joint Photography Experts Group szabványosította, és innen ered a JPEG név. A formátum a fényképfelvételek internetes tárolása és továbbítása volt. Szinte minden operációs rendszer rendelkezik olyan megjelenítőkkel, amelyek támogatják a JPEG képek megjelenítését, amelyeket gyakran JPG kiterjesztéssel is tárolnak. Még a webböngészők is támogatják a JPEG képek megjelenítését. Mielőtt belemennénk a JPEG fájlformátum specifikációiba, meg kell említeni a JPEG létrehozásához szükséges lépések általános folyamatát.

### JPEG tömörítési lépések ###

**Átalakítás:** A színes képeket a rendszer RGB-ből fénysűrűség/chrominancia képpé alakítja (a szem a fénysűrűségre érzékeny, nem a színárnyalatra, így a színárnyalati rész sok adatot veszíthet, és így erősen tömöríthető.

**Lefelé mintavétel:** A lefelé irányuló mintavétel a színes komponensre, nem pedig a fénysűrűség komponensre történik. Így a kép mérete csökken, mivel az 'y' komponenst nem érintik meg, és nincs észrevehető képminőség romlás.

**Rendezés csoportokba:** Az egyes színösszetevők képpontjai 8×2 pixeles csoportokba vannak rendezve, amelyeket „adategységeknek” neveznek, ha a sorok vagy oszlopok száma nem 8 többszöröse, az alsó sor és a jobb szélső oszlopok duplikálva vannak.

**Diszkrét koszinusz-transzformáció:** Diszkrét koszinusz-transzformációt (DCT) alkalmazunk minden adategységre, hogy létrehozzuk a transzformált komponensek 8×8-as térképét. A DCT bizonyos információvesztéssel jár a számítógépes aritmetika korlátozott pontossága miatt. Ez azt jelenti, hogy a térkép nélkül is csökken a képminőség, de általában kicsi.

**Kvantálás:** Az adategységben lévő 64 transzformált komponens mindegyikét elosztják egy külön számmal, amelyet „kvantálási együtthatónak (QC)” neveznek, majd egész számra kerekítik. Itt az információ helyrehozhatatlanul elveszik, a nagy minőségellenőrzés pedig több veszteséget okoz. Általánosságban elmondható, hogy a legtöbb JPEG eszköz lehetővé teszi a JPEG szabvány által javasolt minőségellenőrzési táblázatok használatát.

**Kódolás:** Az egyes adategységek 64 kvantált transzformált együtthatója (amelyek most egész számok) az RLE és a Huffman kódolás kombinációjával vannak kódolva.

**Fejléc hozzáadása:** Az utolsó lépés hozzáadja a fejlécet és az összes használt JPEG-paramétert, és kiadja az eredményt.

A JPEG dekóder a lépéseket fordított sorrendben használja az eredeti kép létrehozásához a tömörített képből.

### Fájlszerkezet ###

A JPEG kép szegmensek sorozataként jelenik meg, ahol minden szegmens egy markerrel kezdődik. Minden marker 0xFF bájttal kezdődik, majd ezt követi a marker flag, amely a marker típusát jelzi. A marker által követett hasznos teher markertípusonként eltérő. A leggyakoribb JPEG markertípusok az alábbiak:

|Rövid név|Bájtok|Payload|Név|Megjegyzések
---|---|---|---|---|
|SOI|0xFF, 0xD8|nincs|Kép eleje|
|S0F0|0xFF, 0xC0|változó méretű|Keret eleje|
|S0F2|0xFF, 0xC2|változó méretű|Kere indítása|
|DHT|0xFF, 0xC4|változó méret|Huffman-táblázatok meghatározása|
|DQT|0xFF, 0xDB|változó méret|Kvantálási táblázat(ok) meghatározása|
|DRI|0xFF, 0xDD|4 bájt|Újraindítási intervallum meghatározása|
|SOS|0xFF, 0xDA|változó méretű|Szkennelés kezdete|
|RSTn|0xFF, 0xD//n//(/hu//n//#0..7)|nincs|Újraindítás|
|APPn|0xFF, 0xE//n//|változó méret|Alkalmazásfüggő|
|COM|0xFF, 0xFE|változó méretű|Megjegyzés|
|EOI|0xFF, 0xD9|nincs|Kép vége|

Az entrópiakódolt adatokon belül minden 0xFF bájt után a kódoló egy 0x00 bájtot szúr be a következő bájt elé, így nem jelenik meg jelölő ott, ahol egyiket sem szánják, megelőzve ezzel a keretezési hibákat. A dekódolóknak ki kell hagyniuk ezt a 0x00 bájtot. Ezt a [byte-töltés](https://en.wikipedia.org/wiki/Byte_stuffing) technikát (lásd a JPEG specifikáció F.1.2.3. szakaszát) csak az entrópiakódolt adatokra alkalmazzák, a hasznos adatok jelölőire nem. . Megjegyzendő azonban, hogy az entrópiakódolt adatoknak van néhány saját markere; konkrétan a Reset markerek (0xD0 – 0xD7), amelyek az entrópiakódolt adatok független darabjainak elkülönítésére szolgálnak, hogy lehetővé tegyék a párhuzamos dekódolást, és a kódolók szabadon beilleszthetik ezeket az alaphelyzetbe állítási jelzőket rendszeres időközönként (bár nem minden kódoló teszi ezt).

