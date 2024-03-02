
{
  "date": "2022-02-06",
  "keywords": [
"comhad .apks",
"síneadh",
"formáid",
"Cartlann Socraigh APK",
"conas comhad .apks a oscailt",
"formáid comhaid apk"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad APKS - Cartlann Socraigh APK",
  "description": "Foghlaim faoi cad is comhad APKS ann?",
  "linktitle": "APKS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-apk-gas"
}
},
  "lastmod": "2022-02-06"
}

## Cad is comhad APKS ann?

Is comhad cartlainne é comhad le síneadh .apks ar bailiúchán de chomhaid ** APK** de phacáiste Android é. Gintear gach comhad APK aonair sa chomhad APKS agus gnéithe éagsúla de na gléasanna á gcur san áireamh. Ina measc seo tá ailtireacht, teanga, dlús scáileáin, agus gnéithe eile gléas. Gintear comhaid APKS trí **bundletool**. Úsáidtear é chun Bundle App Android a thógáil agus beart aipeanna a thiontú ina APKanna éagsúla le himscaradh ar fheistí.

## Formáid Comhaid APKS - Tuilleadh Eolais

Déantar comhaid APKS a shábháil mar chomhaid chomhbhrúite ag úsáid formáid comhaid [ZIP](/compression/zip/).

## Conas comhad APKS a ghiniúint?

Nuair a bheidh an Bundle App Android (AAB) réidh, is féidir a iompar ar Google Play Store a thástáil lena imscaradh chuig gléas. Is féidir comhaid APKS a ghiniúint, chun na críche seo, ó chomhaid AAB agus a shuiteáil ar ghléasanna tástála ag baint úsáide as Android [bundletool](https://developer.android.com/tools/bundletool) Google. Soláthraíonn sé uirlisí líne ordaithe chun an comhad cartlainne APKS a chruthú ó APKanna ag baint úsáide as an ordú seo a leanas.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Chun na APKanna a imscaradh chuig gléas, is féidir an comhad APKS a shíniú le faisnéis sínithe an ghléis mar a leanas.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Tagairtí

 * [bundletool - líne na n-orduithe]( https://developer.android.com/tools/bundletool)

