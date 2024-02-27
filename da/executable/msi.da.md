{
  "date": "2021-06-30",
  "keywords": [
"msi fil",
"MSI filformat",
"hvad er en msi-fil",
"fil",
"msi eksempel",
"msi filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MSI-filformat og API'er, der kan oprette og åbne MSI-filer.",
  "title": "MSI - Windows Installer Package File",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-dai"
}
},
  "lastmod": "2021-06-30"
}

## Hvad er en MSI fil?
En MSI-fil, der bruges til at installere og starte Windows-programmer; en komplet pakke til Microsoft Windows, der indeholder installationsoplysninger for et typisk softwareprogram, inklusive vigtige filer, der skal installeres, og oplysninger om installationsplaceringen. MSI-filerne kan også indeholde pakken til softwareopdateringer. MSI-filer ligner [EXE](/executable/exe/), men nogle gange inkluderer EXE muligvis ikke installationsoplysningerne, og softwareprogrammet kan køre direkte, når EXE-filen udføres.

## MSI filformat
Windows Installer er faktisk en API (Application Programming Interface) og softwarekomponent i Microsoft Windows, der bruges til installation, fjernelse og vedligeholdelse af et softwareprogram. Installationsoplysningerne og de valgfrie filer er pakket som installationspakker og løst relationelle databaser struktureret som COM Structured Storages; velkendt som **MSI-filer**, med filtypenavnet .msi. Pakkerne med filtypenavnet **.mst** indeholder **Transformation Scripts** af Windows Installer, filer med filtypenavnet **.msm** indeholder **Merge Modules** og filtypenavnet **.pcp** bruges til **Patch Creation Properties**. Windows Installer bliver mere avanceret efter at have foretaget væsentlige ændringer fra dens tidligere versioner, Setup API. En GUI-ramme og automatisk generering af afinstallationssekvensen er de nye funktioner i Windows Installer. Det er nu blevet betragtet som et alternativ til selvstændige eksekverbare installationsrammer.

### Logisk struktur af MSI-pakker
En pakke angiver installationen af et eller flere komplette produkter og er generelt identificeret med en **GUID**. Et produkt er opbygget af en eller flere komponenter og grupperet i forskellige funktioner. Windows Installer håndterer ikke afhængigheder mellem forskellige produkter samtidigt. Den logiske struktur af pakker består af følgende elementer:

- **Produkter**: Et enkelt, installeret, fungerende program eller sæt af flere programmer kombineret sammen er et produkt. Et produkt er identificeret med en unik GUID.
- **Funktioner**: Kan indeholde et vilkårligt antal komponenter og andre underfunktioner. Mindre pakker kan bestå af en enkelt funktion.
- **Komponenter**: Komponent behandles af Windows Installer som en enhed; kan indeholde programfiler, mapper, registreringsdatabasenøgler, COM-komponenter og genveje.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## Referencer 

* [Windows Installer - af Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



