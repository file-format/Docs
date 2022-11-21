{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"पीएएस - डेल्फी यूनिट सोर्स फाइल",
  "description":"पीएएस उदाहरण और एपीआई के साथ पीएएस फ़ाइल प्रारूप के बारे में जानें जो पीएएस फाइलें बना और खोल सकते हैं।",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## पीएएस फाइल क्या है?
एक .pas फ़ाइल वास्तव में एक स्रोत कोड फ़ाइल है जो डेल्फी प्रोग्रामिंग प्रोजेक्ट में पाई जा सकती है। डेल्फ़ी एक सॉफ़्टवेयर डेवलपमेंट एप्लिकेशन है जिसका उपयोग डेवलपर्स द्वारा विंडोज़ आधारित सॉफ़्टवेयर बनाने के लिए किया जाता है; डेल्फी भाषा में लिखा गया है। डेल्फी भाषा ऑब्जेक्ट पास्कल भाषा का एक प्रकार है। तो इसे डेल्फी कंपाइलर के साथ मूल Win32 कोड में संकलित किया जा सकता है।

## पीएएस फ़ाइल प्रारूप

PAS फ़ाइल स्वरूप एक कोडिंग फ़ाइल है जो डेल्फी इकाई स्रोत के लिए आरक्षित है। इकाइयों को डेल्फी ऐप्स के मुख्य बिल्डिंग ब्लॉक्स के रूप में महसूस किया जाता है। आप वर्तमान डेल्फी परियोजना के स्रोत कोड को **प्रोजेक्ट> स्रोत देखें** मेनू के माध्यम से देख सकते हैं। प्रोग्रामर एक इकाई को एक स्टैंड-अलोन फ़ाइल के रूप में बना और सहेज सकते हैं जिसका कोई भी प्रोजेक्ट उपयोग कर सकता है। एक बार परियोजना में एक इकाई जुड़ जाने के बाद, डेल्फी इसे परियोजना के उपयोग खंड में पंजीकृत करता है। डीपीआर फ़ाइल।

## पीएएस फ़ाइल उदाहरण
जब हम कोड की एक लाइन लिखते हैं। डेल्फ़ी हमारे लिए समझदारी से कई पंक्तियाँ लिखती है। सभी स्रोत कोड PAS फ़ाइल में लिखे गए हैं। निम्नलिखित डेल्फी स्रोत इकाई या पीएएस फ़ाइल का एक मूल उदाहरण है:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## संदर्भ

* [डेल्फी प्रोजेक्ट और यूनिट सोर्स फाइलों को समझना](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [अपना पहला डेल्फी प्रोग्राम लिखना](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

