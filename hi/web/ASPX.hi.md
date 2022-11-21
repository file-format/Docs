{
  "date" : "2019-10-11",
  "keywords" :["एएसपीएक्स", "एएसपीएक्स फाइल", "एएसपीएक्स फाइल फॉर्मेट", "एएसपीएक्स फाइल टाइप", "फाइल", "टाइप", "एएसपीएक्स फाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एएसपीएक्स फ़ाइल स्वरूप",
  "description" :"एएसपीएक्स फ़ाइल और एपीआई क्या है जो एएसपीएक्स फाइलें बना और खोल सकती है, यह जानने के लिए आपकी फ़ाइल प्रारूप मार्गदर्शिका।",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## एएसपीएक्स फ़ाइल क्या है?

.aspx एक्सटेंशन वाली फ़ाइल वेब सर्वर पर चल रहे Microsoft ASP.NET फ्रेमवर्क का उपयोग करके उत्पन्न एक वेबपेज है। एएसपीएक्स का अर्थ एक्टिव सर्वर पेज एक्सटेंडेड है और ये पेज यूजर एंड पर वेब ब्राउजर में तब प्रदर्शित होते हैं जब यूआरएल एक्सेस किया जाता है। यह [ASP](/hi/web/asp/) तकनीक का उत्तराधिकारी है जो सर्वर के अंत में भी उत्पन्न होता है लेकिन .NET फ्रेमवर्क का उपयोग नहीं करता है। ASP.NET पृष्ठों में [C#](/hi/programming/cs/) या [VB.NET](/hi/programming/vb/) स्क्रिप्ट शामिल हो सकती हैं जो वेब ब्राउज़र में उपयोगकर्ता को प्रस्तुत करने के लिए वेब सर्वर द्वारा HTML में अनुवादित की जाती हैं। ASPX पेज को .NET वेब फॉर्म भी कहा जाता है। इन्हें Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ और किसी भी टेक्स्ट एडिटर जैसे एप्लिकेशन के साथ खोला और बनाया जा सकता है।

## एएसपीएक्स फ़ाइल स्वरूप

ASP.NET वेब फॉर्म वेब एप्लिकेशन के साथ इंटरेक्शन के लिए इवेंट-संचालित मॉडल पर आधारित होते हैं। ब्राउज़र, एक अंतिम उपयोगकर्ता होने के नाते, सर्वर को एक वेब फ़ॉर्म सबमिट करता है और सर्वर प्रतिक्रिया में एक पूर्ण मार्कअप पृष्ठ या HTML पृष्ठ लौटाता है। ASP.NET घटक मॉडल ASPX पृष्ठों के लिए ऑब्जेक्ट मॉडल प्रदान करता है। यह मॉडल वर्णन करता है:

* लगभग सभी एचटीएमएल तत्वों या टैग के सर्वर साइड समकक्ष, जैसे \<form> तथा \<input> .
* सर्वर नियंत्रण, जो जटिल यूजर-इंटरफेस विकसित करने में मदद करते हैं। उदाहरण के लिए, कैलेंडर नियंत्रण या ग्रिडव्यू नियंत्रण।

ASPX फ़ाइलें इन पृष्ठों के निर्माण के लिए ASP.NET **कोड बिहाइंड मॉडल** का उपयोग करती हैं।

### इन-लाइन कोड

नमूना कोड जो एएसपीएक्स पेज में इनलाइन एम्बेड किया गया है और उपयोगकर्ता कार्यान्वयन के लिए सभी कार्यक्षमता प्रदान करता है। निम्नलिखित [सी#](/hi/ प्रोग्रामिंग/सीएस/) कोड नमूना एएसपी.नेट पेज का प्रतिनिधित्व करता है जिसमें इन-लाइन कोड शामिल है:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### कोड के पीछे

प्रेजेंटेशन लॉजिक से HTML को अलग करने के लिए कोड को अलग क्लास फाइल में लिखा और स्टोर किया जा सकता है। यह प्रस्तुति परत को निष्पादन योग्य कोड से स्वतंत्र बनाता है। उपयोगकर्ता को प्रस्तुतिकरण के लिए कोड-बैक निम्नलिखित है।

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

प्रस्तुति परत के लिए वास्तविक तर्क का सी # कार्यान्वयन इस प्रकार है।

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## संदर्भ

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

