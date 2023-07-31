{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier P7S - Mesaj de e-mail semnat digital",
  "description":"Aflați despre formatul de fișier P7S și despre API-urile care pot crea și deschide fișiere P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Ce este un fișier P7S?

Un fișier P7S este o semnătură digitală care este primită cu un e-mail semnat digital. Prezența acestui fișier ca atașament la e-mail verifică că e-mailul este trimis dintr-o sursă autentică. Acest lucru asigură că expeditorul are un certificat de semnare e-mail instalat pe computerul său. Atunci când un astfel de e-mail semnat este trimis de pe computerul utilizatorului, este atașat fișierul P7S care conține numele expeditorului. Clienții de e-mail care acceptă e-mailuri semnate pot vedea informațiile expeditorului.

## Format de fișier P7S - Mai multe informații

Fișierele P7S S/MIME (Secure/Multipurpose Internet Mail Extensions) conțin informații în format text simplu, care pot fi citite de om. Clienții de e-mail, cum ar fi Microsoft Outlook, Apple Mail și Mozilla Thunderbird, acceptă citirea informațiilor semnate digital dintr-un e-mail S/MIME. Semnarea unui e-mail verifică identitatea expeditorului și îi spune destinatarului că mesajul este autentic. Când e-mailurile sunt descărcate de la clienții de e-mail (fie ca [EML](/ro/email/eml/) sau [MSG](/ro/email/msg/)), aceste fișiere P7S se găsesc atașate la aceste e-mailuri.

Un fișier P7S conține următoarele informații:

* Sursa de origine a e-mailului
* Data și ora la care a fost trimis,
* Dacă a fost modificat în timpul transmisiei

Aceste informații sunt încorporate folosind tehnologia Public-Key Cryptography Standard #7 (PKCS7) pentru atașarea digitală a semnăturilor criptate la e-mail.

## Referințe ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

