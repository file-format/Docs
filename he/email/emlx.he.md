{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail Format File",
  "description":"למד על פורמט קובץ EMLX וממשקי API שיכולים ליצור ולפתוח קובצי EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ EMLX?

פורמט הקובץ EMLX מיושם ומפותח על ידי אפל. אפליקציית Apple Mail משתמשת בפורמט הקובץ EMLX לייצוא האימיילים. ישנם גם יישומים אחרים שיכולים לפתוח את קבצי EMLX ולהמיר אותם לפורמטים אחרים של קבצים.

## היסטוריה קצרה של פורמט קובץ EMLX

מערכת ההפעלה Mac OS X אימצה את תוכנת האימייל הקיימת, NeXTMail, שנוצרה על ידי NeXT כחלק ממערכת ההפעלה NeXTSTEP. אפל, לאחר שרכשה את NeXT, העלתה את התכונות שלה והיא הפכה כעת לאפליקציית הדואר האלקטרוני של Apple Mail המשמשת כלקוח דואר ברירת המחדל. הודעות דוא"ל המיוצאות באמצעות Apple Mail נשמרות ישירות כקבצי EMLX. בנוסף, זהו לקוח הדואר המוגדר כברירת מחדל עבור קבצי EMLX כאשר מישהו פותח אותם על ידי לחיצה כפולה על Mac OS.

## פורמט קובץ EMLX

קבצי EMLx הם קבצים מבוססי טקסט פשוטים שניתן לפתוח בכל עורך טקסט כמו פנקס רשימות. מבנה הקובץ EMLX מורכב משלושה חלקים:

* ספירת בתים עבור ההודעה - אורך ההודעה עצמה, כתוב ב-ASCII בעשרוני, מסתיים ב-0x0a
* ההודעה עצמה
* Metadata של הודעה בצורה של XML plist

ניתן להסביר את אלו טוב יותר בעזרת הודעת דוא"ל לדוגמה שחולצה מ-Apple Mail כ-EMLX ופתיחה בעורך טקסט.

### EMLX דוגמה

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1] (******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

בדוגמה זו, ה-875 מציג את האורך הכולל של ההודעה. המטא נתונים של ההודעה מוקפים ב-<plist> התגים והדגלים הם כמתואר כדלקמן:

|שדה|תיאור|ערך
---|---|---|
|0|קרא|1 << 0
|1|נמחק|1 << 1
|2|ענה|1 << 2
|3|מוצפן|1 << 3
|4|מסוגל|1 << 4
|5|אחרונים|1 << 5
|6|טיוטה|1 << 6
|7|ראשוני (לא בשימוש עוד)|1 << 7
|8|העברה|1 << 8
|9|מנותב מחדש|1 << 9
|10-15|ספירת קבצים מצורפים|3F << 10 (6 סיביות)
|16-22|רמת עדיפות|7F << 16 (7 סיביות)
|23|חתום|1 << 23
|24|הוא זבל|1 << 24
|25|זה לא זבל|1 << 25
|26-28|גודל גופן delta|7 << 26 (3 סיביות)
|29|רמת דואר זבל נרשמה|1 << 29
|30|הדגש טקסט ב-toc|1 << 30
|31|(לא בשימוש)|

## ראה גם ##

* [EML](/he/email/eml/)
* [MSG](/he/email/msg/)

