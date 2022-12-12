{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Fișier șablon de raport Elixir",
  "description":"Aflați despre fișierul RML și API-urile care pot crea și deschide fișiere RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Ce este un fișier RML?

Un fișier RML este un fișier șablon de raportare cu motorul de raportare [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Fișierul șablon este utilizat pentru a genera rapoarte cu sursa de date conectată la sistemul de fișiere Elixir. Datele sunt citite și populate în fișierul șablon RML și pot fi exportate într-un număr de formate diferite de fișiere, cum ar fi [PDF](/ro/pdf/), [RTF](/ro/word-processing/rtf/) și foaia de calcul [XLS] (/ro/spreadsheet/xls/). Motorul de raportare Elixir Repertoire poate fi conectat la o mare varietate de surse de date JDBC.

## Format de fișier RML

Detaliile interne ale structurii fișierelor din formatul fișierului RML nu sunt disponibile public. Fișierele sunt generate și salvate intern de aplicația Elixir Repertoire pentru a genera rapoarte cu date populate din sursele de date conectate. Fișierul șablon RML conține informații despre aspectul general și substituenți ale raportului final care urmează să fie generat din date.

## Cum să fișierul șablon RML?

Pentru a genera șablon RML în Elixir Repertoire, pot fi urmați pașii următori.

1. Conectați o sursă de date JDBC la sistemul de fișiere.
1. Lansați expertul pentru șabloane de raport
1. Utilizați software-ul pentru a localiza fișierul sursa de date .ds
1. Alegeți raportul tabelar ca opțiune de export
1. Selectați câmpurile care vor fi incluse în șablonul de raport
1. În cele din urmă, făcând clic pe butonul Finish, First report.rml este adăugat la depozit și deschis pentru a afișa fila Layout.

## Referințe

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)

