{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - פורמט קובץ ארכיון ניתן להרחבה",
  "description":"למד על פורמט קובץ XAR וממשקי API שיכולים ליצור ולפתוח קובצי XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## מהו קובץ XAR?

קובץ עם סיומת .xar (Extensible Archive Format) הוא ארכיון UNIX שעשוי להיות בפורמט דחוס או לא דחוס. הוא משמש גם ב-Mac OS להתקנת חבילות. XAR הוא קוד פתוח והיה חלק מ-Mac OS X 10.5 לשימוש עם דפדפן Safari.

## פורמט קובץ XAR

לקובץ [XAR](https://github.com/mackyle/xar/wiki/xarformat) יש שלושה אזורים עיקריים.

* כותרת ראשית
* תוכן העניינים
* ערימה

### כותרת XAR

כותרת XAR בנויה כדלקמן.

|שדה|סוג נתונים|גודל בבתים|
---|---|---|
|Magic|Unsigned Int 32|4|
|גודל|Unsigned Int 16|2|
|גרסה|Unsigned Int 16|2|
|TOC Length דחוס|Unsigned Int 64|8|
|TOC Length Uncompressed|Unsigned Int 64|8|
|Checksum|Unsigned Int 32|4|
|שם תקציר ההודעה |Null Terminated||

ניתן להגדיר את מבנה C של כותרת XAR כדלקמן.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
שים לב שכל השדות של הכותרת (קסם, גודל, גרסה, toc_length_compressed, toc_length_uncompressed, cksum_alg) מאוחסנים תמיד בקבצי XAR בסדר בייט רשת (המכונה גם big endian).

### XAR תוכן העניינים (TOC)

תוכן העניינים הוא מסמך XML שהוא (וחייב) להיות מקודד כ-UTF-8. זה מאוחסן בתחילת הקובץ, מה שמקל על סריקה בארכיון כדי לחלץ קובץ בודד. ארכיון XAR מאפשר לך לדחוס/לקודד את הקבצים הבודדים בארכיון באופן עצמאי באמצעות סכימות דחיסה שונות כגון [GZIP](/he/compression/gz/), [BZIP2](/he/compression/bz2) ועוד דומים אחרים.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### ערימה

הערימה מתחילה מיד לאחר הטוק הדחוס. זוהי ערימה לא מובנית של נתונים שאליהם מתייחס ה-TOC. ערכי ההיסט הרשומים ב-TOC מתחילים מתחילת הערימה. ערכי האורך ב-toc מתייחסים למספר הבתים בפועל המאוחסנים בערימה (דחוסים או לא) בעוד שערך הגודל מתייחס לגודל המחולץ של הפריט (לאחר שחרור במידת הצורך).

## הפניות

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - ויקיפדיה](https://en.wikipedia.org/wiki/Xar_(archiver))

