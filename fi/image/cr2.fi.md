{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR2-tiedostomuoto - Canon Raw 2 -kuvatiedosto",
  "description":"Opi CR2-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CR2-tiedostoja.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2-fi",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Mikä on CR2-tiedosto?

CR2 (Camera RAW 2) -tiedosto on Canonin digitaalikameroiden luoma RAW-kuvatiedosto. Se tallentaa kameran tallentamat alkuperäiset käsittelemättömät häviöttömät kuvatiedot. Canon on kehittänyt CR2-tiedostomuodon digitaalikameroihinsa, ja se voi tallentaa korkealaatuisia kuvia jopa 14-bittisellä RGB:llä. Tämä tuottaa korkealaatuisia kuvia, joissa on riittävästi tilaa jälkikäsittelylle. Canon on käyttänyt CR2-kuvamuotoa 350D-, 20D- ja 1D-kameramalleissaan. CR2-tiedostot ovat RAW-tiedostoja, ja ne sisältävät lisätietoja metadatasta, kuten kameran tiedot, objektiivitiedot, haarukointitiedot, valkotasapaino ja muut asetukset.

## CR2 tiedostomuoto

CR2-tiedostot tallennetaan kameran muistikortille binääritiedostoina Canonin omistamassa tiedostomuodossa. CR2-tiedostomuoto korvasi alun perin käytetyn CRW-tiedostomuodon ja korvattiin myöhemmin Canon RAW 3 -tiedostomuodolla. CR2-tiedostomuoto perustuu [TIFF](/image/tiff/)-spesifikaatioihin, joissa on 4 kuvatiedostohakemistoa (IFD).

|Offset |Sisältö |Kommentti|
---|---|---|
|0x0000 |Otsikko |sisältää tavujärjestyksen, version ja siirtymän RAW-kuvaan|
|laskettu |IFD#0 |tämä osa sisältää Exif-osan, joka sisältää Makernotes-osion.
Tietoja kuvasta #0|
|laskettu |kuva#0 |pieni versio kuvasta (neljännes alkuperäisen koosta), Jpeg|
|laskettu |IFD#1 |Tietoja kuvasta#1.|
|laskettu |kuva#1 |pieni versio kuvasta, pakattu Jpeg|
|laskettu |IFD#2 |Tietoja kuvasta#2.|
|laskettu |kuva#2 |pieni versio kuvasta, ei pakkaa|
|otsikossa| IFD#3| Tietoja kuvasta #3, täysimittaisesta RAW-kuvasta|
|laskettu |kuva#3 |RAW-kuvadata, häviöttömästi pakattu Jpeg-muodossa (ei RGB-dataa!)|

## CR2-tiedostomuodon etu

Kuvien tallentaminen RAW-muodossa mahdollistaa paljon valokuvan jälkikäsittelyä, kuten valkotasapainon säätämisen. Tämä on paljon vaikeampaa ja aiheuttaa suuren laadun heikkenemisen muilla kuvatiedostomuodoilla, kuten [JPEG](/image/jpeg/).

## Onko CR2 parempi kuin JPEG?

CR2-tiedostot ovat raakatiedostoja ilman tietojen menetystä ja siten laadun heikkenemistä. Toisaalta JPEG on häviöllinen kuvatiedostomuoto, koska se menettää osan tiedoista tiedoston pienentämiseksi. Siten CR2-tiedostot ovat korkealaatuisia ja sopivat paremmin retusointiin ja parannuksiin.

## Viitteet

 * [CR2-tiedostomuoto](http://lclevy.free.fr/cr2/)

