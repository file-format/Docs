{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PAMATfails — ASP.NET galvenās lapas faila formāts",
  "description" : "Uzziniet par MASTER faila formātu un API, lai izveidotu un atvērtu MASTER failus.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master-lv",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Kas ir MASTER fails?

MASTER fails ir galvenais tīmekļa lapas veidnes fails, kas izveidots ar ASP.NET. To izmanto kā sākumpunktu, lai izveidotu vairākas lapas, kurām ir tāds pats izkārtojums un iestatījumi kā MASTER failam. Veidnes MASTER failā ir ietverti galvenes, navigācijas izvēlņu, kājenes, fonta un stila informācijas iestatījumi. MASTER faila izmantošana palīdz ātri izveidot vairākas tīmekļa lapas.

MASTER failu var atvērt, izmantojot Microsoft Visual Studio 2022 un jaunākas versijas.

## MASTER faila formāts — vairāk informācijas

MASTER fails tiek izveidots un saglabāts HTML faila formātā un ir līdzīgs jebkuram citam tīmekļa lapas failam. Tas ir sadalīts rediģējamās un nerediģējamās sadaļās. Rediģējamās sadaļas ir tās, kuras var mainīt, lai tās atbilstu lietotāja prasībām. Nerediģējamās sadaļas ir pelēkas, kad MASTER fails tiek atvērts programmā Microsoft Visual Studio.

Galvenās lapas sastāv no divām daļām, ti, pašas galvenās lapas un vienas vai vairākām satura lapām.

### PAMATlapa

Galvenā lapai ir paplašinājums .master, un tā ir izveidota ASP.NET. Tam ir iepriekš definēts izkārtojums, kas sastāv no statiska teksta, HTML tagiem un servera puses vadīklām. Parastajās .aspx lapās tiek izmantota @ Page direktīva. .master failu gadījumā to aizstāj ar @ Master direktīvu.

### Satura lapas

Satura lapa attēlo galveno lapas vietturu vadīklu saturu. Šīs ir .aspx lapas, kas faktiski ir galvenās lapas kods. Satura lapas tiek piesaistītas, izmantojot @ Page direktīvu, iekļaujot MasterPageFile atribūtu, kas norāda uz galveno lapu, kas jāizmanto, kā parādīts tālāk.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Atsauces

* [ASP.NET galveno lapu pārskats](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))


