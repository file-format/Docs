{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TEX failo formatas",
  "description": "Sužinokite apie TEX failo formatą ir API, kurios gali kurti ir atidaryti TEX failus.",
  "linktitle": "TEX",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-te-ltx"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra TEX failas? ##

**TeX** yra kalba, kurią sudaro programavimas ir žymėjimo funkcijos, naudojamos dokumentams rinkti. Donaldas Knuthas iš Stanfordo universiteto yra šios išradingos rinkimo sistemos kūrėjas. Visame pasaulyje TeX yra geriausias autorių ir leidėjų pasirinkimas, norint parengti aukštos kokybės techninius dokumentus. TeX atlieka puikų sudėtingų matematinių išraiškų formatavimo darbą. Kartu su aukštos kokybės fotospausdintuvu TeX konkuruoja su geriausių tradicinių rinkimo sistemų rezultatais. Todėl laikomos klasiškiausiomis skaitmeninėmis tipografinėmis sistemomis.

TeX įvesties failai yra pagrįsti ASCII kodu, todėl rašytojai, leidybos vadovai ir kritikai gali dalytis rankraščiais. Įvairios skaičiavimo aplinkos, beveik kiekviena moderni platforma ir daug senesnių platformų palaiko TeX. Be to, TeX yra nemokama programinė įranga, prieinama daugeliui vartotojų. Daugelis UNIX įrenginių naudoja UNIX troff ir TeX kaip formatavimo sistemą įvairiems tikslams. Kitos rinkimo užduotys atliekamos labai gerai LaTeX, ConTeXt ir kitų makrokomandų paketų pavidalu.

## Trumpa istorija ##

TeX was designed and written by Donald Knuth in 1978. Guy'us Steele'as iš Masačusetso technologijos instituto peržiūrėjo TeX įvestį / išvestį, kad jis veiktų pagal nesuderinamą operacinę sistemą, pvz., Laiko naudojimo sistemą (ITS). Pirmoji TeX versija buvo sukurta naudojant Stanfordo WAITS operacinę sistemą programavimo kalba (SAIL) ir išbandyta veikti PDP-10. Knuthas pristatė raštiško programavimo idėją pažangioms versijoms. Raštingas programavimas yra būdas generuoti kompiliuojamą šaltinio kodą ir rinkinį (TeX) kryžminei dokumentacijai naudojant originalų failą. Kalba, naudojama kuriant šias pažangias TeX versijas, vadinama WEB, DEC PDP-10 Pascal programų mišiniu, užtikrinančiu nešiojamumą.

A revised new version of TeX published in 1982 and was called TeX82. Pagrindinis pakeitimas yra pradinio brūkšnelio algoritmo pakeitimas naujai parašytu Franko Liango algoritmu. Siekiant užtikrinti perkeliamumą įvairiose platformose, TeX82 vietoj slankaus kablelio naudoja fiksuoto kablelio aritmetiką kartu su realia, visapusiška programavimo kalba. 1989 m. buvo išleistos naujos TeX ir Metafont versijos. Taigi 3.0 TeX versija palengvina 8 bitų įvestį, leidžiančią tekste naudoti 256 skirtingus simbolius. Po 3 versijos atnaujinimai žymimi pridedant papildomą skaitmenį dešimtainio skaičiaus pabaigoje, pvz., dabartinė TeX versija nurodoma kaip 3.14159265. Ši versija paskutinį kartą buvo atnaujinta 2014-12-1.

## TeX įvestis ##

Įvesties failą į TEX galima paruošti naudojant teksto rengyklę, naudojant įprastą tekstą. Kitaip nei įprasta Word procesorius, šis įvesties failas neleidžia jokių nematomų valdymo simbolių. Vienas failas gali būti įterptas į kitą failą, kuriame yra makrokomandų apibrėžimai ir pagalbiniai apibrėžimai, kurie pagerina TeX galimybes. Jei TeX diegimas pateikiamas su bet kokiais makrokomandų failais, vietinė informacija apie TeX parodo makrokomandų failų naudojimą. Standartinė TeX forma integruoja makrokomandų ir kitų apibrėžimų, žinomų kaip paprastas TEX, derinį.

Remdamasis tiksliomis žiniomis apie visų simbolių ir simbolių dydžius, jis apskaičiuoja optimalų raidžių išdėstymą eilutėje ir eilučių puslapyje. Dokumento apdorojimo metu sukuriamas .dvi failas, kur dvi reiškia nepriklausomas nuo įrenginio. Įrenginio tvarkyklės programos reikalingos norint spausdinti arba peržiūrėti dokumentą su dvi plėtiniu. Šiais laikais dvi generavimą aplenkia dažniausiai naudojamas pdf-TeX. Diegiant TeX nėra jokių išankstinių žinių apie šriftus, todėl informacijai apie dokumentą gauti naudojami išoriniai šriftų failai, kurie yra vietinės TeX aplinkos dalis.

## Rašymo sistema Nr.

Bazinė TeX sistema gali suprasti apie 300 primityvų (komandų). Primityvai yra žemo lygio komandos, todėl dažnas vartotojas retai jas naudoja tiesiogiai, o daugumą funkcijų atlieka formato failai. Šie formato failai yra iš anksto įkelti TeX atmintyje vaizdai, po kurių įkeliamos didelės makrokomandų kolekcijos. Pradinis numatytasis kalbos formatas, ty paprastas TeX, prideda apie 600 komandų.

Pasvirasis brūkšnys, sugrupuotas su riestiniais skliaustais, reiškia TeX komandų pradžią. Kadangi TeX yra makrokomandomis ir žetonais pagrįsta kalba, beveik visas TeX sintaksines charakteristikas galima pakeisti vykdymo metu, įskaitant vartotojo nustatytas, išskyrus neišplečiamus prieigos raktus, kurie vėliau vykdomi. Pati plėtra praktiškai be problemų. Kai kurios komandos turi būti po argumentų, padedančių paaiškinti komandos funkciją. Pavyzdžiui, komanda \vskip nurodo TEX praleisti puslapį žemyn / aukštyn, po kurio pateikiamas argumentas, nustatantis, kiek vietos praleisti.

## Versijos ##

LaTeX yra dažniausiai naudojamas formatas, kurį iš pradžių sukūrė Leslie Lamport. LaTeX integruoja skirtingus dokumentų stilius failams, raidėms, knygoms ir skaidrėms ir siūlo nuorodas bei automatinį skirtingų skyrių ir matematinių išraiškų numeravimą. AMS-TeX yra dar vienas populiarus formatas, sukurtas Amerikos matematikų draugijos.

AMS-TeX siūlo daug patogesnių komandų, kurias žurnalai gali iš naujo apibrėžti, kad atitiktų jų vietinį stilių. LaTeX gali pasinaudoti AMS-TeX pranašumais naudodamas AMS paketus, kurie vėliau vadinami AMS-LaTeX. ConTeXt yra kitas Hanso Hageno parašytas formatas, daugiausia naudojamas darbalaukio leidybai.

TeX programinė įranga siūlo keletą funkcijų, kurios jos kūrimo metu buvo nepasiekiamos arba prastesnės kokybės kitose rinkimo sistemose. Kai kurios naujoviškos šios kalbos savybės yra pagrįstos įdomiais algoritmais, gautais iš Knutho mokinių tezių. Nors kitos rinkimo programos dabar į savo programas įtraukia naudingų TeX funkcijų.

## Nuorodos Nr.

* [TeX rinkimo sistema](https://en.wikipedia.org/wiki/TeX)


