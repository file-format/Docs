{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om PYC-filformat och API:er som kan skapa och öppna PYC-filer.",
  "title" :"PYC-filformat - Python-kompilerad fil",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Vad är en PYC fil?

En PYC-fil är en kompilerad utdatafil som genereras från källkod skriven i Python-programmeringsspråket. När PY-filen körs med Python-tolken konverteras den till bytekod för exekvering. Samtidigt sparas den kompilerade bytekoden som .pyc-fil för att kunna återanvändas från cachen vid ett senare tillfälle om tillämpligt.

## Struktur för PYC-filformat

PYC-filer är i bytekod och deras filformatspecifikationer är inte tillgängliga offentligt. Undersökningar från vissa källor visar dock att [strukturen av en PYC-fil](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) består av:

* `En fyra-byte magisk numbe`r - Helt enkelt två byte som ändras med varje ändring av rangeringskoden, och sedan två byte av 0d0a.
* `En fyra-byte modifieringstidsstämpel` - Unix modifieringstidsstämpel för källfilen som genererade .pyc, så att den kan kompileras om om källkoden ändras.
* `A marshalled code object` - utdata från marshal.dump från kodobjektet som är ett resultat av kompileringen av källfilen.

## Referenser

* [Strukturen av .pyc-filer](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

