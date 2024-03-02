{
  "date": "2021-04-08",
  "keywords": [
"comhad deb",
"formáid comhaid deb",
"cad is comhad deb ann",
"comhad",
"sampla deb",
"síneadh comhad deb",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB - Cartlann Tarra Comhbhrúite Bzip",
  "description": "Foghlaim faoi fhormáid comhaid DEB agus APIanna ar féidir leo comhaid DEB a chruthú agus a oscailt.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-gab"
}
},
  "lastmod": "2021-04-09"
}

## Cad is comhad DEB ann?

Is formáid comhaid pacáiste dénártha Debian é comhad le síneadh .deb atá ar fáil chun pacáistí bogearraí a dháileadh ar Linux OS. Tá dhá [TAR](/compression/tar/) chomhad cartlainne ann. Soláthraíonn an DPKG meicníocht chun na pacáistí DEB a léamh agus a shuiteáil. Is féidir pacáistí DEB a shuiteáil ag baint úsáide as comhéadan bainistíochta bogearraí pacáiste APT. Tá Cineál Meán Idirlín ag comhaid DEB mar `app/vnd.debian.binary-package`.

## Formáid Chomhaid DEB

Tá dhá chomhad cartlainne [TAR](/compression/tar/) i gcomhad DEB. Coinníonn cartlann amháin an fhaisnéis rialaithe agus tá na sonraí insuiteáilte i gcartlann eile.

### Eagras Pacáiste

Is comhad cartlainne **ar** é an comhad DEB a bhfuil luach draíochta de `!<arch> `. Ós rud é Debian 0.93, tá trí chomhad in ord sonrach i meicníocht cartlannaithe comhaid DEB.

 1. `Debian Dénártha` - Tá sé i ndán go mbeidh sraith línte ann, scartha le línte nua. Faoi láthair, níl ach líne amháin i láthair a chuireann síos ar uimhir an leagain. Is í uimhir an leagain reatha ná 2.0.
 1. `Cartlann Rialaithe` - Tá cartlann control.tar ann ina bhfuil scripteanna cothabhála agus meiteaisnéis faoin bpacáiste mar ainm pacáiste, leagan, spleáchais agus cothaitheoir.
 1. `Cartlann Sonraí` - Is cartlann tarra í darb ainm data.tar agus tá na comhaid meán in-shuiteáilte iarbhír ann. Is féidir an chartlann a chomhbhrú le gz, bz2, lzma nó xz, agus athraíonn síneadh comhad na gcartlann sonraí dá réir.

### Cartlann Rialaithe

Is féidir inneachar mar seo a leanas a áireamh sa chartlann rialaithe.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * `md5sums` - Tá seiceálacha MD5 de gach comhad sa phacáiste ann chun comhaid truaillithe nó neamhiomlána a bhrath.
 * `conffiles` - Liostaíonn sé comhaid an phacáiste ar cheart déileáil leo mar chomhaid chumraíochta. Ní fhorscríobhtar comhaid chumraíochta le linn nuashonraithe mura sonraítear é.
 * `preinst`, postinst, prerm agus postrm - Scripteanna roghnacha a dhéantar roimh nó tar éis an pacáiste a shuiteáil nó a bhaint
 * Is script roghnach é `config` a thacaíonn leis an meicníocht cumraíochta debconf.
 * `shlibs` - Is liosta de na spleáchais leabharlainne roinnte é.

## Tagairtí

* [DEB - Vicipéid](https://ga.wikipedia.org/wiki/Deb_(file_format))

* [Formáid pacáiste dénártha Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


