{
  "date" : "2019-10-11",
  "keywords" :["cshtml", "cshtml फ़ाइल", "cshtml फ़ाइल स्वरूप", "cshtml फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "cshtml फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET रेजर वेबपेज",
  "description":"CSHTML फ़ाइल स्वरूप और API के बारे में जानें जो CSHTML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## CSHTML फ़ाइल क्या है?

.cshtml एक्सटेंशन वाली फ़ाइल एक [C#](/hi/programming/cs/) HTML फ़ाइल होती है जिसका उपयोग रेज़र मार्कअप इंजन द्वारा सर्वर साइड पर उपयोगकर्ता के ब्राउज़र में वेबपेज फ़ाइलों को रेंडर करने के लिए किया जाता है। यह सर्वर साइड कोडिंग मानक ASP.NET पेज के समान है, जो गतिशील वेब सामग्री निर्माण को सक्षम बनाता है क्योंकि वेबपेज ब्राउजर पर लिखा जाता है। ब्राउज़र में जेनरेट किए गए पेज को भेजने से पहले सर्वर पेज के अंदर सर्वर-साइड कोड को निष्पादित करता है। जटिल कार्य जैसे डेटाबेस तक पहुँचना और जटिल दृश्य प्रस्तुत करना। CSHTML फ़ाइलें Microsoft Visual Studio का उपयोग करके उत्पन्न और प्रोग्राम की जा सकती हैं।

## CSHTML फ़ाइल स्वरूप

CSHTML फाइलें टेक्स्ट फाइलें हैं जो रेजर मार्कअप इंजन द्वारा उल्लिखित सिंटैक्स का पालन करती हैं। रेज़र C# और VB.NET दोनों का समर्थन करता है, और यह क्लासिक ASP और ASP.NET की तुलना में सीखना और उपयोग करना आसान है। W3schools के पास [C# और VB.NET का सिंटैक्स](https://www.w3schools.com/asp/razor_syntax.asp) रेजर की कोडिंग के लिए एक सरल लेकिन प्रभावी गाइड है।

### CSHTML उदाहरण

रेज़र के लिए CSHTML फ़ाइल में उपयोग किया जाने वाला C# कोड उदाहरण निम्नलिखित है।

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

रेजर के लिए समतुल्य VB.NET कोड इस प्रकार है।

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## संदर्भ

* [रेजर सिंटैक्स संदर्भ - माइक्रोसॉफ्ट](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

