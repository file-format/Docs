{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS फाइल - CommonJS कोड फाइल",
  "description":".cjs फाइल के हो र यसलाई कसरी खोल्ने?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## CJS फाइल के हो?

CommonJS (CJS) फाइल CommonJS सिन्ट्याक्समा लेखिएको JavaScript कोड समावेश गर्ने फाइल हो। CommonJS एक मोड्युल प्रणाली हो जुन फ्रन्टएन्ड वेब ब्राउजरहरू भन्दा बाहिरको वातावरणमा काम गर्न डिजाइन गरिएको हो, र यो प्राय: सर्भर-साइड JavaScript वातावरणहरूमा प्रयोग गरिन्छ, जस्तै Node.js।

## CJS फाइल ढाँचा - थप जानकारी

CJS फाइलहरू CommonJS सिन्ट्याक्समा लेखिएका छन् र Microsoft Notepad वा Apple TextEdit जस्ता कुनै पनि पाठ सम्पादकमा सम्पादन गर्न सकिन्छ। CommonJS मोड्युलहरू सामान्यतया छुट्टाछुट्टै फाइलहरूमा भण्डारण गरिन्छ र राम्रो संगठन र मर्मत योग्यताको लागि कोड इनक्याप्सुलेट र मोड्युलराइज गर्ने उद्देश्यले गरिन्छ। यी मोड्युलहरूले निर्भरताहरू आयात गर्न र module.exports वा निर्यात वस्तुलाई कोडका अन्य भागहरूद्वारा प्रयोग गर्न सकिने मान र कार्यहरू उजागर गर्न आवश्यक कार्य प्रयोग गर्दछ।

## CJS कोड उदाहरण

CommonJS मोड्युलहरूसँग एक विशिष्ट वाक्यविन्यास र संरचना हुन्छ जसमा अन्य मोड्युलहरू आयात गर्न आवश्यक कार्य र मोड्युलबाट मानहरू, कार्यहरू वा वस्तुहरू निर्यात गर्नका लागि module.exports वा निर्यात वस्तुहरू जस्ता सुविधाहरू समावेश हुन्छन्। यी मोड्युलहरू ठूला JavaScript कोडबेसहरू व्यवस्थापन र मर्मत गर्न सजिलो बनाउँदै कोडका टुक्राहरूलाई इन्क्याप्सुलेट गर्न र अलग गर्न प्रयोग गरिन्छ। यहाँ CommonJS मोड्युलको आधारभूत उदाहरण हो:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## सन्दर्भहरू

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)