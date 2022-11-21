{
  "date" : "2019-10-11",
  "keywords" :["एएसएक्स", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "एएसएचएक्स", "एएसपी.नेट वेब हैंडलर फाइल"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एएसएचएक्स फाइल एक्सटेंशन - एक एएसपी.नेट वेब हैंडलर फाइल",
  "description" :"एएसएक्स फाइल क्या है और एपीआई जो एएसएक्स फाइलों को बना और खोल सकती है, के बारे में जानें।",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## एएसएचएक्स फाइल क्या है?

एएसएचएक्स फ़ाइल एक वेबपेज है जिसका उपयोग एएसपी.नेट एचटीटीपी हैंडलर द्वारा किया जाता है ताकि उपयोगकर्ता को इस फाइल के अंदर संदर्भित पृष्ठों के साथ सेवा प्रदान की जा सके। ASP.NET HTTP हैंडलर आने वाले अनुरोध को संसाधित करता है, .ashx फ़ाइल से पृष्ठों का संदर्भ देता है, और संकलित पृष्ठ को उपयोगकर्ता के ब्राउज़र पर वापस भेजता है। प्रसंस्करण की विधि ज्यादातर एएसपीएक्स फाइलों के समान होती है जिसमें भिन्नता होती है कि इस मामले में, संदर्भित पृष्ठों/दस्तावेजों को संसाधित किया जाता है और वापस भेजा जाता है।

## एएसएचएक्स फ़ाइल प्रारूप

.ashx फ़ाइलें सादे पाठ फ़ाइल प्रारूप में सहेजी जाती हैं और इसमें अन्य पृष्ठों या दस्तावेज़ों के संदर्भ होते हैं जो अनुरोध पर उपयोगकर्ता के ब्राउज़र पर वापस भेजे जाते हैं। इन्हें किसी भी टेक्स्ट एडिटर और डेवलपर आईडीई जैसे ज़ामरीन स्टूडियो, माइक्रोसॉफ्ट नोटपैड, नोटपैड ++ और कई अन्य में खोला जा सकता है। एएसएक्स फाइलें तब उपयोगी होती हैं जब आपके पास:
* बाइनरी फ़ाइलें
* गतिशील छवि दृश्य
* प्रदर्शन-महत्वपूर्ण वेब पेज
* एक्सएमएल फाइलें
* न्यूनतम वेब पेज

## एएसएक्स फ़ाइल को गतिशील रूप से कैसे संकलित करें?

Microsoft Visual Studio का उपयोग करके ASHX फ़ाइल को जोड़ने और संकलित करने के लिए निम्न चरणों का उपयोग किया जा सकता है।

* दृश्य स्टूडियो में एक सामान्य हैंडलर - हैंडलर1.ashx जोड़ें
* ऑटो-क्रिएट की गई सीएस फाइल को डिलीट कर दें।
* एएसएक्स फिर से खोलें,
** कोडबहाइंड को हटा दें = "हैंडलर1.ashx.cs"
** नीचे सी # कोड जोड़ें

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### एएसएचएक्स उदाहरण

निम्नलिखित एएसएक्स कोड छवि फ़ाइल को उपयोगकर्ता के अनुरोध पर लौटाता है जब एएसएक्स फ़ाइल को इंटरनेट ब्राउज़र में कहा जाता है।


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## संदर्भ

* [एएसएचएक्स फ़ाइल संकलित करें] (https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


