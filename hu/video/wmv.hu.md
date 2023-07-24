{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV fájlformátum",
  "description":"További információ a WMV fájlformátumról és az API-król, amelyek WMV fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Mi az a WMV fájl?

Az Advanced Systems Format (ASF) egy digitális multimédiás tároló, amelyet elsősorban médiafolyamok tárolására és továbbítására terveztek. A Microsoft Windows Media Video (WMV) a tömörített videó formátum, a Microsoft Windows Media Audio (WMA) pedig a tömörített hangformátum a Microsoft által kifejlesztett ASF tárolóban található további metaadatokkal együtt. Miután a WMV vagy WMA fájlokat Windows Media Video és Windows Media Audio kodekekkel kódolták, akkor .asf kiterjesztéssel jelennek meg. A WMV tömöríti a nagy fájlokat a jobb átviteli sebesség érdekében a hálózaton keresztül, miközben megőrzi a videó minőségét. A WMV-t kifejezetten az összes Windows-eszközön való futtatásra tervezték. A Society of Motion Picture and Television Engineers (SMPTE) szabványosítása után a WMV nyílt szabványú formátumnak számít.

## Történelem ##

A Microsoft szabadalmaztatott kodekek segítségével 1999-ben új tömörített videó formátumot fejlesztettek ki WMV7 néven, amely az MPEG-4 2. részén alapult. További két verzió, a WMV8 és a 9. A Microsoft benyújtott egy 9^^th^^ verziót. 2003-ban a WMV-t az SMPTE-nek szabványosítás céljából, amelyet végül 2006-ban SMPTE 421M néven szabványosítottak, más néven VC-1. A WMV mögött az volt az ötlet, hogy olyan médiaformátumot fejlesszenek ki, amelyet a Microsoft által támogatott összes hardver és szoftver támogat. Ezen túlmenően egy másik fő cél az volt, hogy optimális forgatókönyv szerint videofolyamokat továbbítsanak az interneten. Az SMPTE szabványosítása után a WMV a Blu-ray lemezek videoformátuma is lett.

## A fájlformátum specifikációi

### Tároló

A WMV általában ASF tárolóba van csomagolva, de emellett a Matroska vagy az AVI konténer is támogatja .mkv és .avi kiterjesztéssel.

### Windows Media Video 9

Bár a Windows Media Video 9 sorozatban különféle audio- és videokodekek állnak rendelkezésre digitális média létrehozására és lejátszására, a WMV-9 kodek a legújabb és legjobb videokodek, mivel nagyon alacsony, azaz 160x-os bitsebességgel képes az optimális tömörítést elérni. 120 10 Kb/s-tól 1920 x 1080-ig 4-8 Mb/s-ig különféle HD videókhoz.

### A kodek felépítése

A WMV-9 8 bites 4:2:0 belső színformátummal rendelkezik. Az összes többi népszerű MPEG-1 és H.261 videotömörítési szabványhoz hasonlóan a WMV-9 is blokkalapú mozgáskompenzációt és térbeli transzformációs sémát használ. Általánosságban elmondható, hogy ezek a szabványok blokkonkénti mozgáskompenzációt hajtanak végre az előző rekonstruált keretből egy mozgásvektornak (MV) nevezett 2-D mennyiség segítségével a térbeli elmozdulás jelzésére. Az aktuális blokk a mozgásvektor által az aktuális pozícióból eltolt, azonos méretű előző rekonstruált képkockából származó értékek előrejelzésének segítségével jön létre. Végül a maradék hiba a mozgáskompenzált előrejelzett mondat és a tényleges blokk különbségeként kerül kiszámításra. Ezt a maradék hibát lineáris energiatömörítő transzformációval transzformálják, majd kvantálják és entrópiakódolják.

A kvantált transzformációs együtthatók entrópia dekódolása, dekvantálása és inverz transzformációja történik, hogy a dekóder oldalon a maradék hiba közelítését állítsák elő, amelyet azután hozzáadnak a mozgáskompenzált előrejelzéshez a rekonstrukció létrehozásához. A kodek magas szintű leírása a következő képen látható.

A rész további része a WMV-9 új fejlesztéseit tárgyalja, amelyek megkülönböztetik a többi videókódolási megoldástól, például az MPEG szabványoktól. A WMV-9-nek intra (I), előrejelzett (P) és kétirányú előrejelzett (B) keretei vannak. A belső keretek azok, amelyek egymástól függetlenül vannak kódolva, és nem függenek más keretektől. Az előrejelzett képkockák olyan képkockák, amelyek egy múltbeli képkockától függenek. Egy előrejelzett keret dekódolása csak azután történhet meg, hogy a legutóbbi (I) kerettől kezdve az aktuális keret előtti összes referenciakeret dekódolásra került. A B keretek olyan keretek, amelyeknek két hivatkozása van – az egyik az időbeli múltban és a másik az időbeli jövőben. A B kereteket a hivatkozások után továbbítják, ami azt jelenti, hogy a B kereteket nem megfelelően küldik el, hogy biztosítsák, hogy hivatkozásaik elérhetőek legyenek a dekódolás időpontjában. A WMV-9 B képkockái nem referenciaként szolgálnak a következő képkockákhoz. Ez a B képkockákat a dekódoló hurkon kívülre helyezi, lehetővé téve a parancsikonok használatát a B képkockák dekódolása során sodródás vagy hosszú távú vizuális műtermékek nélkül. Az I, P és B keretek fenti meghatározása mind a progresszív, mind a váltottsoros sorozatokra érvényes.

A videokodekek teljesítményét a sebesség-torzítási (RD) diagramjukhoz hasonlítják. Ez egy 2-D görbe, amely a tömörítés által előidézett torzítást mutatja egy bizonyos bitsebesség mellett.

A WMV-9 az alábbiakban felsorolt különféle technikák bevezetésével orvosolta ezt a problémát:

1. Adaptív blokkméret transzformáció

2. Korlátozott pontosságú transzformációs készlet

3. Mozgáskompenzáció

4. Kvantálás és dekvantálás

5. Fejlett entrópia kódolás

6. Hurokszűrés

7. Fejlett B keretkódolás

8. Váltósoros kódolás

9. Átfedési simítás

10. Alacsony teljesítményű szerszámok

11. Fading kompenzáció

## Referenciák ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


