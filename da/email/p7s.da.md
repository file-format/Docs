{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7S-fil - digitalt signeret e-mail-besked",
  "description": "Lær om P7S filformat og API'er, der kan oprette og åbne P7S filer.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-das"
}
},
  "lastmod": "2022.01.31"
}

## Hvad er en P7S fil?

En P7S-fil er en digital signatur, der modtages med en digitalt signeret e-mail. Tilstedeværelsen af denne fil som en vedhæftet fil med e-mailen bekræfter, at e-mailen er sendt fra en autentisk kilde. Dette sikrer, at afsenderen har et e-mailsigneringscertifikat installeret på deres computer. Når en sådan signeret e-mail sendes fra brugerens computer, er P7S-filen vedhæftet den, som indeholder afsenderens navn. E-mail-klienter, der understøtter signerede e-mails, kan se afsenderens oplysninger.

## P7S filformat - flere oplysninger

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S-filer indeholder oplysningerne i almindeligt tekstformat, der kan læses af mennesker. E-mail-klienter såsom Microsoft Outlook, Apple Mail og Mozilla Thunderbird understøtter at læse de digitalt signerede oplysninger fra en S/MIME-e-mail. At signere en e-mail bekræfter afsenderens identitet og fortæller modtageren, at meddelelsen er autentisk. Når e-mails downloades fra e-mail-klienter (enten som [EML](/email/eml/) eller [MSG](/email/msg/)), findes disse P7S-filer vedhæftet disse e-mails.

En P7S-fil indeholder følgende oplysninger:

 * Oprindelseskilde for e-mailen
 * Dato og tidspunkt for afsendelsen,
 * Om det er blevet ændret under transmissionen

Disse oplysninger er indlejret ved hjælp af Public-Key Cryptography Standard #7 (PKCS7) teknologi til digital vedhæftning af de krypterede signaturer til e-mailen.

## Referencer ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


