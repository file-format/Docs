{
  "date" : "2023-01-31",
  "keywords" :["kör fil", "vad är en körfil", "fil", "hur man öppnar en körfil", "kör filtillägg","tillägg"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om RUN-filformat och API:er som kan skapa och öppna RUN-filer.",
  "title" :"KÖR filformat - Linux körbar fil",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Vad är en RUN-fil?

Filformatet .run används ofta för att distribuera program eller programinstallationsprogram i Linux-miljön. För att installera programvaran måste du göra filen körbar, vilket kan göras med följande kommando:

```bash
chmod +x file_name.run 
```

Sedan kan du köra filen med följande kommando:

```bash
./file_name.run 
```

Installationsprocessen kan variera beroende på den specifika fil och program du försöker installera.

Filformatet .run är en typ av skalskript som används för att distribuera program- eller programinstallationsprogram i Linux-miljön. Det är ett fristående paket som innehåller allt som behövs för att installera programvaran, inklusive binära filer, bibliotek och konfigurationsfiler.

Det är viktigt att notera att .run-filer också kan innehålla skadlig kod, så det är alltid en bra idé att verifiera källan till filen och skanna den efter virus innan du kör den.

Dessutom kan vissa .run-filer kräva root-privilegier för att köras och installeras, så du kan behöva använda kommandot "sudo" för att köra filen med förhöjda behörigheter:

```bash
sudo ./filename.run
```

## Hur öppnar man filen RUN?

För att öppna en .run-fil måste du göra den körbar, vilket kan göras med kommandot "chmod":

```bash
chmod +x filename.run 
```

När filen är körbar kan du köra den genom att skriva:

```bash
./filename.run
```

Att köra en .run-fil är inte detsamma som att öppna den i en textredigerare. Att köra en .run-fil kommer att köra dess instruktioner, vilket kan vara allt från att installera ett program till att köra ett skript. För att se innehållet i en .run-fil måste du öppna den i en textredigerare, som nano eller vim:

```
nano filename.run
```
eller
```
vim filename.run
```

## Referenser
* [Hur man kör .bin- och .run-filer i Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


