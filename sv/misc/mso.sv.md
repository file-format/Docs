{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office Macro Reference File",
  "description":"Läs mer om MSO-filer och API:er som kan skapa och öppna MSO-filer.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Vad är MSO fil?

En MSO-fil är ett databehållarfilformat som skapas när ett HTML-meddelande skickas med Microsoft Outlook. Detta händer mest med Microsoft Office 2000-program. I de flesta fall bifogas e-postmeddelandet med namnet **Oledata.mso**-filen. E-postmottagaren, när den öppnar ett sådant e-postmeddelande, kan visa filen korrekt även om de inte har samma programvara installerad. MSO-filer hänvisar till [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO filformat

MSO-filer sparas i Microsoft Compound Document File Format (MCDF) som också är känt som Object Linking and Embedding (OLE) eller Component Object Model (COM) strukturerad lagringssammansatt filimplementering binärt filformat.

### MSO-filformatstruktur

Den interna filformatstrukturen för MSO-filformat är väldefinierad i [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) i MCDF-dokumentationen. Filallokeringstabellen (FAT) hanterar sektorallokeringen och sektorkedjorna. Den innehåller en matris med 32-bitars sektornummer. Varje index i arrayen representerar ett sektornummer medan dess värde representerar nästa sektor i kedjan eller ett speciellt värde.

## Referenser

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

