{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "extensie", "fișier", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier Amazon APNX și despre API-urile care pot crea și deschide fișiere APNX.",
  "title" :"APNX - Indexul numerelor paginii Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Ce este un fișier APNX? ##

Fișierul Amazon Page Number Index care utilizează extensia .apnx este un tip de fișier eBook; folosit de Amazon Kindle. Aceste fișiere sunt de fapt cunoscute ca fișiere de paginare utilizate de dispozitivele Kindle. Prin urmare, fișierele APNX sunt create de obicei pentru a marca paginile cărților electronice Kindle. Funcția de paginare a fost începută pe dispozitivele Amazon Kindle încă de la firmware-ul său 3.1. Acesta caută în fișierul APNX indici de pagini și apoi îl mapează cu numerele paginilor din cartea originală de tipărire. Aceste fișiere sunt salvate pe dispozitivele Kindle împreună cu fișierele Amazon eBooks. Nu puteți deschide sau edita fișierele APNX.

## Specificații pentru formatul fișierului APNX ##

### Aspect

|octeți| continut| comentarii|
---|---|---|
|4 |00010001 | Identificator de format. Valoarea de 65537 little-endian.|
|4 |începutul următorului | Decalajul după locația de încheiere a primului antet. Pornește o nouă secvență de informații din antet|
|4 |lungime| Lungimea primului antet|
|N |primul antet | Șir care conține antet de conținut. Începe următoarea secvență|
|2 |necunoscut | Întotdeauna 1|
|2 |lungime | Lungimea celui de-al doilea antet|
|2 |număr de pagini | Numărul total de octeți după al doilea antet care reprezintă pagini. Acest total include octeții care sunt ignorați de pageMap.|
|2 |necunoscut | Întotdeauna 32|
|N |al doilea antet | Șir care conține antetul de mapare a paginii|
|4*N |captuseala | Primul număr dat în antetul maparii paginii indică numărul de 0 octeți.|
|4*N |lista de pagini ||

### Antet de conținut

Antetul de conținut constă dintr-un șir cuprins în {} care conține perechi cheie, valoare:

|conținut| comentarii|
---|---|
|contentGuid| Ghid.|
|asin | Identificatorul Amazon pentru versiunea Kindle a cărții.|
|cdeType | MOBI cdeType. Ar trebui să fie întotdeauna EBOK pentru cărți electronice.|
|fileRevisionId | Revizuirea acestui dosar.|

#### Exemplu
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Antet de mapare a paginii
Antetul de mapare a paginii constă dintr-un șir cuprins în {} care conține perechi cheie, valoare.

|conținut | comentarii|
---|---|
|asin | ISBN 10 pentru cartea de hârtie cărora le corespund paginile|
|pageMap| Tuplu cu trei valori. Arată astfel: „(N,N,N)\
1) Numărul de octeți după antetul care începe secvența de numerotare a paginii\
2) necunoscut\
3) necunoscut\|
#### Exemplu
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Lista pagini

Lista de pagini este o secvență de offset-uri în HTML brut. Fiecare
valoarea este începutul unei pagini noi. Fiecare intrare este un big endian de 4 octeți
int.



## Referințe

* [Format de fișier Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - de MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

