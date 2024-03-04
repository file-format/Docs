{
  "date": "2019-10-11",
  "keywords": [
"mht",
"mht failą",
"mht failo formatą",
"mht failo tipas",
"failą",
"tipo",
"kas yra mht failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHT – MIME HTML failo formatas",
  "description": "Sužinokite apie MHT failo formatą ir API, kad sukurtumėte ir atidarytumėte MHT failus.",
  "linktitle": "MHT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mh-ltt"
}
},
  "lastmod": "2021-02-29"
}

## Kas yra MHT failas?

Failas su plėtiniu .mht yra MIME įgalintas archyvavimo failo formatas, kuriame yra skirtingų tipų duomenys viename faile. Jis gali saugoti tokius duomenis kaip tekstas, vaizdai, puslapio stilius [CSS](/web/css/) failų pavidalu, JavaScript ir kiti ištekliai kaip įterptieji ištekliai. MHT failai, turintys MIME tipo pranešimą/rfc822, visą HTML failo turinį įtraukia į vieną archyvo failą, skirtą saugoti archyvavimo įrenginiuose. Programinės įrangos programos, pvz., Microsoft Word, leidžia konvertuoti WORD dokumentus į MHT eksportuojant kaip MHT failą. MHT failus galima atidaryti naudojant populiarias naršykles, tokias kaip Microsoft Internet Explore ir Google Chrome.

## MHT failo formatas

Kaip ir [MHTML](/web/mhtml/), MHT taip pat yra sukauptų HTML dokumentų MIME inkapsuliacija. Dokumento turinys MHT dokumente, pvz., eilutiniai paveikslėliai, stiliaus lapai, programėlės ir kt., yra koduojamas MIME, kur jie yra susieti su šakniniu šaltiniu per URI. El. pašto programos, pvz., Microsoft Outlook, saugo el. laiškus (dažniausiai [EML](/email/eml/)) MHT failo formatu. Išsamias MHT failo formato specifikacijas galima rasti [RFC 822](https://tools.ietf.org/html/rfc822) ir jas galima naudoti kuriant programinę įrangą, kuri gali apdoroti MHT failus.

## Skirtumas tarp MHT ir MHTML

Išsaugant internetinį puslapį, vartotojo prašoma nustatyti failo formatą, kuriuo internetinis puslapis turi būti išsaugotas vietinėje sistemoje. Dažniausiai vartotojas susipainioja tarp žymėjimo kalbos ir MHTML failų formatų. Jie pastebi, kad sunku matyti, kad failo formatas yra sveikesnis tarp jų.

Kai vartotojas nusprendžia nešvaistyti internetinio puslapio kaip žymėjimo kalbos, susidaro aplankas, kuriame yra keli failai įvairiam puslapio turiniui, ty visiškai skirtingi failų srities vienetai, sukurti tekstui, grafikai, programėlėms ir pan. internetinis puslapis kaip MHTML sukuria vieną failą visam internetiniam puslapiui. Visi puslapio elementai kartu su grafika, nuorodomis ir alternatyvių failų srities vienetu įterpti į vieną failą.

Žinoma, paprasta tvarkyti MHT arba MHTML failus, nes failas gali būti apsaugotas ir bendrinamas tiesiog el. paštu. Tačiau žymėjimo kalbos failų srities vienetas, esantis žemiau informacijos praradimo, nes net vieno failo praradimas arba ištrynimas gali sukurti visą žymėjimo kalbos aplanką, kuris vartotojui bus nenaudingas.

## Nuorodos

* [MHTML – Vikipedija](https://en.wikipedia.org/wiki/MHTML)

* [MHT RFC](https://tools.ietf.org/html/rfc822)


