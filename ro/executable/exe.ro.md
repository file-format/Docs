{
  "date" : "2021-06-30",
  "keywords" :[ "fișier exe", "format fișier exe", "ce este un fișier exe", "fișier", "exemplul exe", "extensie fișier exe", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Un fișier .exe este un fișier Microsoft Executable care rulează pe sistemul de operare Windows. Aflați mai multe despre formatul fișierului EXE.",
  "title" :"Ce este un fișier EXE executabil?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Ce este un fișier EXE?

Cuvântul EXE este prescurtarea pentru **executable**. Un fișier .exe este un program care poate fi executat pe sistemul de operare Microsoft Windows. Dezvoltatorii de aplicații își publică în cea mai mare parte programele pentru sistemul de operare Windows în format executabil ca fișiere exe. Este formatul de fișier standard pentru a rula aplicații pe Windows. **Setup.exe**, **Install.exe** și **cmd.exe** sunt câteva nume comune și bine familiare ale fișierelor EXE.

## Format de fișier EXE

Compilatoarele MS-DOS au fost introduse cu modelele de memorie având limitarea memoriei de 64K. Conceptul general este de a seta registre de segmente diferite în CPU x86 (CS, DS, ES, SS) pentru a indica segmente diferite sau aceleași, permițând astfel diferite grade de acces la memorie. Unele modele de memorie specifice au fost:

- **Minuscule**: Toate accesele la memorie sunt pe 16 biți (registrele de segmente neschimbate). Produce un fișier .COM în loc de un fișier .EXE.
- **Small**: Toate accesele la memorie sunt pe 16 biți (registrele de segmente neschimbate).
- **Compact**: adresele de date includ atât segment, cât și offset, reîncărcând registrele DS sau ES la acces și permițând până la 1M de date. Accesurile de cod nu modifică registrul CS, permițând 64K de cod.
- **Mediu**: adresele de cod includ adresa segmentului, reîncărcarea CS la acces și permițând până la 1M de cod. Accesul la date nu modifică registrele DS și ES, permițând 64K de date.
- **Large**: Atât adresele de cod, cât și de date sunt perechi (segment, offset), reîncărcând întotdeauna adresele de segment. Întregul spațiu de memorie de 1 M octet este disponibil atât pentru cod, cât și pentru date.
- **Uriaș**: La fel ca și modelul mare, aritmetica suplimentară fiind generată de compilator pentru a permite accesul la matrice mai mari de 64K.

Dezvoltatorii trebuie să decidă ce model ar trebui să fie selectat în timp ce creează un fișier exe.

### Format de fișier EXE portabil

Formatul de fișier executabil portabil (PE) conține o serie de anteturi informaționale, următoarea este lista de anteturi:

- **Antet DOS**: Antetul MS-DOS asigură fie compatibilitate cu versiunile inverse, fie declinul grațios al noilor tipuri de fișiere.
- **PE Antet**: La offset 60 (0x3C) de la începutul antetului DOS este un pointer către antetul fișierului PE
- **COFF Header**: Antetul COFF are unele informații care sunt utile pentru un executabil și unele informații care sunt mai utile pentru un fișier obiect.
- ** Antet opțional PE**: Antetul opțional PE apare direct după antetul COFF, iar unele surse arată chiar că cele două anteturi fac parte din aceeași structură.
- **Tabel de secțiuni**: Imediat după antetul opțional PE găsim un tabel de secțiuni. Tabelul de secțiuni constă dintr-o matrice de structuri IMAGE_SECTION_HEADER.
- **Secțiuni mapabile**: poate economisi spațiu în memorie prin maparea codului unei biblioteci în mai multe procese.

## Puteți rula un fișier EXE pe un Mac?

Fișierele exe nu sunt folosite ca executabile pe Mac OS. Cu toate acestea, dacă doriți să rulați un fișier exe pe Mac OS, puteți utiliza următoarele metode.

1. **Wine** - Wine este soluția perfectă pentru persoanele care doresc să-și folosească aplicațiile PC pe sistemele Mac. Este un acronim care înseamnă „Wine Is Not A Emulator”, adică. Wine creează același mediu de directoare ca cel folosit de Microsoft, astfel încât să puteți rula aplicația Windows folosind-o.
2. **Mașini virtuale** - Creați o mașină virtuală Windows folosind Parallel Desktop sau VM Virtual Box și rulați aplicația în interiorul mașinii virtuale.
3. **Boot Camp** - Instalarea și configurarea Windows Boot Camp pe Mac OS vă permite să rulați sistemul de operare Windows pe computerul Mac.

## Referințe

* [.exe- de la Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [X86 Dezasamblare/Fișiere executabile Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

