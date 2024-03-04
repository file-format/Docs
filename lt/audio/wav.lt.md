{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"failą",
"pratęsimas",
"formatu",
"garso mainų failo formatas",
"muzika"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WAV failo formatą ir API, kurios gali kurti ir atidaryti WAV failus.",
  "title": "WAV – bangos formos garso failo formatas",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-ltv"
}
},
  "lastmod": "2019-12-13"
}

## Kas yra WAV failas?

WAV, žinomas kaip WAVE (Waveform Audio File Format), yra Microsoft Resource Interchange File Format (RIFF) specifikacijos, skirtos skaitmeniniams garso failams saugoti, pogrupis. Formatas netaiko jokio suspaudimo bitų srautui ir saugo garso įrašus su skirtingu atrankos dažniu ir bitų dažniu. Jis buvo ir yra vienas iš standartinių garso kompaktinių diskų formatų. Wave failai yra didesni, palyginti su naujais garso failų formatais, tokiais kaip [MP3](/audio/mp3/), kurie naudoja nuostolingą glaudinimą, kad sumažintų failo dydį, išlaikant tą pačią garso kokybę. Tačiau WAV failus galima suspausti naudojant garso suspaudimo tvarkyklės (ACM) kodekus. Yra keletas API ir programų, kurios gali konvertuoti WAV failus į kitus populiarius garso failų formatus.

**Ar tu žinai?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WAV failo formatas ##

WAVE failo formatas, kuris yra Microsoft RIFF specifikacijos poaibis, prasideda failo antrašte, po kurios seka duomenų dalių seka. WAVE failas turi vieną WAVE dalį, kurią sudaro dvi dalys:

* „fmt“ dalis – nurodo duomenų formatą

* „duomenų“ dalis – yra tikrieji imties duomenys


### WAV failo antraštė ###

WAV (RIFF) failo antraštė yra 44 baitų ilgio ir yra tokio formato:


|Pozicijos|Pavyzdžio reikšmė|Aprašymas
---|---|---|
|1 - 4|RIFF|Pažymi failą kaip riff failą. Kiekvienas simbolis yra 1 baito ilgio.
|5–8|Failo dydis (sveikasis skaičius)|Bendro failo dydis – 8 baitai, baitais (32 bitų sveikasis skaičius). Paprastai tai užpildysite sukūrę.
|9 -12|WAVE|Failo tipo antraštė. Mūsų tikslams tai visada prilygsta BANGA.
|13-16|fmt|Formatuoti gabalų žymeklį. Apima nulį
|17-20|16|Formato duomenų ilgis, kaip nurodyta aukščiau
|21-22|1|Formato tipas (1 yra PCM) – 2 baitų sveikasis skaičius
|23-24|2|Kanalų skaičius – 2 baitų sveikasis skaičius
|25-28|44100|Sample Rate – 32 baitų sveikasis skaičius. Įprastos reikšmės yra 44100 (CD), 48000 (DAT). Mėginių dažnis = mėginių skaičius per sekundę arba hercai.
|29-32|176400|(Sample Rate * BitsPerSample * Kanalai) / 8.
|33-34|4|(BitsPerSample * Kanalai) / 8.1 – 8 bitų mono2 – 8 bitų stereo/16 bitų mono4 – 16 bitų stereo
|35-36|16|Bitai vienam pavyzdžiui
|37-40|duomenys|duomenų dalies antraštė. Žymi duomenų skyriaus pradžią.
|41-44|Failo dydis (duomenys)|Duomenų skyriaus dydis.
|Aukščiau pateiktos 16 bitų stereo šaltinio pavyzdinės reikšmės.

## Nuorodos Nr.

* [WAV – Vikipedija](https://en.wikipedia.org/wiki/WAV)


