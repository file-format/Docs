{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"comhad",
"síneadh",
"formáid",
"formáid comhaid idirmhalartaithe fuaime",
"Ceol"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid WAV agus APIs is féidir comhaid WAV a chruthú agus a oscailt.",
  "title": "WAV - Formáid Chomhaid Fuaime Tonnform",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-gav"
}
},
  "lastmod": "2019-12-13"
}

## Cad is comhad WAV ann?

Is fothacar é WAV, ar a dtugtar WAVE (Waveform Audio File Format), de shonraíocht Formáid Chomhaid Idirmhalartaithe Acmhainne (RIFF) Microsoft chun comhaid fuaime digiteacha a stóráil. Ní chuireann an fhormáid aon chomhbhrú i bhfeidhm ar an sruth giotán agus stórálann sí na taifeadtaí fuaime le rátaí samplála agus giotán rátaí difriúla. Bhí sé agus tá sé ar cheann de na formáid chaighdeánach do dlúthdhioscaí fuaime. Tá comhaid tonnta níos mó i méid i gcomparáid le formáidí nua comhaid fuaime mar [MP3](/audio/mp3/) a úsáideann comhbhrú cailleach chun méid an chomhaid a laghdú agus an caighdeán fuaime céanna á chothabháil ag an am céanna. Mar sin féin, is féidir comhaid WAV a chomhbhrú trí úsáid a bhaint as codecs Bainisteoir Comhbhrú Fuaime (ACM). Tá roinnt API agus feidhmchlár ar fáil ar féidir comhaid WAV a thiontú go formáidí comhaid fuaime eile a bhfuil tóir orthu.

**An raibh a fhios agat?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## Formáid Chomhaid WAV ##

Tosaíonn formáid comhaid WAVE, atá ina fothacar de shonraíocht RIFF Microsoft, le ceanntásc comhaid agus seicheamh smután sonraí ina dhiaidh. Tá smután amháin WAVE i gcomhad WAVE atá comhdhéanta de dhá fhoshamhail:

* a "fmt" smután - sonraítear an fhormáid sonraí

* a "sonraí" smután - tá na sonraí samplacha iarbhír


### Ceanntásc Comhad WAV ###

Tá ceanntásc comhaid WAV (RIFF) 44 beart ar fad agus tá an fhormáid seo a leanas aige:


|Poist|Luach Samplach|Cur Síos
---|---|---|
|1 - 4|RIFF|Marcáil an comhad mar chomhad riff. Tá gach carachtar 1 beart ar fad.
|5 - 8|Méid an chomhaid (slánuimhir)|Méid an chomhaid iomláin - 8 mbeart, i mbearta (slánuimhir 32-giotán). Go hiondúil, líonfá isteach é seo tar éis cruthú.
|9 -12|WAVE | Ceanntásc de Chineál Comhaid. Chun ár gcríoch, is ionann é i gcónaí WAVE.
|13-16|fmt | Marcóir smután formáide. Áirítear rian null
|17-20|16|Fad na sonraí formáide mar a liostaítear thuas
|21-22|1|Cineál formáide (is é PCM 1) - slánuimhir 2 bheart
|23-24|2|Líon na gCainéal - slánuimhir 2 bheart
|25-28|44100|Ráta Samplach - slánuimhir 32 beart. Is iad na comhluachanna ná 44100 (CD), 48000 (DAT). Ráta Samplach = Líon na Samplaí sa soicind, nó Hertz.
|29-32|176400|(Sample Rate * Cainéil BitsPerSample*)/8.
|33-34|4|(BitsPerSample * Cainéil) / 8.1 - 8 giotán mona2 - steirió 8 giotán / 16 giotán mono4 - steirió 16 giotán
|35-36|16|Giotán in aghaidh an tsampla
|37-40|sonraí|sonraí ceanntásc smután. Marcáil tús na rannóige sonraí.
|41-44|Méid an chomhaid (sonraí)|Méid na rannóige sonraí.
|Tugtar luachanna samplacha thuas le haghaidh foinse steirió 16-giotán.

## Tagairtí ##

* [WAV - Le Vicipéid]( https://ga.wikipedia.org/wiki/WAV)


