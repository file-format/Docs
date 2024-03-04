{
  "date": "2019-10-11",
  "keywords": [
"dhtml",
"dhtml failą",
"dhtml failo formatas",
"dhtml failo tipas",
"failą",
"tipo",
"kas yra dhtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DHTML – dinaminis HTML failo formatas",
  "description": "Sužinokite apie DHTML failo formatą ir API, kurios gali kurti ir atidaryti DHTML failus.",
  "linktitle": "DHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dhtm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DHTML failas?

Failas su plėtiniu .dhtml yra dinaminis [HTML](/web/html/) failas, naudojamas kuriant dinaminį tinklalapio turinį. DHTML sukurtas žiniatinklio elementas yra pagrįstas įvykiais ir jo nereikia įkelti iš naujo. Daugeliu atvejų DHTML failas naudojamas kuriant dinaminį tinklalapio turinį, pvz., išskleidžiamuosius meniu, slankiuosius sluoksnius, užvedimo mygtukus ir kitą dinaminį turinį. Beveik kasdien susiduriate su dinaminiais HTML elementais, kai užvedate pelės žymeklį ant meniu elemento ir atidaromos kitos submeniu parinktys. DHTML naudoja žiniatinklio technologijas, tokias kaip [HTML](/web/html/), [Javascript](/web/js/), HTML DOM, HTML įvykiai ir [CSS](/web/css/), kad pasiektų dinamišką elementų elgesį.

## DHTML failo formatas

DHTML failai yra paprasto teksto failai, kuriuose yra DHTML kodas, skirtas dinaminei žiniatinklio elementų veikimui įgyvendinti.


### DHTML DOM

DHTML dokumento objekto modelis (DOM) yra pagrįstas HTML DOM, kuris yra medžio struktūra su elementais, atributais ir tekstu, kaip parodyta kitame paveikslėlyje.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Dokumento mazgas gali būti naudojamas kelioms funkcijoms iškviesti, kad būtų galima įgyvendinti skirtingas funkcijas. Šiame pavyzdyje tiesiog naudojamas JavaScript metodas document.write() DHTML.

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

Šis kodas įrašo tekstą Hello World, kad išvestų naršyklėje.

### DHTML įvykiai

|S.Nr.|Įvykis|Įvykis|
---|---|---|
|1|nabort|Tai atsitinka, kai vartotojas nutraukia puslapio arba medijos failo įkėlimą.|
|2|onblur|Tai atsitinka, kai vartotojas palieka HTML objektą.|
|3|onchange|Tai atsitinka, kai vartotojas pakeičia arba atnaujina objekto reikšmę.|
|4|onclick|Jis atsiranda arba suaktyvinamas, kai bet kuris vartotojas spusteli HTML elementą.|
|5|ondblclick|Tai atsitinka, kai vartotojas du kartus kartu spusteli HTML elementą.|
|6|onfocus|Tai atsitinka, kai vartotojas sutelkia dėmesį į HTML elementą. Ši įvykių tvarkytoja veikia priešingai nei onblur.|
|7|onkeydown|Jis suveikia, kai vartotojas paspaudžia klaviatūros įrenginio klavišą. Ši įvykių tvarkyklė veikia visiems raktams.|
|8|onkeypress|Jis suveikia, kai vartotojai paspaudžia klaviatūros klavišą. Ši įvykių tvarkyklė suaktyvinama ne visiems raktams.|
|9|onkeyup|Tai atsitinka, kai vartotojas atleido klavišą nuo klaviatūros paspaudęs objektą ar elementą.|
|10|įkelti|Tai atsitinka, kai objektas yra visiškai įkeltas.|
|11|onmousedown|Tai atsitinka, kai vartotojas paspaudžia pelės mygtuką virš HTML elemento.|
|12|onmousemove|Tai atsitinka, kai vartotojas perkelia žymeklį ant HTML objekto.|
|13|onmouseover|Tai atsitinka, kai vartotojas perkelia žymeklį ant HTML objekto.|
|14|onmouseout|Jis atsiranda arba suveikia, kai pelės žymeklis perkeliamas iš HTML elemento.|
|15|onmouseup|Jis atsiranda arba suveikia, kai pelės mygtukas atleidžiamas virš HTML elemento.|
|16|onreset|Naudotojas naudoja formą iš naujo nustatyti.|
|17|onselect|Tai įvyksta pasirinkus turinį arba tekstą tinklalapyje.|
|18|onsubmit|Jis suaktyvinamas, kai vartotojas spusteli mygtuką po formos pateikimo.|
|19|onunload|Jis suaktyvinamas, kai vartotojas uždaro tinklalapį.|

## Nuorodos

* [Dinaminis HTML – Vikipedija](https://en.wikipedia.org/wiki/Dynamic_HTML)


