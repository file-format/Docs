{
  "date": "2021-05-20",
  "keywords": [
"shtml",
"comhad shtml",
"Formáid comhaid shtml",
"cineál comhaid shtml",
"comhad",
"cineál",
"Cad is comhad shtml ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHTML - Taobh Freastalaí Cuir Comhad HTML san áireamh",
  "description": "Foghlaim faoi fhormáid comhaid SHTML agus APIs ar féidir leo comhaid SHTML a chruthú agus a oscailt.",
  "linktitle": "SHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-shtm-gal"
}
},
  "lastmod": "2021-05-20"
}

## Cad is comhad SHTML ann?

Is leathanach gréasáin é comhad a bhfuil iarmhír .shtml air atá scríofa in [HTML](/web/html/) agus a chuimsíonn treoracha freastalaí. D’fhéadfadh go mbeadh áirimh ar thaobh an fhreastalaí ann freisin atá cosúil le comhaid ASP le haghaidh luchtú níos tapúla. Is féidir cód inrite a bheith sna comhaid taobh freastalaí freisin a fhéadann an freastalaí a luchtú níos moille ná mar is gnách. Tá comhaid SHTML cosúil le HTML ach ceadaíonn siad freisin úsáid a bhaint as orduithe freastalaí simplí. Déantar na horduithe freastalaí seo i dteanga ríomhchláraithe shimplí ar a dtugtar Server Side Includes (SSI). Tá teangacha ríomhchláraithe taobh an fhreastalaí mar [PHP](/programming/php/) curtha in ionad SHTML den chuid is mó.

## Formáid Chomhaid SHTML

Scríobhtar comhaid SHTML i ngnáth-théacs agus úsáideann siad an [SSI commands](https://www.w3.org/Jigsaw/Doc/User/SSI.html) a dhéantar ar thaobh an fhreastalaí. Is féidir na horduithe seo ó thaobh an fhreastalaí a úsáid chun fiú nascadh leis an mbunachar sonraí trí úsáid a bhaint as tiománaithe an bhunachair shonraí agus chun sonraí úsáideoirí a fháil ó tháblaí.

## Sampla SHTML

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


