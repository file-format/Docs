{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad HTACCESS - Formáid Comhaid Apache HTACCESS",
  "description": "Do threoir formáid comhaid chun a fháil amach cad is comhad HTACCESS ann",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-gas"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad HTACCESS ann?

Comhad cumraíochta Apache is ea comhad HTACCESS a sholáthraíonn meicníocht chun athruithe cumraíochta a cheadú d’fhillteáin/eolairí éagsúla de shuíomh Gréasáin. Áiríonn sé treoracha cumraíochta atá infheidhme maidir leis an eolaire agus na fo-eolaire.

Déanann comhad HTACCESS roinnt seiceálacha ar nós leathanach innéacs an tsuímh Ghréasáin a shainiú, an leathanach earráide 404 (Leathanach Gan Aimsiú) a liostú, athsheolaidh leathanach 301 nó 302 a dhéanamh, rochtain a bhlocáil ó sheoladh IP ar leith nó ó shuíomhanna Gréasáin eile. Mar sin, cuireann úsáid comhaid .htaccess moill ar fheidhmíocht fhoriomlán do fhreastalaí Apache HTTP.

## Formáid Chomhaid HTACCESS

Stóráiltear comhaid HTACCESS go diosca i bhformáid gnáth-théacs. Ciallaíonn sé seo gur féidir leat na comhaid seo a oscailt agus a chur in eagar in aon eagarthóir téacs. Níl aon ainm roimh an . i gcomhad .htaccess, a thaispeánann gur comhad folaithe é laistigh den fhillteán.

## Úsáidí coitianta Comhad HTACCESS

Seo a leanas cúig úsáid choitianta a bhaineann le comhad HTACCESS.

### Mod_Athscríobh

Is féidir comhad HTACCESS a úsáid chun an chaoi a dtaispeántar URLanna agus leathanaigh ghréasáin ar shuíomh Gréasáin a ainmniú agus a athrú do na húsáideoirí.

### Fíordheimhniú

Is féidir fíordheimhniú a bhaint amach le .htaccess trí chomhad pasowrd a chruthú ar a dtugtar .htpasswd. Ligeann sé seo do chuairteoirí an tsuímh pasfhocal a sholáthar más mian leo cuairt a thabhairt ar chuid áirithe den leathanach gréasáin.

### Leathanaigh Earráide Saincheaptha

Is féidir leat leathanaigh earráide saincheaptha a chruthú ar nós 400 Drochiarratas, 401 Údarú ag Teastáil, 403 Leathanach Toirmiscthe, 404 Comhad gan Aimsiú agus 500 Earráid Inmheánach le comhad .htaccess. Mar sin féin, cuirfidh siad seo moill ar fheidhmíocht an tséasúir mar déanfar iad seo go léir a sheiceáil de réir mar a bhíonn rochtain ar na leathanaigh.

### Cineálacha MIME

Is féidir comhaid Apache HTACCESS a mhionathrú chun cineálacha Eisínteachtaí Ilchuspóireacha Ríomhphoist Idirlín (MIME) a áireamh. Ligeann sé seo do fhreastalaí chun tacú le seachadadh na gcomhad feidhmchláir nach bhfuil tacaíocht ag an suíomh.

### SSI

Feidhmíonn Taobh an Fhreastalaí (SSI) mar shábhálaí ama iontach ar shuíomh Gréasáin. Is féidir SSI a chumasú ach an cód seo a leanas a chur isteach i do chomhad .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Sampla Comhad Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Tagairtí

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

