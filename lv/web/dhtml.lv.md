{
  "date": "2019-10-11",
  "keywords": [
"dhtml",
"dhtml failu",
"dhtml faila formātā",
"dhtml faila tips",
"failu",
"veids",
"kas ir dhtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DHTML - dinamisks HTML faila formāts",
  "description": "Uzziniet par DHTML faila formātu un API, kas var izveidot un atvērt DHTML failus.",
  "linktitle": "DHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dhtm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DHTML fails?

Fails ar .dhtml paplašinājumu ir dinamisks [HTML](/web/html/) fails, ko izmanto, lai izveidotu tīmekļa lapas dinamisku saturu. Tīmekļa elements, kas izveidots DHTML, ir balstīts uz notikumu, un tam nav nepieciešams atkārtoti ielādēt lapu. Vairumā gadījumu DHTML fails tiek izmantots, lai izveidotu tīmekļa lapas dinamisku saturu, piemēram, nolaižamās izvēlnes, peldošos slāņus, apgāšanās pogas un citu dinamisku saturu. Jūs gandrīz katru dienu saskaraties ar dinamiskiem html elementiem, kad novietojat peles kursoru uz izvēlnes vienuma, un tas atver papildu apakšizvēlnes opcijas. Lai panāktu elementu dinamisku darbību, DHTML izmanto tādas tīmekļa tehnoloģijas kā [HTML](/web/html/), [Javascript](/web/js/), HTML DOM, HTML Events un [CSS](/web/css/).

## DHTML faila formāts

DHTML faili ir vienkārša teksta faili, kas satur DHTML kodu, lai īstenotu tīmekļa elementu dinamisko darbību.


### DHTML DOM

DHTML dokumenta objekta modelis (DOM) ir balstīts uz HTML DOM, kas ir koka struktūra ar elementiem, atribūtiem un tekstu, kā parādīts nākamajā attēlā.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Mezglu Dokuments var izmantot, lai izsauktu vairākas funkcijas, lai ieviestu dažādas funkcionalitātes. Nākamajā piemērā vienkārši tiek izmantota JavaScript metode document.write() DHTML.

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

Šis kods ieraksta tekstu Hello World, lai izvadītu pārlūkprogrammā.

### DHTML notikumi

|S.Nr.|Notikums|Notikums|
---|---|---|
|1|pārtraukt|Tas notiek, kad lietotājs pārtrauc lapas vai multivides faila ielādi.|
|2|onblur|Tas notiek, kad lietotājs atstāj HTML objektu.|
|3|onchange|Tas notiek, kad lietotājs maina vai atjaunina objekta vērtību.|
|4|onclick|Tas notiek vai tiek aktivizēts, kad kāds lietotājs noklikšķina uz HTML elementa.|
|5|ondblclick|Tas notiek, kad lietotājs divas reizes kopā noklikšķina uz HTML elementa.|
|6|onfocus|Tas notiek, kad lietotājs koncentrējas uz HTML elementu. Šis notikumu apstrādātājs darbojas pretēji onblur.|
|7|onkeydown|Tas tiek aktivizēts, kad lietotājs nospiež taustiņu uz tastatūras ierīces. Šis notikumu apstrādātājs darbojas ar visām atslēgām.|
|8|onkeypress|Tas tiek aktivizēts, kad lietotāji nospiež kādu tastatūras taustiņu. Šis notikumu apdarinātājs netiek aktivizēts visām atslēgām.|
|9|onkeyup|Tas notiek, kad lietotājs pēc objekta vai elementa nospiešanas atlaiž taustiņu no tastatūras.|
|10|ielādēt|Tas notiek, kad objekts ir pilnībā ielādēts.|
|11|onmousedown|Tas notiek, kad lietotājs nospiež peles pogu virs HTML elementa.|
|12|onmousemove|Tas notiek, kad lietotājs pārvieto kursoru uz HTML objekta.|
|13|onmouseover|Tas notiek, kad lietotājs pārvieto kursoru virs HTML objekta.|
|14|onmouseout|Tas notiek vai tiek aktivizēts, kad peles rādītājs tiek pārvietots no HTML elementa.|
|15|onmouseup|Tas notiek vai tiek aktivizēts, kad peles poga tiek atlaista virs HTML elementa.|
|16|onreset|Lietotājs to izmanto, lai atiestatītu veidlapu.|
|17|onselect|Tas notiek pēc satura vai teksta atlases tīmekļa lapā.|
|18|onsubmit|Tas tiek aktivizēts, kad lietotājs noklikšķina uz pogas pēc veidlapas iesniegšanas.|
|19|onunload|Tas tiek aktivizēts, kad lietotājs aizver tīmekļa lapu.|

## Atsauces

* [Dinamiskais HTML — Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)


