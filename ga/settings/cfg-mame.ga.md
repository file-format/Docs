{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"comhad cfg",
"cfg comhad cumraíochta mame",
"Cad is comhad cfg ann",
"Conas a oscailt cfg comhad",
"comhad",
"Síneadh comhad cfg",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid CFG - Comhad Cumraíochta MAME",
  "description": "Foghlaim faoi fhormáid Comhad Cumraíochta CFG MAME agus APIanna ar féidir leo comhaid CFG a chruthú agus a oscailt.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-ga",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Cad is comhad CFG ann?

Is comhad cumraíochta méarchláir XML é comhad CFG a úsáideann aithriseoirí cluiche físeán stua MAME. Is comhpháirt ríthábhachtach é chun rialuithe méarchláir agus eochracha te a shaincheapadh chun freastal ar roghanna an imreora. Stórálann na comhaid seo mapálacha agus socruithe a chinneann conas a idirghníomhaíonn an méarchlár le aithriseoir agus an cluiche á imirt. Tríd an gcomhad seo a chur in eagar, is féidir le húsáideoirí a n-eispéireas cluichíochta a shaincheapadh trí eochracha méarchláir ar leith a shannadh do ghníomhaíochtaí laistigh den chluiche, mar ionsá boinn, tosú, gluaiseacht agus feidhmeanna éagsúla eile.

## Comhad Cumraíochta MAME

Is feidhmchlár é MAME, a sheasann do **Multiple Arcade Machine Emulator**, a ligeann duit cluichí stuara a aithris agus a imirt ar do ríomhaire. Úsáideann MAME comhaid chumraíochta chun a iompar agus a socruithe a shaincheapadh. Go hiondúil bíonn na comhaid cumraíochta seo suite i bhfillteán `cfg` laistigh de d'eolaire MAME.

Seo na príomhchomhaid chumraíochta a d’fhéadfadh teacht ort agus tú ag socrú agus ag cumrú MAME:

1. **mame.ini:** Seo príomhchomhad cumraíochta do MAME. Tá socruithe domhanda ann a bhaineann le gach cluiche. Is féidir leat an comhad seo a fháil i bhfréamheolaire do shuiteáil MAME.

1. **default.cfg:** Stórálann an comhad seo socruithe réamhshocraithe do gach cluiche nach bhfuil a gcomhad cumraíochta féin acu. Úsáidtear é mar chúltaca le haghaidh socruithe a bhaineann go sonrach le cluiche.

1. **game-specific.cfg:** Úsáidtear na comhaid seo chun socruithe do chluichí aonair a stóráil. De ghnáth ainmnítear iad tar éis an chomhaid ROM le haghaidh cluiche a gcomhfhreagraíonn siad dó. Mar shampla, má tá cluiche ar a dtugtar pacman.zip agat, is é pacman.cfg an comhad cumraíochta dó.

Seo roinnt socruithe coitianta a d’fhéadfá a fháil i gcomhad cumraíochta MAME.

1. **rompath:** Sonraítear eolaire ina bhfuil do ROManna cluiche stuara suite.

1. ** cfg_directory:** Sonraítear eolaire ina stórálfar comhaid chumraíochta a bhaineann go sonrach le cluiche.

1. **nvram_directory:** Sonraítear eolaire ina stóráiltear comhaid RAM neamh-luaineach (NVRAM). Stórálann NVRAM scóir arda agus sonraí eile a bhaineann go sonrach le cluiche.

1. **artwork_directory:** Sonraítear eolaire ina stórálfar comhaid saothair ealaíne (cosúil le bezels, marquees, agus fógráin).

1. ** samplepath:** Sonraítear eolaire ina bhfuil comhaid fuaime samplacha suite.

1. **cheatpath:** Sonraítear eolaire ina bhfuil comhaid cheat suite.

Is féidir leat socruithe éagsúla eile a chumrú freisin ar nós roghanna físe agus fuaime, rialuithe agus gléasanna ionchuir. Chun na socruithe seo a mhodhnú, is féidir leat comhad cumraíochta a oscailt san eagarthóir téacs agus na hathruithe riachtanacha a dhéanamh.

## MAME

Is feidhmchlár é MAME, a sheasann do **Il-Stua Meaisín Aithriseoir,** atá deartha chun aithris a dhéanamh agus a mhacasamhlú ar chrua-earraí meaisíní stuara seanré agus consóil stuara. Ligeann sé d’úsáideoirí leabharlann ollmhór de chluichí stuara clasaiceacha a imirt ar ríomhairí nua-aimseartha agus ar ghléasanna comhoiriúnacha eile. Is tionscadal foinse oscailte é MAME agus tá sé tagtha chun bheith ina aithriseoir go dtí seo chun stair shaibhir cluichíochta stua a chaomhnú agus taitneamh a bhaint as.

1. ** Aithrise:** Is é príomhchuspóir MAME aithris chruinn a dhéanamh ar chrua-earraí meaisíní stua, lena n-áirítear a n-aonaid phróiseála lárnacha (LAPanna), sliseanna fuaime, sceallóga grafacha, agus gléasanna ionchuir. Cinntíonn an leibhéal cruinnis seo go n-iompraíonn cluichí chomh gar agus is féidir don taithí stuara bunaidh.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Caomhnú:** Ceann de phríomh-mhisin MAME ná stair an chearrbhachais stuara a chaomhnú. Trí aithris chruinn a dhéanamh ar chrua-earraí stuara, cabhraíonn MAME le cailliúint cluichí clasaiceacha a chosc agus cinntíonn sé gur féidir leis na glúnta atá le teacht dul i dtaithí orthu mar a bhí beartaithe ar dtús.

1. **Tosaigh:** Úsáideann go leor úsáideoirí feidhmchláir tosaigh a sholáthraíonn comhéadan grafach chun cluichí a bhainistiú agus a sheoladh trí MAME. Déanann na foircinn tosaigh seo níos éasca le nascleanúint a dhéanamh i leabharlann fairsing cluichí MAME.

## Conas comhad CFG a oscailt?

Cláir a osclaíonn nó a thagraíonn comhaid CFG

- MAME (Saor in Aisce) (Windows)
- ExtraMAME (Triail)
- MacMAME (MAC)

## Comhaid CFG eile

Seo cineálacha comhaid eile a úsáideann an síneadh comhad **.cfg**.

**Socruithe**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**cluiche**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Córas & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Tagairtí
* [MAME](https://en.wikipedia.org/wiki/MAME)


