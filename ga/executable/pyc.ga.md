{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PYC agus APIanna ar féidir leo comhaid PYC a chruthú agus a oscailt.",
  "title": "Formáid Comhaid PYC- Comhad Tiomsaithe Python",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-gac"
}
},
  "lastmod": "2022-05-09"
}

## Cad is comhad PYC ann?

Is comhad aschuir tiomsaithe é comhad PYC a ghintear ó chód foinse atá scríofa i dteanga ríomhchlárúcháin Python. Nuair a reáchtáiltear comhad PY ag baint úsáide as ateangaire Python, déantar é a thiontú go bytecode lena fhorghníomhú. Ag an am céanna, déantar an bytecode tiomsaithe a shábháil freisin mar chomhad .pyc chun an taisce a athúsáid ag tráth níos déanaí más infheidhme.

## Struchtúr Formáid Chomhaid PYC

Tá comhaid PYC i seachchód agus níl a sonraíochtaí formáid comhaid ar fáil go poiblí. Mar sin féin, léiríonn imscrúdú ó roinnt foinsí go bhfuil an [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) comhdhéanta de:

 * `Uimhir draíochta ceithre bheart' - Níl ort ach dhá bheart a athraíonn le gach athrú ar an gcód marshalling, agus ansin dhá bhearta de 0d0a.
 * `Stampa ama modhnuithe ceithre bheart' - Stampa ama modhnuithe Unix den bhunchomhad a ghin an .pyc, ionas gur féidir é a thiomsú má athraíonn an fhoinse.
 * `Réad cód marshalled` - aschur marshal.dump an oibiachta cód atá mar thoradh ar an gcomhad foinse a thiomsú.

## CCanna

1. **Conas a ghintear comhad PYC?** Cruthaítear comhad PYC nuair a thiomsaítear cód foinse Python ag baint úsáide as an ateangaire Python. Stóráiltear an cód tiomsaithe sa chomhad PYC ansin.

1. **An bhfuil PYC níos tapúla ná py?** Déantar comhaid PYC a shábháil tar éis cód foinse python a thiomsú. Ós rud é go bhfuil siad seo léirithe cheana féin, tá na comhaid seo níos tapúla ná comhaid .py.

1. **Cad é an difríocht idir an comhad py agus pyc?** Tá comhad cód foinse Python do chlár i gcomhaid PY, agus bíonn seachchód léirmhínithe feidhmchláir i gcomhaid .pyc.

1. **An comhad dénártha é PYC?** Sea, is comhad dénártha é comhad PYC ina bhfuil uimhir draíochta 4 beart, stampa ama modhnuithe 4-bheart, agus réad cóid marshalled.

1. **An féidir linn .pyc a thiontú go .py?** Is féidir, is féidir comhaid pyc a thiontú go py. Is féidir dí-thiomsaitheoirí ar nós Decompyle++ a úsáid chun beart-chód Python tiomsaithe a aistriú ar ais go cód foinse Python atá bailí agus inléite ag an duine.

## Tagairtí

* [Struchtúr na gcomhad .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


