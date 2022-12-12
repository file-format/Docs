{
  "date" : "2019-10-11",
  "keywords" :[ "fișier apk", "format fișier apk", "ce este un fișier apk", "fișier", "exemplu apk", "extensie fișier apk", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK – Ce este un fișier APK?",
  "description":"Aflați să știți ce este un fișier APK și API-urile care pot crea și deschide fișiere APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Ce este un fișier APK?

Un fișier cu extensia .apk este un fișier de aplicație Google Android care este utilizat pentru a instala aplicații (aplicații) pe dispozitivele Android. Este creat ca fișier executabil folosind IDE-ul oficial Google Android Studio și este încărcat în magazinul Google Play pentru a fi descărcat și instalat de utilizatorii finali. Fișierele APK pot fi generate și puse la dispoziție pentru instalare manuală și înainte de publicare în magazinul Google Play. Acest lucru ajută la testarea funcționalității și comportamentului fișierului pachet APK generat. Prin urmare, trebuie să vă asigurați că fișierul APK provine dintr-o sursă de încredere și nu conține niciun malware.

## Format de fișier APK

Fișierele APK sunt împachetate ca fiind comprimate în format de fișier [ZIP](/ro/compression/zip/), care poate fi deschis cu orice software de deschidere a fișierelor ZIP. Extensia .apk a unui astfel de fișier poate fi redenumită în .zip și deschide fișierul în orice aplicație ZIP sau extrage conținutul acestuia.

## Conținutul pachetului APK

Un singur fișier APK conține toate fișierele necesare care sunt necesare pentru instalarea și executarea acestuia. Un fișier APK, atunci când este extras cu o aplicație ZIP, conține următoarele fișiere și foldere.

* `META-INF/`: Director care conține fișierul manifest, semnătura și o listă de resurse din arhivă
* `lib/`: Director care conține cod compilat legat de platforme specifice, cum ar fi armeabi-v7a, x86, arm64-v8a etc.
* `res/`: Director care conține resurse necompilate, cum ar fi imagini
* `assets/`: Director care conține activele aplicațiilor, care pot fi preluate de AssetManager.
* `androidManifest.xml`: Conține numele, informațiile de versiune și conținutul fișierului APK
* `classes.dex`: Acestea sunt clase Java compilate care pot fi rulate pe mașina virtuală Dalvik și de către Android Runtime
* `resources.arsc`: fișierul de resurse compilat, cum ar fi șiruri de caractere

## Cum se instalează fișierul APK pe dispozitivul Android?

Pentru a instala un fișier APK pe dispozitivele dvs. Android, puteți utiliza următorii pași.

1. Descărcați APK-ul utilizând browserul web
2. Atingeți-l – ar trebui să puteți vedea cum se descarcă în bara de sus a dispozitivului dvs
3. După ce este descărcat, deschideți Descărcări, apăsați pe fișierul APK și apăsați Da când vi se solicită.

Urmând acești pași, va începe instalarea aplicației pe dispozitivul dvs.

## Referințe

* [Format fișier APK](https://en.wikipedia.org/wiki/Android_application_package)

