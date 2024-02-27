{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MDE-fil - Hvad er en MDE-fil, og hvordan åbner man den?",
  "description":"Lær om MDE-filformat og API'er, der kan oprette og åbne MDE-filer.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-md-dae"
}
},
  "lastmod" : "2023-12-03"
}

## Hvad er en MDE fil?

En .MDE-fil er en kompileret version af en Access-database (.mdb eller .accdb). Når du kompilerer en Access-database til en .MDE-fil, kan den ikke længere redigeres ved hjælp af de standard Access-designværktøjer. Det primære formål med at oprette en .MDE-fil er at distribuere en databaseapplikation uden at afsløre den originale kildekode.

## MDE filformat

En MDE-fil oprettes ved at kompilere VBA-koden, formularer, rapporter og andre objekter. Dette resulterer i oprettelse af MDE binært filformat. Den resulterende .MDE-fil kan distribueres til brugere, der kan køre programmet, men ikke kan ændre designet eller se den originale kode. MDE-filen er faktisk den kompilerede version af en [.MDA file](/database/mda/). Distribution af .MDE-filer kan hjælpe med at beskytte intellektuel ejendom ved at forhindre brugere i at få adgang til eller ændre kildekoden. Det kan også forbedre ydeevnen, da koden kompileres og optimeres.

## Referencer

* [Adgangsspecifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [The Unofficial MDB Guide](http://jabakobob.net/mdb/)
