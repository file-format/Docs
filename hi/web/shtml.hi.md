{
  "date" : "2021-05-20",
  "keywords" :["shtml", "shtml फ़ाइल", "shtml फ़ाइल स्वरूप", "shtml फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "shtml फ़ाइल क्या है" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - सर्वर साइड में HTML फ़ाइल शामिल करें",
  "description":"SHTML फ़ाइल स्वरूप और API के बारे में जानें जो SHTML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## एक एसएचटीएम फ़ाइल क्या है?

.shtml एक्सटेंशन वाली फ़ाइल एक वेबपेज है जो [HTML](/hi/web/html/) में लिखा गया है और इसमें सर्वर निर्देश शामिल हैं। इसमें तेजी से लोड करने के लिए एएसपी फाइलों के समान सर्वर-साइड भी शामिल हो सकता है। सर्वर साइड फाइलों में एक्जीक्यूटेबल कोड भी हो सकता है जो सर्वर को सामान्य से धीमा लोड करने के लिए मजबूर कर सकता है। एसएचटीएम फाइलें एचटीएमएल के समान हैं लेकिन वे सरल सर्वर कमांड के उपयोग की भी अनुमति देते हैं। ये सर्वर कमांड एक साधारण कंप्यूटर प्रोग्रामिंग लैंग्वेज में किए जाते हैं जिसे सर्वर साइड इनक्लूड (SSI) कहा जाता है। [PHP](/hi/programming/php/) सहित अन्य सर्वर साइड प्रोग्रामिंग भाषाओं द्वारा SHTML का स्थान ले लिया गया है।

## एसएचटीएम फ़ाइल प्रारूप

SHTML फ़ाइलें सादे पाठ में लिखी जाती हैं और [SSI कमांड](https://www.w3.org/Jigsaw/Doc/User/SSI.html) का उपयोग करती हैं जिन्हें सर्वर साइड पर निष्पादित किया जाता है। इन सर्वर साइड कमांड का उपयोग डेटाबेस ड्राइवरों का उपयोग करके डेटाबेस से कनेक्ट करने और टेबल से उपयोगकर्ता डेटा लाने के लिए भी किया जा सकता है।

## एसएचटीएम उदाहरण

सर्वर साइड निर्देशों का उपयोग अनुप्रयोगों में किया जाता है जैसे पेज विज़िटर काउंटर या वेब पेज कैलेंडर। निम्न उदाहरण, उपयोगकर्ता डेटाबेस की पहली तीन पंक्तियों के पहले चार कॉलम प्रदर्शित करता है।

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## संदर्भ

* [सर्वर साइड शामिल है](https://en.wikipedia.org/wiki/Server_Side_Includes)

