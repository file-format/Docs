
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS File - APK Set Archive",
  "description":"További információ arról, mi az APKS-fájl?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Mi az APKS fájl?

Az .apks kiterjesztésű fájl egy archív fájl, amely Android csomag **APK** fájlok gyűjteménye. Az APKS-fájlban található minden egyes APK-fájl az eszközök különféle szempontjainak figyelembevételével jön létre. Ide tartozik az architektúra, a nyelv, a képernyő sűrűsége és egyéb eszközfunkciók. Az APKS fájlokat a **bundletool** hozza létre. Az Android App Bundle összeállítására és az alkalmazáscsomagok különböző APK-kká konvertálására szolgál az eszközökön történő telepítéshez.

## APKS fájlformátum – További információ

Az APKS-fájlok tömörített fájlokként kerülnek mentésre [ZIP](/hu/compression/zip/) fájlformátumban.

## Hogyan lehet APKS fájlt generálni?

Amikor az Android App Bundle (AAB) készen áll, a viselkedését a Google Play Áruházban tesztelheti az eszközön való üzembe helyezéshez. E célból APKS-fájlok generálhatók AAB-fájlokból, és telepíthetők teszteszközökre a Google Android [bundletool] (https://developer.android.com/studio/command-line/bundletool) segítségével. Parancssori eszközöket biztosít az APKS archív fájl létrehozásához APK-kból a következő paranccsal.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Az APK-k eszközön való üzembe helyezéséhez az APKS-fájl aláírható az eszköz-aláírási információkkal az alábbiak szerint.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Hivatkozások

* [bundletool – parancssor](https://developer.android.com/studio/command-line/bundletool)

