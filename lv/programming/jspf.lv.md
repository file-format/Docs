{
  "date": "2021-04-20",
  "keywords": [
"JSPF fails",
"jspf",
"JSPF piemērs",
"pagarinājumu",
"formātā",
"jspf apmācība",
"jsp fragments",
"JSPF faila formāts"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF — JSP fragmenta faila formāts",
  "description": "Uzziniet par JSPF faila formātu un API, kas var izveidot un atvērt JSPF failus.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-lvf"
}
},
  "lastmod": "2021-04-21"
}

## Kas ir JSPF fails?
Failu ar paplašinājumu .jspf sauc par JSP fragmentu; statisks fails, kas iekļauts citā JSP failā. JSPF faili netiek apkopoti atsevišķi, tomēr tie tiek apkopoti blakus lapai, kurā tie ir iekļauti. Tā sintakse ir līdzīga Java Server Pages (JSP) kodam. Tas satur tikai JSP fragmentu; nav iekļauts viss JSP dokuments.

## JSPF faila formāts
Tā vietā tiek izmantots termins JSP segments, jo JSP 2.0 specifikācijā termins JSP fragments ir pārslogots. JSP fragmenti var izmantot .jsp vai .jspf paplašinājumus, un tie ir jāievieto mapē **/WEB-INF/jspf** vai kopā ar pārējiem statiskajiem failiem. JSP fragmentiem, kas nav pilnīgas lapas, ir jāizmanto paplašinājums .jspf, un tie jāievieto mapē **/WEB-INF/jspf**

### JSP vai JSP fragmentu failu organizācija
JSP failā ir šādas sadaļas tādā secībā, kādā tās ir norādītas:

1. Atverot komentārus
2. JSP lapas direktīva(s)
3. Izvēles tagu bibliotēkas direktīva(s)
4. Izvēles JSP deklarācija(-as)
5. HTML un JSP kods

Gan JSP, gan JSPF fails sākas ar servera puses stila komentāru, ko sauc par **Opening Comment**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Šis komentārs var būt redzams tikai servera pusē, jo tas tiek noņemts JSP lapas renderēšanas laikā.

## Kad izmantot JSP fragmenta failu?
Ja JSP lapai ir nepieciešama noteikta, bet sarežģīta struktūra, kas var tikt atkārtoti izmantota arī citās JSP lapās, viens no veidiem, kā to rīkoties, ir sadalīt to gabalos, izmantojot Composite View modeli (Java Blueprints sadaļa Patterns). Piemēram, JSP lapas prezentācijas struktūrā dažreiz ir šāds loģiskais izkārtojums:

{{< figure src="../jspf.png" alt="JSPF faila formāts" >}}

Šādā situācijā šo salikto JSP lapu var pārvērst dažādos moduļos, katrs no tiem tiks saukts par atsevišķu JSP fragmentu. Pēc tam JSP fragmentus var ievietot atbilstošās vietās saliktajā JSP lapā. Tādējādi JSPF fails tiek izmantots, ja tiek izmantotas statiskās iekļaušanas direktīvas, lai iekļautu lapu, kas pati par sevi netiks izsaukta, faili ar paplašinājumu .jspf jāievieto tīmekļa lietojumprogrammu arhīva direktorijā /WEB-INF/jspf/ ( karš).

## JSPF piemērs
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Atsauces

 * [Koda konvencijas JavaServer lapām](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

