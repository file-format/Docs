{
  "date": "2023-05-10",
  "keywords": [
"dxb fil",
"hvad er en dxb fil",
"hvad er formatet på dxb-filen",
"hvad indeholder dxb-filen",
"fil",
"dxb filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DXB-filformat - Tegneudveksling binær",
  "description": "Lær om DXB-format og API'er, der kan oprette og åbne DXB-filer.",
  "linktitle": "DXB",
  "menu": {
    "docs": {
      "identifier": "cad-dxb-da",
      "parent": "cad"
}
},
  "lastmod": "2023-05-10"
}

## Hvad er en DXB fil?

DXB står for Drawing Exchange Binary, som er et filformat, der bruges i computer-aided design (CAD) software. DXB-filer indeholder binære data, der repræsenterer 2D vektorgrafik og bruges til at udveksle tegninger mellem forskellige CAD-programmer. De skabes typisk ved at eksportere tegning fra CAD-program i DXB-format og derefter importere det til et andet CAD-program.

DXB-format er mindre almindeligt brugt i dag end andre CAD-filformater som DXF eller DWG. Nogle ældre CAD-programmer kan dog stadig bruge DXB som filformat til eksport eller import af tegninger.

Hvis du har DXB fil og har brug for at se eller redigere den, skal du bruge CAD program, der understøtter DXB format. Nogle eksempler på CAD-programmer, der understøtter DXB, inkluderer AutoCAD, DraftSight og LibreCAD.

## DXB-filformat - flere oplysninger

DXB (Drawing Exchange Binary) er en binær version af DXF (Drawing Exchange Format) filformat, som er et standardformat til udveksling af CAD-tegninger mellem forskellige softwareapplikationer.

DXB-filer indeholder binære data, der repræsenterer 2D vektorgrafik ligesom DXF-filer. DXB-filer er dog mere kompakte og hurtigere at indlæse end DXF-filer, fordi de er gemt i binært format i stedet for almindelig tekst.

For at oprette en DXB-fil kan et CAD-program eksportere tegning i DXB-format, som genererer en binær fil, der kan læses af andre CAD-programmer, der understøtter DXB. For at importere DXB-fil kan et CAD-program på samme måde læse de binære data og konvertere dem til sit eget interne format til redigering.

## Hvad er formatet på DXB fil?

DXB (Drawing Exchange Binary) filformat er et binært filformat, hvilket betyder, at det består af binære data, der kan fortolkes direkte af computeren.

Det binære format, der bruges af DXB, er mere kompakt og hurtigere at indlæse end det tekstbaserede DXF (Drawing Exchange Format) filformat, som også bruges til at udveksle CAD-tegninger mellem forskellige softwareapplikationer.

Strukturen af DXB-filen består af serier af binære poster, som hver indeholder header og data, der repræsenterer enkelt objekt eller entitet i tegningen. Overskriften indeholder oplysninger om typen af objekt eller enhed, der repræsenteres af dataene, såvel som dets størrelse og andre egenskaber.

Dataene i DXB-filen er organiseret hierarkisk med poster på højere niveau, der indeholder referencer til poster på lavere niveau, der repræsenterer underobjekter eller tegningskomponenter. For eksempel kan en post, der repræsenterer polylinjen, indeholde referencer til poster, der repræsenterer individuelle linjesegmenter, der udgør polylinjen.

## Hvad indeholder DXB fil?

DXB (Drawing Exchange Binary) fil indeholder binære data, der repræsenterer 2D vektorgrafik såsom linjer, buer, cirkler, tekst og andre geometriske former, der udgør CAD-tegning.

Når CAD-program eksporterer en tegning til DXB-format, opretter det en binær fil, der indeholder al den information, der er nødvendig for at genskabe tegningen i et andet CAD-program, der understøtter DXB. Dette inkluderer oplysninger om placering, størrelse, farve og stil for hvert objekt i tegningen samt eventuel tekst eller anmærkninger, der kan inkluderes.

Fordi DXB-filer er gemt i binært format, er de typisk mindre i størrelse og hurtigere at indlæse end DXF-filer (Drawing Exchange Format), som er gemt i almindelig tekst. DXB-filer kan dog kun læses af CAD-programmer, der understøtter DXB-formatet, hvorimod DXF-filer kan læses af et bredere udvalg af programmer.

## Referencer
* [DXB File Format](http://web.archive.org/web/20060824054154/https://www.autodesk.com/techpubs/autocad/acadr14/dxf/the_dxb_file_format_al_u05_b.htm)

