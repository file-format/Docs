{
  "date" : "2021-07-29",
  "keywords" :[ "fișier pes", "format fișier pes", "ce este un fișier pes", "fișier", "exemplu pe", "extensie fișier pes", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PES - Format de broderie Brother PE",
  "description":"Aflați despre formatul de fișier PES și despre API-urile care pot crea și deschide fișiere PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Ce este un fișier de broderie PES?

Fișierul de broderie PES este un fișier de design care conține instrucțiuni pentru mașinile de brodat/de cusut. A fost dezvoltat de Brother Industries pentru mașinile lor de brodat, dar ulterior a fost oficializat ca format de fișier general. Fișierele PES sunt folosite de mașinile de cusut pentru a citi instrucțiunile de coasere a modelelor pe material. Aceste fișiere servesc două scopuri; mai întâi, furnizează informații de design pentru aplicația PE-Design dezvoltată de Brother Industries și, în al doilea rând, furnizează numele designului, culorile și codurile mașinii de brodat, cum ar fi „stop”, „salt” și „trim”.

## Format de fișier PES - Mai multe informații

Un fișier PES este salvat pe disc în format binar. Conține mai multe secțiuni care au informații de cusut stocate folosind o metodă predefinită. Formatul fișierului PES este următorul.

* Date despre versiune - Oferă informații despre versiune și poate fi orice valoare `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Valoarea de căutare PEC - Un număr întreg little-endian de 4 octeți care urmează imediat datele versiunii și reprezintă valoarea de căutare pentru secțiunea PEC care conține detalii de proiectare.
* Secțiunea PSE - Conține informații despre design relevante pentru Brother PE-Design și pot fi alte aplicații de cusut
* Secțiunea PCE - Poate fi oriunde în fișierul PSE, dar la care se face referire PEC Seek Value.

## Tip de mașini de cusut folosind fișierul PES

Fișierele PES sunt create în principal de software-ul PE-Design utilizat cu mașinile de cusut Brother. Alte mașini care pot accepta fișiere PES includ mașinile de brodat acasă Babylock și Bernina.

## Cum se convertesc fișiere PSE?

Aplicația software PE-Design poate [converti fișierul PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+fișier) în alte formate, cum ar fi .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd sau .xxx. Se poate face folosind aplicația PE-Design prin deschiderea fișierului și selectând formatul de conversie.

## Referințe

* [PE Design - Manual de instrucțiuni](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

