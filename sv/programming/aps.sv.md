{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ Resource File",
  "description":"Lär dig mer om APS-filformat med APS-exempel och API:er som kan skapa och öppna APS-filer.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Vad är ett APS-filformat?
En APS-fil skapas av Visual C++, ett programutvecklingsprogram från Microsoft. Det sparar den binära representationen av en resurs som ingår i projektet och det tillåter applikationen att ladda resurser snabbare. Du kan enkelt hitta dessa filer med filtillägget .aps. Faktum är att resursredigerarna inte direkt läser resource.h-filerna, det är därför resurskompilatorn kompilerar dem till .aps-filer som konsumeras av resursredigerarna.

## APS filformat
APS-filformatet är bara ett kompileringssteg och lagrar endast symbolisk data. Den icke-symboliska informationen, som att kommentera, kasseras under kompileringsprocessen. Till exempel, när du sparar skriver resursredigeraren över resursskriptfilen och filen resource.h. Eventuella ändringar av själva resurserna förblir inkluderade i resursskriptfilen, men kommentarer kommer alltid att gå förlorade när resursskriptfilen skrivs över.


## Referenser

* [Resursfiler (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


