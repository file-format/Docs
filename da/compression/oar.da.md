{
  "date": "2021-04-08",
  "keywords": [
"åre fil",
"oar filformat",
"hvad er en årefil",
"fil",
"åre eksempel",
"oar filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR - OpenSimulator Archive File Format",
  "description": "Lær om OAR-filformat og API'er, der kan oprette og åbne OAR-filer.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-dar"
}
},
  "lastmod": "2021-04-15"
}

## Hvad er en OAR fil?

En fil med filtypenavnet .oar er en arkivfil, der bruges af OpenSimulator-applikationen, som er en open source 3D-applikationsserver til at skabe et virtuelt miljø, der er tilgængeligt for flere brugere over netværket. OAR-filformatet giver de nødvendige aktivdata, der kræves for fuldt ud at indlæse terræn, objektteksturer og opgørelser på et andet system. OpenSimulator har også valgfrit hypergrid, der giver brugerne mulighed for at besøge andre OpenSimulator-installationer på tværs af nettet. OAR-filer har internet MIME-type applikation/oar og indeholder en eller flere arkiverede filer.


## OAR filformat

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. En OAR-fil er en gzippet tar-fil (tar.gz) i det originale unix-tar-format (ikke USTAR).

## Eksempel på OAR-regioner
AOR-filer kan indeholde flere områder. Strukturen af arkivet er som følger (dette eksempel indeholder 4 regioner):

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

Arkivkontrolfilen indeholder et hovedversionsnummer til at definere kompatibilitet med fremtidige formatændringer. Tilstedeværelsen af aktiver i et OAR-format er angivet med det booleske element<assets_included> . Oplysninger om de inkluderede regioner er indeholdt i et manifest, der findes i kontrolfilen. Et eksempel på Archive.xml er som følger.

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

## Referencer

 * [OAR-format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

