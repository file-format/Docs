{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier EGG - Fișier de distribuție Python",
  "description":"Aflați despre formatul de fișier EGG și despre API-urile care pot crea și deschide fișiere EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Ce este un fișier EGG?

Un fișier EGG, cunoscut și sub numele de ouă Python, este un format de distribuție mai vechi al distribuțiilor Python. Este o arhivă [ZIP](/ro/compression/zip/) comprimată cu extensia .egg și conține fișierele sursă ale aplicației Python împreună cu metainformații despre distribuție. Fișierele EGG sunt alternative la fișierul Windows Executable [EXE](/ro/executable/exe/), dar sunt multiplatforme. Acest format mai vechi pentru distribuțiile Python a fost înlocuit cu noul format de fișier Wheel (WHL) la începutul lui 2010.

## Format de fișier EGG

Fișierele EGG sunt salvate ca arhive ZIP comprimate. Înseamnă că dacă înlocuiți extensia .egg cu .zip, o veți putea deschide cu utilitare standard de decompresie, cum ar fi Corel WinZIP, Microsoft Explorer sau RARLAB WinRAR.

Fișierele EGG pot fi create folosind pachetul **distutils** disponibil de Python. Un alt instrument care poate crea și deschide fișiere EGG este **SetupTools**. Fișierele EGG pot fi instalate ca pachet folosind **easy_install**.

`NOTĂ - Formatul de fișier EGG a fost depășit în favoarea noului format de fișier WHL pentru roată.`

## Referință ##

* [OUĂ Python](https://python101.pythonlibrary.org/chapter38_eggs.html)

