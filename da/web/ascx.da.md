{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"ascx fil",
"ascx filformat",
"ascx filtype",
"fil",
"type",
"hvad er en ascx-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASCX filformat",
  "description": "Lær om, hvad en ASCX-fil og API'er er, der kan oprette og åbne ASCX-filer.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-dax"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en ASCX fil?

En fil med filtypenavnet .ascx er en brugerkontrol, der bruges som en genbrugelig komponent på websider. Det refereres til på ethvert ASP-websted ved at trække det fra kontrolboksen til siden. ASCX-brugerkontroller føjes til projektet som en central kilde, hvilket resulterer i, at enhver ændring i brugerkontrollen afspejles på tværs af hele webstedet. I modsætning til ASMX-filer, der definerer en mekanisme til at kommunikere inden for 2 objekter over internettet, er ASCX-filer brugerkontroller til indlejring på sider eller websteder.

## ASCX filformat

ASCX-filer skrives i almindeligt tekstformat og kan bruge kode bag funktioner som websider, der ender med .ascx.cs. Markup-kode for brugerkontroller starter med @Control-direktivet som vist i følgende eksempel.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Denne webbrugerkontrol kan genbruges på mange sider, såsom sidefod, sidehoved eller en eller anden form for webstedsnavigation. Webbrugerkontroller har egenskaber, metoder og begivenheder som enhver anden kontrol, der gør dem nyttige til at indstille deres visuelle adfærd.

### Eksempel på registrering af brugerkontroller i web.config

For at bruge en enkelt brugerkontrol på mange sider, kan webkontrollen registreres i web.config. Dette giver mulighed for at bruge kontrollen over hele hjemmesiden i stedet for at registrere sig på hver side individuelt. Følgende eksempelkode definerer, hvordan man registrerer en webkontrol i web.config, så den vises som sidefod på hele webstedet.

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
## Referencer

 * [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
 * [ASCX-brugerkontrol](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

