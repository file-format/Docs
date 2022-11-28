{
  "date" : "2021-06-24",
  "keywords" :[ "חלק", "חלקי", "הרחבה", "קובץ", "פורמט", "אינטרנט", "הורדה" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"חלק - קובץ שהורד חלקית",
  "description":"למד על פורמט קובץ PART וממשקי API שיכולים ליצור ולפתוח קבצי PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## מהו קובץ PART? ##

קובץ חלק או סיומת .part הוא קובץ שהורד חלקית. הוא משמש כאשר הורדות מתבצעות או הופסקו עקב בעיה כלשהי, מה שנותן למנהל ההורדות הזדמנות לחדש את ההורדה בכל עת שאפשר.
המשמעות היא שהדפדפן, כגון Firefox או תוכניות העברת קבצים כמו eMule, eMule plus, FlashGet וכו' מאחסן חלק מהקובץ, הנקרא קובץ חלק, בזמן שההורדה מתרחשת במכשיר שלך. קובץ חלק זה יראה לך אם ההורדה מתבצעת או הופרעה לפני השלמתה. לא רק זה אלא שקובץ PART מאחסן את כל הנתונים עד להשלמת ההורדה וזו הסיבה שניתן לחדש חלק מהם מאוחר יותר אם תרצה להתחיל את ההורדה שוב.

## פורמט קובץ PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
