{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Cold Fusion Markup Language",
"Kieli",
"CFM:n verkkosivut",
"CFML moottori",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM - Cold Fusion Markup",
  "description": "Opi CFM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CFM-tiedostoja.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-fim"
}
},
  "lastmod": "2021-07-13"
}

## Mikä on CFM-tiedosto? ##

**Cold Fusion Markup Language** -kielessä käytetyt verkkosivut ja tiedostot sisältävät CFM-laajennuksia, ja niitä kutsutaan CFM-verkkosivuiksi. Tämä verkkokehityksen komentosarjakieli toimii Google App Enginessä, .NET frameworkissa ja JVM:ssä. Se voi sisältää ohjelmointikielen tai kielen koodin. Kun käyttäjä käyttää jotakin sen sivua, ColdFusionin verkkopalvelin suorittaa sen. CFScriptiä (joka on lähellä JavaScriptiä) tai tunnisteita voidaan käyttää CFML:n kirjoittamiseen. CFML:ää voidaan käyttää muiden kielten luomiseen [HTML](/web/html/):n lisäksi, kuten [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/) ja paljon muuta.

Tämän kielen ja sen tukemien tunnisteiden käyttö on enimmäkseen dynaamisten verkkosovellusten kehittämisessä. Tiedostot voidaan ajaa suoraan selaimessa online-tilassa, jos sovelluksen kehitysalustan offline-käytön aikana tapahtuu virhe.
 
CFML toimii siten, että tietyt palvelimen tiedostopäätteet (.cfc, .cfm) annetaan CFML-moottorin käsittelyä varten. Jos moottorit perustuvat Javaan, se saavutetaan Java-servlettien avulla. CFML-moottori käsittelee vain funktioita ja tunnisteita ja palauttaa CFML-tunnisteiden ulkopuoliset funktiot ja tekstit verkkopalvelimelle ilman muutoksia.


## Lyhyt historia ##

Vuonna 1995 sen perusti ensimmäisen kerran yhtiö nimeltä Allaire. Vuonna 2005 Adobe osti sen ja se tarjoaa palveluita ColdFusionin kehittämiseen edelleen. Kuluneiden vuosien aikana monet ihmiset ja yritykset ovat kehittäneet ja päivittäneet sitä. Vuonna 2012 perustettiin säätiö nimeltä OpenCFML. Myöhemmin, vuonna 2015, entinen Railo tarjosi palvelujaan parantaakseen CFM:n suorituskykyä ja vähentäen resursseja paremman toimivuuden saavuttamiseksi. Sen viimeisin päivitys julkaistiin vuonna 2020, ja sen on ilmoitettu jatkuvan vuoteen 2028 asti.

## CFM-tiedostomuoto ##

CFM-tiedostojen ja verkkosivujen koodi sisältää enimmäkseen HTML:n kaltaisia tageja, mutta pienellä erolla. Nämä tiedostot vastaavat useiden ColdFusion-skriptien suorittamista toiminnoista.
* Näitä tiedostoja voi käyttää ja suorittaa suoraan sekä Windowsissa että macOS:ssä minkä tahansa käyttöjärjestelmän selaimella.
* Adobe ColdFusion tarjoaa alustan web-sivujen ja dynaamisten sovellusten kehittämiseen PC:llä.
* Mitä tahansa tekstieditoria, kuten NotePadia tai mitä tahansa käyttöjärjestelmän tekstieditoria, voidaan käyttää näiden tiedostojen avaamiseen, koska nämä tiedostot ovat tekstipohjaisia.
* Kun mikä tahansa CFM-tiedosto avataan tekstieditorissa, se näyttää koodin, joka koostuu tunnisteista ja skripteistä, joita ei ymmärtäisi, ellei hän ole verkkokehittäjä.

## CFM-käyttöesimerkki ##

Seuraavassa on yksinkertainen käyttöesimerkki CFM-tiedostosta.

### CFM-asiakirja ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Viitteet ##

- {{HYPERLINKKI}}

