{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MASTER-fil - ASP.NET Master-sidefilformat",
  "description" : "Lær om MASTER-filformat og API'er til at oprette og åbne MASTER-filer.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master-da",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Hvad er en MASTER fil?

En MASTER-fil er en master-websideskabelonfil, der er oprettet med ASP.NET. Det bruges som udgangspunkt for at oprette flere sider, der har samme layout og indstillinger som MASTER-filen. Skabelonen MASTER-fil indeholder indstillinger for sidehoved, navigationsmenuer, sidefod, skrifttype og stilinformation. Brug af en MASTER-fil hjælper med at oprette flere websider hurtigt.

Du kan åbne en MASTER-fil ved hjælp af Microsoft Visual Studio 2022 og nyere.

## MASTER-filformat - flere oplysninger

En MASTER-fil oprettes og gemmes i HTML-filformat og ligner enhver anden websidefil. Det er opdelt i redigerbare og ikke-redigerbare sektioner. De redigerbare sektioner er dem, der kan ændres for at opfylde brugerens krav. De ikke-redigerbare sektioner er nedtonede, når MASTER-filen åbnes i Microsoft Visual Studio.

Master Pages består af to dele, dvs. selve mastersiden og en eller flere indholdssider.

### MASTER Page

Mastersiden har .master-udvidelsen og er lavet i ASP.NET. Det har et foruddefineret layout, der består af statisk tekst, HTMLtags og serversidekontroller. På almindelige .aspx-sider bruges @ Page-direktivet. I tilfælde af .master filer erstattes dette af @ Master direktiv.

### Indholdssider

En indholdsside repræsenterer indholdet for mastersidens pladsholderkontroller. Disse er .aspx-sider, der faktisk er koden bag mastersiden. Indholdssider bindes ved hjælp af @ Page-direktivet ved at inkludere en MasterPageFile-attribut, der peger på mastersiden, der skal bruges som vist nedenfor.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referencer

* [ASP.NET Master Pages Overview](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))


