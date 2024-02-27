{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "Lær om TNEF filformat og API'er, der kan oprette og åbne TNEF filer.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er TNEF fil?

Transport Neutral Encapsulation Format (TNEF) er en proprietær Microsoft til indkapsling af e-mail-vedhæftede filer baseret på Messaging Application Programming Interface (**MAPI**). Microsoft Outlook og Microsoft Exchange Server understøtter fuldstændig TNEF, mens de senere afkoder TNEF til MAPI og viser de formaterede mails. En e-mail-vedhæftet fil med TNEF-kodning har en MIME-type MS-TNEF og gemmer som winmail/win.dat. Den vedhæftede fil i winmail .dat indkapsler følgende oplysninger:


|Besked|OLE-objekter|Outlook-funktioner
---|---|---|
|<ul><li> Originale vedhæftede filer</li><li> Original formateret version</li><li> skrifttyper, tekststørrelser og tekstfarver</li></ul> |<ul><li> indlejrede billeder</li><li> indlejrede Office-dokumenter</li></ul> |<ul><li> brugerdefinerede formularer</li><li> stemmeknapper</li><li> mødeindkaldelser</li></ul>


Andre e-mail-tjenester, der ikke understøtter TNEF, præsenterer almindelig tekst til TNEF-formaterede beskeder. Outlook integrerer et rigt format af meddelelsen i TNEF-filer (OLE) eller særlige Outlook-funktioner (formularer, afstemningsknapper og konferenceanmodninger). Det er ikke muligt at sanktionere eksplicit TNEF-kodning i Outlook e-mail-klienten, men at vælge RTF-format til afsendelse af en e-mail letter implicit TNEF-kodning.

## TNEF filformat

TNEF-dataalgoritmen etablerer en fladtrykt struktur fra rige hierarkiske meddelelsesegenskaber. Disse fladtrykte strukturer bruges derefter til at repræsentere en seriel datastrøm sammensat af bestemte egenskaber.

I nogle situationer, hvor egenskaber forekommer i grupper eller har flere værdier, kan stream inkludere tællinger og udfyldninger for at håndhæve en specifik datajustering. En karakteristisk situation, hvor brugen af denne algoritme er fordelagtig, er i et ikke-understøttende meddelelsesmiljø. I sådanne miljøer er en rig beskedegenskab kodet ind i en seriel datastrøm af en TNEF Writer. Yderligere kan de egenskaber, der ikke tilhører den underliggende TNEF, indkapsles under transmission. Disse indkapslede egenskaber blev derefter gjort tilgængelige ved afkodning gennem en TNEF for at sikre tilgængeligheden af alle egenskaber af den originale besked til klientapplikationen.

I TNEF er alle numeriske datatyper little-endian og deres størrelse er større end én byte. Håndtering af disse numeriske værdier på ikke-little-endian platforme kræver at udføre de passende transformationer for at få korrekte værdier. Strengværdier er repræsenteret i Augmented Backus-Naur Form (ABNF) format i henhold til [RFC5234] specifikationer. Når strengen afsluttes med nul-tegn, er den også inkluderet; for eksempel `worker@specimen.com %x00`.

{{< figure src="../TNEF.png" alt="TNEF filformat" >}}

## TNEF-attributter og behandlingsregler ##

Datastrømmen i TNEF begynder med et ældre versionsnummer, en signatur, en primitiv nøgleværdi og en attribut repræsenterer tegntabel. Denne tegntabel genereres, når encoder registrerer ANSI-attributter og -egenskaber. Derefter blev strømmen til en række attributter, hvor meddelelsesattributter stod på linje først og derefter efterfulgt af vedhæftede attributter. Forskellige meddelelses- og vedhæftningsegenskaber er indeholdt i specielle attributter som attMsgProps, attachment og attRecipTable. De attributter, der vises i TNEF-strømmen, indeholder den struktur, meddelelsesegenskaber og konverteringer, der er nødvendige for at engagere dem med meddelelsesegenskaber. Hver attribut består af et ID, størrelse og data for attributten, en kontrolsum og et niveau i henhold til dens anvendelse.

## Forholdet til protokoller og andre algoritmer ##

De systemer, der har dårlig mekanisme til at vise rigt meddelelsesformat, har naturligt brug for TNEF-dataalgoritme til transport. Ved at bruge medietypen ms-TNEF består outputtet af algoritmen af en vedhæftet fil (winmail.dat) og en kropsdel af MIME angivet i [RFC2045]. Brødteksten i almindelig tekstbesked transmitteres ved hjælp af UUENCODE i henhold til [MSDN-UAF]-specifikationen, og denne meddelelsestekst eller tilsvarende metode afkodes i modtagerenden. Desuden kan TNEF transmittere beskeddata ved hjælp af forskellige internetprotokoller som SMTP, POP3, IMAP4, og dem, der integrerer MIME i henhold til RFC2045-standarden.

## Anvendelseserklæring ##

Ud over simpel meddelelsestransmission skulle den originale applikation af TNEF oprettes for at bruge meddelelsesklasser og understøtte yderligere funktioner, der ikke har nogen original understøttelse i transportprotokol. Denne applikation blev yderligere forfinet til transmission af rige beskedegenskaber og navngivne egenskaber, som moderne beskedklienter bruger nu om dage. For at overholde den oprindelige implementering bibeholdes den oprindelige attributsyntaks, og en speciel attribut holder de nye meddelelsesegenskaber separat.

## Referencer

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [E-mail-adresser og adressebøger i Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)

* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) Data Algorithm](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


