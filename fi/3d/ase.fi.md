{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"tiedosto",
"muoto",
"tiedostotyyppi",
"laajennus",
"mikä on ASE-tiedosto?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi ASE-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda ASE-tiedostoja.",
  "title": "ASE - Autodesk ASCII -näkymän vientitiedosto",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-fie"
}
},
  "lastmod": "2021-01-22"
}

## Mikä on ASE-tiedosto?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE-tiedostomuoto – lisätietoja

ASE-tiedostot ovat ASCII-muotoon tallennettuja tekstitiedostoja, jotka voidaan avata millä tahansa tekstieditorilla. ASE-tiedosto voi sisältää seuraavan tyyppisiä Autodeskin toimittamia tietoja.

### Lähtöasetukset

 * Mesh Definition - Vie kunkin verkon määritelmän, mukaan lukien geometristen objektien kärki- ja pintatiedot. Lisäksi tämän ottaminen käyttöön ottaa käyttöön alla kuvatut Mesh Options -ryhmäruudun kohteet.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * Transform Animation Keys - Sisältää objektien muunnosanimaatiotiedot. Jos kohde on kohdekamera tai kohdevalo, tämä sisältää kohteen animaatiotiedot.
 * Animated Mesh - Vie täydellisen mesh-määrityksen jokaisesta n:stä kehyksestä. Taajuuden määrittelee Controller Output Spinner, joka on kuvattu alla. Jokainen lohko sisältää samat tiedot, jotka on määritetty alla kuvatussa Mesh Options -ryhmäruudussa. Tämän kytkeminen päälle voi johtaa valtavaan tiedostoon, jopa pienissä kohtauksissa.
 * Animoidut kamera-/valoasetukset - Vie kameroiden ja valojen animaatiotiedot, kuten värit, intensiteetit, putoamiset, kartan poikkeamat ja niin edelleen. Tulostaa lohkon n kehyksen välein Controller Output Spinnerin määrittelemällä tavalla.
 * Käänteiset kinemaattiset liitokset - Vie IK-liitosasetukset Hierarkia-haaraan.

### Objektityypit

Tässä olevien kohteiden avulla voit määrittää, minkä objektiluokan haluat sisällyttää tulosteeseen. Voit sisällyttää geometrisia esineitä, muotoja, kameroita, valoja ja apuobjekteja.

 * Geometrinen
 * Muodot
 * Kamerat
 * Valot
 * Auttajat

### Verkkoasetukset

 * Mesh Normals - Vie kasvo- ja kärkinormaalit. Ensin luetellaan kasvojen normaali ja sen jälkeen kasvoja tukevien kolmen kärjen normaalit. Tämän ottaminen käyttöön tuottaa paljon suuremman tiedoston.
 * `Mapping Coordinates` - Vie luettelon kartoituspisteistä ja kasvoista 3ds Max Software Development Kitissä kuvattujen TVert- ja TVFace-rakenteiden mukaisesti. Jos objekti käyttää kasvojen kartoitusta, kasvokarttaluettelo viedään, joka sisältää kunkin pinnan UVW-koordinaatit.
 * Vertex Colors - Vie kärkivärit.

### Ohjaimen lähtö

 * Käytä avaimia - Vie avainarvot. Jos ohjain ei käytä avaimia, käytetään Force Sample -menetelmää. Muunnosohjainten tapauksessa Käytä avaimia -vaihtoehto toimii vain, jos kaikki muunnosohjaimet ovat joko Lineaarisia/TCB- tai Bezier-säätimiä. Jos jokin muunnosraiteista käyttää erityyppistä ohjainta, Force Sample -menetelmää käytetään kaikille muunnosraiteille.
 * Pakota näytteitä - Ottaa näytteitä ohjaimen arvoista Frames per Sample Controller -kohdassa määritetyn taajuuden perusteella.

## Viitteet

 * [Autodesk – vienti ASCII-muotoon](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

