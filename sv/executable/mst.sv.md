{
  "date" : "2021-06-30",
  "keywords" :[ "mst-fil", "mst-filformat", "vad är en mst-fil", "fil", "mst-exempel", "mst-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om MST-filformat och API:er som kan skapa och öppna MST-filer.",
  "title" :"MST - Windows Installer Package File",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Vad är en MST fil?
Filerna med tillägget .mst används för att transformera innehållet i ett MSI-paket. De används ofta av systemadministratörer för att tillämpa de anpassade inställningarna på en befintlig MSI-fil. MST-filerna används tillsammans med det ursprungliga MSI-paketet i deras mjukvarudistributionssystem som grupppolicyer. MST-filer används vanligtvis i mjukvaruutveckling och testning för att konfigurera deras under utvecklingsversioner av programvaran.

## MST filformat
En MST- eller Transform-fil används för att samla installationsalternativen för program som använder Microsoft Windows Installer i en fil. Dessa filer används vanligtvis på kommandoraden Installer (MSIEXEC.EXE), eller används i en grupprincip för programvaruinstallation; i en Microsoft Active Directory-domän. MST-filerna kan också användas med inslagna körbara installationsprogram. Ett allmänt fall är att någon vill skicka kommandoradsparametrar till det inkapslade installationsprogrammet. För att göra det behöver du en MST-fil som lägger till egenskapen WRAPPED_ARGUMENTS till egenskapstabellen. Dessa filer kan inte skapas eller redigeras med hjälp av allmänna redigerare. Specifika verktyg finns tillgängliga för detta ändamål.

### Hur använder man MST-filer?
MST-filerna kan genereras med hjälp av olika verktyg och Ocra används vanligtvis för att generera MST-filer. Sedan kan inställningar anpassas efter behov och spara dem på en specifik plats. Därefter kan MST-filerna användas i kombination med MSI-filer. Om du vill testa dessa filer; använd följande syntax på kommandoraden

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMERAR egenskap

Du kan också använda egenskapen **TRANSFORMS** för Windows installationsprogram som faktiskt är en lista över de transformeringar som installationsprogrammet tillämpar när paketet installeras. Installationsprogrammet utför transformationerna i samma ordning som de är listade i TRANSFORM-egenskapen. Transformer kan specificeras med filnamn med filtillägget .mst eller fullständig sökväg. För att ange mer än en transformation, separera varje filnamn eller ett semikolon som i följande exempel.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referenser

* [MST Transformation Files](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS-egenskap](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


