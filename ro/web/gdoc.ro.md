{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC File – Google Docs Shortcut",
  "description":"Aflați despre ce este un fișier GDOC și API-urile care pot crea și deschide fișiere GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Ce este un fișier GDOC?

Un fișier GDOC este un fișier de comandă rapidă care indică un fișier aflat pe Google Drive, un serviciu de stocare a documentelor bazat pe cloud. Când clientul Google Drive este instalat pe un computer și un document este creat în interiorul acestuia, unitatea creează un document în stocarea online în cloud și scrie [URL](/ro/web/url/) a acestui document în fișierul GDOC din Google local. Dosarul Drive. Când se face dublu clic pe acest fișier de comandă rapidă, browserul web implicit deschide documentul din locația [URL](/ro/web/url/). Dacă acest fișier de comandă rapidă este mutat din acest dosar, legătura către documentul online este întreruptă.

## Format de fișier GDOC - Mai multe informații

Fișierul GDOC conține o comandă rapidă la documentul online scris în format de fișier [JSON](/ro/web/json/). Browserul care deschide fișierele GDOC citește informațiile URL și deschide documentul legat pentru afișare, cu condiția ca utilizatorul să fie conectat la acest cont Google în care este stocat documentul. Fișierele GDOC nu conțin conținutul documentului.

### Exemplu de fișier GDOC

Fișierul GDOC poate fi deschis într-un editor de text, iar conținutul acestuia arată ca următorul.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

După cum se poate vedea, conținutul este formatat în JSON având adresa URL a documentului și ID-ul documentului asociat.

## Referințe

* [Google Docs nu deschide nici fișierele gdoc, nici docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=ro )

