
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ APK - ארכיון ערכת APK",
  "description":"למד על מהו קובץ APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## מהו קובץ APKS?

קובץ עם סיומת .apks הוא קובץ ארכיון שהוא אוסף של קבצי חבילת אנדרואיד **APK**. כל קובץ APK בנפרד בקובץ ה-APKS נוצר תוך שמירה על היבטים שונים של המכשירים. אלה כוללים ארכיטקטורה, שפה, צפיפות מסך ותכונות אחרות של המכשיר. קבצי APKS נוצרים על ידי **bundletool**. הוא משמש לבניית חבילת אפליקציות אנדרואיד והמרת חבילת אפליקציות ל-APKs שונות לפריסה במכשירים.

## פורמט קובץ APKS - מידע נוסף

קובצי APKS נשמרים כקבצים דחוסים בפורמט קובץ [ZIP](/he/compression/zip/).

## כיצד ליצור קובץ APKS?

כאשר ה-Android App Bundle (AAB) מוכן, ניתן לבדוק את ההתנהגות שלו בחנות Google Play לצורך פריסה במכשיר. ניתן להפיק, למטרה זו, קובצי APKS מקובצי AAB ולהתקין אותם במכשירי בדיקה באמצעות [bundletool] של גוגל (https://developer.android.com/tools/bundletool). הוא מספק כלי שורת פקודה ליצירת קובץ ארכיון APKS מ-APKs באמצעות הפקודה הבאה.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

על מנת לפרוס את חבילות ה-APK במכשיר, ניתן לחתום על קובץ ה-APKS עם פרטי החתימה של המכשיר כדלקמן.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## הפניות

* [bundletool - שורת פקודה](https://developer.android.com/tools/bundletool)

