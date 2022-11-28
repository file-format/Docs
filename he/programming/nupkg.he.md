{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ NUPKG - קובץ חבילת NuGet",
  "description":"למד על פורמט קובץ NUPKG וממשקי API שיכולים ליצור ולפתוח קובצי NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## מהו קובץ NUPKG?

קובץ NUPKG הוא קובץ חבילה המכיל קוד מקור לשימוש תוכנת NuGet ליצירת חבילות לשימוש בפרויקטי NET. רכיב NuGet Package Manager מותקן כחלק מ-Microsoft Visual Studio עבור שליפת חבילות ממאגר אחסון חבילות מקוון. קובצי NUPKG עוזרים למפתחים להביא את החבילות העדכניות ביותר מ-[Nuget.org](https://nuget.org) באמצעות NuGet Package Manager במקום להוריד ולהתקין ידנית את חבילות הפיתוח. קובצי NUPKG בנויים מקובצי NUSPEC, וכאשר הם מועברים, התקן את החבילה במערכת המשתמש.

## פורמט קובץ NUPKG

קובצי NUPKG הם [ZIP](/he/compression/zip/) ארכיונים המכילים את הספריות הארוזות בתוכם. לאחר ההורדה, ניתן לשנות את שמו ל-.zip ולחלץ אותו עם כל כלי עזר zip סטנדרטיים כמו WinZIP, 7-Zip ו-Apple Archive Utility.

## התייחסות

* [Nuget.org](https://nuget.org)
* [התחלה מהירה: התקן והשתמש בחבילה ב-Visual Studio (Windows בלבד)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- סטוּדִיוֹ)
* [כיצד ליצור ולפרסם חבילת Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

