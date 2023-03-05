{
  "date" : "2019-10-11",
  "keywords" :["tpl", "tpl फ़ाइल", "tpl फ़ाइल स्वरूप", "tpl फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "tpl फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"टीपीएल - एचटीटीपी फ़ाइल सर्वर टेम्प्लेट",
  "description" :"टीपीएल फाइल बनाने और खोलने के लिए टीपीएल फाइल और एपीआई क्या है, इसके बारे में जानें।",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## टीपीएल फाइल क्या है?

.tpl एक्सटेंशन वाली फ़ाइल HTTP फ़ाइल सर्वर (HFS) द्वारा बनाई और उपयोग की जाने वाली एक टेम्प्लेट फ़ाइल है, जो FTP प्रोटोकॉल के बजाय वेब तकनीक HTTP पर फ़ाइलें भेजने और प्राप्त करने के लिए फ़ाइल साझा करने वाला एप्लिकेशन प्रोग्राम है। इसका उपयोग [HTML](/hi/web/html/) पृष्ठों को गतिशील रूप से उस टेम्पलेट जानकारी के आधार पर बनाने के लिए किया जाता है जिसे समान लेआउट, स्टाइल और स्क्रिप्ट के साथ सेटिंग करने के लिए परिभाषित किया गया है। जिन अनुप्रयोगों के लिए समान सेटिंग्स की आवश्यकता होती है, उन्हें समान टेम्पलेट फ़ाइल सौंपी जा सकती है और HFS इस टेम्पलेट फ़ाइल के आधार पर रनटाइम पर गतिशील रूप से अनुरोधित पृष्ठ लौटाएगा।


## टीपीएल फ़ाइल स्वरूप

टीपीएल फाइलें मानव पठनीय प्रारूप में संग्रहीत होती हैं और इसमें एचटीएमएल होता है जो मानव पठनीय मार्कअप भाषा है। एचटीएमएल के अतिरिक्त, एक टीपीएल फ़ाइल में टेम्पलेट स्तर सीएसएस और जावास्क्रिप्ट भी शामिल हो सकते हैं ताकि इस टेम्पलेट फ़ाइल से उत्पन्न सभी पृष्ठों द्वारा किए जाने वाले लेआउट और कार्यों को परिभाषित किया जा सके।

### टीपीएल अनुभाग

टीपीएल अनुभागों में एचटीएमएल, सीएसएस या जावास्क्रिप्ट कोड होता है जिसका उपयोग एचएफएस द्वारा आउटपुट पृष्ठ उत्पन्न करते समय किया जाता है। प्रत्येक खंड वर्ग कोष्ठक ([]) से शुरू होता है और प्रतिशत चिह्न (%) द्वारा परिभाषित किया जाता है। एक TPL फ़ाइल में निम्न अनुभाग हो सकते हैं।

#### टीपीएल स्टाइल सेक्शन

इसमें स्टाइलिंग संबंधी जानकारी शामिल है जो एम्बेड की गई CSS फ़ाइलों के संदर्भ का उपयोग कर भी सकती है और नहीं भी। स्टाइलिंग सेक्शन का एक उदाहरण इस प्रकार है।

```
[style]
.row { color: #666 }
span.size_file { font-size:10px; color:#666 }
.button, .big, .little, th { font-weight:normal; font-size:9pt; color:#222; }
#back { background:#222;border:1px solid #000;padding:5px;margin-top:10px;}
.little { font-size: 8pt; color:#2F4F4F;margin-top:10px; }
.path_title { color: #999;margin-top:10px; }
img { border-style:none }
.row { background:#f8f8f8;}
.row a { text-decoration:none; }
.comment { font-size:7pt; color:#666; background:#f3f3f3; padding:3px; border:1px solid #ccc; margin-top:2px; }
.column { color:#222; font-size:13pt; font-weight:bold; padding-bottom:0; }
.flag { font-weight:bold; font-size:8pt; background:#fff; color:#990000; text-align:center; border:1px solid #ff0000; }
.text { color:#222; }
span.desc { color: #999; }
#everything { margin-top:20px;border-top:1px solid #ccc;padding-top:10px; }
html {
font-size: 62.5%;
}
body {margin:0px; padding:0px; background-color:#fff; color:#222; font-family:"Lucida Grande", "Tahoma", "Helvetica", "Arial", sans-serif; font-size:120%;quotes:"\201C" "\201E" "\2018" "\2019";}
table, tr, td {font-size: inherit;}
a:link {color: #222;}
a:visited {color: #666;}
a:hover {	color: #000;}
a:active {}
a:focus {}
img, a img {border: none;}
#path {color: #333;background-color: #f8f8f8; border-bottom: 1px solid #ccc;padding: 3px 8px;margin: 0px;}
#path li {display: inline;padding-left: 13px; padding-right: 3px; background-image: url(arrow.gif);background-repeat: no-repeat;background-position: 1px 5px;}
#path span {font-weight: bold;}
#header {margin: 24px 48px;}
#header h1 {font-size: 250%;color: #222;  margin: 0;margin-bottom: 6px;}
#header h2 {font-size: 120%;color: #aaa;  margin: 0;}
#content { margin: 24px 48px;}
#footer {    margin-top: 48px;    border-top: 1px solid #ccc;    padding: 6px;    text-align: center;    color: #888;    font-size: 80%;}
#footer a {color: #888;}
```

#### टीपीएल लिंक अनुभाग

लिंक अनुभाग में URL के बारे में जानकारी होती है और इसमें बटन और उसकी क्रिया जैसी घटनाओं के संदर्भ शामिल हो सकते हैं।

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### टिप्पणी अनुभाग

टीपीएल के टिप्पणी अनुभाग में टिप्पणियां उत्पन्न करने के लिए शामिल हैं और इसे निम्नानुसार परिभाषित किया गया है।
```
[comment]
<div class=comment>%item-comment%</div>
```

#### अनुभाग अपलोड करें

अपलोड अनुभाग टेम्प्लेट सेटिंग्स के आधार पर सर्वर से वास्तविक HTML प्रतिक्रिया लौटाता है जैसा कि निम्नलिखित उदाहरण में दिखाया गया है।

```
[upload]
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html><head>
<title>myHFS</title>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<style type="text/css">\n%style%\n</style>
</head>
<body>
<ul id=path>
<li><strong>Folder:</strong> <a href="/">root</a>%folder%</li>
</ul>
<div id=header>
<h1>myHFS</h1>
<h2>Final HFS Template Framework for Ishare USM Community</h2>
</div>
<div id=content>

<h3>myHFS Rules</h3>
<p>I'm sharing stuffs unpaid, so please respect me by understanding these rules: </p>
<ul class="contacts">
<li>Sorry if your downloading activity was suddenly interrupted/disconnected. It might be due to some technical problems.</li>
<li>Be nice. Don't use IDM or any download manager program with many connections. Set it to 1 or you will be banned from my server.</li>
<li>Anything I shared here is the right of my freedom. Good or bad, the decision is in your hands. I'm not be responsible for any consequences.</li>
</ul>
<p class=credit>Sharing among my university fellows is an unique culture here, in Engineering Campus, USM. Sharing via LAN by using HFS software is the best underground activity for everyone. Sharing is loving!</p>
</div>

</body></html>
```

## संदर्भ

* [एचएफएस](https://www.rejetto.com/wiki/index.php/Refinements)
* [टीपीएल उदाहरण - जीथब](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

