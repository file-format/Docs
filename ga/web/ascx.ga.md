{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"comhad ascx",
"formáid comhaid ascx",
"cineál comhaid ascx",
"comhad",
"cineál",
"Cad is comhad ascx ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid ASCX",
  "description": "Foghlaim faoi cad is comhad ASCX agus APIs ann ar féidir comhaid ASCX a chruthú agus a oscailt.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-gax"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad ASCX ann?

Is éard atá i gcomhad le síneadh .ascx ná rialú úsáideora a úsáidtear mar chomhpháirt ath-inúsáidte ar leathanaigh ghréasáin. Déantar tagairt dó in aon láithreán gréasáin ASP trí é a tharraingt ón mbosca rialaithe go dtí an leathanach. Cuirtear rialuithe úsáideoirí ASCX leis an tionscadal mar fhoinse lárnach, rud a fhágann go léireofar aon athrú ar an rialú úsáideora ar fud an láithreáin ghréasáin ar fad. Murab ionann agus comhaid ASMX a shainíonn meicníocht chun cumarsáid a dhéanamh laistigh de 2 réad ar an idirlíon, is rialuithe úsáideoirí iad comhaid ASCX chun iad a leabú i leathanaigh nó ar shuíomh Gréasáin.

## Formáid Chomhaid ASCX

Tá comhaid ASCX ag scríobh i bhformáid gnáth-théacs agus is féidir leo cód a úsáid taobh thiar de ghné mar leathanaigh ghréasáin a chríochnaíonn le .ascx.cs. Tosaíonn cód marcála rialuithe úsáideoirí le treoir @Control mar a thaispeántar sa sampla seo a leanas.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Is féidir an rialú úsáideora gréasáin seo a athúsáid ar go leor leathanach ar nós buntásc leathanaigh, ceanntásc nó cineál éigin nascleanúna suímh. Tá airíonna, modhanna agus imeachtaí ag rialuithe úsáideoirí gréasáin mar aon rialtóir eile a fhágann go bhfuil siad úsáideach chun a n-iompraíocht amhairc a shocrú.

### Sampla de rialuithe úsáideora a chlárú i web.config

D'fhonn rialú úsáideora aonair a úsáid ar go leor leathanaigh, is féidir an rialú gréasáin a chlárú i web.config. Ligeann sé seo úsáid a bhaint as an smacht ar an suíomh Gréasáin ar fad seachas clárú ar gach leathanach ina n-aonar. Sainmhíníonn an cód samplach seo a leanas conas rialú gréasáin a chlárú i web.config le taispeáint mar bhuntásc ar an suíomh Gréasáin iomlán.

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
## Tagairtí

 * [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
 * [Rialú Úsáideora ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

