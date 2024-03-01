{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EDB-tiedostomuoto - Exchange Mail -tietokantatiedosto",
  "description": "Opi EDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EDB-tiedostoja.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-fib"
}
},
  "lastmod": "2020-09-16"
}

## Mikä on EDB-tiedosto?

Tiedosto, jonka tunniste on .edb, on Microsoft Exchange Serverin luoma postilaatikkotietokanta sähköpostiin liittyvien tietojen tallentamiseen. EDB, Exchange Database, tallentaa viestit, jotka ovat käynnissä olevia ja ei-SMTP:tä. EDB tunnetaan myös Extensible Storage Engine (ESE) -tietokantatiedostoina ja tallentaa tiedostoja b-tree-rakenteen avulla. Tallennustiedostoina EDB-tiedostot voidaan muuntaa muihin postin tallennustiedostomuotoihin, kuten [PST](/email/pst/) ja [OST](/email/ost/).

## EDB-tiedostomuoto

Ei ole saatavilla virallisia/avoin EDB-tiedostomuotomäärityksiä, joihin voisi viitata. Tiedostomuodon käänteisessä suunnittelussa on edistytty jonkin verran, mikä on johtanut osittaiseen määrittelyjen dekoodaukseen. Näiden mukaan EDB-tiedosto koostuu:
 * Tiedoston otsikko - Sisältää tietokantatiedoston otsikkotiedot
 * Kiinteän kokoiset sivut - Sisältää tietokannan, joka sisältää taulukoita ja indeksejä

### Tietokantatiedoston otsikko
Tietokantatiedoston otsikko sijaitsee ensimmäisellä tietokantasivulla ja on vähintään 668 tavua. Tiedoston otsikko sisältää File Format Version ja File Type muiden kenttien lisäksi.

#### Tiedostotyypit
|Tyyppi|Kuvaus
---|---|
|0| Tietokanta|
|1| Suoratoisto|

`Huom:` Näiden tyyppien tunnisteita ei tunneta.

#### Tiedostomuodon versio
Alkuperäinen EDB-muoto alkoi huhtikuussa 1997, ja se kehittyi sen jälkeen muutoksiin.

|Revsion Date|Version|Revision|description
---|---|---|---|
|huhtikuu 1997| 0x00000620|0x00000000| Alkuperäinen käyttöjärjestelmän beta-muoto.|
|Toukokuu 1997 |0x00000620|0x00000001| Lisää luetteloon sarakkeita ehdollista indeksointia varten ja OLD.|
|Kesäkuu 1997|0x00000620|0x00000002|Lisää fLocalizedText-lippu IDB:hen.|
|Lokakuu 1997|0x00000620|0x00000003|Lisää SPLIT_BUFFER avaruuspuun juurisivuille.|
|Tammikuu 1998|0x00000620|0x00000002|Palauta versio, jotta ESE97 pysyy eteenpäin yhteensopivana.|
||0x00000620|0x00000003|Lisää luetteloon uusia merkittyjä sarakkeita (CallbackData ja CallbackDependencies).|
|Toukokuu 1998|0x00000620|0x00000004|Super Long Value (SLV) -tuki: signSLV, fSLVEsillään tietokantaotsikossa.|
|Toukokuu 1998|0x00000620|0x00000005|Uusi SLV-avaruuspuu.|
|Lokakuu 1998|0x00000620|0x00000006|SLV-avaruuskartta.|
|Joulukuu 1998|0x00000620|0x00000007|4-tavuinen IDXSEG.|
|Tammikuu 1999|0x00000620|0x00000008|Uusi mallin sarakemuoto.|
|Kesäkuu 1999|0x00000620|0x00000009|Lajiteltu mallisarakkeet. Käytetään Windows XP SP3|:ssa
||0x00000620|0x0000000b|Sisältää sivun otsikon ja ECC-tarkistussummaUsed in Exchange|
||0x00000620|0x0000000c|Käytetään Windows Vistassa (SP0)|
||0x00000620|0x00000011|Tuki 2 KiB:n, 16 KiB:n ja 32 KiB:n sivuille.Laajennettu sivuotsikko, jossa on ylimääräisiä ECC-tarkistussummia.Sarakkeiden pakkaus.Avaruusvinkit.Käytetään Windows 7:ssä (SP0)|
|Toukokuu 1999|0x00000623|0x00000000|Uusi Space Manager.|

### Tietokantatiedostot

EDB-tietokantatiedosto sisältää skeeman kaikille tietokannan taulukoille. Lisäksi se sisältää myös tietueet kaikista tietokantataulukoista ja indeksit taulukoille. Sen sijainti määritetään seuraavien tunnisteiden avulla.

* JetCreateDatabase

* JetCreateDatabase2

* JetAttachDatabase

* JetAttachDatabase2


Näiden perusteella tietokannan tilaa voidaan arvioida seuraavasti.

|Arvo|Identifier|Description
---|---|---|
|1|JET_dbstateJustCreated|Tietokanta luotiin juuri.|
|2|JET_dbstateDirtyShutdown|Tietokanta vaatii kovaa tai pehmeää palautusta, jotta se tulee käyttökelpoiseksi tai siirrettäväksi. Tietokantoja ei pidä yrittää siirtää tässä tilassa.|
|3|JET_dbstateCleanShutdown|Tietokanta on puhtaassa tilassa. Tietokanta voidaan liittää ilman lokitiedostoja.|
|4|JET_dbstateBeingConverted|Tietokantaa päivitetään.|
|5|JET_dbstateForceDetachInternal|Tämä arvo on otettu käyttöön WindowsXP:ssä|
 
## Viitteet
 * [Extensible Storage Engine (ESE) tietokantatiedoston (EDB) tekniset tiedot](https://github.com/libyal/libesedb/tree/main/documentation)

