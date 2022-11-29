{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS-filformat - Connection Manager Service Profile File",
  "description":"Läs mer om CMS-filer och API:er som kan skapa och öppna CMS-filer.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Vad är en CMS fil?

En CMS-fil är en datafil som innehåller profilinformation som används av Microsoft Windows Connection Manager. Det låter fjärranvändare ansluta till ett nätverk med hjälp av denna profilinformation. Information som lagras i en CMS-fil inkluderar data om användarens operativsystem och behörigheter som används för att upprätta en anslutning mellan en fjärranvändare och nätverket. CMS-administratörer använder Connection Manager Administrator Kit (CMAK) för att generera CMS-filer.

## CMS-filformat - Mer information

CMS-filer är inte vanliga på användardatorer. Eftersom dessa används specifikt för att tillåta fjärranvändare till ett nätverk, hittar du dessa på datorer som används för att ansluta till ett företagsnätverk eller något specifikt specialbyggt kontor. I de flesta fall används den för att ansluta till ett organisatoriskt nätverk som Virtual Private Network (VPN) som endast är dedikerat till ett företag. Som nätverksadministratör kommer du att ställa in åtkomst till ett sådant nätverk med Connection Manager för att tillåta honom att komma åt företagets nätverk från en fjärrplats.

### Vad är insdie CMS?

En CMS-profilfil skapas med Connection Manager och paketeras med andra konfigurationsfiler innan den tillhandahålls till fjärranvändare. Dessa ytterligare filer kan inkludera en CMP och och en INF-fil som är paketerade tillsammans i en [EXE](/sv/körbar/exe/)-fil. Detta kompletta paket tillhandahålls till fjärranvändaren för anslutning till nätverket.

## Referenser

* [Förstå och konfigurera Windows Connection Manager](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

