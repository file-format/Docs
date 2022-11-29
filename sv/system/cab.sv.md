{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "tillägg", "fil", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet File",
  "description":"Läs mer om CAB-filformat och API:er som kan skapa och öppna CAB-filer.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är CAB fil? ##

En fil med filtillägget .cab tillhör en Windows-kabinettfil som tillhör kategorin systemfiler. Det är en fil som sparas i arkivfilformatet i versionerna av Microsoft Windows som stöder komprimerade dataalgoritmer, såsom [LZX](/sv/compression/lzx/), Quantum och [ZIP](/sv/compression/zip/ ). Filen kommer till avgörande användning när en användare eller utvecklare vill innehålla och dela data och filer för programvaruinstallation. Funktionerna med förlustfri datakomprimering och den digitala certifieringen som ingår i dessa filer gör den här filen perfekt för att lagra och dela sådana filer. Den stöder olika Microsoft-installatörer som Device Installer, SetUp API och AdvPak.

## Kortfattad bakgrund ##

CAB-fil är en datakomprimeringsfiltyp som utvecklats av Microsoft. Det kallades från början "Diamond", men sedan blev det populärt känt som CAB-fil, förkortning för ordet "Cabinet"

## Teknisk specifikation ##

En CAB-fil kan vanligtvis innehålla upp till maximalt 65535 mappar, som i sin tur kan innehålla maximalt 65536 filer var. CAB-fillagringsmekanismen är tids- och utrymmeseffektiv eftersom den sparar varje mapp som ett komprimerat block istället för att komprimera och lagra varje fil separat. Tomma mappar kan inte lagras i CAB-arkivmappar. CAB-filen utvecklades först av Microsoft och används i olika installationsprogram, som InstallShield med ett lite annorlunda format. CAB-filer är vanligtvis kopplade till självextraherande program. Microsoft CAB-filer är lätta att känna igen på grund av deras unika markör som hjälper till att identifiera formatet. Den unika markören för alla Microsoft CAB-filer är ett fyraordsprefix, MSCF. Genom att se den här koden kan en användare enkelt skilja en Microsoft CAB-fil från andra filer och använda den därefter i kompressorer eller versioner. Filerna kan komprimeras med fler programvaruinstallationsdata, eller nuvarande data kan dekomprimeras med rätt programvara.


## CAB Exempel ##

Följande exempel illustrerar förhållandet mellan filer och mappar i en CAB-filstruktur:

{{< figure src="../cab.png" alt="CAB filformat" >}}

## Referens ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
