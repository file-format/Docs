{
  "date": "2021-04-20",
  "keywords": [
"JSPF failą",
"jspf",
"JSPF pavyzdys",
"pratęsimas",
"formatu",
"jspf pamoka",
"jsp fragmentas",
"JSPF failo formatas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF – JSP fragmento failo formatas",
  "description": "Sužinokite apie JSPF failo formatą ir API, kurios gali kurti ir atidaryti JSPF failus.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-ltf"
}
},
  "lastmod": "2021-04-21"
}

## Kas yra JSPF failas?
Failas su plėtiniu .jspf vadinamas JSP fragmentu; statinis failas, įtrauktas į kitą JSP failą. JSPF failai nėra sudaryti atskirai, tačiau jie sudaromi šalia puslapio, kuriame jie buvo įtraukti. Jo sintaksė panaši į Java Server Pages (JSP) kodą. Jame yra tik JSP fragmentas; neįtrauktas visas JSP dokumentas.

## JSPF failo formatas
Vietoj to vartojamas terminas JSP segmentas, nes terminas JSP fragmentas yra perkrautas JSP 2.0 specifikacijoje. JSP fragmentai gali naudoti .jsp arba .jspf plėtinius ir turi būti dedami į **/WEB-INF/jspf** arba kartu su likusiais statiniais failais. JSP fragmentai, kurie nėra baigti puslapiai, turi naudoti .jspf plėtinį ir turi būti dedami į **/WEB-INF/jspf**

### JSP arba JSP fragmentų failų organizavimas
JSP faile yra šie skyriai tokia tvarka, kokia jie yra:

1. Komentarų atidarymas
2. JSP puslapio direktyva (-os)
3. Pasirenkama (-os) žymų bibliotekos direktyva (-os)
4. Neprivaloma (-os) JSP deklaracija (-os)
5. HTML ir JSP kodas

JSP arba JSPF failas prasideda serverio pusės stiliaus komentaru, kuris vadinamas **Atidarymo komentaru**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Šis komentaras gali būti matomas tik serverio pusėje, nes jis pašalinamas JSP puslapio atvaizdavimo metu.

## Kada naudoti JSP fragmento failą?
Kai JSP puslapiui reikalinga tam tikra, bet sudėtinga struktūra, kuri taip pat gali būti pakartotinai naudojama kituose JSP puslapiuose, vienas iš būdų tai padaryti yra suskaidyti jį į dalis, naudojant sudėtinio rodinio šabloną (Java Blueprints skyrių Šablonai). Pavyzdžiui, JSP puslapio pateikimo struktūroje kartais yra toks loginis išdėstymas:

{{< figure src="../jspf.png" alt="JSPF failo formatas" >}}

Esant tokiai situacijai, šis sudėtinis JSP puslapis gali būti konvertuojamas į įvairius modulius, kurių kiekvienas bus vadinamas atskiru JSP fragmentu. Tada JSP fragmentai gali būti dedami į atitinkamas sudėtinio JSP puslapio vietas. Taigi JSPF failas naudojamas, kai naudojamos statinės įtraukimo direktyvos, kad būtų įtrauktas puslapis, kuris pats nebūtų iškviestas, failai su plėtiniu .jspf turi būti patalpinti žiniatinklio programų archyvo /WEB-INF/jspf/ kataloge ( karas).

## JSPF pavyzdys
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

## Nuorodos

 * [Kodo konvencijos, skirtos JavaServer puslapiams](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

