{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid MKV",
  "keywords": [
"mkv",
"Físeán matroska",
"Formáid mkv",
"Conas a imirt comhaid mkv",
"físeán",
"comhad",
"formáid"
],
  "description": "Foghlaim faoi fhormáid comhaid MKV agus APIs ar féidir leo comhaid MKV a chruthú agus a oscailt.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-gav"
}
},
  "lastmod": "2020-17-11"
}


## Cad is Comhad MKV ann? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Tacaíocht do Lorg Fast.
- Cumas chun sruthanna fuaime agus físe éagsúla a roghnú.
- Tacaíocht d'fhotheidil (códaithe crua agus bogchódaithe).
- Tacaíocht do mheiteashonraí, caibidlí, agus biachláir.
- Cumas chun sruth ar líne.
- Cumas a ghnóthú comhaid earráideach a sholáthraíonn an cumas a imirt comhaid truaillithe.

## Stair Ghearr ##

Comhad MKV a tháinig i 2002 sa Rúis. Ba é Lasse Kärkkäinen an príomhfhorbróir a d'oibrigh le bunaitheoir Matroska, Steve Lhomme, agus foireann ríomhchláraitheoirí. Forbraíodh MKV mar thionscadal caighdeáin oscailte, rud a chiallaíonn go bhfuil sé foinse oscailte agus saor in aisce le húsáid. Le himeacht ama, feabhsaíodh an fhormáid agus rinneadh bunús le formáid ilmheán WebM in 2010.

## Dearadh Matroska ##

Cuireann Matroska na srianta seo a leanas leis an tsonraíocht EBML.

- Caithfidh **matroska a bheith i **DocType** an Cheanntásc EBML**.
- Caithfidh **EBMLMaxIDLength** ** Ceanntásc EBML** a bheith 4.
- Caithfidh **EBMLMaxSizeLength** an ceanntásc **EBML** a bheith idir 1 agus 8 (san áireamh).

Déantar na heilimintí barrleibhéil ar fad a chódú i 4 octets.

- Cóid teanga: Bhain Matroska (leagan 1 go dtí 3) úsáid as cóid teanga ar féidir a bheith ina bhfoirm bhibleagrafaíochta ISO-639-2 de 3 litir (cosúil le fre” don Fhraincis), nó d’fhéadfaí cód tíre breise a úsáid mar fre-ca  don Fhraincis Cheanada. Ag tosú le Matroska leagan 4, FÉIDIR ISO 639-2 nó BCP 47 a úsáid le haghaidh cóid teanga, cé go moltar BCP 47.
- Cineálacha Fisiceacha: Tá brí éagsúil acu seo le haghaidh comhaid fuaime agus físe araon. Mar shampla, ciallaíonn ChapterPhysicalEquiv = 60 (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) le haghaidh fuaime agus (DVD / VHS / LASERDISC) le haghaidh físeáin.
- Struchtúr Bloc - Ceanntásca Bloc: Tá faisnéis i gceannteideal an bhloic maidir le huimhir riain, stampaí ama, an cineál lacing, etc.
- Lacing: Is meicníocht é chun spás a shábháil nuair a bhíonn sonraí á stóráil a úsáidtear de ghnáth le haghaidh bloic bheaga sonraí (frámaí). Tá 3 chineál lacing ann:
  - "Xiph: Fráma le iolraí méide de 255 códaithe le 0 ag deireadh an mhéid. Mar shampla, is é an cód le haghaidh 765 ná 255; 255; 255; 0."
  - "EBML: Déantar méid an fhráma a chódú mar dhifríocht idir an méid roimhe seo agus an méid seo. Níl an chéad mhéid sa lása gan síniú ach úsáideann daoine eile athrú raoin chun comhartha a fháil ar gach luach."
  - "méid seasta: Fanann an méid mar a chéile."
- Struchtúr SimpleBlock: Tá sé spreagtha ag an struchtúr bloc** agus is é an príomhdhifríocht ná bratacha **Keyframe** agus **Indisardable** a chur leis. Seachas sin, tá gach rud mar an gcéanna.

## Struchtúr Matroska ##

Caithfidh doiciméad Matroska a bheith comhdhéanta de **Doiciméad EBML** amháin ar a laghad agus úsáid á baint as **Cineál Doiciméid Matroska**. Caithfidh **Ceanntásc EBML** tosú le gach **Doiciméad EBML** agus an **Fréamhghné EBML** ina dhiaidh sin a shainmhínítear mar Dheighleog. Sainmhíníonn Matroska roinnt Eilimintí Barrleibhéil a d’fhéadfadh tarlú laistigh den **Deighleog**.

