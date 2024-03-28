{
  "date" : "2019-10-11",
  "keywords" :["xml", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "limbaj de marcare extensibil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier XML",
  "description":"Aflați despre formatul de fișier XML și despre API-urile care pot crea și deschide fișiere XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier XML?

XML înseamnă Extensible Markup Language, care este similar cu **[HTML](/ro/web/html/)**, dar diferit în utilizarea etichetelor pentru definirea obiectelor. Întreaga idee din spatele creării formatului de fișier XML a fost de a stoca și transporta date fără a fi dependent de instrumente software sau hardware. Popularitatea sa se datorează faptului că este atât uman, cât și citibil de mașină. Acest lucru îi permite să creeze protocoale de date comune sub formă de obiecte care urmează să fie stocate și partajate în rețea, cum ar fi World Wide Web (WWW). „X” în XML este extensibil, ceea ce implică faptul că limbajul poate fi extins la orice număr de simboluri, conform cerințelor utilizatorului. Pentru aceste funcții, multe formate standard de fișiere îl folosesc, cum ar fi Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/ro/web/xhtml/)** și **[SVG](/ro/page-description-language/svg/)**.

## Format de fișier XML

Formatul de fișier XML se bazează pe XML Document Object Model (DOM), care este un API de programare pentru documente HTML și XML. XML DOM definește o metodă standard de accesare și manipulare a elementelor documentului XML. Face o vizualizare a structurii arborescente a unui document XML care poate fi folosit pentru a accesa toate elementele prin arborele DOM. Elementele existente pot fi modificate/șterse, precum și elemente noi pot fi create în arborele XML. Fiecare element al unui document XML este numit nod. XML DOM este așa cum se arată în imaginea următoare.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Abordarea universală a XML

Puterea XML îl face un limbaj universal pentru comunicarea datelor prin rețea, simplificând transportul de date și schimbările platformei. Acest lucru asigură, de asemenea, că schimbul de date între sisteme incompatibile este posibil prin stocarea datelor în format text simplu. HTML este pentru reprezentarea datelor pe web, în timp ce XML este pentru schimbul de date. Perechile de etichete de marcaj utilizate în interiorul XML definesc elementele cheie ale structurii care urmează să fie utilizate de aplicațiile de citire.

## Exemplu XML

Următorul este un exemplu simplificat de catalog de CD-uri în care fiecare înregistrare conține informații despre CD-uri, cum ar fi artistul, țara, compania, prețul și anul de producție.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referințe

* [XML - După Wikipedia](https://en.wikipedia.org/wiki/XML)

