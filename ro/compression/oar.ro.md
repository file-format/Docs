{
  "date" : "2021-04-08",
  "keywords" :[ "fișier vâsle", "format fișier vâsle", "ce este un fișier vâsle", "fișier", "exemplu oar", "extensie fișier vâsle", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Archive File Format",
  "description":"Aflați despre formatul de fișier OAR și despre API-urile care pot crea și deschide fișiere OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Ce este un fișier OAR?

Un fișier cu extensia .oar este un fișier de arhivă utilizat de aplicația OpenSimulator, care este un server de aplicații 3D open-source pentru crearea unui mediu virtual accesibil multi-utilizatori prin rețea. Formatul de fișier OAR oferă datele necesare pentru a încărca complet terenul, texturile obiectelor și inventarele pe un alt sistem. OpenSimulator are, de asemenea, hypergrid opțional, care permite utilizatorilor să viziteze alte instalații OpenSimulator pe web. Fișierele OAR au internet MIME tip application/oar și conțin unul sau mai multe fișiere arhivate.


## Format de fișier OAR

OAR sunt fișiere binare care sunt stocate în format de fișier arhivă comprimat. Cea mai recentă versiune a formatului de fișier OAR este [versiunea 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) care are modificări majore față de anterioară [versiunea 0.8](http://opensimulator.org/wiki/OAR_Format_0) .8). Cea mai recentă versiune acceptă stocarea mai multor regiuni într-un singur OAR și nu este compatibilă cu versiunile de OpenSimulator anterioare 0.7.5. Un fișier OAR este un fișier tar cu gzip (tar.gz) în formatul original unix tar (nu USTAR).

## Exemplu de regiuni OAR
Fișierele AOR pot conține mai multe regiuni. Structura arhivei este următoarea (acest exemplu conține 4 regiuni):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Fișierul de control al arhivei conține un număr major de versiune pentru a defini compatibilitatea cu viitoarele modificări de format. Prezența activelor într-un format OAR este indicată de elementul boolean<assets_included> . Informațiile despre regiunile incluse sunt conținute într-un manifest care este prezent în fișierul de control. Un exemplu de Archive.xml este următorul.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referințe

* [Format OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

