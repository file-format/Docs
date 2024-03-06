{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Cold Fusion iezīmēšanas valoda",
"valodu",
"CFM tīmekļa lapas",
"CFML dzinējs",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM — Cold Fusion Markup",
  "description": "Uzziniet par CFM failu formātu un API, kas var izveidot un atvērt CFM failus.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-lvm"
}
},
  "lastmod": "2021-07-13"
}

## Kas ir CFM fails? ##

**Cold Fusion iezīmēšanas valodā** izmantotajās tīmekļa lapās un failos ir CFM paplašinājumi, un to nosaukums ir CFM tīmekļa lapas. Šī tīmekļa izstrādes skriptu valoda darbojas Google App Engine, .NET framework un JVM. Tas var saturēt programmēšanas valodu vai valodas kodu. Kad lietotājs piekļūst kādai no tās lapām, ColdFusion tīmekļa serveris to izpilda. CFML rakstīšanai var izmantot CFScript (kas ir tuvu JavaScript) vai tagus. CFML var izmantot citu valodu ģenerēšanai, izņemot [HTML](/web/html/), piemēram, [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/) un citas.

Šī valoda un tās atbalstītie tagi galvenokārt tiek izmantoti dinamisku tīmekļa lietojumprogrammu izstrādē. Failus var tieši palaist pārlūkprogrammā tiešsaistē, ja lietojumprogrammas izstrādes platformas bezsaistes lietošanas laikā rodas kļūda.
 
CFML darbojas tādā veidā, ka konkrēti servera failu paplašinājumi (.cfc, .cfm) tiek piešķirti apstrādei CFML dzinējam. Ja dzinēji ir balstīti uz Java, tas tiek panākts, izmantojot Java servletus. CFML dzinējs apstrādā tikai funkcijas un tagus un bez izmaiņām atgriež tīmekļa serverī funkcijas un tekstu ārpus CFML tagiem.


## Īsa vēsture ##

1995. gadā to pirmo reizi izveidoja korporācija ar nosaukumu Allaire. 2005. gadā Adobe to iegādājās un sniedz pakalpojumus ColdFusion izstrādei vēl tagad. Gadu gaitā to ir izstrādājuši un modernizējuši daudzi cilvēki un uzņēmumi. 2012. gadā tika izveidots fonds ar nosaukumu OpenCFML. Vēlāk, 2015. gadā, bijušais Railo sniedza savus pakalpojumus, lai uzlabotu CFM veiktspēju un samazinātu resursus labākai funkcionalitātei. Jaunākais tā atjauninājums tika palaists 2020. gadā, un tiek paziņots, ka tas turpināsies līdz 2028. gadam.

## CFM faila formāts ##

CFM failu un tīmekļa lapu kods galvenokārt ietver tagus, piemēram, HTML, bet ar nelielu atšķirību. Šie faili ir atbildīgi par dažādu darbību veikšanu, kuras nodrošina ColdFusion skripti.
* Šiem failiem var piekļūt un tie var darboties gan operētājsistēmā Windows, gan macOS, izmantojot jebkuras operētājsistēmas pārlūkprogrammu.
* Adobe ColdFusion nodrošina platformu tīmekļa lapu un dinamisku lietojumprogrammu izstrādei datorā.
* Šo failu atvēršanai var izmantot jebkuru teksta redaktoru, piemēram, NotePad vai jebkuru citu teksta redaktoru operētājsistēmā, jo šie faili ir balstīti uz tekstu.
* Kad jebkurš CFM fails tiek atvērts teksta redaktorā, tajā tiek parādīts kods, kas sastāv no tagiem un skriptiem, kurus nevar saprast, ja vien viņš nav tīmekļa izstrādātājs.

## CFM lietošanas piemērs ##

Tālāk ir parādīts vienkāršs CFM faila lietošanas piemērs.

### CFM dokuments ###

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

## Atsauces Nr.

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

