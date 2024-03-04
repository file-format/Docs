{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MKS failo formatas",
  "keywords": [
"mks",
"matroskos vaizdo įrašas",
"mkv formatu",
"failą",
"formatu",
"vaizdo įrašą"
],
  "description": "Sužinokite apie MKS failo formatą, skirtą tik „Matroska“ sukurtiems subtitrams ir API, kurios gali kurti ir atidaryti MKS failus.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-lts"
}
},
  "lastmod": "2021-25-02"
}

## Kas yra MKS failas?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

– .mks. plėtinį naudos Matroska failas (su tik subtitrais).
– **CodecPrivate** naudojama saugoti visą su kodekais susijusią informaciją, kuri yra visuotinė visame sraute.
- Pašalinkite pradžios ir pabaigos laiko žymas, kurios naudojamos laiko žymos savajame saugojimo formate. Vietoj to naudokite blokų laiko žymą ir trukmę.
- Galite naudoti bet ką su permatomu sluoksniu, įskaitant vaizdo įrašą.

## Įprasti subtitrų formatai

Here are some brief notes about more common subtitle formats stored in Matroska:

### Vaizdai Subtitrai
VobSub subtitrų formatas yra pirmasis vaizdo subtitrų formatas, importuojamas į Matroska. Šis formatas sugeneruojamas eksportuojant subtitrus iš DVD. Saugant Matroska takelius reikia atskirti, jei VobSub susideda iš kelių srautų rinkinio.

### SRT subtitrai
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Skaičius, nurodantis subtitrų seką.
 2. Subtitrų atsiradimo ir išnykimo laikas ekrane.
 3. Pats subtitras.
 4. Tuščia eilutė, nurodanti kito subtitrų pradžią.
 
### SSA/ASS subtitrai
Sub Station Alpha (SSA) yra failo formatas, kurį naudoja populiarus subtitrų rengyklė SubStation Alpha. SSA subtitrus plačiai naudoja gerbėjai. Jis turi galimybę rodyti modernias funkcijas, pvz., karaokę, padėties nustatymą, stilių ir kt.
 
### WebVTT subtitrai
Pasaulio žiniatinklio konsorciumas (W3C) sukūrė WebVTT, kuris sutrumpintas kaip Web Video Text Tracks Format. Šis formatas naudojamas išoriniams teksto takelio ištekliams, susijusiems su HTML elementu, pažymėti.

### HDMV pristatymo grafikos subtitrai
HDMV pristatymo grafikos subtitrų formatas (HDMV PGS) yra taškinių schemų serija, kurios visiškai negalime pasakyti tekstu. Kitaip tariant, galima sakyti, kad tai tik tam tikra grafinių vaizdų seka. Norint išgauti informaciją, PGS konvertavimas į SRT yra būtinas procesas.

### HDMV teksto subtitrai
HDMV tekstas yra žinomas kaip tekstinis subtitrų formatas, naudojamas Blu-ray. Matroska leidžia tik UTF-8 simbolių rinkinį When išsaugo TextST subtitrus.

### Skaitmeninio vaizdo transliavimo (DVB) subtitrai
DVB subtitrų formatas buvo įvestas siekiant reguliuoti kelių kalbų subtitrų perdavimą ir rodymą televizijos signaluose. Įprastas subtitravimo formatas taip pat leistų bet kuriam žiūrovui žiūrėti DVB subtitrus transliacijas, nesvarbu, koks perdavimo sistemų gamintojas.


## Nuorodos Nr.

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

