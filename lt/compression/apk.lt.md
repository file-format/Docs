{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APK – kas yra APK failas?",
  "description": "Sužinokite, kas yra APK failas ir API, kurios gali kurti ir atidaryti APK failus.",
  "linktitle": "APK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ap-ltk"
}
},
  "lastmod": "2021-04-27"
}

## Kas yra APK failas?

Failas su plėtiniu .apk yra Google Android programos failas, naudojamas programoms (programoms) įdiegti Android įrenginiuose. Jis sukurtas kaip vykdomasis failas naudojant oficialią IDE Google Android Studio ir įkeliamas į Google Play parduotuvę, kad galėtų atsisiųsti ir įdiegti galutiniai vartotojai. APK failus galima sugeneruoti ir padaryti prieinamus rankiniam įdiegimui, taip pat prieš paskelbiant Google Play parduotuvėje. Tai padeda išbandyti sugeneruoto APK paketo failo funkcionalumą ir elgesį. Todėl reikia įsitikinti, kad APK failas yra iš patikimo šaltinio ir jame nėra kenkėjiškų programų.

## APK failo formatas

APK failai supakuoti kaip suspausti [ZIP](/compression/zip/) failo formatu, kurį galima atidaryti naudojant bet kurią ZIP failų atidarymo programinę įrangą. Tokio failo plėtinį .apk galima pervadinti į .zip ir atidaryti failą bet kurioje ZIP programoje arba išskleisti jo turinį.

## APK paketo turinys

Viename APK faile yra visi reikalingi failai, reikalingi jį įdiegti ir vykdyti. APK faile, ištrauktame naudojant ZIP programą, yra šie failai ir aplankai.

 * META-INF/: katalogas, kuriame yra manifesto failas, parašas ir archyvo išteklių sąrašas
 * lib/: katalogas, kuriame yra sukompiliuotas kodas, susijęs su konkrečiomis platformomis, pvz., armeabi-v7a, x86, arm64-v8a ir kt.
 * res/: katalogas, kuriame yra nesudarytų išteklių, tokių kaip vaizdai
 * Assets/: katalogas, kuriame yra programų išteklių, kuriuos gali gauti AssetManager.
 * androidManifest.xml: yra APK failo pavadinimas, versijų kūrimo informacija ir turinys
 * classes.dex: tai yra sudarytos Java klasės, kurias galima paleisti Dalvik virtualioje mašinoje ir Android Runtime
 * resources.arsc: sukompiliuotas išteklių failas, pvz., eilutės

## Kaip atidaryti APK failus

APK failai turi būti įdiegti Android įrenginiuose. Be to, Windows 11 yra pirmoji Windows versija, oficialiai palaikanti APK failų diegimo funkciją.

### Kaip įdiegti APK failą Android įrenginyje

Norėdami įdiegti APK failą Android įrenginiuose, galite atlikti šiuos veiksmus.

 1. Atsisiųskite APK naudodami žiniatinklio naršyklę
 2. Bakstelėkite jį – tada turėtumėte matyti, kaip jis atsisiunčiamas viršutinėje įrenginio juostoje
 3. Atsisiuntę atidarykite Atsisiuntimus, bakstelėkite APK failą ir palieskite Taip, kai būsite paraginti.

Atlikus šiuos veiksmus bus pradėtas programos diegimas jūsų įrenginyje.

### Kaip atidaryti APK failą sistemoje Windows

Galite naudoti Android emuliatorių Windows kompiuteryje norėdami atidaryti / pasiekti APK failą. BlueStacks yra vienas iš tokių Android emuliatorių, kurį galima naudoti norint atidaryti Android emuliatorių sistemoje Windows. Jei naudojate Windows 11, jums pasisekė, nes Windows 11 oficialiai palaiko galimybę įdiegti APK failus.

### Kaip atidaryti APK failą Mac.

Taip pat galite naudoti BlueStack sistemoje MacOS ir atidaryti APK failus. Tai nemokamas Android emuliatorius ir suteikia galimybę jį naudoti kaip geriausią būdą pasiekti tik Android skirtas programas.

## Kaip sukurti APK failą

Norint sukurti APK failą, reikia naudoti specializuotus įrankius ir kūrimo aplinkas. Android kūrėjai pirmiausia naudoja Android Studio, oficialią integruotą kūrimo aplinką (IDE), skirtą Android programoms kurti. Štai bendra APK failo kūrimo veiksmų apžvalga:

 1. **Kūrimo aplinkos nustatymas:** kompiuteryje įdiekite ir nustatykite Android Studio. Android Studio teikia išsamų įrankių rinkinį, skirtą Android programoms kurti, testuoti ir pakuoti.
 1. **Sukurkite programą:** naudokite Java arba Kotlin programavimo kalbas, kad parašytumėte Android programos kodą. Android Studio teikia daugybę funkcijų ir išteklių, padedančių kurti programą, įskaitant kodo rengykles, emuliatorius ir derinimo įrankius.
 1. **Sukurkite programą:** baigę rašyti kodą ir sukurti vartotojo sąsają, naudokite Android Studio kūrimo įrankius programai kompiliuoti ir supakuoti. Šis procesas sugeneruoja reikiamus failus ir išteklius, reikalingus APK failui.
 1. **Pasirašykite APK failą:** prieš platinant programą, būtina pasirašyti APK failą. Programėlės pasirašymas užtikrina programos vientisumą ir autentiškumą. Android Studio leidžia sugeneruoti pasirašymo raktą ir pasirašyti APK failą naudojant šį raktą.
 1. **Paskirstykite APK failą:** Kai pasirašysite APK failą, galėsite jį platinti įvairiais kanalais. Galite įkelti jį į Google Play parduotuvę, kad platintumėte plačiajai auditorijai, arba bendrinti jį tiesiogiai su vartotojais naudodami el. paštą, atsisiuntimo nuorodas ar kitas platinimo platformas.

Verta paminėti, kad Android Studio sugeneruotas APK failas paprastai yra optimizuotas gamybiniam naudojimui. Kūrimo proceso metu taip pat galite generuoti derinimo APK failus, kurie yra naudingi testavimo ir derinimo tikslais, bet nėra skirti platinti.

## DUK

 * **Ar APK failai gali pakenkti mano įrenginiui?** APK failai gali kelti grėsmę įrenginiams. Taip yra dėl to, kad juose gali būti kenkėjiškų programų. Todėl prieš diegiant patartina APK failams atlikti internetinį virusų nuskaitymą. Be to, Android antivirusinės programos naudojimas yra protinga priemonė. Kad sumažintumėte riziką, kad jūsų įrenginys taps apgaulingos programos auka, geriausia atsisiųsti iš patikimų šaltinių, kuriuos žinote ir kuriais pasitikite.

 * **Ar APK failai yra teisėti?** APK failų atsisiuntimas ir naudojimas programoms diegti iš kitų šaltinių nei Google Play parduotuvė yra visiškai įstatymų ribos. APK, panašus į tokius formatus kaip EXE arba ZIP, yra failo formatas. Nors Google buvo šio formato pradininkė, bet kas gali generuoti ir naudoti APK failus.

 * **Kaip rasti APK failus Android įrenginyje?** APK failai lieka paslėpti nuo naudotojų, nes Android tvarko programų diegimą fone, naudojant Google Play ar kitą programų platinimo platformą. Tačiau iš kitų šaltinių atsisiųstus APK failus galima rasti naudojant Android failų tvarkyklę.

## Nuorodos

* [APK failo formatas](https://en.wikipedia.org/wiki/Android_application_package)


