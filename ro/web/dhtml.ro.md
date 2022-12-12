{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","fișier dhtml", "format fișier dhtml", "tip fișier dhtml", "fișier", "tip", "ce este un fișier dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML – Format de fișier HTML dinamic",
  "description":"Aflați despre formatul de fișier DHTML și despre API-urile care pot crea și deschide fișiere DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DHTML?

Un fișier cu extensia .dhtml este un fișier dinamic [HTML](/ro/web/html/) care este utilizat pentru a crea conținut dinamic al unei pagini web. Un element web creat în DHTML este determinat de evenimente și nu necesită reîncărcarea paginii. În majoritatea cazurilor, un fișier DHTML este utilizat pentru a crea conținutul dinamic al unei pagini web, cum ar fi meniuri derulante, straturi plutitoare, butoane de rulare și alt conținut dinamic. Întâlnești elemente html dinamice aproape zilnic în viața ta atunci când treci cu mouse-ul pe un element de meniu și se deschide alte opțiuni de submeniu. DHTML folosește tehnologii web precum [HTML](/ro/web/html/), [Javascript](/ro/web/js/), HTML DOM, HTML Events și [CSS](/ro/web/css/) pentru a obține dinamica comportamentul elementelor.

## Format de fișier DHTML

Fișierele DHTML sunt fișiere text simplu care conțin cod DHTML pentru a implementa comportamentul dinamic al elementelor web.


### DHTML DOM

Modelul de obiect de document DHTML (DOM) se bazează pe DOM HTML care este o structură arborescentă cu elemente, atribute și text, așa cum se arată în imaginea următoare.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Nodul „Document” poate fi folosit pentru a apela mai multe funcții pentru a implementa diferite funcționalități. Următorul exemplu folosește pur și simplu metoda document.write() a JavaScript în DHTML.

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

Acest cod scrie textul „Hello World” pentru a fi afișat în browser.

### Evenimente DHTML

|S.Nr.|Eveniment|Aparitie|
---|---|---|
|1|onabort|Apare atunci când utilizatorul renunță la încărcarea paginii sau a fișierului media.|
|2|onblur|Apare atunci când utilizatorul părăsește un obiect HTML.|
|3|onchange|Apare atunci când utilizatorul modifică sau actualizează valoarea unui obiect.|
|4|onclick|Apare sau se declanșează atunci când orice utilizator face clic pe un element HTML.|
|5|ondblclick|Apare atunci când utilizatorul face clic pe un element HTML de două ori împreună.|
|6|onfocus|Apare atunci când utilizatorul se concentrează pe un element HTML. Acest handler de evenimente funcționează opus cu onblur.|
|7|onkeydown|Se declanșează atunci când un utilizator apasă o tastă de pe un dispozitiv cu tastatură. Acest handler de evenimente funcționează pentru toate cheile.|
|8|onkeypress|Se declanșează atunci când utilizatorii apasă o tastă de pe o tastatură. Acest handler de evenimente nu este declanșat pentru toate cheile.|
|9|onkeyup|Apare atunci când un utilizator a eliberat o tastă de pe o tastatură după ce a apăsat pe un obiect sau element.|
|10|onload|Apare atunci când un obiect este complet încărcat.|
|11|onmousedown|Apare atunci când un utilizator apasă butonul mouse-ului peste un element HTML.|
|12|onmousemove|Apare atunci când un utilizator mută cursorul pe un obiect HTML.|
|13|onmouseover|Apare atunci când un utilizator mută cursorul peste un obiect HTML.|
|14|onmouseout|Apare sau se declanșează atunci când indicatorul mouse-ului este mutat dintr-un element HTML.|
|15|onmouseup|Apare sau se declanșează atunci când butonul mouse-ului este eliberat peste un element HTML.|
|16|onreset|Este folosit de utilizator pentru a reseta formularul.|
|17|onselect|Apare după selectarea conținutului sau textului pe o pagină web.|
|18|onsubmit|Se declanșează atunci când utilizatorul face clic pe un buton după trimiterea unui formular.|
|19|onunload|Se declanșează atunci când utilizatorul închide o pagină web.|

## Referințe

* [HTML dinamic - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

