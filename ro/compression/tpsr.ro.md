{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier TPSR - Fișier raport al sesiunii pilot TeamViewer",
  "description":"Aflați despre formatul de fișier TPSR și despre API-urile care pot crea și deschide fișiere TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Ce este un fișier TPSR?

Un TPSR este un fișier de protocol de conexiune utilizat de TeamViewer Assist AR (cunoscut anterior ca TeamViewer Pilot). Informațiile stocate într-un fișier TPSR sunt stocate în format de fișier comprimat [ZIP](/ro/compression/zip/). TPSR conține istoricul detaliat al conexiunii TeamViewer între un expert și un tehnician pentru rezolvarea problemei și scopul revizuirii. Informațiile conținute într-un fișier TPSR includ tipul dispozitivului, numele, ID-ul Assist AR, ID-ul expert, data și ora și durata conexiunii. Aceste date sunt stocate într-un fișier [JSON](/ro/web/json/) în interiorul arhivei TPSR comprimate.

## Format de fișier TPSR

Un fișier TPSR este stocat pe disc în format de fișier arhivă ZIP, unde conținutul este stocat într-un fișier JSON. Este generat automat după finalizarea conexiunii Assist AR, cu condiția ca opțiunea de raportare a conexiunii să fie activată în TeamViewer.

TeamViewer Assist AR permite experților să se conecteze la tehnicieni pentru a obține flux LIVE de la distanță prin intermediul camerei mobile. Aceștia pot ajuta tehnicienii să rezolve problema prin telefon.

## Deschideți fișierele TPSR

Puteți deschide fișiere TPSR utilizând versiunea desktop a software-ului TeamViewer. Dacă este instalat pe computer, făcând dublu clic pe fișierul TPSR, îl va deschide în software-ul TeamViewer. Fișierele TPSR pot fi exportate și în fișiere [PDF](/ro/pdf/) sau pot fi tipărite pentru a avea o copie tipărită a fișierului de protocol.

## Referințe ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

