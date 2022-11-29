{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Läs mer om TNEF-filformat och API:er som kan skapa och öppna TNEF-filer.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är TNEF fil?

Transport Neutral Encapsulation Format (TNEF) är ett patentskyddat Microsoft-program för inkapsling av e-postbilagor baserade på Messaging Application Programming Interface (**MAPI**). Microsoft Outlook och Microsoft Exchange Server stöder helt TNEF medan de senare avkodar TNEF till MAPI och visar de formaterade e-postmeddelandena. En e-postbilaga med TNEF-kodning har en MIME-typ av MS-TNEF och lagras som winmail/win.dat. Bilagan i winmail .dat kapslar in följande information:


|Meddelande|OLE-objekt|Outlook-funktioner
---|---|---|
|<ul><li> Originalmeddelandebilagor</li><li> Originalformaterad version</li><li> teckensnitt, textstorlekar och textfärger</li></ul> |<ul><li> inbäddade bilder</li><li> inbäddade Office-dokument</li></ul> |<ul><li> anpassade formulär</li><li> röstningsknappar</li><li> mötesförfrågningar</li></ul>


Andra e-posttjänster som inte stöder TNEF, presenterar vanlig text för TNEF-formaterade meddelanden. Outlook bäddar in ett rikt format av meddelandet i TNEF-filer (OLE) eller särskilda Outlook-funktioner (formulär, polling-knappar och konferensförfrågningar). Det är inte möjligt att sanktionera explicit TNEF-kodning i Outlooks e-postklient, men att välja RTF-format för att skicka ett e-postmeddelande underlättar implicit TNEF-kodning.

## TNEF filformat

TNEF-dataalgoritmen etablerar en tillplattad struktur från rika hierarkiska meddelandeegenskaper. Dessa tillplattade strukturer använder sedan för att representera en seriell dataström som består av särskilda egenskaper.

I vissa situationer, där egenskaper förekommer i grupper eller har flera värden, kan strömmen innehålla räkningar och utfyllnad för att framtvinga en specifik datajustering. En distinkt situation där användningen av denna algoritm är fördelaktig är i en meddelandemiljö som inte stöder. I sådana miljöer kodas en rik meddelandeegenskap in i en seriell dataström av en TNEF Writer. Vidare kan de egenskaper som inte tillhör den underliggande TNEF kapslas in under överföring. Dessa inkapslade egenskaper gjordes sedan tillgängliga genom avkodning genom en TNEF för att säkerställa tillgängligheten av alla egenskaper hos det ursprungliga meddelandet till klientapplikationen.

I TNEF är alla numeriska datatyper little-endian och deras storlek är större än en byte. Hantering av dessa numeriska värden på icke-little-endian-plattformar kräver att man genomför lämpliga transformationer för att få korrekta värden. Strängvärden representeras i Augmented Backus-Naur Form (ABNF) format enligt [RFC5234] specifikationer. När strängen avslutas med noll-tecken ingår den också; till exempel "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="TNEF filformat" >}}

## TNEF-attribut och bearbetningsregler ##

Dataströmmen i TNEF börjar med ett äldre versionsnummer, en signatur, ett primitivt nyckelvärde och ett attribut representerar teckentabell. Denna teckentabell genereras när kodaren registrerar ANSI-attribut och egenskaper. Efter det blev strömmen en serie attribut där meddelandeattributen radades först och sedan följs av bifogade attribut. Olika meddelande- och bifogade egenskaper finns i speciella attribut som attMsgProps, attAttachment och attRecipTable. Attributen som visas i TNEF-strömmen innehåller strukturen, meddelandeegenskaperna och omvandlingarna som är nödvändiga för att engagera dem med meddelandeegenskaper. Varje attribut består av ett ID, storlek och data för attributet, en kontrollsumma och en nivå enligt dess tillämpning.

## Relation till protokoll och andra algoritmer ##

De system som har dålig mekanism för att visa rikt meddelandeformat behöver naturligt TNEF-dataalgoritm för transport. Med hjälp av mediatypen ms-TNEF består utdata från algoritmen av en bifogad fil (winmail.dat) och en kroppsdel av MIME specificerad i [RFC2045]. Textmeddelandetexten sänds med hjälp av UUENCODE enligt [MSDN-UAF]-specifikationen och denna meddelandetext eller motsvarande metod avkodas i mottagaränden. Dessutom kan TNEF sända meddelandedata med hjälp av olika internetprotokoll som SMTP, POP3, IMAP4, och de som integrerar MIME enligt RFC2045-standarden.

## Tillämpningsförklaring ##

Förutom enkel meddelandeöverföring, skulle den ursprungliga applikationen av TNEF skapas för att använda meddelandeklasser och stödja ytterligare funktioner som inte har något originalstöd i transportprotokoll. Denna applikation förfinades ytterligare för överföring av rika meddelandeegenskaper och namngivna egenskaper som moderna meddelandeklienter använder nu för tiden. För överensstämmelse med den ursprungliga implementeringen bibehålls den ursprungliga attributsyntaxen och ett speciellt attribut håller de nya meddelandeegenskaperna separat.

## Referenser

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [E-postadresser och adressböcker i Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) Data Algorithm](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

