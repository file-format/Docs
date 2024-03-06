{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par KIT faila formātu un API, kas var izveidot un atvērt KIT failus.",
  "title" : "KIT faila formāts — CodeKit fails",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit-lv",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Kas ir KIT fails?

Fails ar paplašinājumu .kit ir HTML fails, kas izveidots ar [CodeKit](https://codekitapp.com/) programmēšanas valodas lietojumprogrammu. Papildus esošajiem [HTML](/web/html/) failiem tajā ir ietverti importi un mainīgie, padarot to ideāli piemērotu statiskām vietnēm. CodeKit apkopo KIT failus HTML formātā, ko var viegli izmantot kā statiskus vietņu failus.

## KIT faila formāts

KIT faili ir HTML faili, kas papildus ietver importētos datus un mainīgos. Tie tiek saglabāti kā vienkārša teksta faili, un tos var atvērt ar jebkuru teksta redaktoru vai tīmekļa failu redaktoru.

### KIT failu importēšana

Gandrīz jebkura veida failus var importēt Kit failā. Tālāk ir norādīta importēšanas sintakse, ko izmanto, lai importētu failus .kit failā.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Kad imports tiek pievienots KIT failam un saglabāts, tas tiek aizstāts ar importējamā faila tekstu. Varat arī izmantot @include, nevis @import.

### Vairāki importi KIT failā

Varat arī importēt vairākus failus vienlaikus, izmantojot ar komatu atdalītu sarakstu:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Atsauces

* [Kas ir komplekts?](https://codekitapp.com/help/kit/)


