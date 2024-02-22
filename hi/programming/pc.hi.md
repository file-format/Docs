{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "पीसी फाइल - प्रो*सी सोर्स कोड फाइल - .पीसी फाइल क्या है और इसे कैसे खोलें?",
  "description" : "पीसी प्रो*सी सोर्स कोड फ़ाइल और इसे खोलने के तरीके के बारे में जानें।",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-hi",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## पीसी फ़ाइल क्या है?

PC फ़ाइल या .pc फ़ाइल एक ProC स्रोत कोड फ़ाइल है। ProC एक प्रीकंपाइलर है जिसका उपयोग C या C++ कोड के भीतर SQL कथनों को एम्बेड करने के लिए Oracle डेटाबेस के साथ किया जाता है। जब आप Pro*C फ़ाइल संकलित करते हैं, तो यह एम्बेडेड SQL कमांड के साथ नियमित C या C++ कोड उत्पन्न करता है। यह आपको अपने C या C++ प्रोग्राम के साथ SQL डेटाबेस संचालन को सहजता से एकीकृत करने की अनुमति देता है।

प्रो*सी फ़ाइल कैसी दिख सकती है इसका मूल उदाहरण यहां दिया गया है:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

इस उदाहरण में, SQL कथनों को EXEC SQL के साथ उपसर्ग किया गया है ताकि यह दर्शाया जा सके कि वे एम्बेडेड SQL कथन हैं। फ़ाइल संकलित होने पर इन कथनों को Pro*C प्रीकंपाइलर द्वारा संसाधित किया जाएगा और Oracle डेटाबेस के साथ इंटरैक्ट करने के लिए उचित C कोड उत्पन्न किया जाएगा।

## पीसी फाइल कैसे खोलें?

एक पीसी फ़ाइल खोलने के लिए, आपको आमतौर पर एक टेक्स्ट एडिटर या एक इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (आईडीई) की आवश्यकता होती है जो सी या सी++ स्रोत कोड को संपादित करने का समर्थन करता है। यहां कुछ सामान्य विकल्प दिए गए हैं:

1.  **पाठ संपादक:**
    
- **नोटपैड** (विंडोज़)
- **टेक्स्टएडिट** (मैक)
- **गेडिट** (लिनक्स)
- **उत्कृष्ट पाठ**
- **परमाणु**
- **विजुअल स्टूडियो कोड**
2.  **एकीकृत विकास वातावरण (आईडीई):**
    
- **ग्रहण** सीडीटी (सी/सी++ विकास टूलींग) के साथ
- **विजुअल स्टूडियो** विज़ुअल सी++ के साथ या विज़ुअल स्टूडियो कोड सी++ एक्सटेंशन के साथ
- **कोड::ब्लॉक**
- **नेटबीन्स** सी/सी++ पैक के साथ
  
## संदर्भ
* [प्रो*सी](https://en.wikipedia.org/wiki/Pro*C)


