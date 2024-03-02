{
  "date": "2021-04-20",
  "keywords": [
"Comhad JSPF",
"jspf",
"Sampla JSPF",
"síneadh",
"formáid",
"Teagaisc jspf",
"blúire jsp",
"Formáid comhaid JSPF"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF - JSP Formáid Chomhaid Fragment",
  "description": "Foghlaim faoi fhormáid comhaid JSPF agus APIanna ar féidir leo comhaid JSPF a chruthú agus a oscailt.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-gaf"
}
},
  "lastmod": "2021-04-21"
}

## Cad is comhad JSPF ann?
Tugtar blúire JSP ar an gcomhad le síneadh .jspf; comhad statach atá san áireamh i gcomhad JSP eile. Ní chuirtear na comhaid JSPF le chéile ina n-aonar, áfach, tiomsaítear iad taobh leis an leathanach inar chuimsigh siad. Tá a chomhréir cosúil leis an gcód Leathanaigh Freastalaí Java (JSP). Níl ann ach blúire de JSP; gan doiciméad iomlán an JSP a áireamh.

## Formáid comhaid JSPF
Úsáidtear an téarma deighleog JSP ina ionad sin toisc go bhfuil an téarma bloighean JSP ró-ualaithe i Sonraíocht JSP 2.0. Is féidir leis na blúirí JSP síntí .jsp nó .jspf a úsáid agus ba chóir iad a chur in **/WEB-INF/jspf** nó leis an gcuid eile de na comhaid statacha. Caithfidh na blúirí JSP nach leathanaigh iomlána iad an iarmhír .jspf a úsáid agus iad a chur in **/WEB-INF/jspf**

### JSP nó JSP Eagraíocht Comhad Fragment
Tá na hailt seo a leanas i gcomhad JSP san ord ina bhfuil siad liostaithe:

1. Tráchtanna a oscailt
2. Treoir(eanna) leathanach JSP
3. Treoir(eanna) roghnacha leabharlainne clibeanna
4. Dearbhú/dearbhuithe roghnacha JSP
5. Cód HTML agus JSP

Tosaíonn comhad JSP nó JSPF araon le trácht ar stíl an fhreastalaí ar a dtugtar **Trácht Tosaigh**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Ní féidir an nóta tráchta seo a fheiceáil ach ar thaobh an fhreastalaí toisc go mbaintear é le linn rindreáil leathanaigh JSP.

## Cathain is ceart comhad Fragment JSP a úsáid?
Nuair a éilíonn leathanach JSP struchtúr áirithe ach casta a d’fhéadfaí a athúsáid ar leathanaigh eile de chuid JSP freisin, bealach amháin chun é seo a láimhseáil ná é a bhriseadh ina phíosaí, ag baint úsáide as an patrún Composite View (an chuid Patrúin de Java Blueprints). Mar shampla, uaireanta bíonn an leagan amach loighciúil seo a leanas ag leathanach JSP ina struchtúr léirithe:

{{< figure src="../jspf.png" alt="Formáid Comhaid JSPF" >}}

Sa chás seo, is féidir an leathanach ilchodach JSP seo a thiontú ina modúil éagsúla, tabharfar blúire JSP ar leith ar gach ceann díobh. Is féidir na blúirí JSP a chur ansin in áiteanna cuí ar an leathanach ilchodach JSP. Mar sin, baintear úsáid as an gcomhad JSPF nuair a úsáidtear treoracha áirithinte statacha chun leathanach a chur san áireamh nach nglaofar air féin, ba cheart na comhaid leis an iarmhír .jspf a chur san eolaire /WEB-INF/jspf/ i gcartlann feidhmchlár Gréasáin ( cogadh).

## Sampla JSPF
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

## Tagairtí

 * [Coinbhinsiúin an Chóid do na Leathanaigh JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

