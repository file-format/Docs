{
  "date" : "2019-10-11",
  "keywords" :[ "dicom fájl", "dicom fájl formátum", "mi az a dicom fájl", "fájl", "dicom példa", "dicom fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM – digitális képalkotási és kommunikációs fájlformátum",
  "description":"További információ a DICOM fájlformátumról és az API-król, amelyek DICOM fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DICOM fájl?

A DICOM a digitális képalkotás és kommunikáció az orvostudományban rövidítése, és az orvosi informatika területére vonatkozik. A DICOM-ot orvosi képalkotó eszközök, például nyomtatók, szerverek, szkennerek stb. integrálására használják különböző gyártóktól, és az egyediség érdekében minden egyes páciens azonosító adatait is tartalmazza. A DICOM fájlok megoszthatók két fél között, ha képesek DICOM formátumú képadatok fogadására. A DICOM kommunikációs része az alkalmazási réteg protokoll, és TCP/IP-t használ az entitások közötti kommunikációhoz. A webszolgáltatások által támogatott verziók 1.0, 1.1, 2 vagy újabb.

## Előzmények ##

A DICOM-ot az American College of Radiology (ACR) és a National Electrical Manufacturers Association (NEMA) közösen fejlesztette ki orvosi képek, például MRI-k, CT-vizsgálatok és ultrahangos képek cseréjére és megtekintésére. Kezdetben nehéz volt dekódolni a gépek által készített képeket. Ezért 1983-ban az ACR és a NEMA együtt alkotott egy csapatot, amely 1985-ben kiadta első szabványát, az ACR/NEMA 300-at. A második verziót 1988-ban adták ki, amely népszerűbb volt a gyártók körében, de hamarosan rájöttek, hogy a második verzió is fejlesztésre szorul. A szabvány 3. verziója 1993-ban jelent meg "DICOM" néven. A 3.0 még mindig a legújabb verzió, de 1993 óta folyamatosan frissítik.

## DICOM fájlformátum ##

A DICOM a fájlformátum-definíció és a hálózati kommunikációs protokoll kombinációja. A DICOM a .DCM kiterjesztést használja. A .DCM két különböző formátumban létezik, azaz 1.x formátumban és 2.x formátumban. A DCM Format 1.x két változatban is elérhető, normál és kiterjesztett változatban. A DICOM webszolgáltatásaihoz HTTP és HTTPS protokollokat használnak.

### Fájlfejléc ###

A fájl fejléce 128 bájtos File Preamble-t és 4 bájtos DICOM előtagot tartalmaz.

**Preambulum # 128 bájt**|**Előtag # 4 bájt „D, I, C, M**

A **Preambulum** a DICOM-fájlban található képek és egyéb adatok elérésére szolgál, amely kompatibilis az általánosan használt képfájl-formátumokkal.

Az **Előtag** a „DICM” karakterláncot tartalmazza nagybetűs karakterként.

### Adatkészlet ###

Minden fájlnak egyetlen adatkészletet kell tartalmaznia, amely az SOP-példányt és az SOP-osztályt képviseli a kapcsolódó IOD-vel. Az adatkészlet a valós világ információinak reprezentációja. Az adatkészlet adatelemeket, az adatelemek pedig az adott objektum attribútumainak értékeit tartalmazzák. Az attribútumok szerkezetét az IOD-k határozzák meg. A DICOM adatobjektum számos attribútumból áll, köztük olyan elemekből, mint a név, azonosító stb., valamint egy speciális attribútum, amely a képpixeladatokat tartalmazza.

### Adatelemek ###

Az adatelem a Címke adatelemből, az érték hosszából és az adatelem értékéből áll. 5 típusú adatelem létezik: 1. típusú kötelező adatelemek, 1C típusú feltételes adatelemek, 2. típusú kötelező adatelemek, 2C típusú feltételes adatelemek és 3. típusú választható adatelemek. Alap Az adatelem-struktúrák három típusa a következő.

**Explicit VR-t tartalmazó adatelem**

|Csoportszám|Elemszám|Értékábrázolás|Fenntartott|Érték hossza|Értékmező
---|---|---|---|---|---|
|2 bájt|2 bájt|2 bájt|2 bájt # 0x00, 0x00|4 bájt|"érték hossza bájt"

**Explicit VR-t tartalmazó adatelem**

|Csoportszám|Elemszám|Értékábrázolás|Értékhossz|Értékmező
---|---|---|---|---|
|2 bájt|2 bájt|2 bájt|2 bájt|"érték hossza bájt"

**Adatelem implicit VR-vel**


|Csoportszám|Elemszám|Érték hossza|Érték mező
---|---|---|---|
|2 bájt|2 bájt|4 bájt|"érték hossza bájt"

1. **Adatelem-címke**: Rendezett egész szám, amely a csoportszámot és az elemszámot jelöli
1. **Értékábrázolás VR**: A VR egy karakterlánc, amely az adatelem VR-jét reprezentálja.
1. **Érték hossza**: az előjel nélküli egész szám az értékmező explicit hosszát jelenti.
1. **Értékmező**: Az adatelemek értékeit írja le.

## Átviteli szintaxis ##

Az átviteli szintaxis olyan kódolási szabályok halmaza, amelyek egyértelműen reprezentálják az absztrakt szintaxisokat. Az átviteli szintaxis segítségével a kommunikáló entitások az általuk támogatott általános kódolási technikákról tárgyalnak.

## SOP ##

Az IOD és a DIMSE egyesülése meghatároz egy SOP osztályt. Az SOP osztály definíciója tartalmazza azokat a szabályokat és szemantikát, amelyek korlátozhatják a DIMSE szolgáltatáscsoport szolgáltatásainak vagy az IOD attribútumainak használatát. Példák a szolgáltatáselemekre: Tárolás, beszerzés, keresés, áthelyezés stb. Az objektumok példái a CT-képek, az MR-képek, de ide tartoznak az ütemezési listák, a nyomtatási sorok stb.

## Szolgáltatások ##

A DICOM különféle szolgáltatásokat nyújt, főként adatközléssel kapcsolatban. Az alábbiakban mindegyiket röviden ismertetjük:


**Tárolás:** A DICOM Store szolgáltatás képeket vagy más objektumokat küld egy képarchiváló és kommunikációs rendszerre (PACS) vagy szerverre.


**Tárolási kötelezettség:** A tárolási kötelezettség szolgáltatás annak megerősítésére szolgál, hogy egy kép tartósan el lett-e tárolva az eszközön bármilyen típusú adathordozón.


**Lekérdezés/lekérés:** Ez a szolgáltatás lehetővé teszi a munkaállomás számára, hogy megkeresse a képek vagy egyéb objektumok listáját, majd lekérje azokat a PACS-ből.


**Modalitási munkalista:** A modalitási munkalista szolgáltatás azoknak a képalkotó eljárásoknak a listáját adja meg, amelyek végrehajtását egy képgyűjtő eszköz ütemezte.


**Nyomtatás:** Ez a szolgáltatás képeket küld a nyomtatóra.

## Portszámok IP-n keresztül ##

A DICOM a következő TCP és UDP portokat használja:

1. 104
1. 2761
1. 2762
1. 11112

## Hivatkozások ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

