{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX-filformat",
  "description":"Lär dig mer om TEX-filformat och API:er som kan skapa och öppna TEX-filer.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en TEX-fil? ##

**TeX** är ett språk som består av programmering såväl som uppmärkningsfunktioner, som används för att sätta in dokument. Donald Knuth från Stanford University, är skaparen av detta fyndiga sättsystem. Över hela världen är TeX det ultimata valet av författare och förlag för att producera tekniska dokument av hög kvalitet. TeX utför ett enastående jobb med att formatera komplexa matematiska uttryck. Tillsammans med en högkvalitativ fotosättare konkurrerar TeX med de resultat som genereras av de bästa traditionella sättningssystemen. Anses därför som de mest eleganta digitala typografiska systemen.

TeX-indatafiler är baserade på ASCII-kod, vilket möjliggör manuskriptdelning mellan skribenter, förlagschefer och kritiker. Ett brett utbud av datormiljöer, nästan alla moderna plattformar och många äldre plattformar stödjer TeX. Dessutom är TeX en gratis programvara, tillgänglig för ett brett spektrum av konsumenter. Många UNIX-installationer använder både UNIX troff och TeX som formateringssystem för olika ändamål. Andra typsättningsuppgifter utförs oerhört i form av LaTeX, ConTeXt och andra makropaket.

## Kortfattad bakgrund ##

TeX designades och skrevs av Donald Knuth 1978. Guy Steele från Massachusetts Institute of Technology reviderade input/output av TeX för att få det att köras under det inkompatibla operativsystemet som Timesharing System (ITS). Den första versionen av TeX utvecklades under Stanfords WAITS operativsystem i programmeringsspråket (SAIL) och testades för att köras på en PDP-10. Knuth introducerade idén om läskunnig programmering för avancerade versioner. Läskunnig programmering är ett sätt att generera kompilerbar källkod och typuppsättning (i TeX) för korslänkad dokumentation med hjälp av originalfilen. Språket som används för att utveckla dessa avancerade versioner av TeX kallas WEB, en blandning av DEC PDP-10 Pascal-program för att säkerställa portabilitet.

En reviderad ny version av TeX publicerades 1982 och kallades TeX82. Den största förändringen är ersättningen av den ursprungliga avstavningsalgoritmen med den nyskrivna algoritmen av Frank Liang. För att säkerställa portabilitet över olika plattformar, istället för att använda flyttal, använder TeX82 aritmetik med fast punkt tillsammans med ett riktigt, turing-komplett programmeringsspråk. 1989 släpptes en ny version av TeX och Metafont. Så version 3.0 av TeX underlättar 8-bitars ingångar, vilket tillåter 256 olika tecken i texten. Efter version 3 anges uppdateringar genom att lägga till en extra siffra i slutet av decimalen, t.ex. aktuell version av TeX anges som 3.14159265. Denna version uppdaterades senast 2014-12-1.

## TeX-ingång ##

En indatafil till TEX kan förberedas med en textredigerare med vanlig text. Till skillnad från en vanlig ordbehandlare tillåter den här indatafilen alla osynliga kontrolltecken. En fil kan bäddas in i en annan fil, innehållande makrodefinitioner och hjälpdefinitioner som förbättrar TeX:s möjligheter. Om en TeX-installation kommer med några makrofiler, visar den lokala informationen om TeX hur man använder makrofiler. Standardformen av TeX, integrerar en kombination av makron och andra definitioner som kallas vanlig TEX.

På grundval av exakt kunskap om storlekarna på alla tecken och symboler, beräknar den den optimala organisationen av bokstäver per rad och rader per sida. Vid tidpunkten för dokumentbehandlingen produceras en .dvi-fil, där "dvi" står för "device independent". Enhetsdrivrutinsprogram krävs för att skriva ut eller förhandsgranska dokumentet med en dvi-tillägg. Numera förbigås dvi-generering av en vanlig pdf-TeX. Inga förkunskaper om typsnitt finns inom TeX-installation, så externa teckensnittsfiler, som ingår i lokal TeX-miljö, används för att få information till dokument.

## Typsättningssystem ##

Cirka 300 primitiver (kommandon) kan förstås av TeX-bassystemet. Primitiver är kommandon på låg nivå, därför använde en vanlig användare dem sällan direkt och de flesta funktionerna utförs av formatfiler. Dessa formatfiler är förladdade minnesbilder av TeX som följs av laddning av stora makrosamlingar. Det ursprungliga standardformatet för språket, dvs vanlig TeX, lägger till cirka 600 kommandon.

Ett omvänt snedstreck grupperat med hängslen anger början av TeX-kommandon. Eftersom TeX är ett makro- och tokenbaserat språk, kan nästan alla TeXs syntaktiska egenskaper ändras under körning, inklusive användardefinierade utom icke-expanderbara tokens som sedan exekveras. Expansionen i sig är praktiskt taget problemfri. Vissa kommandon måste komma efter ett argument som hjälper till att förklara ett kommandos funktion. Till exempel dirigerar kommandot \vskip TEX att hoppa nedåt/uppåt på sidan följt av ett argument som bestämmer hur mycket utrymme som ska hoppa över.

## Versioner ##

LaTeX är det mest använda formatet som ursprungligen utvecklades av Leslie Lamport. LaTeX integrerar olika dokumentstilar för filer, brev, böcker och bilder och erbjuder referenser och automatisk numrering för olika avsnitt och matematiska uttryck. AMS-TeX är ett annat populärt format, utvecklat av American Mathematical Society.

AMS-TeX erbjuder mycket mer användarvänliga kommandon, som kan omdefinieras av tidskrifter för att passa med deras lokala stil. LaTeX kan utnyttja fördelarna med AMS-TeX genom att använda AMS-"paketen" som sedan kallas AMS-LaTeX. ConTeXt är ett annat format skrivet av Hans Hagen som främst används för desktop publishing.

TeX-mjukvaran erbjuder flera funktioner som var otillgängliga, eller av lägre kvalitet, i andra typsättningssystem när den skapades. Några av de innovativa funktionerna i detta språk är baserade på intressanta algoritmer som härrör från Knuths elevers avhandlingar. Medan andra typsättningsprogram nu införlivar användbara funktioner i TeX i sina program.

## Referenser ##

* [TeX-typsättningssystem](https://en.wikipedia.org/wiki/TeX)

