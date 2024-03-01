{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS - Lidar LASer -tiedostomuoto",
  "description": "Opi LAS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LAS-tiedostoja.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-fis"
}
},
  "lastmod": "2023-07-18"
}

## Mikä on LAS-tiedosto?

LAS (Lidar LASer) -tiedostomuoto on binääritiedostomuoto, joka on erityisesti suunniteltu lidar-pistepilvitietojen tallentamiseen. Sen on kehittänyt ja ylläpitänyt American Society for Photogrammetry and Remote Sensing (ASPRS) standardoituna muotona lidar-tiedonvaihtoon ja yhteentoimivuuteen.

LAS-tiedostot tallentavat yksityiskohtaisia tietoja yksittäisistä lidar-pisteistä, mukaan lukien niiden 3D-koordinaatit (x, y ja z), intensiteettiarvot, luokituskoodit ja lisäattribuutit. Formaatti tukee sekä erillistä paluuta että täyttä aaltomuoto-lidar-dataa, mikä mahdollistaa useiden palautusten tallentamisen laserpulssia kohti.

## LAS tiedostomuoto

LAS-tiedoston rakenne koostuu kolmesta pääosasta: tiedoston otsikosta, muuttuvapituisista tietueista (VLR) ja pistetietotietueista.

1. Tiedoston otsikko: Tiedoston otsikko sisältää tärkeitä tietoja LAS-tiedostosta, kuten tietomuodon version, pisteen tietomuodon, pisteiden lukumäärän, rajauslaatikon koordinaatit, koordinaattiviittausjärjestelmän (CRS) ja muita metatietoja. Se tarjoaa yhteenvedon tiedoston sisältämistä lidar-tiedoista.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Pistetietotietueet: Pistetietotietueet tallentavat todelliset lidar-mittaukset. Jokainen pistetietotietue edustaa yhtä lidar-pistettä ja sisältää attribuutteja, kuten x-, y- ja z-koordinaatteja, intensiteettiarvoja, luokituskoodeja (esim. maaperä, kasvillisuus, rakennukset) ja muita käyttäjän määrittämiä attribuutteja. Pistetietueet voivat myös tallentaa aikaleimoja, palautuslaskuja ja skannauskulmia.

LAS-tiedostot tukevat erilaisia tietomuotoja (0-10) erityyppisten lidar-tietojen ja tarvittavien tietojen tason mukauttamiseksi. Esimerkiksi muoto 0 edustaa yksinkertaista pistemuotoa perustiedoilla, kun taas muodot 1-3 tarjoavat kattavampia tietoja, mukaan lukien aaltomuototiedot jokaisesta palautuksesta.

Lidar-ohjelmistot ja -käsittelytyökalut tukevat laajasti LAS-tiedostoja, joten ne ovat vakiomuoto lidar-tiedonvaihdossa ja -analyysissä. Lisäksi LAS-tiedostoja voidaan pakata häviöttömällä pakkaustekniikalla tiedoston koon pienentämiseksi säilyttäen samalla alkuperäisen tiedon tarkkuuden. LAS-tiedostojen pakattua versiota kutsutaan usein nimellä LAZ, joka tarjoaa tehokkaat tallennus- ja tiedonsiirtoominaisuudet.

## Viitteet

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
