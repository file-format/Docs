{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "rozšíření", "soubor", "formát", "web", "certifikát", "jazyk" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Formát souboru certifikátu",
  "description":"Další informace o formátu souboru CER a rozhraních API, která mohou vytvářet a otevírat soubory CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Co je soubor CER? ##

Soubor s příponou .cer je zodpovědný za uložení některých informací o certifikátu vlastníka a konkrétním veřejném klíči. Tento formát souborů nemůže ukládat soukromé klíče a má kapacitu pro uložení pouze jednoho certifikátu, kterým je x509. Speciálně zabezpečené certifikační autority jsou ty, které patří k HTTPS, důvěryhodnému a zabezpečenému protokolu pro procházení
CER je certifikát vašeho serveru. Obvykle jej obdrží certifikační autorita pro danou doménu. CER je většinou považován za stejný jako [CRT](/cs/web/crt/), ačkoli oba mají stejný formát certifikátu SSL, ale mají různé přípony souborů.
Ty lze v operačních systémech použít jednoduchým otevřením prohlížeče a kontrolou zabezpečení používaného prohlížeče nebo webové stránky.

## Stručná historie ##

V roce 1995 se Thawte stal prvním certifikačním orgánem pro řešení problému veřejných certifikátů SSL (secureed socket link) mimo USA. Poté existuje řada takových orgánů, která byla založena v letech 1995 až 2020.

## Formát souboru CER ##

Tyto soubory mohou být jednoduše
* PKC S#7 obsahuje Base64 ASCII kódování
* Jeho přípony souborů jsou p7b nebo p7cZ
* U binárního obsahu by certifikát byl DER nebo pkcs12/pfx.
Existuje mnoho typů souborů certifikátů s některými jedinečnými specifikacemi:
* .pem, když organizace usThawteificate řetězí tento formát, je dobře známo, že vytváří certifikáty
* .arm, je-li vyžadována metoda extrahování certifikace s vlastním podpisem, specifikovaný formát pro tento účel je .arm. Je reprezentován v kódování ASCII base-64.
* .der, Skládá se z binárních dat. To znamená, že jej lze použít pouze pro jeden certifikát
* .pfx (PKC512), Skládá se ze soukromého klíče odpovídajícího certifikátu vydaného CA nebo certifikátu s vlastním podpisem. Tento formát je dobře známý pro převod jedné implementace SSL na druhou.


