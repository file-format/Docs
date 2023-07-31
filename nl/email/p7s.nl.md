{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S-bestand - digitaal ondertekend e-mailbericht",
  "description":"Meer informatie over P7S-bestandsindeling en API's die P7S-bestanden kunnen maken en openen.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Wat is een P7S-bestand?

Een P7S-bestand is een digitale handtekening die wordt ontvangen met een digitaal ondertekende e-mail. De aanwezigheid van dit bestand als bijlage bij de e-mail bevestigt dat de e-mail afkomstig is van een authentieke bron. Dit zorgt ervoor dat de afzender een certificaat voor e-mailondertekening op zijn computer heeft geïnstalleerd. Wanneer een dergelijke ondertekende e-mail vanaf de computer van de gebruiker wordt verzonden, wordt het P7S-bestand eraan toegevoegd dat de naam van de afzender bevat. E-mailclients die ondertekende e-mails ondersteunen, kunnen de informatie van de afzender zien.

## P7S-bestandsindeling - Meer informatie

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S-bestanden bevatten de informatie in platte tekst die voor mensen leesbaar is. E-mailclients zoals Microsoft Outlook, Apple Mail en Mozilla Thunderbird ondersteunen het lezen van de digitaal ondertekende informatie uit een S/MIME-e-mail. Het ondertekenen van een e-mail verifieert de identiteit van de afzender en vertelt de ontvanger dat het bericht authentiek is. Wanneer e-mails worden gedownload van e-mailclients (ofwel als [EML](/nl/email/eml/) of [MSG](/nl/email/msg/)), worden deze P7S-bestanden als bijlage bij deze e-mails aangetroffen.

Een P7S-bestand bevat de volgende informatie:

* Bron van herkomst van de e-mail
* Datum en tijd waarop het is verzonden,
* Of het tijdens verzending is gewijzigd

Deze informatie is ingebed met behulp van de Public-Key Cryptography Standard #7 (PKCS7)-technologie voor het digitaal koppelen van de versleutelde handtekeningen aan de e-mail.

## Referenties ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

