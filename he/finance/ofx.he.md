{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange Format File",
  "description":"למד על פורמט קובץ OFX וממשקי API שיכולים ליצור ולפתוח קובצי OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## מהו קובץ OFX?

קובץ OFX (Open Financial Exchange) הוא פורמט קובץ פיננסי המשמש להחלפת מידע פיננסי בין תוכנות ומוסדות פיננסיים. עם התפתחות פתרונות התוכנה לניהול חשבונות פיננסיים פנימיים, פותחו תוכנות שיכולות להתחבר לבנק שלך ולייבא או לייצא נתונים פיננסיים עם הבנקים. זה כולל נתונים פיננסיים כגון עסקאות, פרטי חשבון ותשלומי חשבונות. תוכנות כגון QuickBooks, Microsoft Money, Intuit ו-Quicken שומרות את הנתונים המיובאים כקובץ OFX.

סוג המדיה באינטרנט עבור פורמט קובץ OFX הוא application/x-ofx.

## פורמט קובץ OFX

קובצי OFX נשמרים בפורמט קובץ XML (Extensible Markup Language) ומשתמשים בתגים למבנה הנתונים. קבצי [XML](/he/web/xml/) מאוחסנים בפורמט קריא אנושי וניתן לפתוח ולערוך אותם בכל עורך טקסט כגון Notepad, Notepad++ או Apple TextEdit. הנתונים המאוחסנים בתוך קבצי OFX מבוססים על תקן **SGML (Standard Generalized Markup Language)**. נתונים המאוחסנים בתוך קובצי OFX כוללים בדרך כלל:

* מידע הקשור לבנקים
* פרטי כרטיס אשראי וחיוב
* מידע על חשבונות והשקעות
* כל עסקאות פיננסיות אחרות

### דוגמה לפורמט קובץ OFX

להלן מבנה הנתונים הפנימי ונתונים לדוגמה של קובץ OFX לדוגמה.

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

קובץ OFX לדוגמה זה מכיל את המידע הבא:

* פרטי חשבון בנק כגון שם בנק, מספר חשבון ויתרה
* רשימת העסקאות כולל תאריך, סוג וסכום של כל עסקה

את כל המידע הזה ניתן לייבא בתוכנת מימון אישי כדי לעקוב אחר תנועות והוצאות בחשבון.

## הפניות ##

* [בורסה פיננסית פתוחה - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [תקן ISO לחילופי נתונים אלקטרוניים](https://en.wikipedia.org/wiki/ISO_20022)

