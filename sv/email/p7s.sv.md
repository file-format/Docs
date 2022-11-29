{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S-fil - digitalt signerat e-postmeddelande",
  "description":"Läs mer om P7S-filformat och API:er som kan skapa och öppna P7S-filer.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Vad är P7S fil?

En P7S-fil är en digital signatur som tas emot med en digitalt signerad e-post. Närvaron av denna fil som en bilaga med e-postmeddelandet verifierar att e-postmeddelandet skickas från en autentisk källa. Detta säkerställer att avsändaren har ett e-postsigneringscertifikat installerat på sin dator. När ett sådant signerat e-postmeddelande skickas från användarens dator bifogas P7S-filen som innehåller namnet på avsändaren. E-postklienter som stöder signerade e-postmeddelanden kan se avsändarens information.

## P7S filformat - Mer information

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S-filer innehåller informationen i vanligt textformat som är läsbart för människor. E-postklienter som Microsoft Outlook, Apple Mail och Mozilla Thunderbird stöder för att läsa den digitalt signerade informationen från ett S/MIME-e-postmeddelande. Att signera ett e-postmeddelande verifierar avsändarens identitet och talar om för mottagaren att meddelandet är äkta. När e-postmeddelanden laddas ner från e-postklienter (antingen som [EML](/sv/email/eml/) eller [MSG](/sv/email/msg/)), hittas dessa P7S-filer bifogade med dessa e-postmeddelanden.

En P7S-fil innehåller följande information:

* Ursprungskälla för e-postmeddelandet
* Datum och tid när det skickades,
* Om den har ändrats under sändningen

Denna information är inbäddad med hjälp av Public-Key Cryptography Standard #7 (PKCS7) teknologi för att digitalt bifoga de krypterade signaturerna till e-postmeddelandet.

## Referenser ##

* [Microsoft Sign Tool](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

