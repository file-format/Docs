{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier LRC - Ce este un fișier LRC?",
  "description":"Aflați despre fișierul LRC Lyric și API-urile care pot crea și deschide fișiere LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Ce este un fișier LRC?

Un fișier LRC este un fișier de versuri bazat pe text care conține versurile unui cântec audio. Când melodia audio este redată cu un player de muzică sau cu un software de redare audio pe un computer, fișierul LRC este citit în paralel și afișat în timp. Fișierele LRC conțin puncte cue pentru afișarea versurilor atunci când melodia este redată. În general, fișierele LRC au același nume ca fișierul audio corespunzător, cum ar fi audio.mp3 și audio.lrc. Fișierele LRC sunt similare cu fișierele de subtitrare, cum ar fi [SRT](/ro/video/srt/).

## Format de fișier LRC - Mai multe informații

Fișierele în format liric LRC sunt salvate ca fișiere text simplu și pot fi deschise și editate într-un fișier text. Conținutul unui fișier LRC conține informații de culoare pentru afișarea textului versurilor.

## Formate LRC

Există mai multe formate de fișiere LRC care au fost dezvoltate de-a lungul timpului. Aceste

### Format LRC simplu

Etichetele de timp de linie sunt în formatul [mm:ss.xx] unde mm reprezintă minute, ss este secunde și xx este sutimi de secundă.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Format simplu extins

Include abilitatea de a schimba și de a specifica genul versurilor folosind M: Masculin, F: Femeie, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Format LRC îmbunătățit

Formatul LRC îmbunătățit este o versiune extinsă a formatului Simple LRC. Se adaugă un Word Time Tag în format<mm:ss.xx> la sfârşitul cuvântului precedent.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referințe

* [Format de fișier cu versuri LRC - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

