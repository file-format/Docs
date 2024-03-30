{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDE-fil - Vad är en MDE-fil och hur man öppnar den?",
  "description":"Lär dig om MDE-filformat och API:er som kan skapa och öppna MDE-filer.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-sv-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

Vad är en MDE fil?

En .MDE-fil är en kompilerad version av en Access-databas (.mdb eller .accdb). När du kompilerar en Access-databas till en .MDE-fil kan den inte längre redigeras med hjälp av de vanliga Access-designverktygen. Det primära syftet med att skapa en .MDE-fil är att distribuera en databasapplikation utan att exponera den ursprungliga källkoden.

## MDE-filformat

En MDE-fil skapas genom att kompilera VBA-koden, formulär, rapporter och andra objekt. Detta resulterar i skapandet av MDE binärt filformat. Den resulterande .MDE-filen kan distribueras till användare som kan köra programmet men inte kan ändra designen eller visa originalkoden. MDE-filen är faktiskt den kompilerade versionen av en [.MDA-fil](/database/mda/). Att distribuera .MDE-filer kan hjälpa till att skydda immateriella rättigheter genom att hindra användare från att komma åt eller ändra källkoden. Det kan också förbättra prestandan när koden kompileras och optimeras.

## Referenser

* [Åtkomstspecifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
