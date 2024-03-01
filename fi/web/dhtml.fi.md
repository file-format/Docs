{
  "date": "2019-10-11",
  "keywords": [
"dhtml",
"dhtml-tiedosto",
"dhtml-tiedostomuoto",
"dhtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on dhtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DHTML - Dynaaminen HTML-tiedostomuoto",
  "description": "Opi DHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DHTML-tiedostoja.",
  "linktitle": "DHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dhtm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DHTML-tiedosto?

Tiedosto, jonka pääte on .dhtml, on dynaaminen [HTML](/web/html/)-tiedosto, jota käytetään verkkosivun dynaamisen sisällön luomiseen. DHTML:llä luotu verkkoelementti on tapahtumaohjattu, eikä sitä tarvitse ladata uudelleen. Useimmissa tapauksissa DHTML-tiedostoa käytetään luomaan verkkosivun dynaaminen sisältö, kuten avattavat valikot, kelluvat tasot, vierityspainikkeet ja muu dynaaminen sisältö. Tulet kohtaamaan dynaamisia html-elementtejä melkein päivittäin elämässäsi, kun siirrät hiiren valikkokohdan päälle ja se avaa muita alivalikon vaihtoehtoja. DHTML hyödyntää verkkoteknologioita, kuten [HTML](/web/html/), [Javascript](/web/js/), HTML DOM, HTML Events ja [CSS](/web/css/) elementtien dynaamisen toiminnan saavuttamiseksi.

## DHTML tiedostomuoto

DHTML-tiedostot ovat pelkkiä tekstitiedostoja, jotka sisältävät DHTML-koodia web-elementtien dynaamisen toiminnan toteuttamiseksi.


### DHTML DOM

DHTML Document Object Model (DOM) perustuu HTML DOM:iin, joka on puurakenne, jossa on elementtejä, attribuutteja ja tekstiä seuraavan kuvan mukaisesti.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Document-solmulla voidaan kutsua useita toimintoja erilaisten toimintojen toteuttamiseksi. Seuraava esimerkki käyttää yksinkertaisesti JavaScriptin document.write()-menetelmää DHTML:ssä.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Tämä koodi kirjoittaa tekstin Hello World tulostettavaksi selaimeen.

### DHTML-tapahtumat

|S.No.|Tapahtuma|Tapahtuma|
---|---|---|
|1|onbort|Tapahtuu, kun käyttäjä keskeyttää sivun tai mediatiedoston latauksen.|
|2|onblur|Tämä tapahtuu, kun käyttäjä jättää HTML-objektin.|
|3|onchange|Tämä tapahtuu, kun käyttäjä muuttaa tai päivittää objektin arvoa.|
|4|onclick|Se tapahtuu tai laukeaa, kun joku käyttäjä napsauttaa HTML-elementtiä.|
|5|ondblclick|Tämä tapahtuu, kun käyttäjä napsauttaa HTML-elementtiä kaksi kertaa yhdessä.|
|6|onfocus|Näin tapahtuu, kun käyttäjä keskittyy HTML-elementtiin. Tämä tapahtumakäsittelijä toimii päinvastoin kuin onblur.|
|7|onkeydown|Se laukeaa, kun käyttäjä painaa näppäimistön näppäintä. Tämä tapahtumakäsittelijä toimii kaikille avaimille.|
|8|onkeypress|Se laukeaa, kun käyttäjät painavat näppäimistön näppäintä. Tämä tapahtumakäsittelijä ei laukea kaikille avaimille.|
|9|onkeyup|Näin tapahtuu, kun käyttäjä vapautti näppäimen näppäimistöstä, kun hän on painanut objektia tai elementtiä.|
|10|lataa|Se tapahtuu, kun objekti on ladattu kokonaan.|
|11|onmousedown|Tämä tapahtuu, kun käyttäjä painaa hiiren painiketta HTML-elementin päällä.|
|12|onmousemove|Näin tapahtuu, kun käyttäjä siirtää kohdistimen HTML-objektin päälle.|
|13|onmouseover|Tämä tapahtuu, kun käyttäjä siirtää kohdistimen HTML-objektin päälle.|
|14|onmouseout|Se tapahtuu tai laukeaa, kun hiiren osoitin siirretään pois HTML-elementistä.|
|15|onmouseup|Se tapahtuu tai laukeaa, kun hiiren painike vapautetaan HTML-elementin päällä.|
|16|onreset|Käyttäjä käyttää sitä lomakkeen nollaukseen.|
|17|onselect|Se tapahtuu sen jälkeen, kun Web-sivun sisältö tai teksti on valittu.|
|18|onsubmit|Se käynnistyy, kun käyttäjä napsauttaa painiketta lomakkeen lähettämisen jälkeen.|
|19|onunload|Se käynnistyy, kun käyttäjä sulkee verkkosivun.|

## Viitteet

* [Dynaaminen HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)


