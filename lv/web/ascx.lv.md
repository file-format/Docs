{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"ascx failu",
"ascx faila formātā",
"ascx faila tips",
"failu",
"veids",
"kas ir ascx fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASCX faila formāts",
  "description": "Uzziniet, kas ir ASCX fails un API, kas var izveidot un atvērt ASCX failus.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-lvx"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir ASCX fails?

Fails ar paplašinājumu .ascx ir lietotāja vadīkla, kas tiek izmantota kā atkārtoti lietojams komponents tīmekļa lapās. Uz to ir atsauce jebkurā ASP vietnē, velkot to no vadības lodziņa uz lapu. ASCX lietotāju vadīklas tiek pievienotas projektam kā centrālais avots, kā rezultātā visas lietotāja vadīklas izmaiņas tiks atspoguļotas visā vietnē. Atšķirībā no ASMX failiem, kas definē mehānismu saziņai 2 objektos internetā, ASCX faili ir lietotāja vadīklas iegulšanai lapās vai vietnē.

## ASCX faila formāts

ASCX faili tiek rakstīti vienkārša teksta formātā un var izmantot kodu aiz funkcijas, piemēram, tīmekļa lapas, kas beidzas ar .ascx.cs. Lietotāja vadīklu iezīmēšanas kods sākas ar @Control direktīvu, kā parādīts nākamajā piemērā.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Šo tīmekļa lietotāja vadīklu var atkārtoti izmantot daudzās lapās, piemēram, lapas kājenē, galvenē vai kāda veida vietnes navigācijā. Tīmekļa lietotāju vadīklām ir tādi rekvizīti, metodes un notikumi kā jebkurai citai vadības ierīcei, kas padara tos noderīgus to vizuālās uzvedības iestatīšanā.

### Piemērs lietotāja vadīklu reģistrēšanai vietnē web.config

Lai izmantotu viena lietotāja vadīklu daudzās lapās, tīmekļa vadīklu var reģistrēt vietnē web.config. Tas ļauj izmantot visas vietnes kontroli, nevis reģistrēties katrā lapā atsevišķi. Šis parauga kods nosaka, kā reģistrēt tīmekļa vadīklu vietnē web.config, lai tā tiktu parādīta kā kājene visā vietnē.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Atsauces

 * [ASCX pret ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
 * [ASCX lietotāja vadība](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

