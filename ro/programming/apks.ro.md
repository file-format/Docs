
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier APK - Arhivă set APK",
  "description":"Aflați despre ce este un fișier APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Ce este un fișier APKS?

Un fișier cu extensia .apks este un fișier de arhivă care este o colecție de fișiere **APK** ale pachetului Android. Fiecare fișier APK individual din fișierul APKS este generat ținând cont de diferitele aspecte ale dispozitivelor. Acestea includ arhitectura, limba, densitatea ecranului și alte caracteristici ale dispozitivului. Fișierele APKS sunt generate de **bundletool**. Este folosit pentru a construi Android App Bundle și pentru a converti pachetul de aplicații în diferite APK-uri pentru implementare pe dispozitive.

## Format fișier APK - Mai multe informații

Fișierele APKS sunt salvate ca fișiere comprimate folosind formatul de fișier [ZIP](/ro/compression/zip/).

## Cum se generează un fișier APKS?

Când Android App Bundle (AAB) este gata, comportamentul său în magazinul Google Play poate fi testat pentru implementare pe un dispozitiv. Fișierele APKS pot fi generate, în acest scop, din fișiere AAB și instalate pe dispozitive de testare folosind [bundletool] Android al Google (https://developer.android.com/studio/command-line/bundletool). Oferă instrumente de linie de comandă pentru a crea fișierul de arhivă APKS din APK-uri folosind următoarea comandă.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Pentru a implementa APK-urile pe un dispozitiv, fișierul APK poate fi semnat cu informațiile de semnare a dispozitivului, după cum urmează.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referințe

* [bundletool - commandline](https://developer.android.com/studio/command-line/bundletool)

