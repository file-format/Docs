{
  "date" : "2021-04-08",
  "keywords" :[ "Oar-Datei", "Oar-Dateiformat", "Was ist eine Oar-Datei", "Datei", "Oar-Beispiel", "Oar-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator-Archivdateiformat",
  "description":"Erfahren Sie mehr über das OAR-Dateiformat und APIs, die OAR-Dateien erstellen und öffnen können.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Was ist eine OAR-Datei?

Eine Datei mit der Erweiterung .oar ist eine Archivdatei, die von der OpenSimulator-Anwendung verwendet wird, einem Open-Source-3D-Anwendungsserver zum Erstellen einer virtuellen Umgebung, auf die mehrere Benutzer über das Netzwerk zugreifen können. Das OAR-Dateiformat stellt die notwendigen Asset-Daten bereit, die erforderlich sind, um das Gelände, die Objekttexturen und die Inventare vollständig auf ein anderes System zu laden. OpenSimulator hat auch ein optionales Hypergrid, das es Benutzern ermöglicht, andere OpenSimulator-Installationen über das Internet zu besuchen. OAR-Dateien haben den Internet-MIME-Typ application/oar und enthalten eine oder mehrere archivierte Dateien.


## OAR-Dateiformat

OAR sind Binärdateien, die im komprimierten Archivdateiformat gespeichert werden. Die neueste Version des OAR-Dateiformats ist [Version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), die gegenüber der vorherigen [Version 0.8](http://opensimulator.org/wiki/OAR_Format_0 .8). Die neueste Version unterstützt das Speichern mehrerer Regionen in einem einzigen OAR und ist nicht abwärtskompatibel mit Versionen von OpenSimulator vor 0.7.5. Eine OAR-Datei ist eine gezippte Tar-Datei (tar.gz) im ursprünglichen Unix-Tar-Format (nicht USTAR).

## Beispiel für OAR-Regionen
AOR-Dateien können mehrere Regionen enthalten. Die Struktur des Archivs ist wie folgt (dieses Beispiel enthält 4 Regionen):

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
## OAR-Archiv.xml

Die Archivsteuerdatei enthält eine Hauptversionsnummer zum Definieren der Kompatibilität mit zukünftigen Formatänderungen. Das Vorhandensein von Assets in einem OAR-Format wird durch das boolesche Element angezeigt<assets_included> . Informationen zu den eingeschlossenen Regionen sind in einem Manifest enthalten, das in der Steuerdatei vorhanden ist. Ein Beispiel für Archive.xml ist wie folgt.

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

## Verweise

* [OAR-Format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

