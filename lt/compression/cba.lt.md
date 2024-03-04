{
  "date": "2023-05-24",
  "keywords": [
"cba failą",
"kas yra cba failas",
"kaip sukurti CBA failą",
"kas yra CBA faile",
"koks yra cba failo formatas",
"failą",
"cba failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CBA failo formatas – komiksų archyvas",
  "description": "Sužinokite apie CBA formatą ir API, kurios gali kurti ir atidaryti CBA failus.",
  "linktitle": "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba-lt",
      "parent": "compression"
}
},
  "lastmod": "2023-05-24"
}

## Kas yra CBA failas?

Komiksų archyvo (CBA) failas, taip pat žinomas kaip komiksų archyvas arba komiksų skaitytuvo failas, yra populiarus formatas, naudojamas skaitmeninėms komiksų knygoms saugoti ir platinti. Paprastai jame yra atskirų komiksų puslapių arba vaizdų rinkinys, sujungtas į vieną failą, kad būtų lengviau tvarkyti ir skaityti.

Vienas iš įprastų komiksų archyvo failų kūrimo formatų yra TAR (tape Archive) formatas. TAR yra failų archyvavimo formatas, naudojamas Unix ir Linux aplinkose. Jis sujungia kelis failus į vieną failą, dažnai naudojamą atsarginėms kopijoms kurti.

## Kaip sukurti CBA failą?

Norėdami sukurti komiksų archyvo failą naudodami TAR archyvavimo įrankį, paprastai atlikite šiuos veiksmus:

1. Surinkite visus komiksų puslapius ar vaizdus, kuriuos norite įtraukti į archyvą.
2. Atidarykite komandų eilutę arba terminalo langą.
3. Eikite į katalogą, kuriame yra komiksų puslapiai / vaizdai.
4. Norėdami sukurti archyvą, naudokite komandą TAR su atitinkamomis parinktimis. Pavyzdžiui, komanda gali atrodyti taip:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

Šiame pavyzdyje parinktis -c nurodo TAR sukurti naują archyvą, o parinktis -f nurodo išvesties failo pavadinimą (šiuo atveju comicbook.cbt). Nurodę parinktis, pateikiate failų, kuriuos norite įtraukti į archyvą, pavadinimus (puslapis1.jpg, puslapis2.jpg, puslapis3.jpg).

5. Įvykdžius komandą, TAR įrankis sukurs komiksų archyvo failą (šiame pavyzdyje comicbook.cbt) esamame kataloge.

Kai turėsite komiksų archyvo failą, galite naudoti įvairią komiksų skaitytuvo programinę įrangą arba programas, kad atidarytumėte ir skaitytumėte komiksus savo kompiuteryje ar įrenginyje. Šios programos paprastai teikia tokias funkcijas kaip puslapio naršymas, mastelio keitimas ir žymėjimas, kad pagerintų skaitymo patirtį.

## Kas yra CBA faile?

Komiksų archyvo (CBA) faile, sukurtame naudojant TAR archyvavimo įrankį, yra atskirų komiksų puslapių arba vaizdų, sujungtų į vieną failą, rinkinys. Konkretus archyvo turinys priklauso nuo supakuotos komiksų knygos.

Paprastai komiksų archyvo faile yra:

- **Komiksų puslapiai:** Pagrindinis archyvo turinys yra patys komiksų puslapiai. Šie puslapiai paprastai išsaugomi kaip atskiri vaizdo failai, pvz., JPEG arba PNG, vaizduojantys kiekvieną komikso puslapį. Puslapiai išdėstyti tam tikra tvarka, kad būtų išlaikytas komikso pasakojimo srautas.
- **Metadata:** Some Comic Book Archive formats may include metadata about the comic book, such as the title, author, publisher, publication date, and description. This information helps identify and categorize the comic book.
– **Papildomi failai:** be komiksų puslapių ir metaduomenų, archyve gali būti ir kitų su komiksu susijusių papildomų failų. Šie failai gali būti viršelio menas, reklaminiai vaizdai, papildomas turinys arba tekstiniai failai, kuriuose pateikiama papildomos informacijos ar komentarų.

## Koks yra CBA failo formatas?

Komiksų archyvo (CBA) failo formatas, sukurtas naudojant TAR archyvavimo įrankį, paprastai yra TAR formatu. TAR, trumpinys juostos archyvas, yra failų archyvavimo formatas, dažniausiai naudojamas Unix ir Linux sistemose. Tai nėra būdinga komiksams, bet yra bendros paskirties archyvavimo formatas.

TAR formatas yra paprastas būdas sujungti kelis failus į vieną archyvo failą. Jis pats savaime nesuglaudina, todėl gautas TAR failas gali būti didelis, palyginti su kitais suglaudintais formatais, pvz., ZIP arba RAR. Tačiau TAR failus galima suspausti naudojant papildomus įrankius arba derinti su glaudinimo algoritmais, pvz., gzip arba bzip2, kad būtų sumažintas failo dydis.

TAR formatas išsaugo failų struktūrą, failų leidimus ir įtrauktų failų laiko žymas. Ji saugo failus paeiliui archyve, todėl galima lengvai išgauti atskirus failus arba visą archyvą.

## Nuorodos
* [Komiksų archyvas](https://en.wikipedia.org/wiki/Comic_book_archive)


