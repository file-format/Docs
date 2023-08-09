{
  "date" : "2021-04-08",
  "keywords" :[ "år fil", "år filformat", "vad är en åra fil", "fil", "år exempel", "år filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Archive File Format",
  "description":"Läs mer om OAR-filformat och API:er som kan skapa och öppna OAR-filer.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Vad är en OAR fil?

En fil med tillägget .oar är en arkivfil som används av OpenSimulator-applikationen som är en 3D-applikationsserver med öppen källkod för att skapa en virtuell miljö tillgänglig för flera användare över nätverket. OAR-filformatet tillhandahåller nödvändig tillgångsdata som krävs för att fullständigt ladda terrängen, objekttexturerna och inventarierna på ett annat system. OpenSimulator har också ett hypergrid som tillval som tillåter användare att besöka andra OpenSimulator-installationer på webben. OAR-filer har Internet MIME-typ application/oar och innehåller en eller flera arkiverade filer.


## OAR filformat

OAR är binära filer som lagras i komprimerat arkivfilformat. Den senaste versionen av OAR-filformatet är [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) som har stora förändringar från sin tidigare [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). Den senaste versionen stöder lagring av flera regioner i en enda OAR och är inte bakåtkompatibel med versioner av OpenSimulator före 0.7.5. En OAR-fil är en gzippad tar-fil (tar.gz) i det ursprungliga unix-tar-formatet (inte USTAR).

## Exempel på OAR-regioner
AOR-filer kan innehålla flera regioner. Strukturen för arkivet är som följer (detta exempel innehåller 4 regioner):

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

Arkivkontrollfilen innehåller ett huvudversionsnummer för att definiera kompatibilitet med framtida formatändringar. Förekomsten av tillgångar i ett OAR-format indikeras av det booleska elementet<assets_included> . Information om de inkluderade regionerna finns i ett manifest som finns i kontrollfilen. Ett exempel på Archive.xml är följande.

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

## Referenser

* [OAR-format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

