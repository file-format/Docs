{
  "date": "2023-03-22",
  "keywords": [
"comhad cnf",
"cad is comhad cnf ann",
"Conas a oscailt comhad cnf",
"comhad",
"síneadh comhad cnf",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid CNF - Comhad Cumraíochta MySQL",
  "description": "Foghlaim faoi fhormáid CNF agus APIanna ar féidir leo comhaid CNF a chruthú agus a oscailt.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf-ga",
      "parent": "settings"
}
},
  "lastmod": "2023-03-22"
}

## Cad is comhad CNF ann?

Úsáidtear comhad CNF (ar a dtugtar comhad cumraíochta freisin) i MySQL chun socruithe cumraíochta a stóráil don fhreastalaí MySQL. Féadfaidh suíomh an chomhaid CNF athrú ag brath ar an gcóras oibriúcháin agus ar an modh suiteála a úsáidtear. Cuimsíonn an chumraíocht go hiondúil socruithe éagsúla amhail ionchódú carachtar réamhshocraithe, am istigh, cumraíochtaí taisce agus maoláin, ar féidir iad a choigeartú chun feidhmíocht bhunachar sonraí a bharrfheabhsú bunaithe ar úsáid.

## Formáid Chomhaid CNF – Tuilleadh Eolais

Is féidir leat CNF a chruthú ag baint úsáide as na céimeanna seo a leanas i MySQL:

1. Oscail eagarthóir téacs m.sh. Notepad agus cruthaigh comhad nua.
2. Cuir na roghanna cumraíochta atá ag teastáil leis an gcomhad, ceann in aghaidh an líne. Seo sampla:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Sábháil an comhad le síneadh .cnf, mar shampla, mysql.cnf.
4. Bog an comhad chuig an eolaire cuí. Mar shampla, ar chórais Linux, d'fhéadfadh an t-eolaire a bheith /etc/mysql/conf.d/ or /etc/mysql/.
5. Atosaigh an freastalaí MySQL chun na socruithe cumraíochta nua a chur i bhfeidhm.

Bí cinnte aon athruithe a dhéantar ar an gcomhad CNF a thástáil i dtimpeallacht neamhtháirgthe sula gcuirtear i bhfeidhm iad i dtimpeallacht táirgthe.

## Conas comhad CNF a oscailt?

Is comhad téacs é an comhad CNF agus is féidir é a oscailt go héasca ag baint úsáide as aon eagarthóir téacs cosúil le Notepad. Is féidir leat é a oscailt freisin trí chliceáil ar dheis agus Open With a roghnú ón roghchlár. Nuair a bheidh an comhad oscailte, is féidir leat na socruithe cumraíochta a chur in eagar de réir mar is gá. Tá socruithe éagsúla ag CNF a bhaineann le freastalaí MySQL m.sh. uimhir phoirt, roghanna logála agus méideanna maoláin. Nuair a bheidh na socruithe curtha in eagar agat, sábháil na hathruithe agus dún an t-eagarthóir téacs. Ar deireadh atosú an freastalaí MySQL chun athruithe a chur i bhfeidhm.

Tabhair faoi deara go bhfuil sé tábhachtach a bheith cúramach agus an comhad cumraíochta MySQL á chur in eagar, mar is féidir le socruithe mícheart a chur faoi deara go n-iompraíonn an freastalaí gan choinne nó nach dtosóidh sé ar chor ar bith. Moltar cúltaca a dhéanamh den bhunchomhad sula ndéantar aon athruithe, ionas gur féidir leat é a chur ar ais más gá.

## Tagairtí
* [MySQL](https://ga.wikipedia.org/wiki/MySQL)


