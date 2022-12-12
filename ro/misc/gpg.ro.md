{
  "date" : "2022-02-17",
  "keywords" :["fișier gpg", "format fișier gpg", "ce este un fișier gpg", "fișier", "exemplu gpg", "extensie fișier gpg", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG File - GNU Privacy Guard Public Keyring File",
  "description":"Aflați despre fișierul GPG și API-urile care pot crea și deschide fișiere GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Ce este un fișier GPG?

Un fișier GPG este un fișier cheie de criptare/decriptare care este utilizat de programul de criptare GNU Privacy Guard (GnuPG). Programul GnuPC în sine se bazează pe standardul OpenPGP, așa cum este definit RFC4880 și este cunoscut și ca PGP. Cheia utilizării cu succes a GPG în sistemul de operare modern este sistemul său versatil de gestionare a cheilor. Utilitarul de linie de comandă al GPG îi permite să se integreze cu ușurință cu alte aplicații.

## Format de fișier GPG

Fișierele GPG sunt salvate ca fișiere binare criptate și, desigur, nu pot fi citite de om. Pentru a decripta un fișier GPG criptat, trebuie să utilizați aceeași cheie de securitate. Și de aceea nu se cunoaște formatul de fișier intern al acestor fișiere.

## Criptați și decriptați fișierele cu GPG pe Linux

Utilitarul de linie de comandă GPG poate fi folosit pentru a cripta și decripta fișierele pe Linux.

### Criptarea unui fișier

Un fișier poate fi criptat folosind comanda gpg cu opțiunea -c (creare), așa cum se arată mai jos.

```
gpg -c file1.txt
```
Rularea acestei comenzi cere o expresie cheie cu care să cripteze conținutul fișierului original `file1.txt`. Aceasta are ca rezultat crearea fișierului criptat file1.txt.gpg.

### Decriptarea și extragerea unui fișier

Pentru a decripta și extrage un fișier criptat, se poate folosi următoarea comandă.

```
gpg cfile.txt.gpg
```

## Referințe

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

