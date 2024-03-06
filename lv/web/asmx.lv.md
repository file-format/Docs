{
  "date": "2019-10-11",
  "keywords": [
"asmx",
"asmx fails",
"asmx faila formātā",
"asmx faila tips",
"failu",
"veids",
"kas ir asmx fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASMX — ASP.NET tīmekļa pakalpojuma fails",
  "description": "Uzziniet, kas ir ASMX fails un API, kas var izveidot un atvērt ASMX failus.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asm-lvx"
}
},
  "lastmod": "2021-06-10"
}

## Kas ir ASMX fails?

Fails ar .asmx paplašinājumiem ir ASP.NET Web Service fails, kas nodrošina saziņu starp diviem objektiem internetā, izmantojot vienkāršo objektu piekļuves protokolu (Simple Object Access Protocol — SOAP). Tas tiek izvietots kā pakalpojums Windows tīmekļa serverī, lai apstrādātu ienākošos pieprasījumus un atgrieztu atbildi. Atšķirībā no [ASPX](/web/aspx/) failiem, kas satur kodu ASP.NET tīmekļa lapu vizuālai parādīšanai, ASMX faili darbojas serverī fonā un veic dažādus uzdevumus, piemēram, savienojuma izveidi ar datu bāzi, datu izgūšanu un atgriešanu formātā, kurā tika izteikts pieprasījums. Tie tiek izmantoti īpaši XML tīmekļa pakalpojumiem.

## ASMX faila formāts

ASMX faili ir vienkārša teksta formātā, un tos var atvērt vai rediģēt lietojumprogrammās, piemēram, Microsoft Visual Studio vai teksta redaktoros. Tas ir Microsoft patentēts faila formāts, un tam ir labi definēta sintakse tīmekļa pakalpojumu izveidei. ASMX faila atbildei SOAP XML formātā ir šādi elementi.

 * Envelop — saknes elements, kas identificē XML dokumentu kā SOAP ziņojumu.
 * Galvene — izvēles elements, kas satur lietojumprogrammas informāciju, piemēram, autentifikācijas datus. Ja ir ietverts elements Header, tam ir jābūt elementa Envelope pirmajam atvasinātajam elementam.
 * `Body` — satur adresātam paredzēto SOAP ziņojumu.
 * Kļūme — neobligāts elements, ko izmanto, lai norādītu kļūdu ziņojumus. Ja ir elements Fault, tam ir jābūt elementa Body atvasinātajam elementam.

ASMX failus var rakstīt .NET valodās, piemēram, [C#](/programming/cs/), [Visual Basic](/programming/vb/) vai JScript.

## Kā ASMX atšķiras no ASPX un ASCX?

ASMX faili atšķiras no ASPX un ASCX failiem.

 * ASPX, Active Server Pages, faili ir programmēšanas faili, kas tiek ģenerēti, izmantojot Microsoft ASP.NET ietvaru, kas darbojas tīmekļa serveros. Tie tiek atveidoti klienta tīmekļa pārlūkprogrammā, kad lietotājs pieprasa piekļūt šādai lapai.
 * ASCX, Active Server User Control, definē lietotāja vadīklas, kas tiek izmantotas, lai definētu atkārtoti lietojamas vadīklas ASP.NET tīmekļa lapās vai visā vietnē.

## References

 * [Patērējot ASMX pakalpojumu](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX lietotāja vadība](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

