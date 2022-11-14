{
  "date" : "2021-06-30",
  "keywords" :[ "mst-bestand", "mst-bestandsindeling", "wat is een mst-bestand", "bestand", "mst-voorbeeld", "mst-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over MST-bestandsindeling en API's die MST-bestanden kunnen maken en openen.",
  "title" :"MST - Windows Installer-pakketbestand",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Wat is een MST-bestand?
De bestanden met de extensie .mst worden gebruikt om de inhoud van een MSI-pakket te transformeren. Ze worden vaak gebruikt door systeembeheerders om de aangepaste instellingen toe te passen op een bestaand MSI-bestand. De MST-bestanden worden samen met het originele MSI-pakket gebruikt in hun softwaredistributiesystemen, zoals groepsbeleid. MST-bestanden worden over het algemeen gebruikt bij het ontwikkelen en testen van software voor het configureren van hun in ontwikkeling zijnde versies van de software.

## MST-bestandsindeling
Een MST- of Transform-bestand wordt gebruikt om de installatieopties voor programma's die Microsoft Windows Installer gebruiken in een bestand te verzamelen. Deze bestanden worden vaak gebruikt op de opdrachtregel van het installatieprogramma (MSIEXEC.EXE), of worden gebruikt in een groepsbeleid voor software-installatie; in een Microsoft Active Directory-domein. De MST-bestanden kunnen ook worden gebruikt met ingepakte uitvoerbare installatieprogramma's. Een algemeen geval is dat iemand opdrachtregelparameters wil doorgeven aan het ingepakte installatieprogramma. Om dat te doen heb je een MST-bestand nodig dat de eigenschap WRAPPED_ARGUMENTS aan de eigenschappentabel toevoegt. Deze bestanden kunnen niet worden gemaakt of bewerkt met algemene editors. Hiervoor zijn specifieke tools beschikbaar.

### Hoe MST-bestanden te gebruiken?
De MST-bestanden kunnen worden gegenereerd met behulp van verschillende tools en Ocra wordt over het algemeen gebruikt om MST-bestanden te genereren. Vervolgens kunnen de instellingen naar behoefte worden aangepast en op een specifieke locatie worden opgeslagen. Daarna kunnen de MST-bestanden worden gebruikt in combinatie met MSI-bestanden. Als u deze bestanden wilt testen; gebruik de volgende syntaxis op de opdrachtregel:

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS eigenschap

U kunt ook de eigenschap **TRANSFORMS** van het Windows-installatieprogramma gebruiken, wat in feite een lijst is van de transformaties die het installatieprogramma toepast bij het installeren van het pakket. Het installatieprogramma voert de transformaties uit in dezelfde volgorde als ze zijn vermeld in de eigenschap TRANSFORM. Transformaties kunnen worden gespecificeerd op bestandsnaam met de extensie .mst of volledig pad. Om meer dan één transformatie op te geven, scheidt u elke bestandsnaam of een puntkomma, zoals in het volgende voorbeeld.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referenties

* [MST-transformatiebestanden](https://www.exemsi.com/documentation/mst-transformation-files/)
* [eigenschap TRANSFORMS](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


