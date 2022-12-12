{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier AGI - Format de fișier pentru interfața Asterisk Gateway",
  "description":"Aflați despre ce este formatul de fișier AGI cu exemple și API-uri care pot crea și deschide fișiere AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Ce este un fișier AGI?

Un fișier AGI este un fișier script utilizat de sistemul de telefonie open source, Asterisk. Conține informații care pot fi utilizate pentru automatizarea proceselor și a planului de apel Asterisk. Folosind fișiere script AGI, se pot stabili conexiuni cu baze de date relaționale precum PostgreSQL sau MySQL. În plus, scripturile AGI pot fi folosite pentru a accesa și alte resurse externe. Scripturile AGI pot preda controlul asupra planului de apel către un script AGI extern, permițând lui Asterisk să efectueze sarcini complexe.

## Format de fișier AGI - Mai multe informații

Fișierele script AGI sunt salvate ca fișiere text și pot fi deschise în orice editor de text pentru a face modificări.

### Model standard de comunicare AGI

Scriptul AGI încarcă variabilele și valorile lor trimise de Asterisk. Un aspect comun al acestor variabile este următorul.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Aceste variabile sunt urmate de o linie goală trimisă de Asterisk, care arată că scriptul AGI poate prelua controlul asupra planului de apelare acum.

### Limbajul de programare pentru AGI Script Files

Scripturile AGI pot fi scrise de obicei în Perl, [PHP](/ro/programming/php/), [C](/ro/programming/c/), Pascal sau Bourne Shell.

## Referințe

* [Script Asterisk AGI](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

