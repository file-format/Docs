{
   "date":"2023-11-09",
   "keywords":[
"Zoo",
"zoo fil",
"zoo komprimeret fil",
"hvordan man åbner en zoo-fil",
"fil",
"zoo filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"ZOO-fil - Hvad er en .zoo-fil, og hvordan åbner man den?",
   "description":"Lær om ZOO-komprimeret filformat og API'er, der kan oprette og åbne ZOO-filer.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo-da",
         "parent":"compression"
}
},
   "lastmod":"2023-11-09"
}

## Hvad er ZOO fil?

En `.zoo`-fil er et arkivformat, der bruges til at komprimere og gemme filer og mapper; ligner andre arkivformater som .zip, .tar og .rar. .zoo-formatet var populært i de tidlige dage af computere, men er blevet mindre almindeligt i de senere år. Det blev oprindeligt udviklet af **Rahul Dhesi** og blev primært brugt på Unix- og DOS-systemer.

En `.zoo`-fil indeholder typisk en eller flere filer og mapper, der er blevet komprimeret og arkiveret til en enkelt fil. Du kan oprette og udpakke `.zoo`-filer ved hjælp af forskellige softwareværktøjer, der understøtter dette format.

ZOO-arkiver har en unik funktion, der giver dem mulighed for at gemme flere versioner af samme fil, forudsat at hver version blev ændret på en anden dato. Dette betyder, at ZOO-brugere kan gemme og få adgang til tidligere gentagelser af filer direkte fra ZOO-arkivet. Denne funktion gør det muligt for brugere at vende tilbage til tidligere version af filen eller sammenligne ældre version med nyere, hvilket giver en bekvem måde at administrere filrevisioner og ændringer over tid.

## Almindelige operationer af ZOO-filer

Her er nogle almindelige handlinger forbundet med `.zoo`-filer:

1.  **Oprettelse af en `.zoo`-fil:** Du kan bruge kommandolinjeværktøj som zoo til at oprette en `.zoo`-fil. For eksempel vil følgende kommando oprette `.zoo`-arkiv fra mappen:
    
`zoo a -c archive.zoo directory/`
    
I denne kommando står a for add, -c angiver komprimering og archive.zoo er navnet på outputarkivet.
    
2.  **Udtrækning af filer fra en `.zoo`-fil:** For at udpakke indholdet af `.zoo`-arkivet kan du bruge kommandoen som denne:
    
`zoo e archive.zoo`
    
Denne kommando vil udpakke filer fra filen `archive.zoo`.
    
3.  **Visning af indholdet af en `.zoo`-fil:** Du kan angive indholdet af `.zoo`-arkiv uden at udpakke dem ved at bruge l-indstillingen:
    
    
`zoo l archive.zoo`

## Hvordan åbner jeg filen ZOO?

Programmer, der åbner ZOO filer inkluderer

- **zoo** (gratis) til (Windows, Linux)

## Referencer
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
