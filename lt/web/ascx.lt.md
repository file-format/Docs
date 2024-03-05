{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"ascx failą",
"ascx failo formatas",
"ascx failo tipas",
"failą",
"tipo",
"kas yra ascx failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASCX failo formatas",
  "description": "Sužinokite, kas yra ASCX failas ir API, kurios gali kurti ir atidaryti ASCX failus.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-ltx"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra ASCX failas?

Failas su plėtiniu .ascx yra vartotojo valdiklis, naudojamas kaip daugkartinis tinklalapių komponentas. Jis nurodomas bet kurioje ASP svetainėje, nuvilkant jį iš valdymo laukelio į puslapį. ASCX naudotojų valdikliai pridedami prie projekto kaip pagrindinis šaltinis, todėl bet kokie vartotojo valdymo pakeitimai atsispindės visoje svetainėje. Skirtingai nuo ASMX failų, kurie apibrėžia 2 objektų bendravimo internetu mechanizmą, ASCX failai yra vartotojo valdikliai, skirti įterpti į puslapius ar svetainę.

## ASCX failo formatas

ASCX failai rašomi paprasto teksto formatu ir gali naudoti kodą už funkcijos, pvz., tinklalapių, kurie baigiasi .ascx.cs. Vartotojo valdiklių žymėjimo kodas prasideda @Control direktyva, kaip parodyta kitame pavyzdyje.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Šį žiniatinklio naudotojo valdiklį galima pakartotinai naudoti daugelyje puslapių, pvz., puslapio poraštėje, antraštėje ar tam tikroje svetainės naršymo rūšyje. Žiniatinklio naudotojo valdikliai turi ypatybes, metodus ir įvykius, kaip ir bet kuris kitas valdiklis, todėl jie yra naudingi nustatant jų vizualinį elgesį.

### Vartotojo valdiklių registravimo web.config pavyzdys

Norint naudoti vieną vartotojo valdiklį daugelyje puslapių, žiniatinklio valdiklį galima užregistruoti web.config. Tai leidžia valdyti visą svetainę, o ne registruotis kiekviename puslapyje atskirai. Šis pavyzdinis kodas apibrėžia, kaip užregistruoti žiniatinklio valdiklį web.config, kad jis būtų rodomas kaip poraštė visoje svetainėje.

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
## Nuorodos

  * [ASCX naudotojo valdymas](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)
