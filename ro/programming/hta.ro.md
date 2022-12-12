{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "fișier", "extensie", "format fișier", "implementare hta", "Ghid de programare", "exemplu hta", "aplicație HTML", "aplicație limbaj de marcare hipertext", "fișiere HTA", "Aplicație Microsoft HTML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - Fișiere de aplicație HTML",
  "description":"Aflați despre formatul de fișier HTA și despre API-urile care pot crea și deschide fișiere HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Ce este un fișier HTA?

HTMLA înseamnă **Hypertext Markup Language Application** este un program compatibil cu Microsoft Windows. Codul sursă al acestui program include mai mult de un limbaj de scripting, cum ar fi [HTML](/ro/web/html/) și [JavaScript](/ro/web/js/). Pentru interfața cu utilizatorul, se preferă o aplicație HTML, în timp ce pentru a îndeplini cerințele logicii programului se folosește orice alt limbaj de scripting.

O aplicație HTML este independentă de modelul de securitate al browserului de internet și rulează ca o aplicație de încredere. Extensia folosită pentru fișierele referitoare la aceste aplicații este HTA. Aceste aplicații includ caracteristici ale HTML împreună cu proprietățile altor limbaje de scripting.


## Scurt istoric ##

HTA a fost introdus pentru prima dată în 1999 de Microsoft împreună cu lansarea Internet Explorer 5. Era compatibil cu Internet Explorer și, prin urmare, putea fi executat numai pe sistemul de operare Windows. Această tehnologie a fost brevetată în 2003. Fișierele HTA sunt executate la fel ca orice alte fișiere .exe. Fișierele HTA sunt compatibile și cu versiunea actualizată de astăzi a Windows 11.


## Specificatii tehnice ##

HTA-urile au același format ca orice altă pagină HTML, în timp ce unele atribute sunt folosite pentru a controla stilurile de margini sau pictograme ale programelor. Mai mult, sunt oferite argumente pentru lansarea HTA. Aceste aplicații pot fi executate folosind un program numit mshta.exe. Poate fi accesat făcând dublu clic pe fișier. Aceste programe rulează automat împreună cu Internet Explorer. Pe lângă alte specificații, acestea nu sunt independente de browserul motorului Trident, ci sunt independente de Internet Explorer. Înseamnă că acestea pot fi executate fără a utiliza Internet Explorer.

Etichetele sunt folosite de dragul personalizării aspectului acestor aplicații. Conversia din aplicația Microsoft HTML în format HTA este mai ușoară, adică trebuie doar să schimbați extensia. După cum știm că aceste aplicații sunt deplină de încredere, astfel încât acestea cuprind mai multe caracteristici și avantaje în comparație cu fișierele HTML simple. Editorii de text pot fi utilizați pentru a crea HTA. Acești editori pot fi achiziționați de Microsoft sau de orice altă sursă de încredere.


## Exemplu de format de fișier HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Referință ##

* [HTA - de la Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



