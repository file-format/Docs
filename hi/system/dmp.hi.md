{
  "date" : "2021-07-07",
  "keywords" :["डीएमपी", "एक्सटेंशन", "फाइल", "प्रारूप", "सिस्टम", "मेमोरीडंप", "मिनीडम्प", "प्रोग्राम", "कंप्यूटर", "एप्लिकेशन"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"डीएमपी - मेमोरीडंप फ़ाइल स्वरूप",
  "description":"DMP फ़ाइल स्वरूप और API के बारे में जानें जो DMP फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## डीएमपी फाइल क्या है? ##

डीएमपी फ़ाइल मुख्य रूप से मेमोरीडम्प या मिनीडम्प फ़ाइल प्रारूप से जुड़ी है। इसका उपयोग माइक्रोसॉफ्ट विंडोज ऑपरेटिंग सिस्टम में कंप्यूटर के मेमोरी स्पेस से डंप किए गए डेटा को स्टोर करने के लिए किया जाता है। आमतौर पर, डीएमपी फाइलें तब बनती हैं जब कोई फाइल क्रैश हो जाती है या कोई त्रुटि होती है। कई बार तकनीकी विशेषज्ञों या उन्नत कंप्यूटर उपयोगकर्ताओं के लिए डीएमपी फाइलें आपके सामने आने वाली समस्याओं का निवारण करने और किसी भी प्रकार की एप्लिकेशन समस्या को हल करने के लिए बहुत महत्वपूर्ण होती हैं। DMP फाइलें Microsoft में एक मालिकाना प्रारूप के रूप में संग्रहीत की जाती हैं जिसका उपयोग ऑपरेटिंग सिस्टम द्वारा सिस्टम पर स्थापित किसी भी एप्लिकेशन को डीबग करने के लिए किया जाता है।


## डीएमपी फ़ाइल प्रारूप की तकनीकी विशिष्टता

विंडोज में, "savedump.exe" सिस्टम टूल .dmp फ़ाइलें उत्पन्न करता है जिसे तब उपलब्ध विभिन्न डिबगिंग उपयोगिताओं द्वारा संसाधित किया जा सकता है। मिनी डंप (64/128 Kb) विंडोज़ द्वारा '%SystemRoot%\Minidump' निर्देशिका में संग्रहीत किया जाता है। दूसरी ओर, कर्नेल मेमोरी और पूर्ण मेमोरी डंप को सिस्टम रूट पर 'Memory.dmp' फ़ाइलों के रूप में संग्रहीत किया जाता है। मेमोरी डंप फ़ाइलें अपेक्षाकृत बड़ी फ़ाइलें होती हैं, इसलिए पर्याप्त मात्रा में संग्रहण स्थान ले सकती हैं। इसलिए यह सलाह दी जाती है कि बेकार .dmp फ़ाइलें जो आपको लगता है कि समस्याओं के निवारण के लिए उपयोगी नहीं होंगी, तो उन्हें हटा दें।

आप .dmp फ़ाइलों को मैन्युअल रूप से या अपने कंप्यूटर पर डिफ़ॉल्ट "क्लीन डिस्क विज़ार्ड" का उपयोग करके हटा सकते हैं। DMP एक्सटेंशन का उपयोग Oracle डेटाबेस उत्पादों द्वारा बनाए गए और उपयोग किए गए बैकअप और रिकवरी डेटाबेस फ़ाइलों में .dmp फ़ाइलों का उपयोग करने के लिए किया जाता है। Oracle द्वारा बनाई गई DMP फाइलें डेटाबेस बैकअप हैं जिनका उपयोग डेटाबेस सर्वर के माध्यम से चल रहे डेटाबेस इंस्टेंस में आयात या पुनर्स्थापित करने के लिए किया जा सकता है। ज्यादातर मामलों में, .dmp फ़ाइलों में उनके फ़ाइलनामों के रूप में समय और दिनांक स्टैम्प होते हैं।

### डीएमपी फ़ाइल की सामग्री

मेमोरी डंप फ़ाइल में शामिल हैं:

* स्टॉप स्टेटमेंट और इसके पैरामीटर;
* लोड किए गए ड्राइवरों की सूची;
* विंडोज के सामान्य संचालन को रोकने वाली प्रक्रियाओं के लिए प्रोसेसर का संदर्भ (पीआरसीबी);
* रुकी हुई प्रक्रियाओं के लिए कर्नेल संदर्भ और प्रोसेसर जानकारी (EPROCESSES);
* रुके हुए थ्रेड के लिए कर्नेल संदर्भ और प्रोसेसर जानकारी (ETHREAD);
* कर्नेल-मोड कॉल स्टैक थ्रेड के लिए जिसने प्रक्रिया को प्रदर्शन से समाप्त कर दिया।


## डीएमपी उदाहरण

रोक त्रुटि 0XC0000218 (Registry_File_Failure) निम्नानुसार DMP फ़ाइल बनाता है:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## संदर्भ ##

* [डीएमपी - माइक्रोसॉफ्ट](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

