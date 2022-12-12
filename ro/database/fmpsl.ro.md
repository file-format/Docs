{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier FMPSL și despre API-urile care pot crea și deschide fișiere FMPSL.",
  "title" :"Format de fișier FMPSL - Fișier de legătură instantanee FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Ce este un fișier FMPSL?

Un fișier FMPSL este un fișier instantaneu al bazei de date creat cu FileMaker Pro 12. Acesta stochează rezultatele interogate din baza de date împreună cu alte informații, cum ar fi aspectul vizual și informații vizibile. Fișierul FMPSL poate fi utilizat pentru a restaura toate aceste date într-o altă instanță a bazei de date FileMaker Pro. Acest format de fișier a fost introdus odată cu lansarea FileMaker Pro v 12. Înainte de această versiune, legăturile instantanee au fost introduse ca format de fișier FPSL în FileMaker Pro v 11. Fișierele FMPSL pot fi deschise cu software-ul FileMaker Pro Advanced. Alte formate de fișiere acceptate de FileMaker Pro includ [FP5](/ro/database/fp5/), [FP7](/ro/database/fp7/) și [FMP12](/ro/database/fmp12/).

## Format de fișier FMPSL

Detaliile formatului de fișier intern ale fișierelor FMPSL nu sunt disponibile public pentru referință de către dezvoltatori.

### Cum se salvează înregistrările ca fișier FMPSL?

Datele din baza de date FileMaker Pro pot fi salvate ca fișier de legătură instantanee utilizând pașii următori.

1. Căutați înregistrările din baza de date care trebuie să fie salvate ca fișier de link instantaneu.
1. Folosind opțiunea Trimitere înregistrare ca link instantaneu din meniu, salvați fișierul introducând un nume de fișier.
1. Utilizați Înregistrările în curs de navigare pentru a salva întregul set de înregistrări găsit.

Fișierul instantaneu generat va fi salvat pe disc cu numele specificat.

## Referințe

* [Conversia versiunilor anterioare ale formatelor de fișiere FileMaker Pro în format de fișier FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Salvați înregistrările ca fișier cu link instantaneu](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

