{
  "date": "2021-07-15",
  "keywords": [
"LNK",
"pratęsimas",
"failą",
"formatu",
"sistema",
"LNK failas",
"nuoroda",
"LNK failai",
"LNK dokumentai",
"taikymas",
"programas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LNK - Nuorodų failo formatas",
  "description": "Sužinokite apie LNK failo formatą ir API, kurios gali kurti ir atidaryti LNK failus.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ln-ltk"
}
},
  "lastmod": "2021-07-15"
}

## Kas yra LNK failas? ##

LNK failas, analogiškas tapatybei Mac sistemoje, yra Windows alternatyva arba nuoroda, kuri naudojama kaip ryšys su originalaus vaizdo dokumento aplanku arba programa. Jame yra nuorodos paskirties tipas, padėtis ir failo pavadinimas, taip pat programa, kuri atidaro tikslinį dokumentą, ir papildomas spartusis klavišas.

Sistemoje Windows perkelkite failą, aplanką arba vykdomąją programą ir pasirinkite Kurti nuorodą. Failo formato vieta ir katalogas Pradžia yra dvi pagrindinės LNK failų savybės. LNK failų failo formatas yra užmaskuotas, o lenkta rodyklė rodo, kad tai yra spartieji klavišai.

## LNK failo formatas ##

LNK failų formatai paprastai turi tą pačią piktogramą kaip ir jų paskirties failai, tačiau pridėta šiek tiek riesta rodyklė, rodanti, kad failas nukreiptas į kitą vietą. Dukart spustelėjus nuorodą, ji elgiasi taip, lyg vartotojas būtų dukart spustelėjęs tikrąjį failą.

LNK failai, kuriuose yra programų nuorodų, gali turėti savybių, kurios turi įtakos programos veikimui. Norėdami pakeisti atributus, dešiniuoju pelės mygtuku spustelėkite nuorodos failą ir pasirinkite **Ypatybės**, tada pakeiskite lauką Tikslas.

Vietoj failų plėtinių LNK failai yra Windows Explorer plėtiniai. Kaip terminalo plėtinį, .lnk dokumentai gali būti naudojami tik Windows Explorer, kad pakeistų failą, o Windows Explorer jie gali būti naudojami ne tik kaip nuoroda į vietinį dokumentą, bet ir kitais tikslais. Šie failai taip pat prasideda raide L.

Nors nuorodos susieja su tam tikrais failais ir katalogais, kai jie sukuriami, jie gali neveikti, jei taikinys pakeičiamas į kitą vietą. Explorer pradės taisyti nuorodų aplanką, kuris nukreipia į negyvą taikinį, kai jis bus atidarytas.


## Techninė specifikacija Nr.

Tik tada, kai nepažymėtas aplanko peržiūros nustatymas Slėpti atpažintų failų tipų plėtinius, Windows nerodo .lnk dokumento plėtinio dokumentų nuorodoms. Nors nerekomenduojama, galite įjungti failo plėtinio rodymą pašalindami ypatybę NeverShowExt iš HKEY_CLASSES_ROOT\lnk failo Windows registro elemento.

Norėdami tai padaryti, atlikite šiuos veiksmus:

* Atidarykite Registracijos rengyklę į užduočių juostos paieškos laukelį įvesdami Regedit ir pasirinkę programą
* Programoje eikite į Kompiuteris\HKEY HKEY_CLASSES_ROOT\lnkfile vietą
* Sukurkite atsarginę elemento kopiją spustelėdami jį dešiniuoju pelės mygtuku ir pasirinkdami Eksportuoti
* Pasirinkite ir ištrinkite atributą NeverShowExt.
* Windows turi būti paleistas iš naujo


## Nuoroda ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
