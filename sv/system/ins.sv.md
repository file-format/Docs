{
  "date" : "2021-07-16",
  "keywords" :[ "ins fil", "ins filformat", "vad är en ins fil", "fil", "ins exempel", "ins filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om INS-filformat och API:er som kan skapa och öppna INS-filer.",
  "title" :"INS - Internet Settings File",
  "linktitle" : "INS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-16"
}

## Vad är en INS fil?

Filen med tillägget .ins används vanligtvis av Microsoft Windows för att ställa in uppringda och bredbandsanslutningar till Internet. Egentligen innehåller den information om anslutningsinställningar som gör att Windows kan ställa in Internetåtkomst till en ISP. En INS-fil används vanligtvis för att ställa in Internet Explorer (IE) LAN-anslutningsinställningar. IE-anslutningsinställningsfilerna tillhandahålls ibland av Internetleverantörer och systemadministratörer till användarna med en URL till INS-filen.

## INS filformat
Du kan använda Internet Settings-filerna (INS) tillsammans med Internet Explorer Administration Kit 11 (IEAK 11) för att konfigurera din anpassade webbläsare och dess komponenter. Du kan skriva olika versioner av ditt anpassade paket genom att anpassa kopior av INS-filen.

### Möjliga INS-inställningar
De möjliga INS-inställningarna anges i följande tabell:

| Inställning | Beskrivning |
-----|---------|
| URL | Om en automatiskt konfigurerad proxyserver ska användas. |
| Varumärke | Anpassa varumärket och installationsinformationen i ditt webbläsarpaket. |
| Media | Typer av media där ditt anpassade installationspaket är tillgängligt. |
| BrowserVerktygsfält | Anpassa utseendet på IE-verktygsfältet. |
| CabSigning | Digital signaturinformation för dina program. |
| HideCustom | Om den globalt unika identifieraren (GUID) ska döljas för varje anpassad komponent. |
| Anslutningsinställningar | Info om nätverksanslutningsinställningarna som används för att installera ditt anpassade paket. |
| CustomBranding | URL-plats till din fil för varumärkesskåp (.cab). |
| ExtRegInf | Namn på dina installationsinformationsfiler (.inf) och installationsläget för komponenter. |
| FavoriterEx | Lägg till en sökväg till din ikonfil för favoriter, bestäm om favoriter är tillgängliga offline och lägg till webbadresser till varje favoritwebbplats. |
| ISP_Säkerhet | Rotcertifikatet du lägger till i ditt anpassade paket. |
| Proxy | Om en proxyserver ska användas. |
| Säkerhetsimport | Om du ska importera säkerhetsinformation för ditt anpassade paket. |




## Referenser

* [Använda filer med internetinställningar (.INS) med IEAK 11](https://docs.microsoft.com/en-us/internet-explorer/ie11-ieak/using-internet-settings-ins-files)


