{
  "date": "2021-04-23",
  "keywords": [
"config Comhad",
"comhaid cumraíochta",
"config Formáid comhaid",
"síneadh",
"formáid",
"comhad cumraíochta git",
"Comhaid cumraíochta i Linux",
"cad is comhad cumraíochta ann",
"Cumraigh comhad php",
"sampla comhad config ssh",
"sampla comhad cumraíochta aws",
"sampla comhad cumraíochta python"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG - Comhad Cumraíochta",
  "description": "Foghlaim faoi fhormáid comhaid CONFIG le sampla CONFIG agus APIanna ar féidir leo comhaid CONFIG a chruthú agus a oscailt.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-gag"
}
},
  "lastmod": "2021-04-23"
}

## Cad is comhad CONFIG ann?
Tugtar comhad cumraíochta ar chomhad CONFIG; a úsáidtear chun paraiméadair agus socruithe príomhúla a chumrú do roinnt bogearraí ríomhaireachta. Ní léann roinnt bogearraí ach a **comhaid cumraíochta** nuair a thosaíonn siad. Seiceálann daoine eile na comhaid cumraíochta le haghaidh athruithe go tréimhsiúil.

## CONFIG Formáid comhaid
Úsáidtear an **formáid Comhad CONFIG** le haghaidh próisis fhreastalaí, feidhmchláir bogearraí agus socruithe córais oibriúcháin. Is féidir le ríomhchláraitheoir cód a scríobh chun treoir a thabhairt do bhogearraí na comhaid cumraíochta a léamh arís agus arís eile tar éis tréimhse áirithe ama agus na hathruithe a chur i bhfeidhm ar an bpróiseas reatha. Níl aon chaighdeáin chinntitheacha ná coinbhinsiúin láidre ann maidir le córas comhaid CONFIG. Mar shampla, baineann comhad Web.config Microsoft le formáid comhaid CONFIG, atá comhdhéanta de thacair clibeanna bunaithe ar [XML](/web/xml/); is féidir é a chur in eagar le Microsoft Visual Studio nó le haon eagarthóir téacs eile.

## Samplaí de chomhaid chumraíochta:
Ós rud é nach gcruthaítear na comhaid cumraíochta de réir rialacha, caighdeáin nó coinbhinsiúin ar bith, d'fhéadfadh na comhaid seo a bheith scríofa trí úsáid a bhaint as formáidí éagsúla. Seans go bhfuil comhad .config bunaithe ar XML, [JSON](/web/json/) nó ar fhormáid ar bith eile. Seo a leanas na samplaí de chomhaid chumraíochta do chórais oibriúcháin agus bogearraí aitheanta:

### Comhaid cumraíochta i Linux
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Catagóir|Sampla| Tuairimí|
---|---|---|
|Comhaid rochtana|/etc/host.conf|Insíonn sé don fhreastalaí fearainn líonra conas óstainmneacha a chuardach.|
|Booting agus logáil isteach/logout|/etc/rc.d/rc.local|Ní oifigiúil. Is féidir glaoch ó rc, rc.sysinit, nó /etc/inittab.|
|Córas comhaid|/etc/mtools.conf|Cumraíocht do na hoibríochtaí go léir (mkdir, cóip, formáid, etc.) ar chóras comhaid de chineál DOS.|
|Riarachán córais|/etc/shells|Sealbhaíonn sé liosta na sliogáin” a d'fhéadfadh a bheith ar fáil don chóras.|
|Líonra |/etc/gated.conf|Cumraíocht le haghaidh gated. Úsáidte ag an deamhan gated amháin.|
|Orduithe córais|/etc/logrotate.conf|Cumraíocht don Nascóir Dinimiciúla.|
|Daemons|/etc/httpd.conf|An comhad cumraíochta le haghaidh Apache, an freastalaí Gréasáin. De ghnáth ní bhíonn an comhad seo in /etc.|
|Cláir úsáideora| /etc/lynx.cfg| Socruithe seachfhreastalaí|
### Sampla comhaid AWS CONFIG
Is féidir na socruithe agus na dintiúir cumraíochta a úsáidtear go minic a shábháil i gcomhaid CONFIG atá á gcoimeád ag CLI AWS. Caithfidh an comhad CONFIG a bheith ina chomhad gnáth-théacs a úsáideann an fhormáid seo a leanas:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Sampla comhaid SSH CONFIG
Ainmnítear CONFIG ar chomhad cumraíochta cliant OpenSSH, agus tá sé stóráilte san eolaire .ssh. Tá an struchtúr seo a leanas i gcomhad SSH CONFIG:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Sampla comhaid Python CONFIG
D'fhéadfadh cuma mar seo a bheith ar chomhad Python CONFIG:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Tagairtí

 * [Comhaid cumraíochta Linux a thuiscint](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Comhaid cumraíochta i Python]( https://martin-thoma.com/configuration-files-in-python/)

