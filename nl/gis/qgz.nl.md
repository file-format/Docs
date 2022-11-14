{
  "date" : "2021-03-18",
  "keywords" :[ "qgz file", "qgz file format", "wat is een qgz file", "file", "qgz example", "qgz file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS gecomprimeerd project",
  "description":"Meer informatie over het QGZ-bestandsformaat dat slechts een gecomprimeerde QGS is en API's die QGZ-bestanden kunnen maken en openen.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Wat is een QGZ-bestand?

Het **QGZ** bestandsformaat is een gecomprimeerd archief dat een [QGS](https://docs.fileformat.com/gis/qgs/) bestand en een QGD-bestand bevat. Terwijl het QGD-bestand de sqlite-database is van het qgis-project die bestaat uit hulpgegevens voor het project. Als er geen hulpgegevens zijn, blijft het QGD-bestand leeg.

## Details over het QGZ-bestandsformaat

De QGZ werd geïntroduceerd als een nieuwe variant van het **QGIS 3 projectbestandsformaat**. Dit formaat is een gecomprimeerde container voor het QGS xml-bestand. Als gebruikers QGD kiezen dat een optionele indeling is, is de container in dit geval nuttig om de hulpopslagdatabase op te slaan.

In de klassieke modus wordt de hulpdatabase opgeslagen als een bestand met de extensie .qgd naast het xml-bestand. Bij het kiezen van de gecomprimeerde container, wordt het .qgd-bestand in de .qgz opgenomen. Het vergemakkelijkt de gebruikers zonder enig probleem, de gebruikers kunnen het niet verwijderen of vergeten het te kopiëren bij het delen van projectbestanden!


## Referenties

* [QGZ – Een nieuw standaard projectbestandsformaat voor QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Bestandsindelingen van QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

