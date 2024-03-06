{
  "date": "2020-08-20",
  "keywords": [
"eot failu",
"eot faila formātā",
"kas ir eot fails",
"failu",
"eot piemērs",
"eot faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT — TrueType fonta faila formāts",
  "description": "Uzziniet par EOT faila formātu un API, lai izveidotu un atvērtu EOT failus.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-lvt"
}
},
  "lastmod": "2020-10-21"
}

## Kas ir EOT fails?

Fails ar paplašinājumu .eot ir OpenType fonts, kas ir iegults dokumentā. Tos galvenokārt izmanto tīmekļa failos, piemēram, tīmekļa lapās. To izveidoja Microsoft, un to atbalsta Microsoft produkti, tostarp PowerPoint prezentācijas fails [.pps](/presentation/pps/). Fails nav primārais lietojums, un tas ir sava veida pavaddokuments ar galveno dokumentu vai tīmekļa lapu. Līdzīgi kā OTF fonti, EOT atbalsta gan Postscript, gan TrueType kontūras glifiem. EOT faili ir mazāki, jo tie tiek saspiesti, izmantojot LZ saspiešanu. EOT izmanto Microsoft rīku, lai izveidotu fontu no esošajiem TTF/OTF fontiem.

## Īsa vēsture

EOT fonts tika iesniegts W3C 2007. gadā kā daļa no CSS3, taču tā prasības dēļ pastāvīgi instalētam attālajā sistēmā kļuva par tā noraidīšanas iemeslu. Tas tika atkārtoti iesniegts 2008. gada martā, taču W3C galu galā izvēlējās [Web Font Format](/font/woff/) (WOFF), kas toreiz tika standartizēts.

## EOT faila formāts

Sīkāka informācija par EOT faila formātu ir atrodama vietnē [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat), un tajā ir aprakstīta šī fonta formāta izmantotā struktūra. EOT sastāv no vienas EMBEDDEDFONT struktūras, kas sniedz pietiekami daudz pamatinformācijas par hte fonta nosaukumu un atbalstītajām rakstzīmēm. Šīs informācijas iesaiņošana ļauj lietotāja aģentiem izvairīties no fonta izpakošanas, atspiešanas vai instalēšanas, ja tas jau ir iekārtā.

### EMBEDDEDFONT Struktūra
EMBEDDEDFONT struktūra ir trīs reizes pārskatīta, katras pārskatīšanas reizē struktūras beigās pievienojot papildu datus. Pēdējā EMBEDDEDFONT struktūras pārskatīšana ir tāda, kā parādīts tālāk.

|Datu tips|Ieraksta nosaukums|Apraksts|
---|---|---|
|unsigned long|EOTSize|Kopējais struktūras garums baitos (ieskaitot virknes un fonta datus)|
|unsigned long|FontDataSize|OpenType fonta garums (FontData) baitos|
|unsigned long|Versija|Šī formāta versijas numurs - 0x00020002|
|unsigned long|Karogi|Apstrādā karogus|
|byte[10]|FontPANOSE|Šī fonta PANOSE vērtība — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|Sistēmā Windows tas ir atvasināts no TEXTMETRIC.tmCharSet. Šī vērtība norāda fonta rakstzīmju kopu. DEFAULT_CHARSET (0x01) norāda, ka nav izvēles. - Skatiet https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Ja OS/2.fsSelection ir iestatīts ITALIC bits, vērtība būs 0x01 — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|Šī fonta svara vērtība — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Tips karodziņi, kas sniedz informāciju par iegulšanas atļaujām — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Maģiskais numurs EOT failam — 0x504C. Izmanto, lai pārbaudītu, vai dati nav bojāti.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (biti 0–31) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (biti 32-63) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (biti 64-95) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (biti 96-127) — Skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (biti 0–31) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (biti 32-63) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Rezervēts1|Rezervēts — jābūt 0|
|unsigned long|Rezervēts2|Rezervēts — jābūt 0|
|unsigned long|Rezervēts3|Rezervēts — jābūt 0|
|unsigned long|Rezervēts4|Rezervēts — jābūt 0|
|unsigned short|Padding1|Padding, lai saglabātu garu līdzinājumu. Polsterējuma vērtībai vienmēr jābūt iestatītai uz 0x0000.|
|unsigned short|FamilyNameSize|FamilyName masīva izmantoto baitu skaits|
|byte|FamilyName[FamilyNameSize]|UTF-16 rakstzīmju masīvs FamilyNameSize baitu garumā. Šī ir angļu valodas fontu saimes virkne, kas atrodama fonta nosaukumu tabulā (nosaukuma ID = 1) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Padding vērtība vienmēr ir jāiestata uz 0x0000.|
|unsigned short|StyleNameSize|StyleName izmantoto baitu skaits|
|byte|StyleName[StyleNameSize]|UTF-16 rakstzīmju masīvs StyleNameSize baitu garumā. Šī ir angļu valodas fontu apakšgrupas virkne, kas atrodama fonta nosaukumu tabulā (nosaukuma ID = 2) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Padding vērtība vienmēr ir jāiestata uz 0x0000.|
|unsigned short|VersionNameSize|VersionName izmantoto baitu skaits|
|baiti|VersionName[VersionNameSize]|UTF-16 rakstzīmju masīvs VersionNameSize baitu garumā. Šī ir angļu valodas versijas virkne, kas atrodama fonta nosaukumu tabulā (nosaukuma ID = 5) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Padding vērtība vienmēr ir jāiestata uz 0x0000.|
|unsigned short|FullNameSize|FullName izmantoto baitu skaits|
|byte|FullName[FullNameSize]|UTF-16 rakstzīmju masīvs FullNameSize baitu garumā. Šī ir angļu valodas pilna nosaukuma virkne, kas atrodama fonta nosaukumu tabulā (nosaukuma ID = 4) — skatiet https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Padding vērtība vienmēr ir jāiestata uz 0x0000.|
|unsigned short|RootStringSize|RootString masīva izmantoto baitu skaits|
|byte|RootString[RootStringSize]|UTF-16 rakstzīmju masīvs RootStringSize baitu garumā.|
|unsigned long|RootStringCheckSum|RootString CheckSum vērtība. Skatiet tālāk algoritmu, lai apstrādātu RootStringChecksum.|
|unsigned long|EUDCCodePage|Koda lapas vērtība nepieciešama EUDC fontu atbalstam.|
|unsigned short|Padding6|Padding vērtība vienmēr ir jāiestata uz 0x0000.|
|unsigned short|SignatureSize|Paraksta masīva izmantoto baitu skaits. Pašlaik rezervēts un jāiestata uz 0x0000.|
|baits|Paraksts[SignatureSize]|Šobrīd rezervēts. Ja SignatureSize ir 0x0000, šim masīvam nav garuma.|
|unsigned long|EUDCFlags|Apstrādā EUDC fonta karogus. Tipiskās vērtības varētu būt TTEMBED_XORENCRYPTDATA un TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Paraksta masīva izmantoto baitu skaits.|
|baits|EUDCFontData[EUDCFontSize]|EUDC fontu datiem izmantoto baitu skaits. Ja EUDCFontSize ir 0x00000000, šim masīvam nav garuma.|
|byte|FontData[FontDataSize]|Šī EOT faila fonta dati. Dati var būt saspiesti vai XOR šifrēti, kā norāda apstrādes karodziņi.|

## Atsauces

 * [EOT faila formāts](https://www.w3.org/Submission/EOT/)
 * [Iegultais OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Fontu iegulšana](https://en.wikipedia.org/wiki/Font_embedding)

