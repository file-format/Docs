{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extensie", "fișier", "format", "sistem", "Cold Fusion Markup Language", "limbă", "pagini web CFM", "motor CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Markup Fusion rece",
  "description":"Aflați despre formatul de fișier CFM și despre API-urile care pot crea și deschide fișiere CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Ce este un fișier CFM? ##

Paginile web și fișierele utilizate în **Cold Fusion Markup Language** conțin extensii ale CFM și sunt denumite pagini web CFM. Acest limbaj de scripting pentru dezvoltare web rulează pe Google App Engine, .NET framework și JVM. Poate conține un limbaj de programare sau un cod al limbajului. Când oricare dintre paginile sale este accesată de utilizator, serverul web al ColdFusion o execută. CFScript (care este aproape de JavaScript) sau etichete pot fi folosite pentru a scrie CFML. CFML poate fi folosit pentru a genera alte limbaje în afară de [HTML](/ro/web/html/), cum ar fi [CSS](/ro/web/css/), [JavaScript](/ro/web/js/), [XML](/ro/web/ xml/), și multe altele.

Utilizarea acestui limbaj și a etichetelor pe care le acceptă este în principal în dezvoltarea de aplicații web dinamice. Fișierele pot fi rulate direct în browser online, dacă apare vreo eroare în timpul utilizării offline a platformei de dezvoltare a aplicației.
 

CFML funcționează într-un mod în care anumite extensii de fișiere de server (.cfc, .cfm) sunt date pentru procesare către motorul CFML. Dacă motoarele sunt bazate pe Java, se realizează folosind servlet-uri Java. Motorul CFML procesează numai funcții și etichete și returnează funcțiile și textul din afara etichetelor CFML către serverul web fără nicio modificare.


## Scurt istoric ##

În 1995, a fost creat pentru prima dată de o corporație numită Allaire. În 2005, Adobe l-a achiziționat și oferă servicii pentru dezvoltarea ColdFusion și în prezent. Cu anii care au trecut, a fost dezvoltat și modernizat de mulți oameni și companii. În 2012, a fost lansată o fundație numită OpenCFML. Mai târziu, în 2015, fostul Railo și-a oferit serviciile pentru a îmbunătăți performanța CFM și a redus resursele pentru o funcționalitate mai bună. Cea mai recentă actualizare a acesteia a fost lansată în 2020, care se anunță a fi continuată până în 2028.

## Format fișier CFM ##

Codul fișierelor și paginilor web CFM cuprinde în mare parte etichete precum HTML, dar cu o ușoară diferență. Aceste fișiere sunt responsabile pentru efectuarea diferitelor operațiuni pe care scripturile ColdFusion le permit să le ruleze.
* Aceste fișiere pot fi accesate și rulate direct atât pe Windows, cât și pe macOS, folosind browserul oricărui sistem de operare.
* Adobe ColdFusion oferă platforma pentru dezvoltarea paginilor web și a aplicațiilor dinamice pe PC.
* Orice editor de text precum NotePad sau orice alt editor de text dintr-un sistem de operare poate fi folosit pentru a deschide aceste fișiere, deoarece aceste fișiere sunt bazate pe text.
* Când orice fișier CFM este deschis într-un editor de text, acesta afișează cod care constă din etichete și scripturi pe care nu le-ar înțelege decât dacă este un dezvoltator web.

## Exemplu de utilizare CFM ##

Următoarele arată un exemplu de fișier CFM simplu de utilizare.

### Document CFM ###

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

## Referințe ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

