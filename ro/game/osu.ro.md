{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier OSU și despre API-urile care pot crea și deschide fișiere OSU.",
  "title" : "Fișier OSU - Osu! Format de fișier script",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-ro",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Ce este un fișier OSU?

Un fișier OSU este un script de joc scris pentru osu! joc de ritm. Conține informații despre o hartă de beatmap folosită în joc, cum ar fi nivelul de dificultate, melodia care urmează să fie redată și momentele obiectelor lovite cu care jucătorul trebuie să se sincronizeze cu muzica. Le permite jucătorilor de jocuri de ritm să dezvolte provocări personalizate și să le împărtășească comunității de joc.

**Tipul MIME de format de fișier OSR:** x-osu-beatmap

## Format de fișier OSU

Fișierele OSU sunt salvate ca fișiere text simplu pe disc și structura acestuia este definită foarte clar în [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) de către osu!.

### Secțiuni în fișierul OSU

Un fișier OSU tipic are următoarele secțiuni.

|Sectiunea |Descriere |Tip de continut|
---|---|---|
|[General]| Informații generale despre beatmap| cheie: perechi valori|
|[Editor]| Setări salvate pentru editorul beatmap| cheie: perechi valori|
|[Metadate] |Informații utilizate pentru identificarea beatmap| perechi cheie:valoare|
|[Dificultate] |Setări de dificultate| perechi cheie:valoare|
|[Evenimente]| Beatmap și evenimente grafice storyboard| Liste separate prin virgulă|
|[Puncte de timp]| Puncte de sincronizare și control| Liste separate prin virgulă|
|[Culori]| Combo și culori ale pielii| cheie : perechi valori|
|[HitObjects]| Obiecte lovite| Liste separate prin virgulă|

## Referințe

* [OSU! Joc de ritm](https://osu.ppy.sh/home)

* [Format de fișier OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