Úsáideann EBML córas Eilimintí chun Doiciméad EBML a chumadh, Seo a leanas liosta na n-eilimintí Barrleibhéil sa chomhad Matroska:

- **Doiciméad EBML**: Fillteán don chomhad iomlán.
- **Ceanntásc EBML**: Tá an fhaisnéis ceanntásc ann don chomhad amhail DocType.
- **Deighleog**: An eilimint uachtarach ina bhfuil gach eilimint barrleibhéil eile.
- **SeekHead**: Tá suíomh Deighleoga Eilimintí Barrleibhéil eile ann.
- **Eolas**: Tá faisnéis ghinearálta ann faoin Deighleog.
- **Rianta**: Gné Barrleibhéil faisnéise agus cur síos ar go leor rianta.
- **Chapters**: It is used to define basic menus and partition data.
- **Braisle**: An Eilimint Barrleibhéil ina bhfuil struchtúr na mBloc.
- **Cues**: Eilimint Barrleibhéil ina bhfuil na hiontrálacha go léir atá suite go háitiúil don Deighleog agus a luasann lorg rochtana.
- **Ceangaltáin**: Tá comhaid ceangailte leis seo.
- **Clibeanna**: Tá meiteashonraí sa eilimint seo a chuireann síos ar Rianta, Eagráin, Caibidlí, Ceangaltáin, nó an Deighleog ina iomláine.

Taispeánann an tábla seo a leanas struchtúr an doiciméid Matroska agus an chuid is mó de na heilimintí ar taispeáint san ordlathas:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Ceanntásc EBML | | | |
| Deighleog | SeekHead| Lorg | SeekID |
| | | | SeekPosition |
| | Eolas | DeighleogUID | |
| | | Deighleog Ainm an Chomhaid | |
| | | Roimhe Seo | |
| | | RoimheAinm an Chomhaid | |
| | | Ar AghaidhUID | |
| | | NextAinm comhaid | |
| | | DeighleogFamily | |
| | | CaibidilAistrigh | |
| | | Scála Stampa Ama | |
| | | Fad | |
| | | DátaUTC | |
| | | Teideal | |
| | | MuxingApp | |
| | | WritingApp | |
| | Traiceanna | TrackIontráil | Uimhir Rian |
| | | | TrackUID |
| | | | Cineál Rian |
| | | | Ainm |
| | | | Teanga |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Físeán | Brat Idirléite |
| | | | | Ordú Réimse |
| | | | | SteirióMód |
| | | | | AlfaMód |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | TaispeáinWidth |
| | | | | TaispeáinAirde |
| | | | | Cineál Cóimheas Gné |
| | | | | Dath |
| | | | Fuaime | Minicíocht Samplála |
| | | | | Cainéil |
| | | | | GioDdepth |
| | caibidlí | EagránEntry | EagránUID |
| | | | EagránFlagHidden |
| | | | EagránFlagDefault |
| | | | EagránFlagOrdered |
| | | | CaibidilAtom | CaibidilUID |
| | | | | CaibidilStringUID |
| | | | | CaibidilTimeStart |
| | | | | CaibidilTimeDeireadh |
| | | | | CaibidilFlagHidden |
| | | | | Taispeántas Caibidil | ChapString |
| | | | | | Séiplíneacht |
| | Braisle | Stampa Ama |
| | | Amhráin Chiúin |
| | | Seasamh |
| | | Réamhmhéid |
| | | SimpleBlock |
| | | BlockGrúpa |
| | | EncryptedBlock |
| | Leideanna | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Ceangaltáin | Comhad Ceangailte | ComhadCur Síos |
| | | | Ainm an Chomhaid |
| | | | CineálCime |
| | | | FileUID |
| | | | Atreoraithe Comhad |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Clibeanna | Chlib | Spriocanna | SpriocCineálLuach |
| | | | | Cineál Sprioc |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagTeanga |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagDénártha |
| | | | | SimpleTag |


### Ag baint úsáide as codecs ###

Mura dteastaíonn seinnteoir meáin nua uait agus más fearr leat an t-imreoir atá agat cheana féin a úsáid, beidh ort roinnt codecs a shuiteáil (luathghaire le haghaidh comhbhrú/dí-chomhbhrú). Cé gur rogha bhailí é codecs a íoslódáil, ba chóir duit a bheith cúramach faoin bhfoinse agus d’fhéadfadh go mbeadh malware iontu.

## Tagairtí ##

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

