{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lisätietoja ACCDT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ACCDT-tiedostoja.",
  "title": "ACCDT - Microsoft Access 2007 mallitietokantatiedostomuoto",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-fit"
}
},
  "lastmod": "2020-11-12"
}

## Mikä on ACCDT-tiedosto?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT-tiedostomuoto

ACCDT-mallitiedostot perustuvat Office Open XML -spesifikaatioihin ja kaikki tiedot sisältyvät ZIP-pakettiin. Tietokannan rakenne- ja sisältötiedot sisältyvät [XML](/web/xml/)-tiedostoihin ja tekstitiedostoihin ja linkitetty toisiinsa suhteiden kautta. Voit nimetä ACCDT-tiedoston uudelleen tunnisteeksi [.zip](/compression/zip/) ja purkaa ZIP-arkiston sisällön millä tahansa pakkausohjelmistolla.

### Tiedoston rakenne

ACCDT-tiedostot ovat paketteja, jotka sisältävät kokoelman toisiinsa liittyviä osia. Jokainen **osa** tallentaa tietoja tietokantasovelluksen sisällöstä XML-, teksti- ja binäärimuodoissa, mukaan lukien:

 * Tietokantaobjektit
 * Liittyvät metatiedot
 * Pakkauksen rakenne

#### Paketti

Paketti on {{HYPERLINKKI}}-arkisto, joka sisältää useita osia ja noudattaa kohdassa [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html) määritettyjä Open Packaging -käytäntöjä. ACCDT-tiedostoissa on oltava vähintään yksi Mallin metadaa-osa, jonka tulisi olla suhteen kohteena. Tämä mallin metatiedot ovat ACCDT-tiedoston aloitusosa.

#### Osa

Osa on tavuvirta, johon on liitetty tyyppi siihen tallennetun sisällön luonteen ja tyypin määrittämiseksi. Osien luettelo määrittää kelvolliset osat, kelvolliset sisältötyypit ja pakolliset suhteet paketin kaikkien osien välillä.

#### Suhde

Pakettisuhde - jossa kohde on osa ja lähde on paketti kokonaisuutena.

Part-to-Part Relationship - jossa kohde on osa ja lähde on osa paketissa.

Explicit Relationship - jossa resurssiin viitataan lähdeosan sisällöstä viittaamalla suhdeelementtiin sen ID-attribuutin arvolla.

Implicit Relationship - suhde, joka ei ole eksplisiittinen.

Sisäinen suhde - jossa kohde on osa pakettia.

Ulkoinen suhde - jossa kohde on ulkoinen resurssi, joka ei ole paketissa.

## Viitteet ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

