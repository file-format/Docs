{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM फाइल फॉर्मेट - असेंबली लैंग्वेज सोर्स कोड फाइल फॉर्मेट",
  "description":"ASM फ़ाइल स्वरूप और API के बारे में जानें जो ASM फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## एएसएम फाइल क्या है? ##

एक ASM फ़ाइल निम्न स्तर की प्रोग्रामिंग भाषा में लिखा गया एक प्रोग्राम है जिसे असेंबली भाषा के रूप में जाना जाता है। यह मुख्य रूप से हार्डवेयर से संबंधित कोड लिखने के लिए उपयोग किया जाता है जैसे प्रोग्रामिंग माइक्रो-नियंत्रक के लिए। प्रोग्राम सरल असेंबली लैंग्वेज सिंटैक्स का उपयोग करके लिखा गया है जिसमें विभिन्न ऑपरेशन करने के लिए ऑपरेटर और ऑपरेंड शामिल हैं। ASM फाइलें टेक्स्ट एडिटर्स में लिखी और संपादित की जाती हैं और HLA, MASM, FASM, NASM, या GAS जैसे असेंबलर प्रोग्राम का उपयोग करके निष्पादित की जाती हैं।

## एएसएम फ़ाइल स्वरूप

ASM फ़ाइलों में संचालन का एक क्रम होता है जो **ऑब्जेक्ट कोड** उत्पन्न करने के लिए एक कोडांतरक द्वारा निष्पादित किया जाता है। परिणामी ऑब्जेक्ट कोड mnemonics और एड्रेसिंग मोड्स के संयोजन का उनके संख्यात्मक समकक्षों में अनुवाद है।

### ASM फ़ाइल स्वरूप उदाहरण

निम्नलिखित x86 आर्किटेक्चर के लिए **Hello World** एप्लिकेशन का एक उदाहरण है।
```
global  go
extern  _ExitProcess@4
extern  _GetStdHandle@4
extern  _WriteConsoleA@20

section .data
msg:    db      'Hello, World', 10
handle: db      0
written:
db      0

section .text
go:
; handle = GetStdHandle(-11)
push    dword -11
call    _GetStdHandle@4
mov     [handle], eax

; WriteConsole(handle, &msg[0], 13, &written, 0)
push    dword 0
push    written
push    dword 13
push    msg
push    dword [handle]
call    _WriteConsoleA@20

; ExitProcess(0)
push    dword 0
call    _ExitProcess@4
```

## संदर्भ ##

* [विधानसभा भाषा - विकिपीडिया द्वारा] (https://en.wikipedia.org/wiki/Assembly_language)
* [असेंबली लैंग्वेज - बेसिक सिंटेक्स](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

