{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Muuta tiedostomuotoa",
  "description":"Opi OSC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OSC-tiedostoja.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-fi",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Mikä on OSC-tiedosto?

OSC-tiedosto on Change File Format, joka sisältää muokatut katukarttatiedot olemassa olevalle .osm-katukartalle. Se sisältää tietoja muutoksista, joita {{HYPERLINKKI}} tapahtuu. OSC-tiedostossa voi olla kolme mahdollista OSM-tietojen muokkaustoimintoa eli lisää, muokkaa tai poista. Näitä muutostiedostoja käytetään yleisesti tietojen viemiseen OSM-editorista ja tuomiseen toiseen editoriin.

Voit avata OSC-tiedostoja Merkaartar- ja osmchange-ohjelmistolla.

## OSC-tiedostomuoto

OSC-tiedostot tallennetaan yleensä JOSM-tiedostomuodossa, jossa muutokset esitetään tunnisteilla. Se alkaa osmChange-tunnisteella, joka osoittaa tiedoston alun. Alitagit määrittävät, onko kyseessä lisäys-, muokkaus- tai poistotoiminto, joka suoritetaan vastaavalle OSM-tiedoston solmulle. Solmun sisältö todella sisältää osm-tunnisteen sisällön.

### Esimerkki OSC-tiedostomuodosta

Seuraavassa on esimerkki solmun muokkaustoiminnosta. Jokaisella elementillä on oltava muutossarjan tunnus ja versionumero.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Viitteet

* [JOSM-tiedostomuoto](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


