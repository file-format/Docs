{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier FDF - Ce este un fișier FDF?",
  "description":"Aflați despre formatul de fișier FDF și despre API-urile care pot crea și deschide fișiere FDF.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier FDF?

Un fișier FDF (**Forms Data Format**) este un document text care este generat prin exportarea datelor din câmpurile de formular ale unui fișier [PDF](/ro/pdf/). Include doar datele câmpurilor de text care sunt extrase din câmpurile de formular disponibile într-un fișier PDF. Acest lucru are ca rezultat un fișier de date relativ mic, deoarece datele exportate nu conțin formularul în sine. Adobe Acrobat oferă caracteristica de export de date din câmpurile formularului utilizând opțiunea „Export Forms Data” din meniul aplicației.

## Format de fișier FDF - Mai multe informații

FDF este format text simplu și este inclus ca parte a [standardului ISO 32000](https://www.iso.org/standard/51502.html) pentru formatul de document portabil. A fost dezvoltat de Adobe pentru a permite importul și exportul de date din Acrobat Forms sau AcroForms.

Există două tipuri de fișiere FDF:

• `Classic FDF` – Oferă date pentru a completa un formular static existent.

• `Template FDF` – Construiește un nou PDF bazat pe șabloane din interiorul fișierelor PDF specificate. Formularele din noul document sunt completate prin furnizarea de date.

## Crearea FDF folosind Adobe Acrobat

[Setul de instrumente FDF](https://opensource.adobe.com/dc-acrobat-sdk-docs/) de la Adobe vă permite să creați fișiere FDF din date text.

## Referințe ##

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Resurse pentru dezvoltatori Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

