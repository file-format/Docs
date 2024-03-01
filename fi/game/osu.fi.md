{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Opi OSU-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OSU-tiedostoja.",
  "title" : "OSU-tiedosto - Osu! Komentosarjan tiedostomuoto",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-fi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Mikä on OSU-tiedosto?

OSU-tiedosto on osulle kirjoitettu peliskripti! rytmipeli. Se sisältää tietoa pelissä käytetystä beatmapista, kuten vaikeustasosta, soitettavasta kappaleesta ja osumaobjektien ajoituksista, joihin pelaajan on synkronoitava musiikin kanssa. Sen avulla rytmipelien pelaajat voivat kehittää mukautettuja haasteita ja jakaa niitä peliyhteisön kanssa.

**OSR-tiedostomuodon MIME-tyyppi:** x-osu-beatmap

## OSU tiedostomuoto

OSU-tiedostot tallennetaan pelkkänä tekstinä levylle ja sen rakenne on erittäin selkeästi määritelty osu!:n {{HYPERLINKKI1}}.

### OSU-tiedoston osiot

Tyypillisessä OSU-tiedostossa on seuraavat osat.

|Oso |Kuvaus |Sisältötyyppi|
---|---|---|
|[Yleistä]| Yleistä tietoa beatmapista| avain: arvoparit|
|[Toimittaja]| Tallennetut beatmap-editorin asetukset| avain: arvoparit|
|[Metatiedot] |Beatmapin tunnistamiseen käytetyt tiedot| avain:arvoparit|
|[Vaikeusaste] |Vaikeusasetukset| avain:arvoparit|
|[Tapahtumat]| Beatmap- ja kuvakäsikirjoitusgrafiikkatapahtumat| Pilkuilla erotetut luettelot|
|[Aikapisteet]| Ajoitus ja tarkastuspisteet| Pilkuilla erotetut luettelot|
|[Värit]| Yhdistelmä ja ihonvärit| avain : arvoparit|
|[HitObjects]| Osuma esineisiin| Pilkuilla erotetut luettelot|

## Viitteet

* [OSU! Rytmipeli](https://osu.ppy.sh/home)

* [OSU-tiedostomuoto](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


