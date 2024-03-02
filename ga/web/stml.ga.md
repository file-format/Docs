{
  "date": "2021-05-20",
  "keywords": [
"stml",
"comhad stml",
"formáid comhaid stml",
"cineál comhaid stml",
"comhad",
"cineál",
"Cad is comhad stml ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "STML - Comhad HTML SSI",
  "description": "Foghlaim faoi fhormáid comhaid STML agus APIanna ar féidir leo comhaid STML a chruthú agus a oscailt.",
  "linktitle": "STML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-stm-gal"
}
},
  "lastmod": "2021-05-20"
}

## Cad is comhad STML ann?

Is leathanach gréasáin é comhad le síneadh .stml le treoracha taobh an fhreastalaí a fhorghníomhaítear nuair a lódálann úsáideoir an leathanach sa bhrabhsálaí gréasáin. Tá taobh-chód freastalaí ar leathanaigh STML a chuimsíonn taobh an fhreastalaí chun tascanna a dhéanamh nach féidir a bhaint amach le HTML simplí. Cé go bhfuil sé cosúil le [HTML](/web/html/), cuireann STML níos mó cumhachta ar fáil trí na horduithe a rith ar an bhfreastalaí, ar a dtugtar Server Side Includes (SSI) freisin. Le tabhairt isteach na dteangacha ríomhchlárúcháin nua le scripteáil ar thaobh an fhreastalaí ar nós PHP, laghdaítear úsáid STML cé go dtacaíonn gach teicneolaíocht taobh an fhreastalaí leis go fóill. Is féidir comhaid STML a oscailt in aon eagarthóir téacs agus iad a chur in eagar chun na horduithe a nuashonrú.

## Formáid Chomhaid STML

Tá STML bunaithe ar ghnáthfhormáid comhaid téacs ascii atá inléite ag an duine. Mar sin féin, leanann sé an chomhréir mar atá sainmhínithe agus feidhmithe ag baint úsáide as an [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) a dhéantar ar thaobh an fhreastalaí. Cosúil le haon teanga scriptithe taobh freastalaí eile, is féidir le STML orduithe taobh an fhreastalaí a úsáid chun tascanna a dhéanamh ar nós cuntar cuairteoirí leathanach, féilire leathanaigh ghréasáin, taifid a aisghabháil ón mbunachar sonraí, agus cinn eile dá samhail.

## Sampla STML

Úsáidtear treoracha taobh an fhreastalaí in iarratais ar nós cuntar cuairteoirí leathanach nó féilire leathanaigh ghréasáin. Taispeánann an sampla seo a leanas na chéad cheithre cholún de na chéad trí líne de bhunachar sonraí na n-úsáideoirí.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Tagairtí

* [Áirítear Taobh an Fhreastalaí]( https://en.wikipedia.org/wiki/Server_Side_Includes)


